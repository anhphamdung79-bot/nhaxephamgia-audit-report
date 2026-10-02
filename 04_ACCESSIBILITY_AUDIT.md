# Accessibility Audit

## 1. Objective
Accessibility đảm bảo website có thể sử dụng được bởi người dùng có khó khăn về thị lực, di chuyển bằng bàn phím hoặc sử dụng công nghệ hỗ trợ như screen reader.

## 2. Key Findings

| Area | Status | Notes |
|---|---|---|
| Color contrast | ⚠️ Weak | Một số text/background chưa đạt AA |
| Keyboard navigation | ❌ Weak | Menu và button c��n hỗ trợ Tab/Enter |
| Focus indicator | ❌ Missing | Chưa rõ ràng khi focus vào element |
| Form labels | ⚠️ Partial | Cần rõ ràng hơn |
| Alt text | ❌ Weak | Một số hình ảnh không có mô tả rõ nghĩa |
| Heading hierarchy | ❌ Weak | Không nhất quán |
| Responsive UI | ⚠️ Moderate | Nút và links cần dễ bấm hơn trên mobile |

## 3. Recommendations
- Tăng contrast theo tiêu chuẩn WCAG AA.
- Thêm focus-visible state cho menu, button và input.
- Đảm bảo các CTA có thể truy cập bằng bàn phím.
- Chạy các test với WAVE, axe DevTools và Lighthouse.
- Đặt label cho form và thông báo lỗi phù hợp.

## 4. Priority Fixes
### P1
- Focus states
- Contrast
- Alt text
- Keyboard usability

### P2
- Form labels
- Heading consistency
- Mobile tap target size

## 5. Expected Impact
Cải thiện accessibility giúp mở rộng đối tượng người dùng, tuân thủ chuẩn web và nâng trải nghiệm tổng thể.
