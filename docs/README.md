# LINE Mini App - 予約フォーム

**最終更新:** 2025年7月10日 20:47 (JST)

## 概要
LINE Mini App用の予約フォームアプリケーションです。

## 機能
- 氏名、学校名、学年の入力
- APIを通じた予約データの送信
- レスポンシブデザイン
- ローディング表示
- 完了メッセージ表示

## 技術仕様
- HTML5 + CSS3 + JavaScript (Vanilla)
- Fetch API使用
- レスポンシブ対応

## API設定
APIエンドポイントは `index.html` の `API_ENDPOINT` 定数で管理されています。

```javascript
const API_ENDPOINT = 'https://port7071.gamebox777.work/api/miniapp-api/reservations';
```

## ファイル構成
```
lineminiapp-dev/
├── docs/
│   └── README.md      # このファイル
├── index.html         # メインアプリケーション
├── .nojekyll          # GitHub Pages用設定ファイル
└── .gitignore
```

### .nojekyll について
GitHub Pagesでサイトを公開する際に、Jekyll処理をスキップするためのファイルです。

- **目的**: GitHubが自動的にJekyll（静的サイトジェネレータ）でページを処理することを防ぐ
- **効果**: HTMLファイルをそのまま配信する（Jekyllの変換処理なし）
- **配置**: リポジトリのルートディレクトリ
- **内容**: 空ファイル（存在するだけで効果を発揮）

このファイルがあることで、`index.html`が直接GitHub Pagesで配信されます。

## リポジトリ情報

### Gitリモートリポジトリ
```bash
origin  https://github.com/ccb-shinro-github/lineminiapp-dev.git (fetch)
origin  https://github.com/ccb-shinro-github/lineminiapp-dev.git (push)
```

- **リポジトリURL**: https://github.com/ccb-shinro-github/lineminiapp-dev.git
- **組織/ユーザー**: ccb-shinro-github
- **リポジトリ名**: lineminiapp-dev
- **デフォルトブランチ**: main

### GitHub Pages
このリポジトリは GitHub Pages で公開されています。

#### サイト情報
- **公開URL**: https://ccb-shinro-github.github.io/lineminiapp-dev/
- **デプロイソース**: `main` ブランチ
- **最終デプロイ**: @gamebox777 により5分前
- **ビルド方式**: pages build and deployment workflow

#### 設定詳細
- **HTTPSの強制**: 有効（デフォルトドメイン使用のため必須）
- **カスタムドメイン**: 設定可能（現在は未設定）
- **Jekyll処理**: 無効（`.nojekyll` ファイルにより）

#### アクセス方法
本番環境には以下のURLでアクセスできます：
```
https://ccb-shinro-github.github.io/lineminiapp-dev/
```

#### 注意事項
- `main` ブランチにプッシュすると自動的にサイトが更新されます
- HTTPSが強制されているため、セキュアな通信が保証されます
- `.nojekyll` ファイルにより、`index.html` がそのまま配信されます

## 開発メモ
- URLは定数化済み（変更が必要な場合は `API_ENDPOINT` を修正）
- バージョン: ver6
- プライバシーポリシーリンクは要更新 