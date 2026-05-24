# AIDEOM-VN — Bộ 12 bài tập Mô hình ra quyết định

Web tổng hợp 12 bài tập về phát triển kinh tế Việt Nam trong kỉ nguyên AI
(Cobb-Douglas, LP, MIP, TOPSIS, NSGA-II, tối ưu động, quy hoạch ngẫu nhiên,
Q-learning…). Có trang chủ tổng quan + điều hướng + tiêu chí chấm điểm.

**Mọi tính toán & biểu đồ chạy bằng JavaScript trong trình duyệt** — không cần
máy chủ Python. File `app.py` chỉ để phục vụ web qua HTTP cho tiện.

## Cấu trúc thư mục
```
aideom_web/
├── index.html         # toàn bộ web (tự chứa, gồm 12 bài + trang chủ)
├── app.py             # máy chủ Flask đơn giản (tùy chọn)
├── requirements.txt   # thư viện cần cài (flask)
└── README.md          # file này
```

## Cách chạy

### Cách 1 — Mở trực tiếp (nhanh nhất)
Nhấp đúp `index.html` để mở bằng trình duyệt. Cần internet vì biểu đồ
(Chart.js) và công thức (KaTeX) tải qua CDN.

### Cách 2 — Chạy bằng Python có sẵn (không cần cài gì)
```bash
cd aideom_web
python -m http.server 5000
```
Mở http://127.0.0.1:5000

### Cách 3 — Chạy bằng Flask (app.py)
```bash
cd aideom_web
pip install -r requirements.txt
python app.py
```
Mở http://127.0.0.1:5000

## Đưa lên mạng (deploy)

**Vercel / Netlify / GitHub Pages:** chỉ cần upload `index.html` là chạy được
(không cần `app.py`). Trên Vercel: tạo project, kéo thả thư mục, hoặc đặt
`index.html` vào thư mục `public/`.

## Điều hướng
- Trang chủ: `index.html#home`
- Từng bài: `index.html#bai1`, `#bai2`, … `#bai12`

## Nguồn dữ liệu
Cục Thống kê quốc gia (NSO/GSO), Ngân hàng Thế giới, Bộ KH-CN,
Global Innovation Index 2025. Số liệu CSV được làm tròn phục vụ giảng dạy.
