# Dashboard trưng bày demo đối thủ

Website tĩnh, mở bằng `index.html`. Dữ liệu nằm trong thư mục `data/`.

## Đưa lên GitHub Pages
1. Tạo repository mới trên GitHub, upload toàn bộ nội dung thư mục này (giữ nguyên thư mục `data/`).
2. Vào **Settings → Pages**, mục *Source* chọn **Deploy from a branch**, branch `main`, thư mục `/ (root)`, bấm **Save**.
3. Sau 1–2 phút, website có địa chỉ dạng `https://<tên-tài-khoản>.github.io/<tên-repo>/`.

## Cập nhật dữ liệu
Thay các file trong `data/` bằng file mới cùng cấu trúc cột:
- `shops.csv`: shop_id, shop_name, chain, area, checker, checked_at
- `items.csv`: r, shop_id, category, brand, item, qty
- `models.csv` (bảng giá & phân khúc): brand, ptype, item, list_price, promo_price, ref_version, segment, note — segment là một trong: ≤ 3M, 3-5M, 5-7M, 7-10M, 10-15M, 15-20M, 20-30M, Above 30M, Chưa có giá

## Xem thử trên máy
Mở thẳng file `index.html` sẽ không tải được dữ liệu (trình duyệt chặn). Chạy trong thư mục này:
`python -m http.server 8000` rồi mở http://localhost:8000
