# Bài 6 : Sự cố tài liệu dự án trên GitHub
## Phần 1. Phân tích lỗi và So sánh Rich Text vs. Markdown
1. Chỉ ra 2 sai lầm trong tư duy của Nam

- Sai lầm 1: Sử dụng định dạng tệp Rich Text (.docx) cho mã nguồn và tài liệu kỹ thuật trên Git.
Bản chất File Word là định dạng nhị phân nén, lưu trữ nhiều thông tin định dạng phức tạp . Hệ thống quản lý mã nguồn Git được thiết kế tối ưu cho văn bản thuần túy , nên nó không thể so sánh chi tiết từng dòng văn bản bên trong file .docx mà chỉ xem đó là một cục dữ liệu thay đổi toàn bộ.

- Sai lầm 2: Bỏ qua tính năng hiển thị trực tiếp (Markdown Preview) trên trình duyệt web của GitHub.
Bản chất Nam nghĩ rằng đưa file nào lên GitHub cũng đọc được như mở trên máy tính cá nhân. Tuy nhiên, các cộng tác viên (như Minh Anh, Hướng, Đức) không thể xem trực tiếp nội dung file .docx ngay trên trình duyệt mà bắt buộc phải tải về máy, gây cản trở nghiêm trọng trong việc review code/documentation chung của nhóm.

2. Tại sao Markdown an toàn và nhẹ hơn?

- Cơ chế lưu trữ Plain Text: Markdown lưu trữ hoàn toàn bằng ký tự chữ cái thông thường. Kích thước file cực kỳ nhẹ chỉ vài KB, tốc độ truyền tải và đồng bộ trên Git nhanh chóng.

- Khả năng kháng lỗi dữ liệu: Nếu một file Word bị lỗi mạng làm mất hoặc sai lệch chỉ 1 byte dữ liệu ở phần cấu trúc nén XML, toàn bộ file sẽ hỏng hoàn toàn và không thể mở được. Ngược lại, với file Markdown, nếu một ký tự bị hỏng hoặc mất, chỉ vị trí đó lỗi hiển thị, các phần nội dung văn bản còn lại vẫn đọc được bình thường.

- Tối ưu hóa Git Diff & Tránh Conflict: Khi hai người cùng sửa file Markdown, Git có thể so sánh chính xác từng dòng và tự động trộn các thay đổi nhỏ. Nếu có xung đột, việc giải quyết conflict trên file text vô cùng dễ dàng và trực quan.

## Phần 2. Hoàn thiện: Sử dụng StackEdit để chuyển đổi đoạn giới thiệu từ Word sang Markdown (.md).
### GreenTech Project

Hệ thống ứng dụng công nghệ để bảo vệ môi trường, giúp cuộc sống xanh và bền vững.

---

###  1. Giới thiệu
**GreenTech** là dự án hướng tới việc ứng dụng công nghệ số để bảo vệ môi trường, giúp cuộc sống xanh và bền vững cho cộng đồng.

###  2. Mục tiêu
- Tạo ra giải pháp công nghệ xanh.
- Nâng cao ý thức cộng đồng.
- Phát triển bền vững.