# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Project Overview

This is a personal academic homepage built with **Hugo** static site generator + **Wowchemy Academic v5** theme. The site is bilingual (English default + Simplified Chinese) and deployed via Netlify.

- **Site owner**: Yu Xu (许煜), Ph.D. Candidate @ HKBU CS
- **Repo**: `yuxu-1/yuxu_personal_page`

## Bilingual Content Sync Rule (IMPORTANT)

**Any change to English content MUST be mirrored in the Chinese (`zh/`) version.**

| English File | Chinese File |
|---|---|
| `content/_index.md` | `content/zh/_index.md` |
| `content/authors/yuxu/_index.md` | `content/zh/authors/yuxu/_index.md` |
| Any new content page | `content/zh/<same-path>/` |

Before committing changes that touch English content, always:
1. Check if a corresponding Chinese file exists under `content/zh/`
2. If it exists, update it with the equivalent Chinese translation
3. If it doesn't exist, create it with translated content
4. The Chinese pages have an AI-generated disclaimer at the top — keep it in place

## Key File Map

```
config/_default/
├── config.yaml       # Site config (title, baseURL, Hugo modules)
├── params.yaml       # Theme settings (appearance, SEO, features)
├── menus.yaml        # Navigation menu items
└── languages.yaml    # Bilingual config (en + zh)

content/
├── _index.md         # English homepage (landing page with widget blocks)
├── zh/_index.md      # Chinese homepage ← KEEP IN SYNC
├── authors/yuxu/     # English author profile
├── zh/authors/yuxu/  # Chinese author profile ← KEEP IN SYNC
└── publication/      # 7 publications (each a subdirectory with index.md)

data/
├── page_sharer.toml  # Social sharing buttons (Twitter disabled)
├── fonts/.gitkeep
└── themes/.gitkeep

static/uploads/
└── XUYu_2026.pdf     # CV/Resume PDF
```

## Common Tasks

- **Add publication**: Create `content/publication/<slug>/index.md` with frontmatter
- **Update author info**: Edit `content/authors/yuxu/_index.md` AND `content/zh/authors/yuxu/_index.md`
- **Update homepage sections**: Edit `content/_index.md` AND `content/zh/_index.md`
- **Disable a sharing button**: Set `enable = false` in `data/page_sharer.toml`

## Build & Deploy

- Hugo builds and deploys via Netlify automatically on push to `main`
- Local preview: `hugo server`
- Chinese version is served at `/zh/` path
