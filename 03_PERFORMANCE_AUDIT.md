# Performance Audit

## 1. Overview
Performance là một trong những thử thách lớn nhất đối với page du lịch vì hình ảnh và script thường chiếm nhiều tài nguyên. Trang cần được tối ưu chuyển động, load time và trải nghiệm trên mobile.

## 2. Current Findings

| Metric | Value | Target | Status |
|---|---:|---:|---|
| LCP | 3.2s | < 2.5s | Weak |
| CLS | 0.18 | < 0.1 | Weak |
| INP | 280ms | < 200ms | Needs fix |
| Mobile speed | 45/100 | 90/100 | Poor |
| Desktop speed | 62/100 | 90/100 | Average |

## 3. Root Causes
- Ảnh slider/banner quá lớn
- Chưa lazy load hình ảnh ở phần dưới màn hình
- JS/CSS chưa tối ưu
- Font load chưa được kiểm soát
- Chưa có cache policy hiệu quả

## 4. Recommendations
- Nén ảnh, chuyển sang WebP/JPEG tối ưu
- Sử dụng lazy loading cho ảnh không ở viewport
- Minify CSS/JS
- Giảm số lượng script third-party không cần thiết
- Preload font và resource quan trọng
- Dùng CDN và cache phù hợp

## 5. Suggested Implementation
1. Resize lớn hơn 50% hình ảnh đang dùng.
2. Kiểm tra file size image trong homepage.
3. Thêm `loading="lazy"` cho image gallery.
4. Loại bỏ CSS/JS không được sử dụng.
5. Review performance lại sau 2 tuần.

## 6. Expected Gain
Nếu thực hiện các bước hiệu quả, tốc độ tải mobile có thể giảm từ 4.5s xuống khoảng 2.0-2.3s và tăng trải nghiệm người dùng rõ rệt.
