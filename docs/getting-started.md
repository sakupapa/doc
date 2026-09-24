# Getting started

このページの構成について

## はじめに

- **カレンダー連携**: 今日の会議や空き時間の即時確認
- **メール要約**: 重要メール・未読メールの自動抽出
- **Webex自動化**: スペースの会話要約やフォローアップ通知

## 次に

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

