# 詳細編（Advanced Guide）

このドキュメントでは、環境変数の設定、本番環境向けのビルド、およびトラブルシューティングについて解説します。

## 環境変数の設定（.env）

プロジェクトのルートディレクトリに `.env` ファイルを作成し、必要な環境変数を定義してください。

| 変数名 | 説明 | デフォルト値 |
| :--- | :--- | :--- |
| `API_BASE_URL` | バックエンドAPIの基底URL | `http://localhost:8080/api` |
| `TIMEOUT_MS` | APIリクエストのタイムアウト時間（ミリ秒） | `5000` |
| `ENABLE_LOGS` | 詳細ログの出力フラグ (`true` / `false`) | `false` |

```env
# .env の記述例
API_BASE_URL=https://example.com
TIMEOUT_MS=3000
ENABLE_LOGS=true
```

## 本番環境向けのビルド

本番環境にデプロイするための最適化されたファイルを生成するには、以下のコマンドを実行します。

```bash
npm run build
```

コマンドが成功すると、ルートディレクトリに `dist/` フォルダが生成されます。このフォルダ内の静的ファイルをWebサーバーに配置してください。

## トラスブルシューティング

### 依存関係の競合エラーが発生する場合

`npm install` 時にエラーが出る場合は、一度キャッシュをクリアして再試行してください。

```bash
# キャッシュのクリアと再インストール
rm -rf node_modules package-lock.json
npm install
```
