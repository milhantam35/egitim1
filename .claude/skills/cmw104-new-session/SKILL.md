---
name: cmw104-new-session
description: Oturumu kapatır - CLAUDE.md'yi bu oturumda yapılanlarla günceller, gerekirse git repo oluşturur, değişiklikleri anlamlı bir mesajla commit eder ve remote varsa push eder. Kullanıcı /cmw104-new-session yazdığında veya oturumu kaydetmek/kapatmak istediğinde kullan.
---

# cmw104-new-session

Bu adımları **sırayla** uygula. Bir adım başarısız olursa dur, hatayı kullanıcıya göster ve sonraki adıma geçme.

## 1. CLAUDE.md'yi güncelle

- Proje kökündeki `CLAUDE.md` dosyasını oku. Yoksa oluştur (başlık: proje adı + kısa açıklama).
- Bu oturumda yapılanları konuşma geçmişinden çıkar: eklenen/değiştirilen dosyalar, alınan kararlar, öğrenilen proje kuralları, yarım kalan işler.
- Bunları `CLAUDE.md` içine ekle:
  - Kalıcı bilgiler (proje yapısı, komutlar, kurallar) ilgili bölümlere işlensin; mevcut bilgiyle çelişen eski satırları güncelle, kopya oluşturma.
  - `## Oturum Geçmişi` bölümüne en üste yeni bir madde ekle: `### YYYY-MM-DD` başlığı altında 3-6 kısa madde (ne yapıldı, ne kaldı).
- Dosyayı kısa ve okunur tut; kod veya uzun çıktı yapıştırma.

## 2. Git reposu yoksa oluştur

```bash
git rev-parse --is-inside-work-tree 2>/dev/null || git init
```

- Yeni repo oluşturulduysa ve `.gitignore` yoksa, projeye uygun temel bir `.gitignore` ekle (ör. `node_modules/`, `.env`, `__pycache__/`, `.claude/settings.local.json`).

## 3. Commit et

- `git status` ve `git diff` ile değişiklikleri incele.
- Gizli bilgi içerebilecek dosyaları (`.env`, `credentials.json`, anahtar dosyaları, `.claude/settings.local.json`) **ekleme**; varsa kullanıcıyı uyar.
- Dosyaları ekle (`git add` ile, gizli dosyalar hariç).
- Değişikliklerin özünü anlatan, Türkçe, anlamlı bir commit mesajı yaz:
  - İlk satır: en fazla ~70 karakter, ne yapıldığını özetler (ör. `Oturum: komut özeti eklendi, CLAUDE.md güncellendi`).
  - Gerekirse boş satırdan sonra madde madde ayrıntı.
- Commit edilecek değişiklik yoksa bunu söyle ve 4. adıma geç.

## 4. Remote varsa push et

```bash
git remote
```

- Çıktı boşsa: push yapma, kullanıcıya "remote tanımlı değil, push atlandı" de.
- Remote varsa: `git push` çalıştır. Upstream tanımlı değilse `git push -u <remote> <mevcut-dal>` kullan.
- Push reddedilirse (ör. remote önde) **force push yapma**; durumu kullanıcıya bildir.

## Sonuç

Kısa bir özet ver: CLAUDE.md'de neler değişti, commit hash'i ve mesajı, push yapıldı mı / neden atlandı.
