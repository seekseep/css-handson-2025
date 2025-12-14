# CSS Handson 2025 ドキュメント

## 本リポジトリの目的

このリポジトリは、HTMLとCSSによる視覚表現を学ぶためのデモサイトを提供することを目的としています。

## ディレクトリ構成

### public/

実際のデモサイトのコンテンツを格納します。HTMLとCSSファイルが配置され、GitHub Pagesを通じて公開されます。

### docs/

リポジトリの運用に関するドキュメントを格納します。開発方針、ガイドライン、技術的な説明などを記載します。

## 開発方針

このリポジトリは、Issueを追加しながら段階的にコンテンツを拡張していく方針です。新しいデモや機能の追加は、まずIssueで提案し、議論した上で実装を進めます。

## GitHub Pages デプロイ

### 公開サイト

https://seekseep.github.io/css-handson-2025/

### デプロイの仕組み

1. **自動デプロイ**: `main` ブランチへの push により、GitHub Actions が自動的にサイトをデプロイします
2. **ワークフロー**: `.github/workflows/pages.yml` にデプロイ設定が記述されています
3. **公開ディレクトリ**: `public/` ディレクトリの内容が GitHub Pages で公開されます

### 必要な設定

リポジトリで GitHub Pages を有効にするには、以下の設定が必要です:

1. **GitHub Pages の有効化**
   - リポジトリの Settings → Pages に移動
   - Source を "GitHub Actions" に設定

2. **権限設定**
   - ワークフローには以下の権限が必要です（すでに設定済み）:
     - `contents: read`
     - `pages: write`
     - `id-token: write`

### デプロイ状況の確認

デプロイ状況は以下の方法で確認できます:

1. **GitHub Actions タブ**: リポジトリの Actions タブから "Deploy to GitHub Pages" ワークフローの実行状況を確認
2. **Environments**: リポジトリの Environments タブから `github-pages` 環境のデプロイ履歴を確認
3. **Settings → Pages**: GitHub Pages の設定画面でデプロイされた URL を確認
