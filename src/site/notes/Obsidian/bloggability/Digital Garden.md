---
{"dg-publish":true,"permalink":"/obsidian/bloggability/digital-garden/"}
---


[oleeskild/obsidian-digital-garden](https://github.com/oleeskild/obsidian-digital-garden)

## 實做

### 安裝步驟
大致照 [Initial Setup](https://github.com/oleeskild/obsidian-digital-garden#initial-setup)，但注意：
1. GitHub 帳戶：同
2. Vercel 帳戶：新建的時候會問說要把 Vercel 安裝在哪個 GitHub repo，我就先建一個空的然後弄進去
  e.g. `digital-garden`
4. 但是要把 [oleeskild/digitalgarden](https://github.com/oleeskild/digitalgarden) 這個 repo `Deploy` 到 Vercel 時，又是要新建一個不同的 repo，而且這個 repo 的名稱就會影響到 Digital Garden 網域名稱的樣子
  結果我的就變成 https://my-digital-garden-xi.vercel.app/ 了
4. 取得 token，可設為 `No expiration`，其他設定不用改
  → `Generate`
5. 安裝 [Digital Garden](obsidian://show-plugin?id=digitalgarden)，然後設定，貼入 token
6. 新增個[[Obsidian/Digital Garden Home\|頁面]]，裡面要有 `dg-home` 及 `dg-publish` 兩個 front matter
7. ==Command Palette== `Publish Single Note` ✅（我的 Gmail 還會收到更新通知 😆）
8. 成功了，Vercel 網站上看到推送上去的頁面了！

### 後續建構
- 一開始的頁面是最陽春的，什麼附加功能都沒有
- 但什麼都可以新增
- 太好了，transclude 的頁面內容都順利呈現！比 Mixa 強多了

## 觀感
- 似乎比 [[Mixa\|Mixa]] 強多
	- 左邊欄還有一個 Digital Garden Publish Center，真猛
