# Claude Code による IaC 実装

このディレクトリには、Claude Code を使用して開発されたAWS IaCの実装が含まれます。

## Claude Code について

Claude Code は Anthropic の Claude モデルを活用したCLIベースの開発エージェントです。対話的なインターフェースを通じて、コード生成、リファクタリング、デバッグなどの開発タスクをサポートします。

## 特徴

- **対話的な開発体験**: 自然言語での対話を通じた開発
- **コンテキスト理解**: プロジェクト全体の構造を理解した提案
- **マルチファイル編集**: 複数ファイルにわたる変更の一括処理
- **高度な推論能力**: 複雑な要件の理解と実装

## セットアップ

1. Claude Code のインストール（必要に応じて）
```bash
npm install -g @anthropic-ai/claude-code
```

2. 認証設定
```bash
claude login
```

## 開発ワークフロー

### 1. 要件から設計への移行
```bash
# .kiro/specs/ 内の要件仕様を確認
claude code "要件を確認して設計を提案してください"
```

### 2. IaC実装
```bash
# cc-sddの仕様に基づいた実装
claude code "設計仕様に基づいてTerraformコードを生成してください"
```

### 3. レビューと修正
```bash
# 生成されたコードのレビュー
claude code "セキュリティベストプラクティスに準拠しているか確認してください"
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
claude/
├── README.md           # このファイル
├── main.tf            # Terraformメイン設定
├── variables.tf       # 変数定義
├── outputs.tf         # 出力定義
├── modules/           # モジュール
└── docs/              # ドキュメント
```

## 参考リンク

- [Claude Code ドキュメント](https://claude.ai/code)
- [cc-sdd](https://github.com/gotalab/cc-sdd)
