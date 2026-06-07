# Balenciaga 商品追蹤

自動追蹤 Balenciaga 官網商品資訊的靜態網站。

🌐 **公開網址：https://yajinyee.github.io/balenciaga-web/**

## 追蹤地區

| 地區 | 幣別 | 狀態 |
|------|------|------|
| 台灣 | TWD (NT$) | ✅ 運作中 |
| 日本 | JPY (¥) | ✅ 運作中 |
| 法國 | EUR (€) | ✅ 運作中 |
| 西班牙 | EUR (€) | ✅ 運作中 |

## 功能

- 商品列表與地區篩選
- 商品詳情頁（價格、圖片、尺寸、庫存狀態）
- 店家庫存顯示
- 上架 / 下市狀態追蹤
- 下架區（含 Outlet 預測日期與價格）
- 每 6 小時自動更新

## Outlet 預測規則

- 上架後一年仍有庫存 → 進入 Outlet
- Outlet 價格：原價六折以下

## 更新頻率

每 6 小時由 Balenciaga 爬蟲 Agent 自動執行：
- 爬取 4 個地區的全站商品
- 跨分類去重
- 產生靜態 HTML（含商品詳情頁）
- 自動推送到本 repo
- GitHub Pages 自動部署

## 技術

- 爬蟲：Go + chromedp（headless Chrome）
- 翻頁：自動滾動 + Load More 點擊
- 去重：跨分類 SKU 去重
- 網站：純靜態 HTML + CSS（響應式設計）
- 部署：GitHub Pages

## 資料來源

所有資料來自 Balenciaga 官方網站公開頁面。

## 相關專案

- 主系統：https://github.com/yajinyee/blue_ai_agent
