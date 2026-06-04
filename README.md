# 🌹 Gửi em một bó hồng

Trang web tương tác: một **bó hồng** mà **mỗi bông hồng là một tấm ảnh của em**, xếp khít thành mâm tròn, viền hoa baby trắng, gói giấy đen–đỏ, nơ + ruy băng. Mở quà → hoa nở → chạm vào từng bông để xem ảnh phóng to kèm lời nhắn. Có mưa tim, lấp lánh và nhạc nền.

## Cấu trúc folder

```
flower-gift/
├── index.html        ← trang chính (mở file này)
├── tao-qr.html       ← công cụ tạo mã QR
├── photos/           ← ảnh của em: img1.jpg, img2.jpg, ... (đánh số liên tục từ 1)
└── music/            ← nhạc nền (đặt file tên song.mp3 vào đây)
```

## Thêm / đổi / bớt ảnh

Web **tự nhận** mọi ảnh trong `photos/` đặt tên `img1.jpg, img2.jpg, ...`

- Càng **nhiều ảnh, bó hồng càng đầy và tròn** (giống bó thật). Gợi ý: ~40–60 ảnh để mâm hồng dày đẹp; hiện đang có 27.
- Thêm ảnh: đặt tiếp `img28.jpg, img29.jpg...`
- Đổi ảnh: ghi đè file cùng tên.
- Bớt ảnh: xoá file và đánh số lại liên tục từ 1 (đừng để trống số ở giữa).

## Sửa lời nhắn

Mở `index.html` bằng Notepad, tìm `const CONFIG = {` (gần cuối), sửa:
`title`, `subtitle`, `finalMsg` (xuống dòng bằng `\n`), `signature`, và `captions` (lời nhắn cho từng ảnh theo thứ tự img1, img2, ...).

## Thêm nhạc nền

Đặt 1 file nhạc tên **`song.mp3`** vào folder `music/`. Nhạc tự phát khi em bấm "Chạm để mở", có nút bật/tắt ở góc phải.

## Đẩy lên GitHub (để em quét QR / mở link)

1. github.com → **New repository** → đặt tên ví dụ `flower-gift`, chọn **Public** → **Create**.
2. **Add file → Upload files** → kéo **toàn bộ** nội dung folder `flower-gift` (file `index.html`, folder `photos`, `music`...) vào → **Commit**.
3. **Settings → Pages** → Source chọn nhánh **main**, thư mục **/(root)** → **Save**.
4. Đợi ~1 phút, có link: `https://<tên-github>.github.io/flower-gift/` → gửi cho em.

## Tạo mã QR

Mở `tao-qr.html` → dán link GitHub Pages ở trên → **Tạo QR** → **Tải ảnh QR** về để in/gửi.
