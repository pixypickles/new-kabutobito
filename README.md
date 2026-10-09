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

v50: 1-3の細い枝は一方通行足場。下から通過可能、横から壁つかまり不可、上から着地可能。

v51: 全12ステージの細い足場(ledges)を一方向足場に統一。下から通過、上から着地、横から壁つかまり不可。太い地面や障害物は従来どおり。季節構成は次回以降の制作方針（春・夏・秋・冬）として提案。


v52 春のワールド1：1-1〜1-4に春の若葉色、桜色の花、舞う花びらを追加。足場・操作・敵の判定はv51を維持。1-4の旧城ステージ構造は現状維持。

v53: 春ワールド1-1〜1-4のクワガタ・飛行カブトムシを蝶々の人の姿へ変更（当たり判定と移動は従来のまま）。背景の大きな葉と幹の葉を黄緑色に調整。夏ワールド2は未変更。

v54: 春の蝶は飛行のみ・上下にひらひら移動、歩行敵は若草色のイモムシ人へ。1-3の最上段は横道から巨木の洞へゴール、両端に掴める幹。

v55: 春の敵を色違いの蝶々5種とテントウムシへ。敵の踏みつけで高くバウンド、当たり判定縮小。1-1延長と蝶増量。1-2を始点・終点・中間3枝のみの空中ステージにし、斜めに流れる一方通行の葉と蝶で渡る。

v56: 春のテントウムシは元からいるキャラのみ。蝶々は低速・接触無害・下に落とす鱗粉で約2秒行動停止。1-2の背景を淡い桜色、乗れる葉を濃い桃色に変更。

v57: 春1-1〜1-3の踏みつけ跳躍を控えめに。1-2は背景を若葉の緑に戻し、乗れる葉のみピンク。葉は水平を保ち、斜め下へ一方向に流れて画面下で再登場。


v58: 1-1〜1-3の蝶々は接触無害（踏みつけは可能、鱗粉はしびれる）。1-2の空中足場を水平の巨大桜の花びらに変更し、52枚を独立したランダム位置・速度で連続的に斜め落下させる。

v59: 大角の体色を濃く。1-2の蝶を上空で高さ違いに配置、足場を桜花弁の切れ込み形状へ。1-3に外壁の張り出し枝、中央の縦幹、左樹液・右蝶3匹の分岐を追加。


v60: Spring stages 1-1..1-3: mint-green old berry; large green horn-hit selector fruit cycles red/blue/yellow, touch to equip. Only one elemental horn at a time, persistent across stages until death. Red strengthens normal horn to dash level and dash one further level; blue speeds walking; yellow increases jumps.


v61: Attribute horn colors now remain visible during normal movement as well as horn dash (World 1-1 to 1-3). World 1-2 falling platforms redrawn as single notched cherry-blossom petals.


v62: Smaller, less crowded side-profile sakura petal platforms in 1-2; 1-3 sap attached to the center trunk and an extended upper climbing section with branches and butterflies.


v63: Spring beehives in World 1-1 through 1-4. Contact triggers three pursuing worker bees; untouched hives remain peaceful. World 1-4 has many hives and an aerial queen bee boss with periodic worker summons and straight diagonal stinger dives. Queen takes five hits; defeating her opens the gate.


v64: Removed early beehives near spawn/sap, removed all 1-2 hives and added three floating workers; horn attacks can defeat bees. 1-3 outer trunk boundary clamps the player inside the course.


v65: Hive workers emerge one by one at 22-frame intervals, and bees are rendered in the foreground over tree trunks. Pending workers cannot be hit before they appear.


v66: World 1-4 rebuilt as open spring forest athletics (no castle switches/guards), with straight-line worker bees, five spaced hives, and queen summoning one bee at a time less often. World 1-1 to 1-3: finer shimmering pollen and electric stun effects.


v67: brighter fine pollen in all three spring stages. World 1-4: no castle blocks, forest trunk obstacles, butterfly decorations and straight bees; normal hive contact warns then releases 3 bees, horn dash drops hive and spawns 5 bees rising from below; queen worker summons slowed.


v68: Rebuilt 1-4 branch obstacle course based on 1-1, with varied upper/lower detours and narrow routes. Removed surprise straight-line bees. Hives in 1-1, 1-3 and 1-4 fall to horn dash and release five delayed bees from below; ordinary touch releases three after a warning. 1-2 deliberately remains hive-free.


v69: World 1-4 rebuilt with seven collision-solid branch barricades, alternating low/high/middle passageways, climbing ledges and hives guarding each narrow passage. The route can no longer be cleared by simply walking underneath or jumping over every obstacle.


v70: World 1-2 adds buffered/coyote jumps and carries the player with descending petals. World 1-4 opens alternate hive-avoidance paths, uses the same butterfly-person sprite as 1-1 through 1-3, and adds eight sap/leaf pickups.


v71: World 1-4 alternating low/high solid branches with tight detours; sap droplets grow from bark instead of bottles; queen movement smoothed and stinger-only contact hitbox; humanoid spear/stinger bees; spring butterflies shed sparkling pollen with electrical stun effect.


v72: 1-4 butterflies can be defeated with horn attacks and stop producing pollen once defeated. 1-4 sap now appears by horn-scraping bark on solid trunks, matching 1-1/1-3. 1-1 and 1-3 hive dash detection moved after the horn hitbox is computed, with falling hive and staggered five-bee response.


v73: Shared anthropomorphic spear-carrying worker-bee sprite across 1-1 to 1-4; 1-4 bark scars repositioned and rendered in front of trunks; queen stinger removed, queen now wanders smoothly toward randomized aerial waypoints and attacks only by periodically summoning one worker bee.


v74: Queen bee in 1-4 now fires aimed stinger projectiles from her abdomen while remaining harmless on body contact. World 2-1 built anew on the World 1-1 horizontal forest framework: summer green canopy, sunflowers, cicadas, anthropomorphic dragonflies, no spring pollen, and one early elemental selector berry.


v75: 1-3 boundary clamps preserve wall-grabbing. Summer 2-1 dragonflies no longer flutter or drop pollen; they detect nearby player and charge in a straight line with contact damage, while horn reach remains unchanged. Summer cicadas perch, take off when approached, drop three falling droplets, and escape.


v76: World 1-4 butterflies and queen bee can now be stomped from above, with bounce and defeat; queen remains harmless on ordinary body contact. World 2-1 dragonflies redrawn in side profile with elongated horizontal body, visible large side eye, legs, and four paired symmetrical wings.


v77: Redesigned summer dragonfly wings: four anatomically grouped, distinct tapered wings, two on each side of the thorax with separated roots, no intersecting ellipse propeller shapes.


v79: Color berries moved to starting ground; dispersed falling platforms with some horizontal right-to-left platforms; summer 2-2 green leaves, dragonflies and cicadas. Improved stomps against enemies coming from below.


v80: Queen stinger projectiles are stopped by tree trunks, obstacles and branches. World 2-3 is a summer vertical climbing course using 1-3's wall-climb layout, with summer canopy, sunflowers, flying metallic-green beetles (kanabun), and stag-beetle enemies on branches.


v81: World 2-3 stag beetles walk back and forth on their branches and cannot be stomped because of their upward mandibles; horn attacks still defeat them. Flying kanabun spot the player and charge directly, dealing contact damage during the charge.


v82: World 2-4 rebuilt from the summer World 2-1 forest: three mandatory one-on-one stag-beetle miniboss duels (3 horn hits each) and a final king stag boss (7 hits). Each duel seals the arena with tree barriers until victory. Stag beetles telegraph straight charges, pause to recover, and cannot be safely stomped because their pincers point upward. The exit unlocks only after all four fights.


v83: All four stag-beetle duel arenas in World 2-4 have continuous solid floors; no gaps inside the locked battles.


v84: World 2-4 stag minibosses and final boss visibly rotate 90 degrees for horizontal pincer-first charges. They telegraph by crouching/shaking with an exclamation point, then freeze briefly after charging. Body contact is harmless at all times; only forward pincers during active charges damage the player.
