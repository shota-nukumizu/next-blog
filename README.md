# Nextでブログアプリ

これは、Nextでブログアプリを開発したチュートリアルである。

# インストール方法

以下のコマンドを入力して、nextアプリを作成する。

```
npm init next-app next-blog
```

こちらで開発者サーバを立ち上げる。`http://localhost:3000/`にアクセスできたら成功。

```
npm run dev
```

# ページのナビゲーション

`pages`フォルダに新しく`posts`フォルダを作成して、その下に`first-post.js`を新規作成する。

`pages/posts/first-post.js`

```js
import Link from "next/link" // Nextではリンクを作成する際にはLinkライブラリを活用する

export default function FirstPost() {
    return (
        <>
            <h1>First Post</h1>
            <h2>
                <Link href="/">
                    <a>Back to Home</a>
                </Link>
            </h2>
        </>
    )
}
```

これで開発者サーバを立ち上げたら`http://localhost:3000/posts/first-post/`にアクセスできる。

# 開発環境

* Visual Studio Code 1.63
* Node.js 17.4.0