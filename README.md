# ninomaedev.github.io

公開しているアプリの**サポート窓口と規約**を置く静的サイト。
作品紹介や記事は [ninomae-renichi.com](https://ninomae-renichi.com/) 側にまとめているので、ここでは扱わない。

GitHub Pages（`main` ブランチのルートをそのまま配信）。ビルドは無し。push すると反映される。

## 構成

```
/                              公開アプリのサポート窓口（一覧）
/questodo/                     QuesToDo のサポートページ
/privacy.html                  QuesToDo プライバシーポリシー（日英）
/app-ads.txt                   AdMob 用
/portfolio/index.html          QuesToDo 開発ポートフォリオ
/portfolio/mobile-tech-guide.html
/portfolio/app-starter-guide.html
```

## 動かしてはいけない URL

次の3つは外部に登録済みで、**パスを変えると壊れる**。

| URL | どこに登録されているか |
| --- | --- |
| `https://ninomaedev.github.io` | App Store Connect のサポートURL・マーケティングURL |
| `https://ninomaedev.github.io/privacy.html` | App Store Connect のプライバシーポリシーURL、および App Store の説明文本文 |
| `https://ninomaedev.github.io/app-ads.txt` | AdMob（仕様上ホスト直下にしか置けない） |

`privacy.html` のURLは、審査1回目の却下（Guideline 3.1.2）を解消するために説明文へ直接書いたもの。
移動・改名すると同じ却下が再発する。

## アプリを追加するとき

1. `/<アプリ名>/index.html` を作る（`/questodo/index.html` をひな形にする）
2. そのアプリのプライバシーポリシーを `/<アプリ名>/privacy.html` に置く
   - QuesToDo だけ例外でルート直下（上記の理由）
3. ルートの `index.html` の「公開中のアプリ」にカードを1枚足す
4. App Store Connect のサポートURL・プライバシーポリシーURLに、作ったURLを登録する

## 注意

- 問い合わせ先はアプリごとに `ninomae.contact+<アプリ名>@gmail.com` のエイリアスを使う。
  どこから届いたメールかを切り分けられる（App Store 掲載のアドレスは収集される）。
- ビルドツールを入れない。HTML/CSS を直接書く。
