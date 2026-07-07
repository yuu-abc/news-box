# GitHub分析メモ付きニュースボード

GitHub関連ニュースを、要約・分析・影響メモ・自分用メモつきのカードとして整理できるシングルページアプリです。ブラウザだけで動き、登録データは `localStorage` に保存されます。

## 主な機能

- ChatGPTなどから受け取ったJSONニュースの貼り付け、検証、整形
- タイトル、カテゴリ、重要度、信頼度、ステータスによる一覧管理
- GitHubリポジトリ名とGitHub URLの記録
- 要約、背景、分析、影響メモ、自分用メモ、不確実な点、次に見るべきこと、出典の表示
- ボード画面で件数・重要ニュース・GitHubリンク付きニュースを俯瞰
- JSONエクスポート、ニュース単体のJSONコピー、Markdownコピー
- 検索とフィルタリング

## 使い方

1. `index.html` をブラウザで開きます。
2. 「プロンプトをコピー」からニュース整形用プロンプトをコピーします。
3. ChatGPTなどで生成したJSONを「JSON貼り付け」に入れます。
4. 必要に応じてプレビュー画面で編集し、「登録」を押します。
5. 「ボード」または「詳細」で登録済みニュースを確認します。

## JSON形式

```json
{
  "title": "",
  "category": "",
  "importance": "medium",
  "github_repo": "owner/repo",
  "github_url": "https://github.com/owner/repo",
  "main_point": "",
  "summary": "",
  "background": "",
  "analysis": "",
  "impact": "",
  "memo": "",
  "uncertainty": "",
  "watch_next": [],
  "sources": [
    {
      "title": "",
      "url": "",
      "published_at": ""
    }
  ],
  "confidence": "medium",
  "status": "AI生成",
  "created_by": "chatgpt"
}
```
