# 相寓檢測科技驗屋團隊 — 官方網站

> 提供完整修繕規劃報告書,幫助客戶儘快完成交屋,獲得一個安心的家。

這個 repository 是 [siangyu-sy.com](https://siangyu-sy.com) 的靜態網站原始碼,透過 **GitHub Pages** 部署。

---

## 🌐 線上網址

- 主網域: <https://siangyu-sy.com>
- GitHub Pages 預設網址: <https://bill80362.github.io/siangyu-sy.com>

---

## 📁 專案結構

```
siangyu-sy.com.github.io/
├── index.html              ← GitHub Pages 入口檔
├── README.md
├── CNAME                   ← 自訂網域綁定 (siangyu-sy.com)
└── assets/
    ├── css/                ← 樣式表 (Bootstrap / FontAwesome / 自訂)
    ├── js/                 ← JavaScript (jQuery / Bootstrap / Owl Carousel)
    ├── images/             ← 案例照片、Logo、社區圖示
    ├── fonts/              ← FontAwesome / IcoFont 字型檔
    └── img/lightbox/       ← Lightbox 燈箱圖示
```

---

## 🧰 技術棧

- **HTML5** + 原生 JS,無建置流程
- **Bootstrap 4** — 版面與元件
- **jQuery 1.12.4** + 各種外掛(Owl Carousel / Filterizr / PageScroll2id / Waypoints / Counter-Up / Lightbox)
- **FontAwesome 4.7** + **IcoFont** — 圖示
- **Google Analytics (G-DK1VGLZYZH)** — 流量分析

---

## 🚀 本地預覽

由於網站全部是純靜態檔案,可以直接用任何 HTTP server 開啟:

```bash
# 方案 A:Python 內建 server
python3 -m http.server 8765

# 方案 B:Node.js
npx serve .

# 方案 C:VS Code Live Server 擴充套件
```

開啟瀏覽器前往 <http://localhost:8765/> 即可。

> ⚠️ **不要直接用 `file://` 開啟 index.html** — 部分功能(如 GA 與相對路徑)會失效。

---

## 📤 部署到 GitHub Pages

### 第一次部署

1. **確認 repository 設定**
   - 到 GitHub → **Settings** → **Pages**
   - **Source** 選擇 `Deploy from a branch`
   - **Branch** 選擇 `main`、資料夾 `/ (root)`
   - 儲存後等待 1-2 分鐘讓 GitHub 建立 Pages

2. **自訂網域綁定**
   - repository 根目錄已建立 [`CNAME`](./CNAME) 檔案,內容為 `siangyu-sy.com`
   - 到 GitHub → **Settings** → **Pages** → **Custom domain** 確認已綁定
   - 勾選 **Enforce HTTPS**(需要 DNS 生效後才能啟用)

3. **DNS 設定(網域商介面)**
   在 `siangyu-sy.com` 的 DNS 加上下列紀錄:

   | 類型 | 名稱 | 內容 |
   |---|---|---|
   | `A` | `@` | `185.199.108.153` |
   | `A` | `@` | `185.199.109.153` |
   | `A` | `@` | `185.199.110.153` |
   | `A` | `@` | `185.199.111.153` |
   | `CNAME` | `www` | `bill80362.github.io.` |

   > DNS 生效需要 5 分鐘到 48 小時不等。

### 後續更新

```bash
git add .
git commit -m "更新內容"
git push origin main
```

GitHub Pages 會在 push 後約 1 分鐘自動重新部署。

---

## 🔄 從舊站遷移(本次異動紀錄)

| 動作 | 說明 |
|---|---|
| HTML 重組 | 下載的中文檔名 HTML 整理為標準 `index.html` |
| 資源分類 | 從中文資料夾重新分類到 `assets/{css,js,images,fonts,img}/` |
| 內部連結 | 將 `http://siangyu-sy.com/#xxx` 改為相對錨點 |
| 遠端資源本地化 | slider 背景圖、favicon、字型、style.css/lightbox.css 圖檔 |
| `<html lang>` | 從 `en` 改為 `zh-Hant` |

---

## 📞 聯絡資訊

- 公司:相寓檢測科技驗屋團隊
- 電話:0917-836-281
- 服務範圍:中南部地區

---

## 📄 授權

© 相寓檢測科技驗屋團隊 All rights reserved.
