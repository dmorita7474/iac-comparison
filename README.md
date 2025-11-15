# IaC Comparison with AI-Driven Development

AIコーディングエージェントによるInfrastructure as Code（IaC）開発の比較プロジェクト

## プロジェクト概要

このプロジェクトは、複数のAIコーディングエージェントを使用してAWS向けのIaC（Infrastructure as Code）を開発し、各エージェントの特性や違いを比較・検証することを目的としています。仕様駆動開発（Specification-Driven Development）フレームワークである[cc-sdd](https://github.com/gotalab/cc-sdd)を採用し、「要件 → 設計 → タスク → 実装」という構造化されたワークフローで開発を進めます。

## 対象AIコーディングエージェント

- **Claude Code** - Anthropic Claude を使用したCLIベースの開発エージェント
- **Codex CLI** - OpenAI Codex を使用したコマンドラインツール
- **Cursor** - AIペアプログラミングエディタ
- **Github Copilot Agent** - GitHub統合型のAIアシスタント

## 技術スタック

- **クラウドプロバイダ**: AWS
- **IaCツール**: Terraform（エージェント毎に選択）
- **開発フレームワーク**: cc-sdd（仕様駆動開発）
- **仕様形式**: EARS（Easy Approach to Requirements Syntax）

## プロジェクト構造

```
iac-comparison/
├── README.md                 # このファイル
├── .kiro/                    # cc-sdd仕様管理ディレクトリ
│   └── specs/               # 生成された仕様ファイル
├── claude/                   # Claude Code による実装
│   ├── docs/
│   ├── CLAUDE.md
│   └── （実装ファイル）
├── codex/                    # Codex CLI による実装
│   ├── docs/
│   ├── AGENTS.md
│   └── （実装ファイル）
├── cursor/                   # Cursor による実装
│   ├── docs/
│   ├── README.md
│   └── （実装ファイル）
└── github/                   # GitHub Copilot Agent による実装
│   ├── docs/
    ├── README.md
    └── （実装ファイル）
```

## cc-sdd ワークフロー

### 1. 初期化（spec-init）
プロジェクトの基本設定と初期化を行います。

```bash
npx cc-sdd spec-init
```

### 2. 要件定義（spec-requirements）
EARS形式で要件を定義します。

```bash
npx cc-sdd spec-requirements
```

### 3. 設計（spec-design）
アーキテクチャ図を含む詳細設計を作成します。

```bash
npx cc-sdd spec-design
```

### 4. タスク分解（spec-tasks）
依存関係を持つタスクに分解します。

```bash
npx cc-sdd spec-tasks
```

### 5. 実装（spec-impl）
各エージェントを使用して実装を実行します。

```bash
npx cc-sdd spec-impl
```

## 比較評価項目

各AIエージェントの評価は以下の観点で行います：

### 1. 開発効率
- 仕様から実装までの所要時間
- コード生成の速度
- 修正・デバッグの効率

### 2. コード品質
- IaCベストプラクティスへの準拠
- セキュリティ考慮
- 可読性・保守性
- ドキュメント品質

### 3. 仕様理解度
- 要件の正確な理解
- 設計意図の反映
- エッジケースの考慮

### 4. ユーザビリティ
- 対話性・インタラクション
- エラー処理と修正提案
- 学習曲線

### 5. 機能性
- 対応可能なIaCツールの範囲
- 複雑なインフラ構成への対応
- マルチサービス連携

## 使用方法

### 前提条件

- Node.js (v18以上)
- npm または yarn
- AWS CLI（認証情報設定済み）
- 各AIエージェントのセットアップ

### セットアップ

1. リポジトリのクローン
```bash
git clone <repository-url>
cd iac-comparison
```

2. cc-sddのインストール
```bash
npm install -g cc-sdd
```

3. プロジェクトの初期化
```bash
npx cc-sdd spec-init
```

### 開発の進め方

各エージェントディレクトリで独立して開発を進めます：

```bash
cd claude/  # または codex/, cursor/, github/
# 各エージェントの指示に従って開発
```

## ドキュメント

- [cc-sdd公式ドキュメント](https://github.com/gotalab/cc-sdd)
- 各エージェントディレクトリ内のREADME.md

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。詳細は[LICENSE](LICENSE)ファイルを参照してください。

## 貢献

Issue報告やプルリクエストを歓迎します。

## 関連リンク

- [cc-sdd GitHub](https://github.com/gotalab/cc-sdd)
- [Claude Code](https://claude.ai/code)
- [AWS](https://aws.amazon.com/)
