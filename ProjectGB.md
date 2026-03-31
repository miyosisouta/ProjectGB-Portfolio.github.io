<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=e8c56a,d4872a&height=140&section=header&text=🎮%20ProjectGB&fontSize=36&fontColor=3a2808&fontAlignY=55&animation=fadeIn" width="100%"/>

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white)
![DirectX12](https://img.shields.io/badge/DirectX_12-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![K2Engine](https://img.shields.io/badge/K2Engine-%E5%AD%A6%E5%86%85%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%B3-F5A623?style=flat-square)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

</div>

---

## 📋 目次

| No. | セクション |
|:---:|---|
| 1 | [👤 自己紹介](#1-自己紹介) |
| 2 | [📄 作品概要](#2-作品概要) |
| 3 | [🎮 ゲーム紹介](#3-ゲーム紹介) |
| 4 | [💻 担当コード](#4-担当コード) |
| 5 | [⚙️ 技術紹介](#5-技術紹介) |
| 6 | [🔧 今後の実装予定](#6-今後の実装予定) |

---

## 1. 自己紹介

<table>
  <tr>
    <td width="120px" align="center"><b>名前</b></td>
    <td>三好 爽太（みよし そうた）</td>
  </tr>
  <tr>
    <td align="center"><b>学校</b></td>
    <td>河原電子ビジネス専門学校　ゲームクリエイター科</td>
  </tr>
  <tr>
    <td align="center"><b>メール</b></td>
    <td><a href="mailto:CA01244028@st.kawahara.ac.jp">CA01244028@st.kawahara.ac.jp</a></td>
  </tr>
</table>

---

## 2. 作品概要

<table>
  <tr>
    <td width="140px" align="center"><b>タイトル</b></td>
    <td>がぶっとバスター</td>
  </tr>
  <tr>
    <td align="center"><b>ジャンル</b></td>
    <td>3D アクションゲーム</td>
  </tr>
  <tr>
    <td align="center"><b>制作人数</b></td>
    <td>3人</td>
  </tr>
  <tr>
    <td align="center"><b>制作期間</b></td>
    <td>2026年3月 〜 現在</td>
  </tr>
  <tr>
    <td align="center"><b>プレイ人数</b></td>
    <td>1人</td>
  </tr>
  <tr>
    <td align="center"><b>対応ハード</b></td>
    <td>PC（Windows 11）</td>
  </tr>
  <tr>
    <td align="center"><b>コントローラー</b></td>
    <td>Xbox 360 コントローラー</td>
  </tr>
</table>

<br>

### 🔗 リンク

| | |
|---|---|
| **GitHub** | [miyosisouta/ProjectGB](https://github.com/miyosisouta/ProjectGB.git) |
| **YouTube** | （動画投稿後に追記予定） |

<br>

### 🛠️ 使用ツール

| カテゴリ | ツール |
|---|---|
| エンジン | 学内エンジン（K2Engine） |
| エディタ | Visual Studio 2022 |
| 使用言語 | C++, HTML |
| 3D モデル | 3ds Max 2025 |
| エフェクト | Effekseer |
| 画像編集 | Adobe Photoshop |
| バージョン管理 | GitHub, Fork |

---

## 3. ゲーム紹介

### 🐲 ボス登場シーン

> このボスを倒すことがゲームの目標です。

<img src="movie\BossAppearance.gif" width="450" alt="ボス登場シーン">

---

### 🕹️ プレイヤーアクション

#### 通常攻撃

<img src="movie\PlayerNormalAttack.gif" width="450" alt="プレイヤーの通常攻撃">

#### 特殊攻撃

<img src="movie\PlayerSpecialAttaack.gif" width="450" alt="プレイヤーの特殊攻撃">

#### 回避

> ダメージを受けるパターンと回避成功パターンの2種類を掲載しています。

| ダメージあり | 回避成功 |
|:---:|:---:|
<img src="movie\PlayerAvoidFailure.gif" width="300" alt="回避失敗"> | <img src="movie\PlayerAvoidSuccess.gif" width="300" alt="回避成功"> |

---

### 👾 ボスの攻撃パターン

#### 通常攻撃

<img src="movie\BossNormalAttack.gif" width="450" alt="ボスの通常攻撃">

#### 回転攻撃

<img src="movie\BossSpinAttack.gif" width="450" alt="ボスの回転攻撃">

#### ヒットスタンプ

<img src="movie\BossHitStamp.gif" width="450" alt="ボスのヒットスタンプ">

---

### 🔊 音量設定

<img src="movie\SoundSetting.gif" width="450" alt="音量設定">

<!-- 💡 提案: 音量設定はゲーム紹介というよりUI紹介に近い内容です。
     「技術紹介」や独立した「UI紹介」セクションに移したほうが
     ゲームの流れを見せるゲーム紹介セクションがスッキリするかもしれません。
     現状はゲーム紹介の末尾に置いています。 -->

---

## 4. 担当コード

### 👤 プレイヤー
`Player` `PlayerState` `PlayerController`

### 👾 ボス
`BossCharacter` `BossState` `BossSpawner` `NPCController`

### 🏗️ 基底・共通
`Actor` `Character` `ActorStatus` `IState` `StateMachine` `CharacterDataBase`

### ⚔️ スキル
`ISkill` `NormalAttack` `AbilityBase` `DefaultAttack` `Utility`

### 💥 当たり判定
`GhostBody` `GhostBodyManager` `GhostPrimitive` `BroadphaseInterface` `BroadphaseImpl` `CollisionHitManager` `BoundingVolume` `PhysicalBody`

### 🎥 カメラ
`CameraCommon` `CameraController` `CameraManager` `CameraSteering`

---

## 5. 技術紹介

### ⚙️ 1. 階層型クラス設計

> 新キャラは継承するだけ

<img src="sprite/ClassDesign.png" width="450" alt="クラス設計">

---

### ⚙️ 2. ステートマシン

> グローバル遷移で死亡を最優先

<img src="sprite/StateMachine.png" width="450" alt="ステートマシーン">

---

### ⚙️ 3. 攻撃タイムライン

> タイミングを秒数で一括管理

<img src="sprite/TaskScheduler.png" width="450" alt="ステートタスクスケジュール">

---

### ⚙️ 4. 無敵フラグ管理

> 複数の無敵要因を同時管理

<img src="sprite/InvincibleFlag.png" width="450" alt="ステートマシーン">

---

### ⚙️ 5. 重み付き抽選AI

> 距離で行動パターンが変化

<img src="sprite/WeightedLottery.png" width="450" alt="ステートマシーン">

---

### ⚙️ 6. 当たり判定パイプライン

> 3段階で判定コストを最小化

<img src="sprite/CollisionDetectionPipeline.png" width="450" alt="当たり判定">

---

### ⚙️ 7. カメラブレンドシステム

> 時間指定でなめらかに遷移

<img src="sprite/CameraBlend.png" width="450" alt="カメラ">

---

## 6. 今後の実装予定

- プレイヤーのスキルを2つ追加予定
- ボスを2種類追加、攻撃パターンをボス1体につき4種類作成

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=e8c56a,d4872a&height=80&section=footer" width="100%"/>
</div>
