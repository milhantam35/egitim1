# egitim

Claude Code eğitim çalışma klasörü: komut notları ve projeye özel skill'ler.

## Proje Yapısı

- `claude-code-komutlari.pdf` — Claude Code komutları üzerine eğitim dokümanı.
- `.claude/skills/cmw104-new-session/SKILL.md` — oturum kapatma skill'i.

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
- Açık iş yok.
