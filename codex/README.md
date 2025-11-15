# Codex CLI による IaC 実装

このディレクトリには、Codex CLI を使用して開発されたAWS IaCの実装が含まれます。

## Codex CLI について

Codex CLI は OpenAI の Codex モデルを活用したコマンドラインツールです。自然言語からコードを生成し、開発タスクを効率化します。

## 特徴

- **迅速なコード生成**: 簡潔なプロンプトから即座にコード生成
- **多言語対応**: 様々なプログラミング言語とIaCツールに対応
- **コマンドライン統合**: シェルスクリプトやCI/CDパイプラインとの統合が容易

## セットアップ

1. Codex CLI のインストール
```bash
npm install -g @openai/codex-cli
```

2. API キーの設定
```bash
export OPENAI_API_KEY="your-api-key"
```

## 開発ワークフロー

### 1. 仕様の確認
```bash
# cc-sdd仕様ファイルを参照
codex "仕様に基づいたインフラ構成を生成"
```

### 2. IaC実装
```bash
codex "AWS VPCとサブネットをTerraformで定義"
```

### 3. テストとデプロイ
```bash
terraform plan
terraform apply
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
codex/
├── README.md           # このファイル
├── main.tf            # Terraformメイン設定
├── variables.tf       # 変数定義
├── outputs.tf         # 出力定義
├── modules/           # モジュール
└── docs/              # ドキュメント
```

## 参考リンク

- [OpenAI Codex](https://openai.com/codex)
- [cc-sdd](https://github.com/gotalab/cc-sdd)
