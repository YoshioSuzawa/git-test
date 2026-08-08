# ドキュメント一覧（Document List）

Update: 2026/08/08

| Doc.No | ドキュメント名 | Document Name | Owner | 内容 | Description | ファイル構成 | File Structure |
| ------ | -------------- | ------------- | ----- | ---- | ----------- | ------------ | -------------- |
| 1.0 | システム概要 | System Overview | BA | | | 日本語、ベトナム語は分ける | Tách riêng tiếng Nhật và tiếng Việt |
| 2.0 | 機能要件（CRUD） | Functional Requirements (CRUD) | BA | 機能毎に作成する。基本的に画面番号の単位（例: `11000` / `H1130`） | Tạo theo từng function. Cơ bản theo đơn vị Screen No（vd: `11000` / `H1130`） | 日本語、ベトナム語は分ける | Tách riêng tiếng Nhật và tiếng Việt |
| 3.0 | 用語集 | Glossary | BA | **AddPet** 共通用語、サブシステム用語と、ユーザー業務用語に分ける。 | Phân thành AddPet common terms, Subsystem terms và User business terms | 日本語、ベトナム語は分ける | Tách riêng tiếng Nhật và tiếng Việt |
| 4.0 | DB設計書 | DB Design | BA | テーブル毎 | Theo từng table | １つのファイルに併記する | Gộp trong 1 file |
| 5.0 | ER図 | ER Diagram | BA | DB設計書を元にAIで自動生成する | Tự động generate bằng AI từ DB Design | １つのファイルに併記する | Gộp trong 1 file |
| 6.0 | ロールと権限の定義 | Role & Permission Definition | BA | サブシステムの全ての利用者を定義する | Định nghĩa toàn bộ user của subsystem | １つのファイルに併記する | Gộp trong 1 file |
| 7.0 | Code値設計書 | Code Value Design | BA | | | １つのファイルに併記する | Gộp trong 1 file |
| 8.0 | メッセージ定義書 | Message Definition | Designer | | | １つのファイルに併記する | Gộp trong 1 file |
| 9.0 | サンプルデータ | Sample Data | Designer | テーブル毎に、実際のデータで作成する | Tạo bằng dữ liệu thực theo từng table | 日本語、ベトナム語は分ける | Tách riêng tiếng Nhật và tiếng Việt |
| 10.0 | カラーシステム | Color System | UI Designer | サブシステムのカラーを定義する | Định nghĩa màu sắc của subsystem | １つのファイルに併記する | Gộp trong 1 file |
| 10.1 | フィールドサイズ定義 | Field Size Definition | UI Designer | フィールドの幅を 1/4・2/4・3/4・4/4 で定義（`003_Common/Field_Size_Standards.md`）。入力・表示専用の両方が対象。全モックアップ・画面設計が従う | Định nghĩa chiều rộng field theo 1/4・2/4・3/4・4/4（`003_Common/Field_Size_Standards.md`）. Áp dụng cho cả field nhập liệu và field chỉ hiển thị. Toàn bộ mockup và screen design tuân theo | １つのファイルに併記する | Gộp trong 1 file |
| 11.0 | アイコン、画像データ | Icon, Image Data | UI Designer | | | | |
| 12.0 | 画面設計 | Screen Design | Designer | **Overview**（業務）と **Design**（実装）の2文書。詳細は `Screen_Design_Standards.md`（10000）／`Screen_Design_Standards.20000.md`（20000） | **Overview**（nghiệp vụ）và **Design**（triển khai）. Xem `Screen_Design_Standards.md`（10000）/ `Screen_Design_Standards.20000.md`（20000） | 日本語とベトナム語は**分ける**（`*_jp.md` / `*_vn.md`）。**1画面＝2ファイル**（Overview + Design） | Tách JP / VN（`*_jp.md` / `*_vn.md`）。**1 màn = 2 file**（Overview + Design） |
| | ・概要（Overview） | ・Overview | | 画面の目的・利用者・操作フロー・確認事項（stakeholder） | Mục đích, user, luồng thao tác, điểm xác nhận | | |
| | ・設計（Design） | ・Design | | フィールド定義・アクション・バリデーション等（developer）。Field / Action は本ファイルに含める | Định nghĩa field・action・validation（developer）. Field / Action nằm trong file này | | |
| 13.0 | UIモックアップ | UI Mockup | Designer | AIにて生成 | Generate bằng AI | ヘッダーに言語切り替えボタンを配置する（該当する場合） | Đặt language switch trên header（nếu có） |
| 14.0 | 意匠設計 | UI Design | UI Designer | Pencil（`.pen`） | Pencil（`.pen`） | | |
| 15.0 | Field定義書 | Field Definition | FE | **AddPet では原則 Design に含める**（別ファイル分割はしない） | **Trong AddPet, mặc định nằm trong Design**（không tách file） | （旧運用の分割モデル。新規は 12.0 Design を正とする） | （Mô hình cũ. Mới lấy 12.0 Design làm chuẩn） |
| 16.0 | Action定義書（FE） | Action Definition (FE) | FE | 同上 | Như trên | 同上 | Như trên |
| 17.0 | Action定義書（BE） | Action Definition (BE) | BE | 同上 | Như trên | 同上 | Như trên |
| 18.0 | 日次作業履歴 | Daily Work History | BA / Designer | 対象日・更新者の作業を抜け漏れなく、対象コード単位の表でまとめる（個人＋全員マージ）。基準書: `Daily_Work_History_Standards.md` | Tóm tắt công việc theo ngày・người, không sót, theo mã đối tượng（cá nhân＋gộp tất cả）. Chuẩn: `Daily_Work_History_Standards.md` | `008_Work_history/Japanese|Vietnamese/Work_History_YYYYMMDD_<Name>.md` と全員 `Work_History_YYYYMMDD.md`（言語別） | `008_Work_history/Japanese|Vietnamese/Work_History_YYYYMMDD_<Name>.md` và `Work_History_YYYYMMDD.md`（tách ngôn ngữ） |

## 更新履歴

| 日付 | 内容 |
| ---------- | -------------------------------------------------------------------- |
| 2026/04/23 | 初版（S-NET 由来） |
| 2026/07/24 | AddPet 用語・画面2文書モデル・画面 CODE 例に更新。Field/Action は Design 内包を明記。 |
| 2026/08/01 | 10.1 フィールドサイズ定義（`003_Common/Field_Size_Standards.md`）を追加。 |
| 2026/08/01 | 12.0 画面設計の基準書を 10000 / 20000 の2本立てに変更（`Screen_Design_Standards.20000.md` を新設）。 |
| 2026/08/04 | 18.0 日次更新まとめ（`Daily_Update_History_Standards.md` / `008_Update_history`）を追加。 |
| 2026/08/08 | 18.0 を日次作業履歴（`Daily_Work_History_Standards.md` / `008_Work_history`）に更新。 |
