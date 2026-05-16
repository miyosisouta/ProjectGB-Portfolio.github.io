<link href="style.css" rel="stylesheet" />

<img src="sprite\title.png" width="600" alt="タイトル画像">

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

> - 攻撃ごとの影響力と影響範囲をjsonにて設定  
> - 時間経過でもとに戻ります  
<img src="movie\GrassBend.gif" width="280" alt="草が曲がる">  

---

<br>
<u><span style="font-size: 18px;"><b>LOD＋ディザリング＋インスタンシング</b></span></u>  
<br>

<span style="display:block;margin-bottom:0.5em;"></span> 

> - カメラからの距離に応じて、モデルの切り替えとディザリングを行っています。  
> - また、300個近く草が作成しているのでインスタンシング描画を行っています。

<span style="display:block;margin-bottom:0.5em;"></span> 

| 近く | 遠い |
|:---:|:---:|
<img src="sprite\LOD.png" width="300" alt="回避失敗"> | <img src="sprite\LOD2andDhithering.png" width="300" alt="回避成功"> |



### 🐛 2. 草用デバッグシーン

> - ステージ上の草をランダム配置するための専用デバッグシーンです。  
> - 納得いく配置が生成されたら JSON に書き出し、インゲームで読み込みます。  

| 操作 | 内容 |
|:---|:---|
| F2 | カメラを自由に操作 |
| J ボタン | 草を再抽選して再配置 |
| K ボタン | 現在の配置を JSON に書き出し |

<span style="display:block;margin-bottom:0.5em;"></span>  

<img src="movie\DebugGrassCreate.gif" width="280" alt="デバックシーン">



---

### 🎯 3. ミッションシステム

> ミッションの内部を他のクラスが知らなくていい設計にしました。  
> 新しいミッションを追加するときも、既存のコードを一切触らずに完結します。

<br>

<u><span style="font-size: 20px;"><b>新ミッション追加手順</b></span></u>

> 1. `MissionType.h` の `MissionID` に新しいIDを1行追加  
> 2. `MissionManager` の `SetupBoss()` に `AddMission` を1行追加  
> 3. `MissionCondition.h` に条件クラスを追加（条件が新しい場合のみ）

<img src="sprite/MissionSystem.png" width="450" alt="ミッションシステム">

---

### ⚙️ 4. 当たり判定パイプライン

> 3段階で判定コストを最小化

<img src="sprite/CollisionDetectionPipeline.png" width="450" alt="当たり判定">

---

### ⚙️ 5. 攻撃タイムライン

> タイミングを秒数で一括管理

<img src="sprite/TaskScheduler.png" width="450" alt="ステートタスクスケジュール">

---

### ⚙️ 6. 重み付き抽選AI

> 距離で行動パターンが変化

<img src="sprite/WeightedLottery.png" width="450" alt="ステートマシーン">

---

### ⚙️ 7. カメラブレンドシステム

> 時間指定でなめらかに遷移

<img src="sprite/CameraBlend.png" width="450" alt="カメラ">


---

<br>

## 6. 今後の実装予定

- プレイヤーのスキルを2つ追加予定
- ボスを2種類追加、攻撃パターンをボス1体につき4種類作成

---

[目次へ戻る](#目次)
