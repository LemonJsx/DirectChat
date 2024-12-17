# リアルタイムチャット機能
## 機能
現代のDM機能のような、ほかの人との対話ができるものを想定とする。
Next.jsとSupabaseを使用し、Dockerによる環境構築を行う

```mermaid
graph TD
    A[スタート] --> B[ログインボタンをクリック]
    B --> C[GitHub OAuth認証]
    C -->|ログイン成功| D[メッセージ投稿ページを表示]
    C -->|ログイン失敗| J[終了]
    D --> F[メッセージを入力して送信]
    F --> G[Supabaseにメッセージを保存]
    G --> H[メッセージリストを更新]
    H --> I[ログインアウトボタンを押しサインアウト]
    I --> J[終了]
````



# 仮
## 構築
まずは、適当なディレクトリを作成し、添付されているcompose.yml, Dockerfileを配置。

## ファイルを配置された以降の手順
1. docker compose build
2. docker compose run --rm app npx create-next-app@latest .
    2.のコマンド入れた後に選択する選択。
    - Would you like to use TypeScript? ... Yes
    - Would you like to use ESLint? … Yes
    - Would you like to use Tailwind CSS? … Yes
    - Would you like to use `src/` directory? … Yes
    - Would you like to use App Router? (recommended) … Yes
    - Would you like to customize the default import alias (@/*)? … No
3. docker compose up  # 起動

### 参考
URL: https://yasdtech.com/blog/i10869kx7tv 

URL: https://www.youtube.com/watch?v=-xXASlyU0Ck&t=478s&ab_channel=DailyWebCoding
