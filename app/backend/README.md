# Todo Backend API

FastAPIを使用したTodoアプリケーションのバックエンドAPIです。

## セットアップ

1. 仮想環境の作成と有効化:
```bash
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

2. 依存関係のインストール:
```bash
pip install -r requirements.txt
```

3. サーバーの起動:
```bash
uvicorn main:app --reload
```

APIドキュメントは http://localhost:8000/docs で確認できます。

