# nobody-zo.github.io

「もしもし」の Universal Links 用ホスト。

- `/.well-known/apple-app-site-association` … iOSに「このドメインのリンクはアプリで開いてOK」と教えるファイル（Team ID + Bundle IDのみ・公開情報）
- `/add` … 招待リンク `https://nobody-zo.github.io/add?u=<id>` のフォールバックページ（アプリ未インストールの人向け案内）
- `/` … zo-kikaku.com/moshimoshi へリダイレクト

zo-kikaku.com 本体は Framer（Basicプランは .well-known 配置不可）のため、ここに分離してホストしている。
Framer Pro 化 or 独自サブドメインに移行する場合は、アプリ側 `app.json` の `associatedDomains` と
`constants/config.ts` の `INVITE_LINK_BASE` を更新して再ビルドすること。
