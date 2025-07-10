# LINE Mini App - 予約フォーム

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
└── .gitignore
```

## 開発メモ
- URLは定数化済み（変更が必要な場合は `API_ENDPOINT` を修正）
- バージョン: ver6
- プライバシーポリシーリンクは要更新 