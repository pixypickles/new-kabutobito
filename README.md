# カブトビト大冒険

カブトムシ系の亜人「カブトビト」を操作する、ブラウザ向け横スクロールアクションゲームです。

## 遊び方

GitHub Pages を有効にすると `index.html` からそのまま遊べます。ローカルでも `index.html` をブラウザで開けば開始できます。

- ← → : 移動
- ↓ : しゃがむ
- ↑ : 上を見る
- A / Z / Space : ジャンプ（空中長押しで滑空）
- B : 角攻撃 / グローブ時はパンチ
- ↑ + B : 上方向へ攻撃

青い葉っぱは30枚につき、クリア時の最終ミス数を1回減らします。
一度クリアするとタイトル画面から2周目を開始できます。

## GitHub Pages

1. このフォルダの中身をリポジトリのルートへアップロードします。
2. GitHub の Settings → Pages を開きます。
3. Deploy from a branch を選び、`main` / `/ (root)` を指定します。
4. 公開されたURLへアクセスすると `index.html` が起動します。

## 構成

`index.html` がタイトル画面、`world1-1.html` ～ `world3-4.html` が各ステージです。セーブ・クリア・2周目の状態はブラウザの localStorage を使用します。


## v2 fixes
- Blue leaves use the same broad, veined blue-leaf artwork in every stage.
- Tree sap is shown in a labeled glass bottle in every stage.
- Fixed stage-clear routing, including WORLD 1-3 -> WORLD 1-4 and later worlds.

## v28 操作追加
- 前方向 + B: ホーンダッシュ（短距離の角突進）
- 空中で壁方向を入力したまま接触: 壁につかまる
- 壁につかまり中に A/Z: 壁ジャンプ
- 方向入力を離す: 壁から手を離す

※ 現段階では巨大樹ステージ化前の試作のため、既存の横壁を「つかまれる壁」として扱っています。今後、樹皮・木の幹だけに限定可能です。
