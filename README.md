# 商品條碼掃描錄入系統

本專案是一個基於網頁的商品條碼掃描與錄入工具，支援即時掃描條碼並將資料儲存至 Firebase Firestore。適合用於門市、倉儲等場景，快速建立商品條碼清單。

## 主要功能
- 使用相機即時掃描商品條碼
- 條碼自動錄入 Firebase Firestore
- 條碼快取避免重複錄入
- 條碼清單即時顯示，支援刪除
- 介面美觀，行動裝置友善

## 使用說明
1. 下載或複製本專案，並將 `barcode.html` 重新命名為 `index.html`。
2. 開啟 `index.html`，於 `<script type="module">` 內填入你的 Firebase 設定（apiKey、authDomain、projectId 等）。
3. 於瀏覽器開啟 `index.html`，點擊「開始掃描」即可使用相機掃描條碼。
4. 條碼掃描成功後會自動儲存至 Firebase，並於下方清單顯示。
5. 點擊「刪除」可移除條碼（同步刪除 Firebase 資料）。

## Firebase 設定
請至 [Firebase Console](https://console.firebase.google.com/) 建立專案，並啟用 Firestore。
將專案設定填入 `index.html` 內的 firebaseConfig 物件。

```js
const firebaseConfig = {
  apiKey: "你的apiKey",
  authDomain: "你的authDomain",
  projectId: "你的projectId",
  storageBucket: "你的storageBucket",
  messagingSenderId: "你的messagingSenderId",
  appId: "你的appId"
};
```

## 相依資源
- [Tailwind CSS](https://tailwindcss.com/)
- [jQuery](https://jquery.com/)
- [Firebase](https://firebase.google.com/)
- [zxing-js/browser](https://github.com/zxing-js/browser)

## 注意事項
- 本專案僅用於學習與內部管理，請勿用於商業用途。
- 條碼資料儲存於 Firebase，請妥善管理專案權限。

---

如有問題歡迎提出 Issue 或聯絡作者。