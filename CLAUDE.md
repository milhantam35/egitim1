# egitim

Claude Code eğitim çalışma klasörü: komut notları ve projeye özel skill'ler.

## Proje Yapısı

- `claude-code-komutlari.pdf` — Claude Code komutları üzerine eğitim dokümanı.
- `.claude/skills/cmw104-new-session/SKILL.md` — oturum kapatma skill'i.

## Skill'ler

- `/cmw104-new-session` — sırayla: CLAUDE.md'yi oturumda yapılanlarla günceller, klasör repo değilse `git init` yapar, değişiklikleri Türkçe anlamlı mesajla commit eder, remote varsa push eder (force push yok, gizli dosyalar commit'lenmez).

## Kurallar

- İletişim ve commit mesajları Türkçe.
- `.env`, `credentials.json`, `.claude/settings.local.json` gibi dosyalar commit'lenmez (`.gitignore`'da).

## Oturum Geçmişi

### 2026-11-21

- `cmw104-new-session` skill'i oluşturuldu.
- CLAUDE.md ilk kez oluşturuldu.
- Klasör git reposu olarak başlatıldı, `.gitignore` eklendi.
- Remote henüz tanımlı değil.
