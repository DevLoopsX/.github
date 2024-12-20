# <span style="color:red;">🌐 Swiftera Project (E-commerce)</span>

## <span style="color:red;">📚 Mục lục</span>
- [<span style="color:red;">Tên dự án và chủ đề</span>](#tên-dự-án-và-chủ-đề)
- [<span style="color:red;">Công nghệ sử dụng</span>](#công-nghệ-sử-dụng)
- [<span style="color:red;">Lấy ý tưởng dự án</span>](#lấy-ý-tưởng-dự-án)
- [<span style="color:red;">Nguyên tắc làm việc</span>](#nguyên-tắc-làm-việc)

## <span id="tên-dự-án-và-chủ-đề" style="color:red;">🚀 Tên dự án và lý do lựa chọn dự án</span>
**Ý nghĩa tên Swiftera**: Kết hợp giữa “Swift” (nhanh như chớp) và “Era” (kỷ nguyên, thời đại) thể hiện đây là nền tảng thương mại điện tử với một kỷ nguyên mua sắm siêu tốc, nơi mọi giao dịch diễn ra nhanh nhẹn, tiện lợi, giá cả phải chăng và dễ sử dụng.

**Lý do lựa chọn dự án**: 
1. Một số công ty sẽ yêu cầu ứng viên có kinh nghiệm trong việc xây dựng website về thương mại điện tử nên làm chủ đề này có thể giúp điền vào profile.
2. Có nhiều website mẫu để tham khảo về giao diện, tính năng,... như Shopee, Lazada, Tiki, Amazon.
3. Chủ đề phổ biến và có rất nhiều tính năng nên học được nhiều và tăng kinh nghiệm làm dự án. Có nhiều tính năng phổ biến như: quản lý sản phẩm vào giỏ hàng, đặt hàng, thanh toán,... có thể sử dụng ở nhiều dự án khác không chỉ riêng e-commerce.

## <span id="công-nghệ-sử-dụng" style="color:red;">🛠️ Công nghệ sử dụng</span>
- **Front-end**: React.js, Redux Toolkit (RTK quản lý local state), React Query (quản lý remote state), Tailwind CSS (+shadcn/ui), Axios, TypeScript, Socket.IO (chat real time).
- **Back-end**: Java Core 21, Spring Ecosystem (Spring Boot 3, Spring Security, Spring Data/JPA), MySQL, Maven, Socket.IO (chat real time).
- **Others**: AWS (EC2, RDS, S3), Git & GitHub, GitHub Actions (CI/CD).

## <span id="lấy-ý-tưởng-dự-án" style="color:red;">💡 Lấy ý tưởng dự án</span>
### <span style="color:blue;">Các tính năng chính:</span>
- **Đăng ký, đăng nhập, đăng xuất tài khoản người dùng**.
- **Chat tin nhắn thời gian thực giữa người bán và người mua về sản phẩm**:
  - Tin nhắn văn bản.
  - Hỗ trợ Emoji.
  - Upload file: hình ảnh, video (<= 5MB)

## <span id="nguyên-tắc-làm-việc" style="color:red;">📏 Nguyên tắc làm việc</span>

> ### <span style="color:blue;">🟢 Commit Convention (Quy ước khi commit code lên GitHub):</span>
> ```
> feat:     thêm một feature mới
> fix:      sửa lỗi trong hệ thống
> refactor: sửa code mà không thêm tính năng hoặc fix bug
> docs:     cập nhật hoặc thay đổi tài liệu
> chore:    thay đổi nhỏ, không liên quan đến logic code
> style:    thay đổi về giao diện, CSS/UI
> perf:     cải thiện hiệu năng xử lý
> vendor:   cập nhật phiên bản dependencies, packages
> ```

> ### <span style="color:blue;">🔵 Branch Naming Conventions (Quy ước đặt tên nhánh):</span>
> ```
> feature/: dành cho phát triển tính năng mới
> bugfix/:  dành cho sửa lỗi
> 
> Quy ước: Tên nhánh ngắn gọn, rõ ràng, không dùng ký tự đặc biệt hay viết hoa.
> Ví dụ: feature/add-friend-functionality, bugfix/chat-not-loading
> ```

### <span style="color:blue;">🖼️ Cấu hình Prettier</span>
Cấu hình Prettier để tự động định dạng code:
```json
"editor.formatOnPaste": false,
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"prettier.singleQuote": true,
"prettier.semi": true
