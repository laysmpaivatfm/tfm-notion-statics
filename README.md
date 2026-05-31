# tfm-notion-statics

Durable hosting for static creative images embedded in Notion biweekly reports.

## Why this exists

Google Drive thumbnail links and Meta CDN URLs expire (Drive signed URLs go stale
within ~1 day), which breaks static images in published Notion pages. Raw
GitHub URLs never expire, and Notion proxies them through its own CDN once embedded.

## Structure

One subfolder per client. Add new clients as needed.

```
ww/   Workweek biweekly statics
il/   Insider Living biweekly statics
```

## Naming

Use the DCT filename with underscores, no spaces:
`DCT_<num>_<BRAND>_<Name>_v<version>.png`

## Embed in Notion

```
![](https://raw.githubusercontent.com/laysmpaivatfm/tfm-notion-statics/main/<client>/<filename>.png)
```

Always use empty alt text `![]( ... )` so Notion does not render a visible caption.
