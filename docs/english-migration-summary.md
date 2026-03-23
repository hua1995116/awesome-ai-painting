# English-First Localization Summary

## Audit

### Source languages found

- Simplified Chinese was the dominant source language.
- Several files already had partial English translations, but they were incomplete or mixed with Chinese.

### Content that required translation

- Root documentation in [README.md](../README.md)
- Subproject documentation in `animatediff`, `stable-cascade`, `webui-essential-plugin`, and `ai-product`
- Historical news digests under `news/`
- Mixed-language headings, summaries, link labels, and descriptive copy

### Content intentionally left unchanged

- Third-party product names, repository names, model identifiers, and URLs
- Workflow JSON internals in [animatediff/workflow_animatediff.json](../animatediff/workflow_animatediff.json)
- Chinese brand names in a few English tables where the original branding is the most searchable identifier

### Risk review

- The repository is documentation-heavy, so identifier-level refactor risk was low.
- The only potentially disruptive surface was the README layout. To preserve compatibility, the old `README_en.md` entry points were kept as English stubs that redirect readers to the main English documents.
- No API payloads, database schema names, routes, CLI flags, or runtime configuration keys required renaming.

## Translation Rules Used

- Translate prose by intent rather than word-for-word.
- Prefer natural technical English over literal phrasing.
- Preserve official names for products, models, libraries, and external services.
- Keep historical dates and file layout intact unless a change clearly improves readability without increasing risk.

## Key Changes

- Converted the main repository documentation to English-first.
- Standardized subproject READMEs into clear English.
- Rewrote mixed-language English files so they no longer switch languages mid-document.
- Translated the news roundup files into English while preserving the original outbound links.
- Fixed broken local image paths in [ai-product/README.md](../ai-product/README.md) by pointing them to `news/images`.

## Compatibility Notes

- [README_en.md](../README_en.md), [animatediff/README_en.md](../animatediff/README_en.md), [stable-cascade/README_en.md](../stable-cascade/README_en.md), and [webui-essential-plugin/README_en.md](../webui-essential-plugin/README_en.md) were retained as lightweight compatibility shims.
- Existing directory names were not changed.
- No code-level compatibility shims were necessary because the repository contains almost no executable source beyond static workflow data.

## Naming Decisions

- "AI painting" was normalized to the more natural English phrase "AI art" in most documentation, while some existing product names still use "AI Painting" because that is their published branding.
- Chinese platform names were translated only when an obvious English name existed; otherwise the original brand name was preserved.

## Remaining Follow-Up Options

- If bilingual support is still desired, add dedicated `README_zh.md` files rather than reintroducing mixed-language primary documents.
- Some external article titles were translated from Chinese for readability; if exact source-title fidelity matters more than English readability, add the original Chinese titles in parentheses.
- The repository still contains historical, date-based markdown files rather than a normalized docs structure. That was left unchanged to avoid unnecessary structural churn.
