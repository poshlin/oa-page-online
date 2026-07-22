# oa-page-online — 線上課程 Landing Page

取代官網 `https://orangeapple.co/campaigns/online`（原 Rails 頁），做法比照 `oa-page-classroom`：單檔 `index.html`（含 CSS／JS／JSON-LD），`<oa-header>`／`<oa-footer>` 由母站 shell 注入，試聽 CTA 用 `<button data-oa-cta>` 開母站留單 modal。

## 檔案
- `index.html` — 整頁（head meta＋JSON-LD＋內容＋樣式＋互動）
- `oa.config.json` — slug／path 設定（path = `/campaigns/online`）
- `設計提案_v1.md` — 重設計提案與決策紀錄（含現況診斷、說服架構、紅線自檢）

## 設計主軸
說服對線上課有疑慮的家長：hero 直接回應「學不學得會」，第二區直球回答 5 大疑慮（坐不住／看影片學不會／效果追蹤／缺課／設備），雙師制為核心差異化論述。

## SEO/AEO 結構
JSON-LD `@graph`：Organization(＋AggregateRating)／WebSite／WebPage(＋Speakable)／BreadcrumbList／Course×11／VideoObject×1／FAQPage×12。單一 H1；FAQ 採答案先行寫法。

## data-oa-cta 位置代號
`hero`／`middle`／`bottom`／`sticky`（共 4 顆，全部為 `<button type="button">`）。

## 上架
push 至 `OrangeApple-Lab/oa-page-online` → 跑 `/oa-webpage-preflight` → 首次上架通知數位長（marketing@orangeapple.co）沿用 `/campaigns/online` 路由。
