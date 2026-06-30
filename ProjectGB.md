<link rel="stylesheet" href="style.css">
<img src="sprite\mainKeyVisual_logo.png" width="750" alt="タイトル画像">

---

<br>

## 目次

| No. | セクション |
|:---:|---|
| 1 | [自己紹介](#1-自己紹介) |
| 2 | [作品概要](#2-作品概要) |
| 3 | [ゲーム紹介](#3-ゲーム紹介) |
| 4 | [担当コード](#4-担当コード) |
| 5 | [技術紹介](#5-技術紹介) |
| 6 | [今後の実装予定](#6-今後の実装予定) |


<br>

## 1. 自己紹介


<u><span style="font-size: 20px;"><b>名前</b></span></u>  
　　　　三好 爽太（みよし そうた）  

<u><span style="font-size: 20px;"><b>学校</b></span></u>  
　　　　河原電子ビジネス専門学校　ゲームクリエイター科  

<u><span style="font-size: 20px;"><b>メール</b></span></u>   
　　　　<a href="mailto:CA01244028@st.kawahara.ac.jp">CA01244028@st.kawahara.ac.jp  </a>

<br>

## 2. 作品概要  


### 📝 基本情報 
| 項目 | 内容 |
| :--- | :--- |
| **タイトル** | がぶっとバスター |
| **ジャンル** | 3D アクションゲーム |
| **制作人数** | 2人 |
| **制作期間** | 2026年3月 〜 現在 |
| **プレイ人数**| 1人 |
| **対応ハード**| PC（Windows 11） |
| **コントローラー** | Xbox 360 コントローラー |

<br>

### 🔗 リンク

|　項目　| リンク |
|---|---|
| **GitHub** | [miyosisouta/ProjectGB](https://github.com/miyosisouta/ProjectGB.git) |
| **YouTube** | [がぶっとバスターPV](https://youtu.be/hErKex9rLmE)|

<br>

### 🛠️ 使用ツール

| カテゴリ | ツール |
|---|---|
| **エンジン** | 学内エンジン（K2Engine） |
| **エディタ** | Visual Studio 2026 |
| **使用言語** | C++, HTML |
| **3D モデル** | 3ds Max 2026 |
| **エフェクト** | Effekseer |
| **画像編集** | Adobe Photoshop |
| **バージョン管理** | GitHub, Fork |

<br>


## 3. ゲーム紹介

### 🦍 ボス登場シーン

> アウトゲームにて挑戦するボスを選択できます。  
> 選択したボスを倒すことがゲームの目標です。

<img src="movie\BossAppearance.gif" width="560" alt="ボス1登場シーン">

---

### 🕹️ プレイヤーアクション

<br>
<u><span style="font-size: 20px;"><b>通常スキル</b></span></u>
<br>

| 噛みつき |
|:---:|
<img src="movie\PlayerNormalAttack.gif" width="370" alt="プレイヤーの通常攻撃"> |


<br>
<u><span style="font-size: 20px;"><b>特殊スキル</b></span></u>
<br>

| デフォルト攻撃 | 地雷 | 火魔法 |
|:---:|:---:|:---:|
<img src="movie\PlayerDefaultAttaack.gif" width="310" alt="プレイヤーの特殊攻撃"> | <img src="movie\PlayerLandMine.gif" width="310" alt="プレイヤーの地雷"> | <img src="movie\PlayerFireMagic.gif" width="310" alt="プレイヤーの火魔法"> |


<br>
<u><span style="font-size: 20px;"><b>汎用スキル</b></span></u>
<br>

> ダメージを受けるパターンと回避成功パターンの2種類を掲載しています。

| 回避（ダメージあり） | 回避（成功） |
|:---:|:---:|
<img src="movie\PlayerAvoidFailure.gif" width="370" alt="回避失敗"> | <img src="movie\PlayerAvoidSuccess.gif" width="370" alt="回避成功"> |


<br>

### 👾 ボスの攻撃パターン

| 通常攻撃 | 回転攻撃 | ヒットスタンプ |
|:---:|:---:|:---:|
<img src="movie\BossNormalAttack.gif" width="310" alt="ボスの通常攻撃"> | <img src="movie\BossSpinAttack.gif" width="310" alt="ボスの回転攻撃"> | <img src="movie\BossHitStamp.gif" width="310" alt="ボスのヒットスタンプ"> |

#### レーザー攻撃

| 通常 | 3連射 | チャージ |
|:---:|:---:|:---:|
<img src="movie\BossNormalLaser.gif" width="310" alt="レーザー通常"> | <img src="movie\BossMultLaser.gif" width="310" alt="レーザー3連射"> | <img src="movie\BossChargeLaser.gif" width="310" alt="レーザーチャージ"> |

---

### ⚙️ 設定

| 🔊 音量設定 | 🎮 キーコンフィグ | 📷 カメラ設定 |
|:---:|:---:|:---:|
<img src="movie\SoundSetting.gif" width="310" alt="音量設定"> | <img src="movie\KeyConfig.gif" width="310" alt="キー設定"> | <img src="sprite\UnderPreparation.png" width="310" alt="カメラ設定"> |

<br>

## 4. 担当コード

### 👤 プレイヤー
`Player` `PlayerState` `PlayerController`

### 👾 ボス
`BossCharacter` `BossState` `BossSpawner` `NPCController`

### 🏗️ 基底・共通
`Actor` `Character` `ActorStatus` `IState` `StateMachine` `CharacterDataBase` `AttackObject` `AttackObjectManager`

### 🎯 バトル
`BattleManager` `Mission` `MissionCondition` `MissionEvent` `MissionManager` `MissionType`

### ⚔️ スキル
`ISkill` `NormalAttack` `AbilityBase` `DefaultAttack` `Utility` `Bomb` `Magic`

### 💥 当たり判定
`GhostBody` `GhostBodyManager` `GhostPrimitive` `BroadphaseInterface` `BroadphaseImpl` `CollisionHitManager` `BoundingVolume` `PhysicalBody`

### 🎥 カメラ
`CameraCommon` `CameraController` `CameraManager` `CameraSteering`

### 🏔️ ステージ
`StageBase` `StageManager` `StaticObject`

### 🌾 草システム
`GrassBendManager` `GrassObject` `grass.fx` `RenderToBufferFor3DModel.fx` `DitherCBData`

### 🧩 コアシステム
`KeyConfig` `ParameterManager`

### 🖥️ UI
`UIManager`

### 🐛 デバッグ
`DebugGrassScene`

<br>


## 5. 技術紹介

### 🌾 1. 草システム

<br>
<u><span style="font-size: 18px;"><b>頂点シェーダーによるプロシージャルアニメーション</b></span></u>  
<br>

<span style="display:block;margin-bottom:0.5em;"></span> 

> - 地面が平らで何もないのが見た目的に寂しかったため、草を配置して自然なフィールドにしたいと思い実装しました。  
> - 時間経過で自然にもとに戻るようにしています。

<img src="movie\GrassBend.gif" width="350" alt="草が曲がる">  


<br>
<u><span style="font-size: 20px;"><b>なぜ頂点シェーダーか</b></span></u>
<br>

> - インスタンシング描画と頂点シェーダーの相性がいいため。
> - LODやデータ管理が非常にシンプルで済むため
> - GPUの処理が比較的軽かったため
---

<br>
<u><span style="font-size: 18px;"><b>LOD＋ディザリング＋インスタンシング</b></span></u>  
<br>

<span style="display:block;margin-bottom:0.5em;"></span> 


| 技術 | 採用理由 |
|:---|:---|
| LOD | 草のモデルが多くGPUの処理が重かったため、距離に応じてモデルを切り替えて負荷を下げた |
| ディザリング | LODでモデルを切り替えたときの境界が目立ったため、距離が遠いほどディザがかかるようにして切り替えを目立ちにくくした |
| インスタンシング | 300個以上の草をすべて個別に描画するとCPU側のドローコールが膨大になるため、一括描画で削減した |
| LOD ＋ ディザリング |LODでモデルを切り替えたときが目立ったので、カメラとの距離が遠いほど、ディザがかかるようにすることで目立ちづらくしました。|


<span style="display:block;margin-bottom:0.5em;"></span> 

| 近く | 遠い |
|:---:|:---:|
<img src="sprite\LOD.png" width="370" alt="近く"> | <img src="sprite\LOD2andDhithering.png" width="370" alt="遠い"> |

<br>

<u><span style="font-size: 16px;"><b>こだわった点</b></span></u>

> - 攻撃ごとの影響力、影響範囲などのパラメータをJSONで設定できるようにしました
> - 単発攻撃には `AddSource`、スピン攻撃など連続攻撃には `SetSource` とAPIを使い分けました

<br>

| 単発攻撃（AddSource） | スピン攻撃（SetSource） |
|:---:|:---:|
| <img src="movie\Grass_Single_Bend.gif" width="350" alt="単発攻撃の草曲げ"> | <img src="movie\Grass_Spin_Bend.gif" width="350" alt="スピン攻撃の草曲げ"> |

> - スピン攻撃用に固定スロット `SPIN_ATTACK_SLOT` を設けて他の攻撃と干渉しないようにしました
> - LOD0・LOD1のみ草曲げシェーダーを適用し、遠景のLOD2はデフォルトシェーダーで軽量化しました

---

### 🐛 2. 草用デバッグシーン

> 3dsMaxで1本ずつ手動配置するのは非効率で面白みがないため、ランダム生成とJSON書き出しができる専用シーンを作りました。  
> 納得いく配置が生成されたら JSON に書き出し、インゲームで読み込みます。

<div style="display: flex; gap: 24px; align-items: flex-start;">
  <img src="movie\DebugGrassCreate.gif" width="370" alt="草の再抽選デバッグシーン">
  <table>
    <tr><th>操作</th><th>内容</th></tr>
    <tr><td>F2</td><td>カメラを自由に操作</td></tr>
    <tr><td>J ボタン</td><td>草を再抽選して再配置</td></tr>
    <tr><td>K ボタン</td><td>現在の配置を JSON に書き出し</td></tr>
  </table>
</div>

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. ステージに配置した2点の座標から草を生成する範囲を計算する
> 2. その範囲内でランダムに座標を生成する
> 3. AABBで既存の草と重なりチェックを行う
> 4. 重ならなければ配置、重なれば再抽選する（無限ループ防止のため上限100回）
> 5. 300個分繰り返す
> 6. 納得いく配置が生成されたらJSONに書き出す
> 7. インゲームでJSONを読み込んで草を配置する

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>
<br>

> - AABBを使った重なり判定で草同士が重ならないように配置しました
> - エリアが狭い場合の無限ループを防ぐため、再抽選の上限を設けました
> - 草を消してから生成し直すまでに猶予時間を持たせ、見た目が不自然にならないようにしました

---

### 🎨 3. テクスチャブレンド（スプラットマップ）

> 草を実装した結果、地面が単色のままでは浮いて見えたため、複数テクスチャをブレンドして自然な地面にしました。  
> スプラットマップはペイントソフトで手書きし、明るさや彩度もパラメータで調整できるようにしました。

| チャンネル | テクスチャ |
|:---:|:---:|
| R（赤） | 草 |
| G（緑） | 岩土 |
| B（青） | 腐葉土 |

<div style="display: flex; gap: 24px; align-items: flex-start;">
  <div>
    <p><b>スプラットマップ</b></p>
    <img src="sprite/SplatMapData.png" width="400" alt="スプラットマップ">
  </div>
  <div>
    <p><b>適用前後</b></p>
    <img src="sprite/SplatMap_before.png" width="370" alt="適用前">
    <p>▲ 適用前</p>
    <br>
    <img src="sprite/SplatMap_after.png" width="370" alt="適用後">
    <p>▲ 適用後</p>
  </div>
</div>

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. ペイントソフトでRGBスプラットマップを手書きする（R=草・G=岩土・B=腐葉土）
> 2. `SetupSplatShader()` でスプラットマップと3種類のテクスチャをシェーダーに渡す
> 3. シェーダー側でスプラットマップのピクセルのRGB値を読み取る
> 4. RGB値の割合に応じて3種類のテクスチャをブレンドして描画する
> 5. 明るさ・彩度パラメータで色味を調整する

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>
<br>

> - `SetupSplatShader()` を `Init()` より前に呼ぶ設計にして、シェーダーのセットアップ順序を保証しました
> - 草・岩土・腐葉土の明るさと全体の彩度を個別にパラメータで調整できるようにしました

<br>

---

### 🔴 4. 攻撃予測インジケーターシステム

> エフェクトで円形を表現しようとすると引き延ばして使うことになり形が崩れてしまったため、専用のメッシュとシェーダーで実装しました。  
> またプレイヤーの攻撃かボスの攻撃か、自分が攻撃を受けるかどうかを見分けられるようにしたかったため実装しました。

| Circle | Line |
|:---:|:---:|
<img src="movie\DamageIndicator_Circle.gif" width="350" alt="Circleインジケーター"> | <img src="movie\DamageIndicator_Line.gif" width="350" alt="Lineインジケーター"> |

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. 攻撃ステートの `Enter()` で種類（Circle / Line / Box）・座標・サイズ・速度などのパラメータを設定して `AttackRange` を生成する
> 2. 生成時の `Start()` でメッシュとテクスチャを読み込み、種類に応じたシェーダーをセットして初期トランスフォームをモデルに反映する
> 3. 毎フレームの `Update()` でシェーダーパラメータを更新し、Circle はパルスリング拡大・Line は描画進捗・Box はタイリング値をそれぞれ計算して渡す
> 4. 攻撃予測フェーズが終わるタイミングでタスクラムダから `SetDraw(false)` または `DeleteGO` を呼んで非表示・削除する
> 5. 攻撃ステートの `Exit()` で `DeleteGO` を呼び、ステート中断時でもメモリリークが起きないよう確実に破棄する

<br>

<u><span style="font-size: 16px;"><b>実装した内容</b></span></u>

| 種類 | 内容 |
|:---|:---|
| Circle | 中心から外縁へ向かうパルスリングアニメーション（攻撃タイミングに同期して正確に外縁到達） |
| Line | ボスから対象方向へ徐々に伸びる描画進捗アニメーション（clip命令で先端をリアルタイム制御） |
| Box | 9スライス UV タイリング（サイズが変わってもテクスチャが崩れない） |

<br>

<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>
<br>

> - Circle はパルスリングアニメーションを加えることで、攻撃タイミングが視覚的にわかりやすくなるようにしました
> - Circle・Line・Box の3種類を用意することで、どのような攻撃形状にも対応できるようにしました
> - Line はただ瞬時に表示するのではなく、描画アニメーションを加えて視覚的な面白さを持たせました
> - 攻撃の予測時間に合わせて `pulseSpeed` を計算し、リングが攻撃発動タイミングで正確に外縁到達するよう同期しました

<br>

---

### 🎯 5. ミッションシステム

> ただ攻撃してボスを倒すだけでは単調なため、プレイヤーに目標を与えるミッションシステムを実装しました。  
> 新しいミッションを追加するときも、既存のコードを一切触らずに完結します。

<img src="sprite/MissionSystem.png" width="560" alt="ミッションシステム">

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. ボスの種類に応じて `MissionManager::InitByBossType()` でミッションを初期化する
> 2. プレイヤーやボスのアクションが発生したら `MissionManager::Notify〇〇()` でイベントを通知する
> 3. `MissionManager` が各 `Mission` にイベントを転送する
> 4. `Mission` が `MissionConditionBase` に条件チェックを委譲する
> 5. 条件を満たしたら1フレームだけ判定を行う用のフラグを立てて状態を `Cleared` に遷移させる
> 6. UIがフラグを読み取ってクリア演出を再生する

<br>

<u><span style="font-size: 16px;"><b>新ミッション追加手順</b></span></u>

> 1. `MissionType.h` の `MissionID` に新しいIDを1行追加
> 2. `MissionManager` の `SetupBoss()` に `AddMission` を1行追加
> 3. `MissionCondition.h` に条件クラスを追加（条件が新しい場合のみ）

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>
<br>

> - `MissionEventData` を使った疎結合設計で、Player・Boss はミッションの内部を知らなくていい作りにしました
> - `clearedThisFrame_` などの1フレーム限りフラグを丁寧に管理し、UIとのタイミングのずれが起きないようにしました

<br>

---

### 💥 6. 当たり判定パイプライン

> 攻撃の対象を柔軟に設定できるようにしたかったため、3段階で判定コストを最小化する仕組みを実装しました。

<img src="sprite/CollisionDetectionPipeline.png" width="560" alt="当たり判定">

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. Broadphase（広域判定）でBVH（2分木）を使って衝突候補のペアを絞り込む
> 2. オブジェクト1つ1つを球で包み、球同士が当たらなければ判定を弾く
> 3. 2でかなり候補を絞った上で、形状ごとに正確な衝突判定を行う
> 4. 衝突ペアを `CollisionHitManager` に登録する
> 5. 状態ごとの処理がやりやすいよう `Enter`・`Stay`・`Exit` の3段階に分ける
> 6. 状態に応じてダメージ処理や演出を実行する

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>
<br>

> - ビットマスクで攻撃属性と被弾属性を管理し、「誰の攻撃が誰に当たるか」を柔軟に設定できるようにしました
> - 形状タイプをID順に並べ替えることで、`Sphere vs Box` と `Box vs Sphere` の重複実装をなくしました
> - `Enter`・`Stay`・`Exit` の3状態管理で、ダメージ処理を一度だけ・継続・離脱時に実行できるようにしました

<br>

---

### ⚙️ 7. 攻撃タイムライン

> 攻撃ごとに毎回時間計算をUpdateに書くのが大変だったため、タイミングを秒数で一括管理できる `TaskSchedulerSystem` を利用して演出を実装しました。

<img src="sprite/TaskScheduler.png" width="560" alt="ステートタスクスケジュール">

<br>

<u><span style="font-size: 16px;"><b>活用した内容</b></span></u>

> - ヒットスタンプ攻撃では「準備 → 上昇 → 空中待機 → 急降下 → 着地」の各フェーズの切り替えタイミングを秒数で管理しました
> - レーザー攻撃では「予測 → 発射 → 連射」の間隔をタイマーで制御し、攻撃パターンごとに時間を変えています

<br>

---

### ⚙️ 8. 重み付き抽選AI

> ただ攻撃してくるだけでは単調なため、距離別に攻撃の発動率を設定して行動パターンに変化を持たせました。

<img src="sprite/WeightedLottery.png" width="560" alt="重み付き抽選AI">

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. プレイヤーとの距離を計算し、近距離・中距離・遠距離・射程外の4段階に分類する
> 2. 距離に対応した攻撃パターンリストを取得する
> 3. 0〜9の乱数を生成し、各攻撃の重みを累積して比較する
> 4. 乱数が累積値を下回った時点でその攻撃に決定し、ボスのステートを切り替える
> 5. ステートが終わったら待機（Idle）を挟んで次の行動を選び直す

<br>

<u><span style="font-size: 16px;"><b>この設計で生じるメリット</b></span></u>

> - 距離によって行動パターンが変化するため、プレイヤーが一定の位置にいると単調にならない
> - 重みの数値を変えるだけで攻撃頻度を調整できるため、バランス調整が容易
> - 新しいボスを追加する際は攻撃ルールを1つ追加するだけで対応できる
> - ボス本体のコードを一切変えずにAIの行動パターンを変更できる

<br>

---

### ⚙️ 9. カメラブレンドシステム

> ボス登場シーンからゲームプレイへ切り替わる際にカメラが瞬間移動すると違和感があるため、時間を指定してなめらかに遷移できるようにしました。

<img src="sprite/CameraBlend.png" width="560" alt="カメラブレンド">

<br>

<u><span style="font-size: 16px;"><b>処理の流れ</b></span></u>

> 1. `SwitchCamera()` でカメラの切り替えを要求し、ブレンド時間を指定する
> 2. ブレンド開始時点のカメラ位置・ターゲット・視野角を保存する
> 3. 毎フレーム経過時間をブレンド時間で割り、0〜1の補間値を計算する
> 4. `CameraData::Lerp()` で現在のカメラと切り替え先のカメラを線形補間する
> 5. 補間値が1.0に達したら切り替え完了とし、新しいカメラをアクティブにする

<br>

<u><span style="font-size: 16px;"><b>この設計で生じるメリット</b></span></u>

> - ブレンド時間を引数で指定するだけでどのカメラ切り替えにも対応できる
> - `ICameraController` インターフェースを挟んでいるため、新しいカメラを追加しても既存コードを変更しなくていい
> - 位置・ターゲット・視野角をすべて補間しているため、どんな角度からの切り替えでも自然に見える

<br>

## 6. 今後の実装予定

- 非同期にする
- 敵のAIの強化
- 感情システム（ボスとの駆け引きをさらに面白くする中核要素として実装中）

---

[目次へ戻る](#目次)