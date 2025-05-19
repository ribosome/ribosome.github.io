# Ribosome GitHub Pages

此專案已改寫成 [Jekyll](https://jekyllrb.com/) 架構，以便於擴充與維護。透過 Jekyll 可在本地產生靜態網頁，並直接部署至 GitHub Pages。

## 如何使用

1. **複製或分支此專案**
   - 透過 `git clone` 下載程式碼，或在 GitHub 上建立分支以進行開發。
2. **安裝 Jekyll（可選）**
   - 若要在本地端預覽，需先安裝 Ruby 與 Jekyll，執行 `gem install jekyll bundler`。
   - 安裝完成後，在專案目錄執行 `jekyll serve` 即可啟動本地伺服器。
3. **修改頁面內容**
   - 主要頁面位於 `index.md`，並使用 `_layouts/default.html` 佈局。
   - 亦可新增其他頁面或文章資料夾如 `_posts/` 進行擴充。
4. **提交並推送變更**
   - 使用 `git add`、`git commit` 以及 `git push` 將變更推送至 GitHub。
5. **啟用 GitHub Pages**
   - 在 GitHub 專案設定的「Pages」區塊，選擇對應分支並儲存，GitHub 會依照 Jekyll 設定自動建置並部署。

## 目錄結構

```
/ (專案根目錄)
├── _config.yml        # Jekyll 設定檔
├── _layouts/          # 佈局檔案
│   └── default.html
├── index.md           # 主要頁面
├── robots.txt         # 機器人爬蟲設定
└── README.md
```

## 相關資源

- [GitHub Pages 官方文件](https://docs.github.com/pages)
- [Jekyll 官方文件](https://jekyllrb.com/docs/)
