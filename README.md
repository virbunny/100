# 熊兔制霸百大城 PWA v1

## 內容
- `index.html`：由 APK v4.6 的 WebView 版抽出，版本顯示改為 `v4.6-PWA3`。
- `manifest.webmanifest`：PWA 安裝設定。
- `service-worker.js`：離線快取與更新控制。
- `icons/`：PWA / Android / iOS 捷徑圖示。

## 使用方式
1. 把整個資料夾上傳到 GitHub Pages、Firebase Hosting、Render static site，或任何 HTTPS 網站。
2. 用 Chrome / Edge / Android Chrome 開啟網址。
3. 瀏覽器出現「安裝」或「新增至主畫面」後即可安裝。

## 注意
- 直接雙擊 `index.html` 用 `file://` 開啟時，PWA 安裝不會生效。
- PWA 必須在 `https://` 或 `localhost` 才能註冊 service worker。
- 原本資料存在瀏覽器 localStorage；換網址、換瀏覽器或清除網站資料都可能看不到舊紀錄，請用 JSON 匯出備份。
- Tailwind 與字型仍沿用原本 CDN；第一次載入需要網路。之後 service worker 會嘗試快取已載入資源。


## v4.6-PWA3 修正
- 修正 v4.6-PWA1 因 PWA 標籤誤插入匯出 HTML 模板，造成 JavaScript 語法中斷、所有功能鍵失靈的問題。
- 更新 service worker cache 名稱，部署後會清掉舊版快取。


- v4：桌面圖示改為透明背景，並移除 manifest 的 maskable 圖示設定，避免系統優先使用有底色圖示。
