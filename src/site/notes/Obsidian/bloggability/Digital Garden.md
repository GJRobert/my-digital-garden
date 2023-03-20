---
{"dg-publish":true,"permalink":"/Obsidian/bloggability/Digital Garden/","created":"2023-03-19T23:40:32.182+08:00","updated":"2023-03-20T12:16:30.879+08:00"}
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
- 原來網站名稱是在 plugin 設定裡處理
- 其他頁面元素也都可以輕鬆打開 👍
- 細細研究 [Digital Garden Docs](https://dg-docs.ole.dev/) 吧
- 內容的更新、設定的異動，都會用 GitHub commit 追蹤
  e.g. [Commits · GJRobert/my-digital-garden](https://github.com/GJRobert/my-digital-garden/commits/main)

## 觀感
- 似乎比 [[Mixa\|Mixa]] 強多
	- Ob 內左邊欄還有一個 Digital Garden Publish Center，真猛
- 網站上一開始的頁面是最陽春的，什麼附加功能都沒有
- 但什麼都可以新增
- 太好了，transclude 的頁面內容都順利呈現！比 Mixa 強多了
- 不過網站名稱、CSS 等可能還有得自訂，值得細細研究
- 支援大量 Ob theme 實在太棒，太漂亮了
	- 還吃 ==Style Settings== 設定也太猛，真的是為了 Obsidian 而生
	- 好像沒有吃自訂輔色

## Tip
- 自動切換日夜 theme #待研究
  官方說，[The Threshold](https://hermitage.utsob.me/) 的作者做了一個可切換日夜 theme 的按鈕 ☞ [topobon/001-floatingControls.njk at main · uroybd/topobon](https://github.com/uroybd/topobon/blob/main/src/site/_includes/components/user/common/footer/001-floatingControls.njk)
- [ ] 批次加入 `dg-publish` 

## 問題
- [x] 但並沒有 blog 功能 XD #勉強解決
  → 想到找個能自動產生最近更新檔案列表的 plugin ☞ [Vault Changelog](obsidian://show-plugin?id=obsidian-vault-changelog) ← 不過問題是它無法被 `dg-publish`，因為它的 front matter 都會被覆寫 XD
  - 哇！還好可以開一個頁面叫 [[blog/blog\|blog]]，transclude [[changelog\|changelog]] 的內容，然後 publish 上 Digital Garden，可以耶！😢 這樣勉強算有個簡單的最新 log 了！

## 其他
- [ ] 什麼是「digital garden」？
  好像是個筆記界/架站界的新術語……
	- 喔，原來就是我這 20 年來在追尋及建構的「blog+wiki」嘛！！！☞ [什麼是 Digital Garden？](https://ithelp.ithome.com.tw/m/articles/10293438)；[How to set up your own digital garden - Ness Labs](https://nesslabs.com/digital-garden-set-up)