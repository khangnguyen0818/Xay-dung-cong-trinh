# Sổ Xây Nhà

Ứng dụng quản lý chi phí và hồ sơ bản vẽ khi xây nhà. Toàn bộ nằm trong một file `index.html` (HTML + CSS + JavaScript, không cần cài đặt hay build).

Bản đang chạy trên claude.ai: https://claude.ai/artifact/KBY1YHTSXs7Gs1XtdsEbCC

## Chức năng

**Thu chi:** 12 hạng mục, mỗi hạng mục là một bảng gồm Ngày, Việc chi, Số tiền:
CÔNG THẦU, GẠCH ỐP LÁT, ĐIỆN NƯỚC, LẶT VẶT, VẬT LIỆU XÂY DỰNG, SƠN NƯỚC, SẮT THÉP, THANG MÁY, CỬA, THIẾT BỊ VỆ SINH, CÁC HẠNG MỤC NHỎ, GIẤY TỜ.

- Thêm, sửa, xóa khoản chi. Mỗi hạng mục có dòng tổng.
- Xuất từng hạng mục ra Excel (.xlsx), nhập khoản chi từ file Excel.
- Mục TỔNG HỢP cộng tất cả hạng mục. Nút xuất Excel tổng hợp tạo 12 sheet và 1 sheet TỔNG HỢP có công thức liên kết.

**Bản vẽ:** BẢN VẼ (Bản vẽ chi tiết thi công, Bản vẽ bố trí vật dụng, Bản vẽ điện nước), PHỐI CẢNH, NỘI THẤT. Mỗi thư mục cho phép tải lên ảnh, PDF và video.

## Dữ liệu được lưu ở đâu

| Mở ở đâu | Chi phí | Bản vẽ (tải tệp lên) |
|---|---|---|
| claude.ai (link artifact ở trên) | Lưu trên claude.ai, đồng bộ mọi thiết bị | Có |
| Mở trực tiếp `index.html` hoặc GitHub Pages | Chỉ lưu trong trình duyệt đang dùng | Không |

File trong repo này chỉ chứa mã nguồn. Số liệu chi tiêu và bản vẽ không nằm trong repo.

## Cách chỉnh sửa

1. Sửa `index.html` (ví dụ đổi danh sách hạng mục trong biến `CATS`, đổi thư mục trong biến `FOLDERS`).
2. Muốn cập nhật bản trên claude.ai: mở Claude, gửi file `index.html` kèm link artifact ở trên và nhờ Claude cập nhật vào đúng link đó.

Đừng đổi `id` của hạng mục hay thư mục đã có dữ liệu, vì dữ liệu được lưu theo `id` đó.

## Thư viện dùng

- [SheetJS](https://sheetjs.com/) 0.18.5 để đọc và ghi Excel, tải từ cdnjs.
- Font Barlow Condensed, Be Vietnam Pro, IBM Plex Mono từ Google Fonts.
