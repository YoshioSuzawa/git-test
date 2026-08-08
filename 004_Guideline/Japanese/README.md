# 004_Guideline

## 役割

全サブシステムで共有する共通仕様、開発基準、ルールを集約します（**AddPet** / 共有ドライブ `750_AddPet`）。

## ファイル一覧

### 基準書（`*_Standards.md`）

| ファイル名（英語） | 内容 |
| ----------------------------------- | ------------------------------------------ |
| **AI_Agents_Standards.md** | AIエージェント利用の基準 |
| **DB_Design_Standards.md** | DB設計書の基準 |
| **ER_Diagram_Standards.md** | ER図（draw.io）の基準・グループ構造の参照 |
| **Code_Master_Standards.md** | Code値設計書の基準 |
| **OperationManual_Standards.md** | オペレーションマニュアル（HTML）の作成基準 |
| **Requirement_Design_Standards.md** | 要件定義書の基準 |
| **Screen_Design_Standards.md** | 画面設計の基準（10000 診療予約システム／顧客） |
| **Screen_Design_Standards.20000.md** | 画面設計の基準（20000 診療管理システム／病院スタッフ） |
| **Mockup_Standards.md** | HTMLモックアップ（202_Mockups）の作成基準 |
| **Screen_Layout_Standards.md** | 画面レイアウトの Draw.io 変換・座標ルール |
| **TestCase_Creation_Standards.md** | テスト定義Markdownの作成基準 |
| **Translation_Standards.md** | 翻訳の基準 |
| **Daily_Work_History_Standards.md** | 日次作業履歴（`008_Work_history`）の作成基準 |
| **Daily_Update_History_Standards.md** | 旧名称ポインタ（→ Daily_Work_History_Standards） |

### ガイドライン・手順（Guideline_* / 手順）

| ファイル名 | 内容 |
| ----------------------------------------------- | ------------------------------------------------------------------------------ |
| **Guideline_Cursor.md** | Cursor 使い方マニュアル（AI モデル選定・利用料確認の会社方針を含む） |
| **Guideline_Mockup_From_Pencil.md** | Pencilファイルからモックアップを生成する手順（併せて **Mockup_Standards.md**） |
| **Guideline_Screen_Implementation_Prompt.md** | 画面実装プロンプト作成手順（add_pet / PetKind 基準。BE・FE テンプレートあり） |
| **設計手順.md** | AddPet 設計手順（仕様確定〜基本設計） |
| **開発手順.md** | 設計→実装プロンプト→AIコーディングの役割分担 |
| **Document_List.md** | 成果物ドキュメント一覧 |
| **GoogleDrive_for_Desktop.md** | 共有ドライブ `750_AddPet` の同期手順 |
| **Excel2MarkDown_Conversion.md** | Excel→Markdown 変換手順（移行用） |

> **未作成:** `Guideline_Git.md`（Git 手順はチーム運用に従う。必要になったら本フォルダに追加する）

### テンプレート（`templates/`）

設計書・モック等の雛形は **`004_Guideline/templates/`** に置く。

| パス（`templates/` からの相対） | 内容 |
| -------------------------------------------- | -------------------------------------------------------------------------- |
| **99.Screen_Implementation/** | 画面実装プロンプト（Backend / Frontend / Improvement）+ H1130/H1131 記入例 |
| **Screen_Design_Template.md** | 画面設計書 Design のテンプレート（10000） |
| **Screen_Design_Overview_Template.md** | 画面設計書 Overview のテンプレート（10000） |
| **Screen_Design_Template.20000.md** | 画面設計書 Design のテンプレート（20000） |
| **Screen_Design_Overview_Template.20000.md** | 画面設計書 Overview のテンプレート（20000） |
| **Requirement_Design_Template.md** | 要件定義書（Markdown）のテンプレート |
| **DB_Design_Template.md** | DB設計書（Markdown）のテンプレート |
| **TestCase_Creation_Template.md** | テスト定義（Markdown）のテンプレート |
| **Code_Master_Template.md** | Codeマスタ（Markdown）のテンプレート |
| **OperationManual_Template.html** | オペレーションマニュアルHTMLのテンプレート |
| **Mockup_Template_20000.html** | HTMLモック（20000・単ページ） |
| **Mockup_Template_20000_Dashboard.html** | HTMLモック（20000・ダッシュボード系） |
| **Mockup_Template_20000_List.html** | HTMLモック（20000・一覧系） |
| **Mockup_Template_20000_Display.html** | HTMLモック（20000・表示系） |
| **Mockup_Template_20000_Add.html** | HTMLモック（20000・追加系） |
| **Mockup_Template_20000_Edit.html** | HTMLモック（20000・修正系） |

> **未配置:** `Screen_Layout_Template.py`（Screen_Layout_Standards が参照するが、AddPet では未配置。画面フロー・ER は Draw.io を直接作成する）

### 共通定義

| パス / 置き場 | 内容 |
| ------------- | ---- |
| サブシステム配下の Code Master / Glossary（例: `10000_Reservation_System/...`、`003_Common/101_Requirement_Defination/Glossary_Reservation.md`） | サブシステム固有の Code・用語。共通権限モデル用の `003_Common` は **AddPet には置かない**（旧 S-NET 構成）。 |

- パス・ファイル名はすべて **英語** で統一すること（AIエージェントが日本語パスを扱えないため）。ただし本フォルダの手順書名（`設計手順.md` 等）は例外として残す。

## 運用メモ

- 共通仕様を変更する場合は、影響範囲を十分に検討し、関係者に周知すること
- 開発基準まわり（基準書・テンプレート・ベースコード）の変更は、全開発者に影響するため、慎重に検討すること
- 変更時は、該当ドキュメントを即座に更新すること

## 更新履歴

| 日付 | 名前 | 内容 |
| ---------------- | ------ | -------------------------------------------------------------------- |
| 2026/07/24 11:10 | Cursor | AddPet 索引に更新。欠落参照（Guideline_Git / Layout.py / 003_Common）を整理し、手順書・Overview テンプレを追記。 |
| 2026/08/01 22:20 | Suzawa | 用語集 No.32 に従い「飼い主」を「顧客」に統一（更新履歴の過去記述は当時の記録として残す）。 |
| 2026/08/04 08:25 | Suzawa | `Daily_Update_History_Standards.md` を追加（日次更新まとめ）。 |
| 2026/08/05 11:33 | Suzawa | `Guideline_Cursor.md` に AI モデル選定の会社方針を追加した旨を索引に反映。 |
| 2026/08/06 15:15 | Suzawa | モック HTML テンプレート6種を `Mockup_Template_20000_*.html`（単ページは `Mockup_Template_20000.html`）に改名。 |
| 2026/08/08 04:12 | Suzawa | `Daily_Work_History_Standards.md` を正本に。索引を日次作業履歴（`008_Work_history`）へ更新。旧基準書はポインタ。 |
