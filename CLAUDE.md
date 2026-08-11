# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Project Overview

This is a personal academic homepage built with **Hugo** static site generator + **Wowchemy Academic v5** theme. The site is trilingual (English default + Simplified Chinese + Traditional Chinese) and deployed via Netlify.

- **Site owner**: Yu Xu (许煜), Ph.D. Candidate @ HKBU CS
- **Repo**: `yuxu-1/yuxu_personal_page`
- **URLs**: English at `/en/`, Simplified Chinese at `/zh/`, Traditional Chinese at `/zh-hant/`, root `/` auto-redirects to `/en/`

## Architecture: Language-Isolated Content

Each language has its own content directory with `defaultContentLanguageInSubdir: true`. This prevents Hugo auto-translation conflicts.

```
content/
├── en/                   # English (default language)
│   ├── _index.md         # type: widget_page
│   ├── home/             # Widget pages (headless bundle)
│   │   ├── index.md
│   │   ├── about.md, featured.md, publications.md, ...
│   ├── authors/yuxu/     # Author profile
│   └── publication/      # 7 publications
│
├── zh/                   # Chinese (Simplified)
│   ├── _index.md         # type: widget_page
│   ├── home/             # Widget pages (headless bundle)
│   │   ├── index.md
│   │   ├── about.md, positions.md, academic.md, ...
│   └── authors/yuxu/     # Author profile (Simplified Chinese)
│
└── zh-Hant/              # Chinese (Traditional)
    ├── _index.md         # type: widget_page
    ├── home/             # Widget pages (headless bundle)
    │   ├── index.md
    │   ├── about.md, positions.md, academic.md, ...
    └── authors/yuxu/     # Author profile (Traditional Chinese)
```

## Trilingual Content Sync Rule (IMPORTANT)

**Any change to English content MUST be mirrored in both Chinese versions.**

| English File | Simplified Chinese | Traditional Chinese |
|---|---|---|
| `content/en/_index.md` | `content/zh/_index.md` | `content/zh-Hant/_index.md` |
| `content/en/home/*.md` | `content/zh/home/*.md` | `content/zh-Hant/home/*.md` |
| `content/en/authors/yuxu/_index.md` | `content/zh/authors/yuxu/_index.md` | `content/zh-Hant/authors/yuxu/_index.md` |
| `content/en/publication/*/index.md` | Currently not translated | Currently not translated |

Before committing:
1. Check if corresponding Chinese files exist under `content/zh/` and `content/zh-Hant/`
2. If they exist, update them with the equivalent Chinese translation
3. If they don't exist, create them with translated content
4. Chinese pages have an `⚠️ AI-generated` disclaimer — keep it in place
5. Use `zhconv` (Python) to convert Simplified → Traditional: `zhconv.convert(text, 'zh-Hant')`

## Key Config Files

```
config/_default/
├── config.yaml       # defaultContentLanguageInSubdir: true, Hugo modules
├── params.yaml       # show_language: true, twitter: '' (disabled)
├── menus.yaml        # English nav menu
└── languages.yaml    # en + zh (Simplified) + zh-Hant (Traditional)
```

## Key Data Files

```
data/
├── page_sharer.toml  # Social sharing buttons (Twitter: enabled=false)
├── fonts/.gitkeep
└── themes/.gitkeep
```

## Common Tasks

- **Add publication**: Create `content/en/publication/<slug>/index.md`
- **Update homepage**: Edit `content/en/home/*.md` AND `content/zh/home/*.md` AND `content/zh-Hant/home/*.md`
- **Update author info**: Edit `content/en/authors/yuxu/_index.md` AND `content/zh/authors/yuxu/_index.md` AND `content/zh-Hant/authors/yuxu/_index.md`
- **Change nav menu**: Edit `config/_default/menus.yaml` (English) and `config/_default/languages.yaml` (both Chinese menus)

## Build & Deploy

- Hugo builds and deploys via Netlify automatically on push to `main`
- Local preview: `hugo server` (English at http://localhost:1313/en/, Simplified Chinese at /zh/, Traditional Chinese at /zh-hant/)
- Root `/` auto-redirects to `/en/` (default language)
