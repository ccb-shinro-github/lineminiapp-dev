# LINE Mini App - 予約フォーム

**最終更新:** 2025年7月10日 21:15 (JST)

## 概要
LINE Mini App用の予約フォームアプリケーションです。

**LIFFアプリ情報:**
- **アプリ名**: 入力フォーム
- **LIFF ID**: 2007366489-ZaL835MB
- **LIFF URL**: https://liff.line.me/2007366489-ZaL835MB
- **サイズ**: Full（フルスクリーン表示）

## 機能
- 氏名、学校名、学年の入力
- APIを通じた予約データの送信
- レスポンシブデザイン
- ローディング表示
- 完了メッセージ表示
- **LIFF自動クローズ**: 予約完了後、3秒で自動的にアプリが閉じます
- **トークメッセージ送信**: 予約完了後、LINEトーク画面に予約内容を自動送信

## 技術仕様
- HTML5 + CSS3 + JavaScript (Vanilla)
- Fetch API使用
- レスポンシブ対応
- **LIFF SDK v2**: LINE Mini App機能（自動クローズ等）

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

## LIFF設定
LIFF IDは `index.html` 内で設定済みです：
```javascript
const LIFF_ID = '2007366489-ZaL835MB'; // 入力フォーム (Full)
await liff.init({ liffId: LIFF_ID });
```

**アクセス方法:**
- **LINE内からアクセス**: https://liff.line.me/2007366489-ZaL835MB
- **GitHub Pages**: https://ccb-shinro-github.github.io/lineminiapp-dev/

**自動クローズ機能:**
- 予約完了後、3秒で自動的にアプリが閉じます
- OKボタンクリックでも即座に閉じます
- LIFF環境外では従来通りメッセージ非表示のみ

## トラブルシューティング

### メッセージが表示されない場合

1. **LIFF IDの設定確認**
   ```javascript
   const LIFF_ID = '2007366489-ZaL835MB'; // 設定済み
   ```

2. **テスト環境の確認**
   - ブラウザで直接開いていませんか？
   - LINEアプリ内からアクセスしてください

3. **デバッグ用設定**
   ```javascript
   const ENABLE_TEST_MODE = true; // テスト用モードを有効化
   ```

4. **コンソールログの確認**
   - ブラウザの開発者ツールでエラーを確認
   - LIFF初期化状況をチェック

### LIFFアプリの管理
1. **LINE Developers コンソール**: https://developers.line.biz/console/
2. **現在の設定**: LIFF ID `2007366489-ZaL835MB` で設定済み
3. **サイズ**: Full（フルスクリーン表示）
4. **エンドポイントURL**: GitHub Pages URL 