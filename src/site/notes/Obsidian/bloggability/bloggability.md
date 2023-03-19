---
{"dg-publish":true,"permalink":"/Obsidian/bloggability/bloggability/","title":"Obsidian blog 可能性","created":"2023-03-13T23:23:12.604+08:00","updated":"2023-03-19T23:46:14.945+08:00"}
---


# 典型部落格需要：
- 自動由新至舊依時序列出文章
- 依年、月彙整文章
- 依標籤彙整文章
- 依分類彙整文章
- 最好有側邊欄
#整理到DW 👆

# Mixa
結果有這個：
[mixasite/obsidian-mixa: Publish your notes and blog posts directly from Obsidian with Mixa](https://github.com/mixasite/obsidian-mixa)
☞ [[Mixa\|Mixa]]

1. 裝起這個 plugin
2. Obsidian 是有 folder tree 組織的！→ 建個 /blog/2023/03/[[blog/2023/03/13-test\|13-test]]
3. 到 Mixa.site 上登入，然後很快建個新網站，其實只是個殼
4. Generate token → 填到 Obsidian 的 Mixa 設定中
5. → `Publish` → [我的測試 Mixa 站](https://ghsrobert.mixa.site/)
  網路上很快就有全部的頁面，blog 裡也有樹狀結構，以及彙整？ 
	- ✅ 時序列出
	- ✅ 年、月彙整：自己建資料夾
	- 標籤彙整：似無

## 技巧
- [x] 完整文章標題 vs. 簡易檔名
  ```
  ---
  title: Why You Should Use Markdown For Blogging
  description: We've all been there. Wasted our precious time styling our posts before publishing, and eventually got tired of ...
  cover: "markdown-blogging.jpg"
  date: "2023-02-20"
  ---
  ```
  這些要放到檔案最前面的樣子
  → 成功了，很好 😃
{ #706cdd}

	- 不僅可用在 blog 頁面
{ #75ec5c}

	- 任何頁面都可用
- [x] 設定網站 CSS

# 其他
- [Jekyll-Garden/jekyll-garden.github.io: A Digital Garden Theme for Jekyll. Jekyll Garden lets you create a static HTML version of your markdown notes and publish via Github pages. Made for Obsidian users!](https://github.com/Jekyll-Garden/jekyll-garden.github.io)

# Digital Garden

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/obsidian/bloggability/digital-garden/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





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

## 觀感
- 似乎比 [[Mixa\|Mixa]] 強多
	- Ob 內左邊欄還有一個 Digital Garden Publish Center，真猛
- 網站上一開始的頁面是最陽春的，什麼附加功能都沒有
- 但什麼都可以新增
- 太好了，transclude 的頁面內容都順利呈現！比 Mixa 強多了
- 不過網站名稱、CSS 等可能還有得自訂，值得細細研究


</div></div>
