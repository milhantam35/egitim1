# egitim

Claude Code eğitim çalışma klasörü: komut notları ve projeye özel skill'ler.

## Proje Yapısı

- `claude-code-komutlari.pdf` — Claude Code komutları üzerine eğitim dokümanı.
- `.claude/skills/cmw104-new-session/SKILL.md` — oturum kapatma skill'i.
- `cv-site/index.html` — kişisel CV sitesi (tek dosya, statik HTML/CSS/JS). TR/EN dil ve açık/koyu tema geçişi; varsayılan dil TR. Kaynak: LinkedIn "Save to PDF" çıktısı.

## CV Sitesi Kararları

- Deneyimde yalnızca Siemens (SI B PSE, Nisan 2024 – Günümüz) gösterilir; önceki işler bilinçli olarak çıkarıldı.
- Eğitim: İYTE Yüksek Lisans + Beykent Lisans; lise yok.
- Telefon numarası gizlilik için sitede yok; e-posta ve LinkedIn var.
- Yayın hedefi: GitHub Pages → `https://milhantam35.github.io/egitim1/cv-site/` (Pages ayarı: `master` / root).

## Git

- Dal: `master`, upstream `origin/master`.
- Remote: `origin` → https://github.com/milhantam35/egitim1 (repo adı `egitim1`, `egitim` değil).

## Skill'ler

- `/cmw104-new-session` — sırayla: CLAUDE.md'yi oturumda yapılanlarla günceller, klasör repo değilse `git init` yapar, değişiklikleri Türkçe anlamlı mesajla commit eder, remote varsa push eder (force push yok, gizli dosyalar commit'lenmez).

## Kurallar

- İletişim ve commit mesajları Türkçe.
- `.env`, `credentials.json`, `.claude/settings.local.json` gibi dosyalar commit'lenmez (`.gitignore`'da).
- Kullanıcıya örnek komut verirken yer tutucuları (ör. `KULLANICI_ADINIZ`) açıkça "değiştirin" diye belirt.

## Ortam Notları

- Windows + PowerShell 5.1. Eski PSReadLine, Türkçe klavyede AltGr harflerinde "Oops, something went wrong" verip çökebiliyor; zararsız. Çözüm: `Install-Module PSReadLine -Force -SkipPublisherCheck`.

## Oturum Geçmişi

### 2026-11-21

- `cmw104-new-session` skill'i oluşturuldu, CLAUDE.md ilk kez yazıldı.
- Klasör git reposu yapıldı, `.gitignore` eklendi, ilk commit atıldı.
- Remote önce yer tutucu adresle eklenmişti (400 hatası); `milhantam35/egitim1` olarak düzeltildi ve push edildi.
- LinkedIn profilinden (PDF) `cv-site/index.html` CV sitesi oluşturuldu; deneyimde yalnızca Siemens var.
- Yapılacak: GitHub'da Settings → Pages'ten `master` / root seçilerek yayın açılmalı (repo gizliyse önce public yapılmalı).
