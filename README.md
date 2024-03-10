# Flutter 実践開発

## 第６章 実践ハンズオン

- 画像編集アプリを開発

# Memo

## Flutter で Android の画像ライブラリにアクセスする

- **パーミッションの設定**: Android デバイスの画像ライブラリにアクセスするためには、適切なパーミッションが必要です。`AndroidManifest.xml`に以下のパーミッションを追加します。

  ```xml
  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
  ```

  Android 10 (API レベル 29)以降、`READ_EXTERNAL_STORAGE`パーミッションの代わりに、scoped storage を利用することが推奨されています。そのため、特定のパーミッションをリクエストする必要がなくなりますが、`AndroidManifest.xml`に以下を追加することで、アプリが画像やメディアファイルにアクセスできることを示します。

  ```xml
  <application
      ...
      android:requestLegacyExternalStorage="true">
  ```
