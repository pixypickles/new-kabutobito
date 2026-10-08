## v38
- v36ベースでグローブを安全に無効化（描画・ゲーム進行コードは極力維持）
- グローブ配置は青い葉へ置換
- B攻撃は角攻撃に統一

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

## v31 update
- Fixed Horn Dash velocity being overwritten by normal movement on the next frame.
- Command remains: forward, release, forward, then B within the short input window.
- During Horn Dash, speed is locked at 10.8 for the full dash duration.

v35: ホーンダッシュ時も通常時の丸い頭・丸い胴体の比率を維持。角は額から生える湾曲したカブト角に戻し、脚は空中で後方へ流す専用ポーズに修正。


## v35 horn-dash pose
Horn Dash now uses a horizontal airborne pose while preserving the hero’s compact round head and torso. The curved beetle horn grows naturally from the forehead and points forward; limbs trail in the air.

## v39 test
- WORLD 1-1 only: added vertical camera follow test.
- Added a staircase of high ledges around the early-middle section for climbing tests.
- Other stages and core actions are unchanged from v38.


v41: WORLD 1-1 forest systems: removed stump/pipe stag beetles, added flying stag-beetle folk, horn-reactive sap bark patches with direct tree sap, and branch-grown blue berries worth 5 blue leaves.


v43: WORLD 1-1 flying stag smaller; horizontal forward mandibles; walking/flying stags share normal/dash horn throw/destroy rules.


v44: 1-1 flying beetles now rhinoceros beetles, forward horn; climbable vines (hold up, climb up/down, jump off); improved dash hit sweep.


v45: 1-1のツルの上端に幹につながる木の枝を描画。飛行カブトムシは茶・琥珀色へ変更。歩行クワガタのアゴを胴体と同じ紫色に変更。

v46: 1-1ゴールを巨大な幹の洞へ変更。歩行クワガタの顔を紫系へ。大角ダッシュの破壊判定を入力直後にも保持。

v47: 1-1のテントウムシを大角ダッシュで破壊。1-2を巨大樹の斜め上ルート・ツル・森の敵に改造。

v48: 1-3は巨大樹の幹を真上へ登る縦スクロールステージ。枝24段、ツル4本、最上部ゴールから1-4へ。

v49: 1-1→1-2→1-3の大角・青角引継ぎを修正。1-3の枝24段を復旧し、飛行カブトムシ3体、歩行クワガタ3体、テントウムシ3体を配置。
