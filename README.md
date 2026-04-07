# Andrew Hui 火炭 Personal Training Funnel Page

此專案為健身教練 Andrew Hui 製作的銷售漏斗（Sales Funnel）頁面，主打火炭銀禧會的 1 對 1 增肌、減脂、塑形與體驗課程預約。

Funnel 的核心目的，是讓用戶填寫表單後，系統能自動將 leads 寫入 Google Sheets 的 Funnel Leads CRM，協助 Andrew 先做好人流篩選，集中處理高意向客戶，提升整體跟進與轉化效率。

## 📦 專案內容

此專案包含：

- `index.html` — 頁面結構、表單流程、Google Sheets / webhook 串接邏輯
- `style.css` — 視覺樣式與版面設計
- `content.json` — 所有文案內容集中管理
- `images/` — 圖片素材
- `Make automation（外部）` — 表單提交 → Google Sheets CRM 的自動化流程

## 🎯 Funnel 與 CRM 目的

此頁面並非一般展示型網站，而是一個以 **名單收集與篩選** 為核心的 Funnel：

- 吸引對健身、增肌減脂、姿勢改善有需求的潛在客戶
- 透過多步驟表單進行初步篩選
- 將填寫資料的 leads 自動整理到 Google Sheets CRM
- 資料送出後，可進一步引導用戶傳送 default message 到 Andrew 的 WhatsApp，方便即時跟進
- 協助 Andrew 優先跟進高意向客戶
- 減少無效查詢，提升預約與成交效率

## 🎨 UX/UI 設計

此專案在 UX / UI 上，重點放在 **提升閱讀清晰度、降低操作阻力、增加表單完成率**：

- 採用清晰的單頁式 funnel 結構，讓用戶快速理解服務價值
- 利用多步驟表單，減少一次過填寫太多內容的壓力
- CTA、標題層級與資訊區塊清楚分明，方便快速掃讀
- 表單選項以易理解的互動方式呈現，提升用戶填寫意願
- 針對行動裝置體驗作優化，方便手機用戶直接預約與提交表單

## 🧠 Branding 設計

在 branding 上，頁面圍繞 Andrew Hui 的專業形象與健身服務定位，建立一致的品牌感：

- 突出「增肌、減脂、塑形、姿勢改善」等核心服務訊息
- 視覺語言偏向健康、力量感與專業信任感
- 文案風格貼近目標客群，兼顧親切感與行動引導
- 配合 CTA 與體驗課設計，強化轉化導向的品牌溝通
- 讓整體頁面既有銷售功能，同時保持個人教練品牌形象一致

## 🎨 Color Palette

此專案的配色以 **深色底 + 青綠主色 + 金色點綴** 為核心，營造專業、健康、力量感與高質感兼備的品牌形象：

- `#5EBDB5` — Brand Primary（主品牌色 / CTA / 重點互動）
- `#4AA39C` — Brand Primary Dark（主色加深 / hover 狀態）
- `#C9A96E` — Brand Gold（高級感點綴 / icon / accent）
- `#1E0F05` — Brand Background（主背景深色）
- `#2A1408` — Brand Background 2（區塊漸層深色）
- `#371A09` — Brand Background 3（卡片 / 次層背景）
- `#FFFFFF` — Brand White / Text（主要文字與對比色）

這組色彩有助於：

- 建立穩重、專業且具信任感的健身品牌形象
- 突出 CTA 按鈕與重要內容，提高視覺聚焦
- 讓整體頁面在深色風格下仍保持清晰可讀性

深色背景主要用於 Hero 區與主要內容區塊，營造沉穩與專業感；青綠主色與金色點綴則用於互動元素與視覺焦點，提升轉化率。

## ✍️ Typography（字體系統）

此專案的字體系統以 **標題吸睛 + 內文易讀** 為原則，兼顧品牌感與轉化效率：

- `Bebas Neue` — 主要用於 Hero headline 與大型標題，強調力量感與視覺衝擊
- `Noto Sans TC` — 主要用於內文、說明文字與表單內容，提升中文閱讀清晰度
- Fallback fonts：`Arial, Helvetica, sans-serif`
- 標題與內文之間保留清楚層級，方便快速掃讀重點
- 字重與大小分層明確，有助用戶快速理解 CTA 與服務價值

## 📐 Spacing / Layout 原則

此頁面在版面與留白安排上，重點是讓 funnel 流程 **清楚、有節奏、易於行動**：

- 採用單頁式 section flow，讓用戶由上而下自然閱讀
- 各區塊之間保留足夠留白，避免資訊過度擁擠
- CTA、表單與內容模組之間有明確視覺分隔
- 使用一致的 grid 與 spacing 節奏，提升整體專業感與穩定感
- 手機版優先考慮可讀性與按鈕點擊便利性
- 行動裝置上採用更緊湊但仍保持可讀性的 spacing，確保 CTA 與表單元素易於點擊

## 🧭 Funnel 架構圖（文字版）

```text
廣告 / 社交流量
        ↓
進入 Landing / Funnel Page
        ↓
閱讀服務價值、特色與體驗課資訊
        ↓
點擊 CTA（預約體驗課）
        ↓
填寫多步驟表單
  1. 目標需求
  2. 可上課時間
  3. 開始意向 / 體驗時間
        ↓
資料送出至 webhook / Make
        ↓
Make automation 負責將表單資料寫入 Google Sheets CRM，並確保資料一致性與自動化流程穩定運作
        ↓
自動寫入 Google Sheets Funnel Leads CRM
        ↓
用戶可一鍵傳送 default message 到 Andrew WhatsApp
        ↓
Andrew 優先跟進高意向客戶
        ↓
提升預約率與成交轉化
```

## 🛠 使用方式

### 本機預覽
直接以瀏覽器開啟 `index.html` 即可。

## 📝 更新內容

### 更新文案（建議）
如需修改頁面文案、表單問題、CTA 等，請優先編輯：

- `content.json`

### 更新 Funnel 流程 / 串接 / 版面
如需調整互動邏輯、Google Sheets 串接、樣式或表單流程，請編輯：

- `index.html`
- `style.css`

## 👤 製作者資訊

![UX Shari Logo](./images/Logo.png)

本專案由 **UX Shari** 製作與設計。

- Website: https://uxshari.com/
- Instagram: https://www.instagram.com/uxshari/
- Facebook: https://www.facebook.com/uxshari
- YouTube: https://www.youtube.com/@uxshari

## 📌 備註

如需客製化 landing page、表單流程優化、品牌網站設計或轉換率優化，可直接聯絡 **UX Shari**。
