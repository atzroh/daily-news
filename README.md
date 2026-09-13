# Daily News

ChatGPTのスケジュール機能で毎朝ニュースをまとめ，GitHub Pagesで表示するリポジトリです．

## 記事の保存場所

日々の記事は次の命名規則で保存します．

```text
_posts/YYYY-MM-DD-daily-news.md
```

各記事には次のFront Matterを付けます．

```yaml
---
layout: post
title: "YYYY年MM月DD日のニュース"
date: YYYY-MM-DD 08:00:00 +0900
categories: [ニュース]
---
```

## 公開

GitHub Pagesの公開元として `main` ブランチの `/ (root)` を使用します．

<!-- redeploy: 2026-09-13 -->
