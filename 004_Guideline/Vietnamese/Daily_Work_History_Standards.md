# Tiêu chuẩn Lịch sử công việc hàng ngày

## AI向け要約 / Tóm tắt cho AI

- **正本 / Bản chính**: Tài liệu này. Tên cũ `Daily_Update_History_Standards.md` chỉ còn pointer.
- **目的 / Mục đích**: Liệt kê đủ việc trong ngày（không phải nhật ký theo thời gian）.
- **抽出 / Nguồn**: (1) dòng lịch sử cập nhật trên tài liệu（ngày + người） (2) nội dung chat hiện tại.
- **保存先 / Lưu**: `008_Work_history/Japanese/` và `008_Work_history/Vietnamese/`（tách file theo ngôn ngữ）.
- **個人 / Cá nhân**: `Work_History_YYYYMMDD_<tên>.md`
- **全員 / Gộp cả team**: `Work_History_YYYYMMDD.md`（merge theo mã **Đối tượng**; tạo lại mỗi lần cập nhật cá nhân）
- **更新者 / Người cập nhật**: tên người làm việc（thiếu thì hỏi trước）.
- Trigger: **「作業履歴を作成して」**（「日報を作成して」 cùng nghĩa）.
- Đọc tài liệu này trước khi làm. Mẫu cũ trong `008_Update_history/` chỉ để tham khảo.

## Mục đích

- Ghi lại công việc trong ngày（tài liệu / quyết định） để tra cứu sau.
- Ưu tiên **không bỏ sót**（không tái hiện hội thoại / không sắp theo giờ）.
- Giúp review / bàn giao nắm nhanh đã tạo / đã đổi gì.
- File gộp cả team xem theo **mã đối tượng**（screen / req / table…）.

## Phạm vi

| Include | Exclude（原則） |
| ------- | --------------- |
| File có dòng lịch sử cập nhật đúng ngày + đúng người | Chỉ người khác cập nhật（có thể ghi ngắn ở「参考」） |
| Req / screen design / DB / Code Master / script / PPTX… | Chỉ thảo luận chat, file không đổi |
| Artifact tạo／sửa trong ngày dù không có bảng lịch sử（PPTX, Mock…） | File tạm / log điều tra |
| Artifact chat xác nhận đã tạo／sửa dù quên ghi lịch sử | |

Thiếu **ngày** hoặc **tên người** → **hỏi trước**, không đoán.

## 1. Quy trình bắt buộc khi nhận「作業履歴を作成して」

1. Xác định ngày（`YYYY/MM/DD`）và tên người. Thiếu thì hỏi và dừng.
2. Nếu đã có file cá nhân → Read và **merge hợp nhất**（không xóa nội dung cũ）.
   - JP: `008_Work_history/Japanese/Work_History_YYYYMMDD_<tên>.md`
   - VN: `008_Work_history/Vietnamese/Work_History_YYYYMMDD_<tên>.md`
3. Search toàn repo lấy **hết** dòng lịch sử đúng ngày + đúng người（không cắt sớm）.
4. Trích từ **chat hiện tại** các artifact đã tạo／sửa và「đã đổi gì」（bắt buộc）.
5. Hợp nhất history + chat + file cá nhân cũ → hàng theo **Đối tượng × Loại công việc**.
6. Hàng tóm tắt mỏng（chỉ「đã cập nhật」）→ đọc lại history／chat để bổ sung.
7. Tạo／cập nhật **cả file JP và VN**（khớp `#` và Đối tượng）.
8. Ngay sau đó regenerate `Work_History_YYYYMMDD.md` ở cả hai thư mục ngôn ngữ.
9. Đối chiếu bảng công việc với danh sách file cuối tài liệu.

### Nhiều chat

- Mỗi chat chỉ cần mention tiêu chuẩn +「作業履歴を作成して」.
- Chat sau merge vào file cá nhân hiện có, rồi tạo lại file gộp.
- Hoàn tất khi mọi chat dùng trong ngày đã chạy quy trình này ít nhất một lần.

## 2. Tên file / thư mục

| Hạng mục | Quy tắc |
| -------- | ------- |
| Root | `008_Work_history/` |
| Language | `Japanese/` / `Vietnamese/` |
| Cá nhân | `Work_History_YYYYMMDD_<tên>.md` |
| Gộp | `Work_History_YYYYMMDD.md` |
| Legacy | Giữ `008_Update_history/`；không dùng cho file mới |

## 3. Cấu trúc file cá nhân

1. Title: `Lịch sử công việc — YYYY/MM/DD（tên）`（hoặc `作業履歴 — YYYY/MM/DD（tên）` nếu đội thống nhất JP title；ưu tiên tiếng Việt trong file VN）
2. Căn cứ（1–2 câu, tiếng Việt）
3. Bảng công việc
4. Ghi chú（chỉ khi cần）
5. Danh sách file đối tượng（check）

**Không** tạo các mục dài `## 1. …` theo theme như format cũ.

### 3.1 Bảng công việc

| # | Đối tượng | Loại công việc | Tóm tắt |
| - | --------- | -------------- | ------- |

#### Đối tượng

| Tính chất | Ghi gì | Ví dụ |
| --------- | ------ | ----- |
| Yêu cầu | Mã req | `1008` |
| Chức năng | Mã function | theo hệ thống dự án |
| Màn hình | Mã screen | `13000` / `1A200` |
| DB | Tên table | `reservations` |
| Message | Message ID / tên định nghĩa | `1A200-V03` |
| Guideline | Tên tài liệu | `Daily_Work_History_Standards` |
| Estimate | Tên file estimate | `Estimate_FE_BE_10000_Danh` |
| Mock | Mã screen | `1A110` |
| Xuyên suốt | Phạm vi | `12000–19000` |

#### Loại công việc（từ vựng cố định）

| JP | VN |
| -- | -- |
| 要件定義 | Định nghĩa yêu cầu |
| 機能設計 | Thiết kế chức năng |
| 画面設計 | Thiết kế màn hình |
| DB設計 | Thiết kế DB |
| メッセージ定義 | Định nghĩa message |
| モック | Mock |
| ガイドライン | Guideline |
| 工数見積 | Estimate |
| Code Master | Code Master |
| その他 | Khác |

#### Tóm tắt

- Cấm chỉ viết「đã cập nhật」／「đã review」.
- Viết **đã đổi gì**（1–2 câu）.
- Lấy ý từ dòng lịch sử + quyết định trong chat.
- Thuật ngữ IT theo [`Translation_Standards.md`](../Japanese/Translation_Standards.md)（giữ English cho IT terms）.

### 3.2 Ghi chú（ngoài bảng）

Chỉ khi cần: căn cứ quyết định, merge nhiều chat, việc còn lại. Tham chiếu `#` của bảng.

### 3.3 Danh sách file

- Dùng Markdown link relative path（không chỉ backtick tên file）.
- Đánh dấu（mới）khi tạo mới.

## 4. File gộp `Work_History_YYYYMMDD.md`

- Input: `Work_History_YYYYMMDD_*.md` trong cùng thư mục ngôn ngữ（loại trừ chính file gộp）.
- Group / sort theo **Đối tượng**.
- Cột: `| # | Đối tượng | Loại công việc | Tóm tắt | Người |`
- Cùng Đối tượng nhưng khác loại／nội dung → **giữ nhiều hàng**.
- Cuối file: danh sách file（gộp cả team, bỏ trùng path）.
- Title: `Lịch sử công việc — YYYY/MM/DD（Tất cả）`

## 5. Prompt tối thiểu

```text
@004_Guideline/Vietnamese/Daily_Work_History_Standards.md
作業履歴を作成して
```

hoặc:

```text
@004_Guideline/Japanese/Daily_Work_History_Standards.md
作業履歴を作成して
```

Dù mention JP hay VN, vẫn cập nhật **cả hai** file cá nhân ngôn ngữ + cả hai file gộp.

「日報を作成して」= cùng quy trình.

## 6. Ví dụ（cá nhân, trích）

```md
# Lịch sử công việc — 2026/08/07（Danh）

Căn cứ: đối chiếu lịch sử cập nhật 2026/08/07・Danh và sản phẩm tạo／sửa trong chat.

## Danh sách công việc

| # | Đối tượng | Loại công việc | Tóm tắt |
| - | --------- | -------------- | ------- |
| 1 | 1A200 | Thiết kế màn hình | Cho phép giống（breed_id）tùy chọn; gỡ tham chiếu V03 |
| 2 | 1A200-V03 | Định nghĩa message | Bỏ message lỗi chưa chọn giống |
| 3 | 13000 | Thiết kế màn hình | Khởi tạo bắt buộc visit_type; bỏ validate／V01 |

## Ghi chú

- #1: Theo Req 1008／họp 2026/08/05

## Danh sách file đối tượng（check）

- （liệt kê link relative）
```

## 7. Tài liệu liên quan

| Tài liệu | Vai trò |
| -------- | ------- |
| [`Translation_Standards.md`](../Japanese/Translation_Standards.md) | Thuật ngữ / dịch |
| [`Daily_Update_History_Standards.md`](./Daily_Update_History_Standards.md) | Tiêu chuẩn cũ（pointer） |
| `008_Update_history/` | Format cũ（tham khảo） |

## Lịch sử cập nhật

| Ngày | Người | Nội dung |
| ---- | ----- | -------- |
| 2026/08/08 03:42 | Suzawa | Bản đầu（Lịch sử công việc）. Đổi tên từ cập nhật履歴; tách JP/VN; bảng Đối tượng／Loại／Tóm tắt; file gộp theo mã; prompt tối thiểu. |
