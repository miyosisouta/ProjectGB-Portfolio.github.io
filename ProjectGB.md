<link href="style.css" rel="stylesheet" />

<img src="sprite\mainKeyVisual_logo.png" width="600" alt="タイトル画像">

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
| **制作人数** | 3人 |
| **制作期間** | 2026年3月 〜 現在 |
| **プレイ人数**| 1人 |
| **対応ハード**| PC（Windows 11） |
| **コントローラー** | Xbox 360 コントローラー |

<br>

### 🔗 リンク

|　項目　| リンク |
|---|---|
| **GitHub** | [miyosisouta/ProjectGB](https://github.com/miyosisouta/ProjectGB.git) |
| **YouTube** | （動画投稿後に追記予定） |

<br>

### 🛠️ 使用ツール

| カテゴリ | ツール |
|---|---|
| **エンジン** | 学内エンジン（K2Engine） |
| **エディタ** | Visual Studio 2022 |
| **使用言語** | C++, HTML |
| **3D モデル** | 3ds Max 2025 |
| **エフェクト** | Effekseer |
| **画像編集** | Adobe Photoshop |
| **バージョン管理** | GitHub, Fork |

<br>


## 3. ゲーム紹介

### 🦍 ボス登場シーン

> アウトゲームにて挑戦するボスを選択できます。  
> 選択したボスを倒すことがゲームの目標です。

| ゴリラ |
|:---:|
<img src="movie\BossAppearance.gif" width="300" alt="ボス1登場シーン"> 

---

### 🕹️ プレイヤーアクション

<br>
<u><span style="font-size: 20px;"><b>通常スキル</b></span></u>  
<br>

#### 噛みつき

<img src="movie\PlayerNormalAttack.gif" width="450" alt="プレイヤーの通常攻撃">


---
<br>
<u><span style="font-size: 20px;"><b>特殊スキル</b></span></u>  
<br>

#### デフォルト攻撃

<img src="movie\PlayerDefaultAttaack.gif" width="450" alt="プレイヤーの特殊攻撃">

#### 地雷

<img src="movie\PlayerLandMine.gif" width="450" alt="プレイヤーの地雷">

#### 火魔法

<img src="movie\PlayerFireMagic.gif" width="450" alt="プレイヤーの火魔法">


---
<br>
<u><span style="font-size: 20px;"><b>汎用スキル</b></span></u>  
<br>

#### 回避

> ダメージを受けるパターンと回避成功パターンの2種類を掲載しています。

| ダメージあり | 回避成功 |
|:---:|:---:|
<img src="movie\PlayerAvoidFailure.gif" width="300" alt="回避失敗"> | <img src="movie\PlayerAvoidSuccess.gif" width="300" alt="回避成功"> |


---
<br>

### 👾 ボスの攻撃パターン

#### 通常攻撃

<img src="movie\BossNormalAttack.gif" width="450" alt="ボスの通常攻撃">


#### 回転攻撃

<img src="movie\BossSpinAttack.gif" width="450" alt="ボスの回転攻撃">


#### ヒットスタンプ

<img src="movie\BossHitStamp.gif" width="450" alt="ボスのヒットスタンプ">


#### レーザー攻撃

| 通常 | 3連射 | チャージ |
|:---:|:---:|:---:|
<img src="movie\BossNormalLaser.gif" width="300" alt="レーザー通常"> | <img src="movie\BossMultLaser.gif" width="300" alt="レーザー3連射"> | <img src="movie\BossChargeLaser.gif" width="300" alt="レーザーチャージ"> |

---

### 🔊 音量設定

<img src="movie\SoundSetting.gif" width="450" alt="音量設定">

<br>

---

###  🎮 キーコンフィグ

<img src="movie\SoundSetting.gif" width="450" alt="キー設定">

<br>

---

### 📷 カメラ

<img src="movie\SoundSetting.gif" width="450" alt="カメラ設定">

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

<img src="movie\GrassBend.gif" width="280" alt="草が曲がる">  

---

<br>
<u><span style="font-size: 18px;"><b>LOD＋ディザリング＋インスタンシング</b></span></u>  
<br>

<span style="display:block;margin-bottom:0.5em;"></span> 

> 〇 草の描画処理によりFPS低下があったため以下の内容を実装しました。
> - カメラからの距離に応じて、モデルの切り替えとディザリングを行っています。  
> - 300個以上の草が作成しているのでインスタンシング描画を行っています。

<span style="display:block;margin-bottom:0.5em;"></span> 

| 近く | 遠い |
|:---:|:---:|
<img src="sprite\LOD.png" width="300" alt="近く"> | <img src="sprite\LOD2andDhithering.png" width="300" alt="遠い"> |

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>  
<br>

> - 攻撃ごとの影響力、影響範囲などのパラメータを設定できるようにしました。
> - 攻撃ごとにパラメータがあるので、jsonファイルにて保存、読み込みを行いました。

<br>

---

### 🐛 2. 草用デバッグシーン

> 3dsMaxで1本ずつ手動配置するのは非効率で面白みがないため、ランダム生成とJSON書き出しができる専用シーンを作りました。  
> 納得いく配置が生成されたら JSON に書き出し、インゲームで読み込みます。

<div style="display: flex; gap: 24px; align-items: flex-start;">
  <img src="movie\DebugGrassCreate.gif" width="300" alt="草の再抽選デバッグシーン">
  <table>
    <tr><th>操作</th><th>内容</th></tr>
    <tr><td>F2</td><td>カメラを自由に操作</td></tr>
    <tr><td>J ボタン</td><td>草を再抽選して再配置</td></tr>
    <tr><td>K ボタン</td><td>現在の配置を JSON に書き出し</td></tr>
  </table>
</div>

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>  
<br>

> - AABBを使った重なり判定で草同士が重ならないように配置しました  
> - エリアが狭い場合の無限ループを防ぐため、再抽選の上限を設けました  
> - 草を消してから生成し直すまでに猶予時間を持たせ、見た目が不自然にならないようにしました  

<br>

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
    <img src="sprite/SplatMapData.png" width="320" alt="スプラットマップ">
  </div>
  <div>
    <p><b>適用前後</b></p>
    <img src="sprite/SplatMap_before.png" width="300" alt="適用前">
    <p>▲ 適用前</p>
    <br>
    <img src="sprite/SplatMap_after.png" width="300" alt="適用後">
    <p>▲ 適用後</p>
  </div>
</div>

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>  
<br>

> - `SetupSplatShader()` を `Init()` より前に呼ぶ設計にして、シェーダーのセットアップ順序を保証しました  
> - 草・岩土・腐葉土の明るさと全体の彩度を個別にパラメータで調整できるようにしました  

<br>

---

### 🎯 4. ミッションシステム

> ただ攻撃してボスを倒すだけでは単調なため、プレイヤーに目標を与えるミッションシステムを実装しました。  
> 新しいミッションを追加するときも、既存のコードを一切触らずに完結します。

<br>

<u><span style="font-size: 20px;"><b>新ミッション追加手順</b></span></u>

> 1. `MissionType.h` の `MissionID` に新しいIDを1行追加  
> 2. `MissionManager` の `SetupBoss()` に `AddMission` を1行追加  
> 3. `MissionCondition.h` に条件クラスを追加（条件が新しい場合のみ）

<br>

<img src="sprite/MissionSystem.png" width="450" alt="ミッションシステム">

<br>
<u><span style="font-size: 18px;"><b>こだわった点</b></span></u>  
<br>

> - `MissionEventData` を使った疎結合設計で、Player・Boss はミッションの内部を知らなくていい作りにしました  
> - `clearedThisFrame_` などの1フレーム限りフラグを丁寧に管理し、UIとのタイミングのずれが起きないようにしました  

<br>

---

### ⚙️ 5. 当たり判定パイプライン

> 攻撃の対象を柔軟に設定できるようにしたかったため、3段階で判定コストを最小化する仕組みを実装しました。

<img src="sprite/CollisionDetectionPipeline.png" width="450" alt="当たり判定">

---

### ⚙️ 6. 攻撃タイムライン

> 攻撃ごとに毎回時間計算をUpdateに書くのが大変だったため、タイミングを秒数で一括管理できる仕組みを使いました。

<img src="sprite/TaskScheduler.png" width="450" alt="ステートタスクスケジュール">

---

### ⚙️ 7. 重み付き抽選AI

> ただ攻撃してくるだけでは単調なため、距離別に攻撃の発動率を設定して行動パターンに変化を持たせました。

<img src="sprite/WeightedLottery.png" width="450" alt="ステートマシーン">

---

### ⚙️ 8. カメラブレンドシステム

> ボス登場シーンからゲームプレイへ切り替わる際にカメラが瞬間移動すると違和感があるため、時間を指定してなめらかに遷移できるようにしました。

<img src="sprite/CameraBlend.png" width="450" alt="カメラ">

---

<br>

## 6. 今後の実装予定

- 非同期にする
- 敵のAIの強化

---

[目次へ戻る](#目次)
