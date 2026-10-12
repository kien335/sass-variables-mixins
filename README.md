# Thực hành SASS Variables & Mixins

Chuyển đổi các quy tắc CSS mẫu (`h1`, `h2`, `.button`, `.card`) sang SCSS có biến, mixins, nesting và partials.

## Cấu trúc

- `abstracts/_variables.scss`: biến màu sắc, cỡ chữ, padding, box-shadow.
- `abstracts/_mixins.scss`: hai mixin `button-style` và `box-style`.
- `base/_typography.scss`: tiêu đề `h1`, `h2` dùng biến.
- `components/_buttons.scss`, `components/_cards.scss`: dùng `@include` và nesting.
- `main.scss`: điểm vào tập hợp các module bằng `@use`.
- `main.css`: CSS đầu ra dùng trong `index.html`.

> SASS hiện đại khuyến nghị `@use` thay cho `@import`. Mỗi partial `@use` các module biến/mixin cần thiết vì module có namespace riêng.

## Chạy trên Windows (PowerShell)

```powershell
sass.cmd -v
sass.cmd main.scss main.css
sass.cmd main.scss main.css --watch
```

Khi watch đang chạy, đổi `$primary-color: red;` thành `$primary-color: blue;` trong `abstracts/_variables.scss`, lưu file và kiểm tra `main.css`. Nhấn `Ctrl + C` để dừng watch. Sau đó mở `index.html` trên trình duyệt.

## Nộp bài

Đưa toàn bộ thư mục lên GitHub và dán link repository vào CodeGym. Đề không bắt buộc ảnh chụp.
