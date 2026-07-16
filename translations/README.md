# 🌐 Translations

This course's mission is to reach **every** non-technical person in the world — and most
of the world doesn't read English. Translations are the single most valuable contribution
this project can receive.

## What's translated today

The **course homepage** is available in the languages below. Full lesson translations
follow as the community contributes them.

| Language | Code | Folder | Status |
|---|---|---|---|
| العربية (Arabic) | `ar` | [translations/ar](ar/README.md) | Homepage ✅ · Lessons welcome |
| বাংলা (Bengali) | `bn` | [translations/bn](bn/README.md) | Homepage ✅ · Lessons welcome |
| Deutsch (German) | `de` | [translations/de](de/README.md) | Homepage ✅ · Lessons welcome |
| Español (Spanish) | `es` | [translations/es](es/README.md) | Homepage ✅ · Lessons welcome |
| Français (French) | `fr` | [translations/fr](fr/README.md) | Homepage ✅ · Lessons welcome |
| हिन्दी (Hindi) | `hi` | [translations/hi](hi/README.md) | Homepage ✅ · Lessons welcome |
| Bahasa Indonesia | `id` | [translations/id](id/README.md) | Homepage ✅ · Lessons welcome |
| 日本語 (Japanese) | `ja` | [translations/ja](ja/README.md) | Homepage ✅ · Lessons welcome |
| Português (Portuguese) | `pt` | [translations/pt](pt/README.md) | Homepage ✅ · Lessons welcome |
| Русский (Russian) | `ru` | [translations/ru](ru/README.md) | Homepage ✅ · Lessons welcome |
| Kiswahili (Swahili) | `sw` | [translations/sw](sw/README.md) | Homepage ✅ · Lessons welcome |
| தமிழ் (Tamil) | `ta` | [translations/ta](ta/README.md) | Homepage ✅ · Lessons welcome |
| తెలుగు (Telugu) | `te` | [translations/te](te/README.md) | Homepage ✅ · Lessons welcome |
| اردو (Urdu) | `ur` | [translations/ur](ur/README.md) | Homepage ✅ · Lessons welcome |
| 中文-简体 (Chinese, Simplified) | `zh` | [translations/zh](zh/README.md) | Homepage ✅ · Lessons welcome |

## How translations are organized

```
translations/
  <language-code>/            ← ISO 639-1 code (es, hi, zh…)
    README.md                 ← translated course homepage
    modules/                  ← translated lessons, mirroring the English structure
      01-what-is-a-computer/
        README.md
        lab.md
        ...
```

A translated page must mirror the exact path of its English original, so links stay
predictable. Anything not yet translated simply links to the English version.

## How to contribute a translation

1. **Open an issue first** titled `Translation: <language> — <files>` so two people don't
   translate the same page. Check existing issues before starting.
2. **Fork and branch** ([Module 08](../modules/08-git-and-github/README.md) teaches this).
3. Copy the English file into `translations/<code>/…` at the mirrored path and translate.
4. Open a pull request. A speaker of that language reviews it if available.

### Translation rules (important!)

- **Translate meaning, not words.** The course's voice — a patient friend explaining over
  coffee — matters more than literal accuracy. Rewrite analogies if a local equivalent
  works better (a cricket example may beat a baseball one).
- **Keep technical terms bilingual on first use.** Many terms (server, commit, deploy) are
  used untranslated in real workplaces. Write the local translation followed by the
  English term in parentheses, e.g. Hindi: सर्वर (server). Learners must recognize the
  English word — job postings and error messages will use it.
- **Follow the [Style Guide](../docs/style-guide.md)** — the banned-words rule and
  "define every term on first use" apply in every language.
- **Don't translate**: code snippets, file names, URLs, or commands. Do translate code
  *comments* and expected-output descriptions.
- **Machine translation drafts are acceptable, unreviewed machine output is not.** If you
  start from machine translation, you must read and repair every sentence — our audience
  can't tell broken jargon from real jargon, which makes bad translation worse than none.

## Adding a new language

Open an issue titled `New language: <name>`. We'll create the folder and add your language
to the tables here and on the homepage. Every language is welcome — including ones with
few speakers. "Every non-technical person in the world" means every one.
