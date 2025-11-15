# GitHub Copilot Agent による IaC 実装

このディレクトリには、GitHub Copilot Agent を使用して開発されたAWS IaCの実装が含まれます。

## GitHub Copilot Agent について

GitHub Copilot Agent は GitHub に統合されたAIアシスタントで、コード生成、説明、デバッグなど幅広い開発タスクをサポートします。VS Code や GitHub.com から直接利用できます。

## 特徴

- **GitHub統合**: リポジトリやイシューとの密接な連携
- **コード補完**: リアルタイムのインテリジェントな提案
- **チャット機能**: 対話的な問題解決
- **PR支援**: プルリクエストのレビューと改善提案
- **セキュリティスキャン**: 脆弱性の自動検出

## セットアップ

### VS Code での利用

1. GitHub Copilot 拡張機能のインストール
```bash
code --install-extension GitHub.copilot
code --install-extension GitHub.copilot-chat
```

2. GitHub アカウントでサインイン
   - VS Code のステータスバーから認証

### GitHub.com での利用

1. リポジトリページで Copilot チャットを開く
2. @copilot でエージェントを呼び出し

## 開発ワークフロー

### 1. 仕様の確認
```
@copilot .kiro/specs/ の要件を確認してインフラ設計を提案
```

### 2. IaC実装
```
@copilot Terraformで以下のAWSリソースを実装:
- VPC
- サブネット
- EC2
```

### 3. コードレビュー
```
@copilot このTerraformコードをレビューしてセキュリティ上の問題を指摘
```

## 実装予定

- [ ] VPC設定
- [ ] EC2インスタンス設定
- [ ] RDS設定
- [ ] S3バケット設定
- [ ] IAMロール・ポリシー設定
- [ ] セキュリティグループ設定

## 評価メトリクス

### 開発効率
- 実装開始時刻: [TBD]
- 実装完了時刻: [TBD]
- 合計所要時間: [TBD]

### コード品質
- ベストプラクティス準拠: [評価待ち]
- セキュリティ考慮: [評価待ち]
- 可読性: [評価待ち]

### 特記事項
- [開発中に気づいた点や特徴を記録]

## ファイル構成

```
github/
├── README.md           # このファイル
├── main.tf            # Terraformメイン設定
├── variables.tf       # 変数定義
├── outputs.tf         # 出力定義
├── modules/           # モジュール
└── docs/              # ドキュメント
```

## GitHub Copilot のコマンド

- `/explain`: コードの説明
- `/fix`: エラーの修正提案
- `/tests`: テストコードの生成
- `/doc`: ドキュメント生成

## 参考リンク

- [GitHub Copilot](https://github.com/features/copilot)
- [Copilot ドキュメント](https://docs.github.com/copilot)
- [cc-sdd](https://github.com/gotalab/cc-sdd)
