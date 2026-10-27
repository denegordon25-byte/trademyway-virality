# TradeMyWay Virality Board

A static dashboard showing what hit hardest in UK trade content each day: top posts with real metrics, keywords, formats and 3 Reel ideas.

- `index.html`: the page. No build step. It fetches `data.json` and has a picker for past days.
- `data.json`: an array of day objects, newest added each run.
- `logo.png`: the TradeMyWay logo.

## Day schema
```json
{"date":"YYYY-MM-DD","window":"...","summary":"...",
 "hits":[{"url":"","handle":"","text":"","likes":0,"reposts":0,"views":0,"video_views":0,"replies":0,"format":"","posted":""}],
 "benchmarks":[], "keywords":[""], "formats":[""], "sounds":[""],
 "ideas":[{"title":"","hook":"","why":"","build":"","assets":[""]}]}
```
`views` is X impressions and `video_views` is media plays. Optional fields can be left out. A missing value shows as –.

## Local preview
`python3 -m http.server` in this folder, then open http://localhost:8000.

## Hosting
GitHub Pages, deployed from `main` / root. On the free plan the repo must be public.
