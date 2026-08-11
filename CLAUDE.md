# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Project Overview

This is a personal academic homepage built with **Hugo** static site generator + **Wowchemy Academic v5** theme. The site is bilingual (English default + Simplified Chinese) and deployed via Netlify.

- **Site owner**: Yu Xu (许煜), Ph.D. Candidate @ HKBU CS
- **Repo**: `yuxu-1/yuxu_personal_page`
- **URLs**: English at `/en/`, Chinese at `/zh/`, root `/` auto-redirects to `/en/`

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
└── zh/                   # Chinese
    ├── _index.md         # type: widget_page
    ├── home/             # Widget pages (headless bundle)
    │   ├── index.md
    │   ├── disclaimer.md, about.md, featured.md, ...
    └── authors/yuxu/     # Author profile (Chinese)
```

## Bilingual Content Sync Rule (IMPORTANT)

**Any change to English content MUST be mirrored in the Chinese version.**

| English File | Chinese File |
|---|---|
| `content/en/_index.md` | `content/zh/_index.md` |
| `content/en/home/*.md` | `content/zh/home/*.md` |
| `content/en/authors/yuxu/_index.md` | `content/zh/authors/yuxu/_index.md` |
| `content/en/publication/*/index.md` | Currently not translated |

Before committing:
1. Check if a corresponding Chinese file exists under `content/zh/`
2. If it exists, update it with the equivalent Chinese translation
3. If it doesn't exist, create it with translated content
4. Chinese pages have an `⚠️ AI-generated` disclaimer — keep it in place

## Key Config Files

```
config/_default/
├── config.yaml       # defaultContentLanguageInSubdir: true, Hugo modules
├── params.yaml       # show_language: true, twitter: '' (disabled)
├── menus.yaml        # English nav menu
└── languages.yaml    # en (contentDir: content/en) + zh (contentDir: content/zh)
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
- **Update homepage**: Edit `content/en/home/*.md` AND `content/zh/home/*.md`
- **Update author info**: Edit `content/en/authors/yuxu/_index.md` AND `content/zh/authors/yuxu/_index.md`
- **Change nav menu**: Edit `config/_default/menus.yaml` (English) and `config/_default/languages.yaml` (Chinese menu)

## Build & Deploy

- Hugo builds and deploys via Netlify automatically on push to `main`
- Local preview: `hugo server` (English at http://localhost:1313/en/, Chinese at /zh/)
- Root `/` auto-redirects to `/en/` (default language)
