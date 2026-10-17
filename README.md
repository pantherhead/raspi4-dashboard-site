# raspi4 Dashboard — public information site

公開してよい紹介ページのみを配置した独立ディレクトリです。
`dashboard/`、`collector/`、OAuth JSON、API キー、取得データは公開しないでください。

## 公開前の確認

- 記載した連絡先 `pantherhead@gmail.com` を公開してよいことを運営者が確認する。
- プライバシーポリシーが実際の運用と合致することを確認する。

## GitHub Pages の設定順

1. このディレクトリの内容だけで専用リポジトリ `raspi4-dashboard-site` を作成する。
2. Settings → Pages → Deploy from a branch → main / root を設定する。
3. カスタムドメイン利用前に、GitHub Settings → Pages でドメインを検証する（表示された DNS TXT を登録）。
4. リポジトリの Pages 設定に `raspi4-dashboard.pantherhead.com` を設定する。
5. DNS に CNAME `raspi4-dashboard` → `<GitHubユーザー名>.github.io` を登録する。
   プロジェクト名を CNAME の値に含めない。既存 raspi4 / raspi400 の DNS は変更しない。
6. Pages の DNS チェックと証明書発行が終わったら Enforce HTTPS を有効化する。
7. 外部からトップ・privacy.html が読めることを確認する。

GitHub Pages のカスタムドメイン設定時に CNAME ファイルが生成されます。
稼働中の Pages リポジトリから独自ドメイン設定を外すときは、DNS も適切に削除してください。

## Google Cloud

- アプリ名: `raspi4 Dashboard`
- ホームページ: `https://raspi4-dashboard.pantherhead.com/`
- プライバシーポリシー: `https://raspi4-dashboard.pantherhead.com/privacy.html`
- 利用規約（任意入力欄）: `https://raspi4-dashboard.pantherhead.com/terms.html`
- 承認済みドメイン: `pantherhead.com`

必要に応じて Google Search Console の DNS TXT 方式でドメイン所有権を確認する。
設定保存後 Audience で本番環境へ切り替え、Google 連携を再承認する。
紹介サイトの公開は個人データのあるダッシュボードの公開とは無関係。
