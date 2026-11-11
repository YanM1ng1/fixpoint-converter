# Fixed / Floating Point 轉換器

純前端（單一 `index.html`，無外部依賴）的數值格式轉換工具：

- **Fixed point Qm.n**：signed / unsigned，可選 m 是否包含 sign bit（TI 慣例 vs ARM 慣例）、5 種 rounding、saturate / wrap overflow
- **Floating point EeMm**：自訂 exponent / mantissa 位元與 bias；IEEE、FN（OCP FP8 E4M3）、無特殊值（MX FP6/FP4）三種 Inf/NaN 規則；subnormal 或 flush-to-zero
- 雙向轉換：十進位 → bits，或 binary / hex → 十進位
- 點擊 bit 可直接翻轉、顯示精確值、誤差（LSB / ULP / 相對誤差）、格式範圍
- 全部用 BigInt 做精確有理數運算，不受 JS double 精度限制
- 設定會存在網址 `#...` 中，可以直接分享連結

## 部署到 GitHub Pages

```bash
cd FixPoint_FP
git init
git add index.html README.md
git commit -m "Fixed/Float converter"
git branch -M main
git remote add origin https://github.com/<你的帳號>/<repo 名稱>.git
git push -u origin main
```

接著在 GitHub repo 頁面：**Settings → Pages → Build and deployment**
- Source：`Deploy from a branch`
- Branch：`main`，資料夾 `/ (root)` → Save

約 1 分鐘後就可以從 `https://<你的帳號>.github.io/<repo 名稱>/` 開啟。

## 本機使用

直接用瀏覽器打開 `index.html` 即可。
