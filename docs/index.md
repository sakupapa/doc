# MyAgent ドキュメントポータル

ようこそ！このポータルでは、各種機能の使い方や連携手順について解説しています。

!!! info "お知らせ"
    本ドキュメントは GitHub Pages にて公開されています。

## 主な機能

- **カレンダー連携**: 今日の会議や空き時間の即時確認
- **メール要約**: 重要メール・未読メールの自動抽出
- **Webex自動化**: スペースの会話要約やフォローアップ通知

## クイックスタート

=== "Webex 経由"
    ```text
    @MyAgent 今日のスケジュールを教えて
    ```

=== "REST API 経由"
    ```bash
    curl -X POST https://api.example.cisco.com/v1/chat \
      -H "Authorization: Bearer $TOKEN" \
      -d '{"prompt": "今日の予定"}'
    ```

## 関連リンク

| リソース | リンク | 備考 |
|---|---|---|
| ソースコード | [GitHub Repository](https://github.com/) | リポジトリ |
| サポート | Webex Space | 質問・問い合わせ |
