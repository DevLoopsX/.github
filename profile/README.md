# <span style="color:#e74c3c;">🌐 Swiftera Project (E-commerce)</span>

## <span style="color:#e74c3c;">📚 Mục lục</span>
- [<span style="color:#e74c3c;">Tên dự án và chủ đề</span>](#tên-dự-án-và-chủ-đề)
- [<span style="color:#e74c3c;">Công nghệ sử dụng</span>](#công-nghệ-sử-dụng)
- [<span style="color:#e74c3c;">Lấy ý tưởng dự án</span>](#lấy-ý-tưởng-dự-án)
- [<span style="color:#e74c3c;">Nguyên tắc làm việc</span>](#nguyên-tắc-làm-việc)

---

## <span id="tên-dự-án-và-chủ-đề" style="color:#e74c3c;">🚀 Tên dự án và lý do lựa chọn dự án</span>
**Ý nghĩa tên Swiftera**:  
Kết hợp giữa **“Swift”** (nhanh như chớp) và **“Era”** (kỷ nguyên), thể hiện đây là nền tảng thương mại điện tử tạo nên một **kỷ nguyên mua sắm siêu tốc**, nơi mọi giao dịch diễn ra nhanh nhẹn, tiện lợi, giá cả phải chăng và dễ sử dụng.

**Lý do lựa chọn dự án**:  
1. **Kinh nghiệm chuyên môn**: Nhiều công ty yêu cầu ứng viên có kinh nghiệm làm E-commerce, dự án này giúp nâng cao profile.  
2. **Tham khảo phong phú**: Giao diện, tính năng có thể học hỏi từ Shopee, Lazada, Tiki, Amazon.  
3. **Chủ đề phổ biến**: Dễ học nhiều tính năng hữu ích (giỏ hàng, thanh toán, chat,...), áp dụng cho nhiều dự án sau này.

---

## <span id="công-nghệ-sử-dụng" style="color:#e74c3c;">🛠️ Công nghệ sử dụng</span>
- **Front-end**:  
  - <span style="color:#2980b9;">React.js</span>, <span style="color:#2980b9;">Redux Toolkit (RTK)</span>, <span style="color:#2980b9;">React Query</span>,  
    <span style="color:#2980b9;">Tailwind CSS (+shadcn/ui)</span>, <span style="color:#2980b9;">Axios</span>,  
    <span style="color:#2980b9;">TypeScript</span>, <span style="color:#2980b9;">Socket.IO</span> (chat real-time)
  
- **Back-end**:  
  - <span style="color:#27ae60;">Java Core 21</span>, <span style="color:#27ae60;">Spring Boot 3</span>,  
    <span style="color:#27ae60;">Spring Security</span>, <span style="color:#27ae60;">Spring Data/JPA</span>,  
    <span style="color:#27ae60;">MySQL</span>, <span style="color:#27ae60;">Maven</span>,  
    <span style="color:#27ae60;">Socket.IO</span> (chat real-time)
  
- **Others**:  
  - <span style="color:#8e44ad;">AWS (EC2, RDS, S3)</span>, <span style="color:#8e44ad;">Git & GitHub</span>,  
    <span style="color:#8e44ad;">GitHub Actions (CI/CD)</span>

---

## <span id="lấy-ý-tưởng-dự-án" style="color:#e74c3c;">💡 Lấy ý tưởng dự án</span>
### <span style="color:#3498db;">Các tính năng chính:</span>
- **Đăng ký, đăng nhập, đăng xuất tài khoản người dùng**.
- **Chat tin nhắn thời gian thực giữa người bán và người mua**:
  - Tin nhắn văn bản.
  - Hỗ trợ Emoji.
  - Upload file: hình ảnh, video (<= 5MB).

---

## <span id="nguyên-tắc-làm-việc" style="color:#e74c3c;">📏 Nguyên tắc làm việc</span>

> ### <span style="color:#3498db;">🟢 Commit Convention (Quy ước commit)</span>
> ```
> feat:      thêm một feature mới
> fix:       sửa lỗi trong hệ thống
> refactor:  sửa code mà không thêm tính năng hoặc fix bug
> docs:      cập nhật hoặc thay đổi tài liệu
> chore:     thay đổi nhỏ, không liên quan đến logic code
> style:     thay đổi về giao diện, CSS/UI
> perf:      cải thiện hiệu năng xử lý
> vendor:    cập nhật phiên bản dependencies, packages
> ```

> ### <span style="color:#3498db;">🔵 Branch Naming Conventions (Quy ước tên nhánh)</span>
> ```
> feature/:  dành cho phát triển tính năng mới
> bugfix/:   dành cho sửa lỗi
>
> Ví dụ:
> feature/add-friend-functionality
> bugfix/chat-not-loading
> ```

### <span style="color:#3498db;">🖼️ Cấu hình Prettier</span>
Cấu hình Prettier để tự động định dạng code:
```json
"editor.formatOnPaste": false,
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"prettier.singleQuote": true,
"prettier.semi": true
