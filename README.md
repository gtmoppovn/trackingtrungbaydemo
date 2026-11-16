# Dashboard trưng bày demo đối thủ

Website tĩnh, mở bằng `index.html`. Dữ liệu nằm trong thư mục `data/`.

## Đưa lên GitHub Pages
1. Tạo repository mới, upload toàn bộ nội dung thư mục này (giữ nguyên thư mục `data/`).
2. **Settings → Pages** → *Deploy from a branch* → branch `main`, thư mục `/ (root)` → **Save**.
3. Sau 1–2 phút, website có địa chỉ `https://<tên-tài-khoản>.github.io/<tên-repo>/`.

## Cập nhật dữ liệu
- `shops.csv`: period, shop_id, shop_name, chain, area, checker, checked_at
- `items.csv`: period, r, shop_id, category, brand, item, qty
- `models.csv` (giá và phân khúc): brand, ptype, item, list_price, promo_price, ref_version, segment, note — segment: ≤ 3M, 3-5M, 5-7M, 7-10M, 10-15M, 15-20M, 20-30M, Above 30M, Chưa có giá

Thêm kỳ mới: nối thêm dòng vào `shops.csv` và `items.csv` với giá trị `period` mới (vd. `2026-12`), rồi đổi `period: '2026-11'` trong `index.html` (dòng `const DEFAULTS`) thành kỳ mới nhất.

## Xem thử trên máy
Mở thẳng file `index.html` sẽ không tải được dữ liệu. Chạy `python -m http.server 8000` trong thư mục này rồi mở http://localhost:8000
