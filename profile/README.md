# <span style="color:red;">🌐 Swiftera Project (E-commerce)</span>

## <span style="color:red;">📚 Mục lục</span>
- [<span style="color:red;">Tên dự án và chủ đề</span>](#tên-dự-án-và-chủ-đề)
- [<span style="color:red;">Công nghệ sử dụng</span>](#công-nghệ-sử-dụng)
- [<span style="color:red;">Lấy ý tưởng dự án</span>](#lấy-ý-tưởng-dự-án)
- [<span style="color:red;">Nguyên tắc làm việc</span>](#nguyên-tắc-làm-việc)

---

## <span id="tên-dự-án-và-chủ-đề" style="color:red;">🚀 Tên dự án và lý do lựa chọn dự án</span>
**Ý nghĩa tên Swiftera**: Kết hợp giữa “Swift” (nhanh như chớp) và “Era” (kỷ nguyên, thời đại) thể hiện đây là nền tảng thương mại điện tử với một kỷ nguyên mua sắm siêu tốc, nơi mọi giao dịch diễn ra nhanh nhẹn, tiện lợi, giá cả phải chăng và dễ sử dụng.

**Lý do lựa chọn dự án**:  
1. Một số công ty sẽ yêu cầu ứng viên có kinh nghiệm trong việc xây dựng website về thương mại điện tử nên làm chủ đề này có thể giúp điền vào profile.  
2. Có nhiều website mẫu để tham khảo về giao diện, tính năng,... như Shopee, Lazada, Tiki, Amazon.  
3. Chủ đề phổ biến và có rất nhiều tính năng nên học được nhiều và tăng kinh nghiệm làm dự án. Có nhiều tính năng phổ biến như: quản lý sản phẩm vào giỏ hàng, đặt hàng, thanh toán,... có thể sử dụng ở nhiều dự án khác không chỉ riêng e-commerce.

---

## <span id="công-nghệ-sử-dụng" style="color:red;">🛠️ Công nghệ sử dụng</span>

Dư án **Swiftera** sử dụng công nghệ từ Front-end, Back-end đến các công cụ khác để triển khai và CI/CD.

<details open>
<summary><strong>💻 Front-end</strong></summary>
<br>

- **React.js**:  
  ![ReactJS](https://img.shields.io/badge/-ReactJS-000?style=for-the-badge&logo=react)

- **Redux Toolkit (RTK)** & **React Query**:  
  ![Redux Toolkit](https://img.shields.io/badge/-Redux_Toolkit-000?style=for-the-badge&logo=redux&logoColor=9370DB)  
  ![React Query](https://img.shields.io/badge/-React_Query-000?style=for-the-badge&logo=reactquery)

- **Tailwind CSS (+ shadcn/ui)**:  
  ![Tailwind CSS](https://img.shields.io/badge/-Tailwind_CSS-000?style=for-the-badge&logo=tailwindcss)

- **Axios & TypeScript**:  
  ![Axios](https://img.shields.io/badge/-Axios-000?style=for-the-badge&logo=axios)  
  ![TypeScript](https://img.shields.io/badge/-TypeScript-000?style=for-the-badge&logo=typescript)

- **Socket.IO (chat real time)**:  
  ![Socket.io](https://img.shields.io/badge/-Socket.io-000?style=for-the-badge&logo=socket.io)

</details>

<details open>
<summary><strong>⚙️ Back-end</strong></summary>
<br>

- **Java Core 21**:  
  ![Java](https://img.shields.io/badge/-Java-000?style=for-the-badge&logo=openjdk)

- **Spring Ecosystem (Spring Boot 3, Spring Security, Spring Data/JPA)**:  
  ![Spring Boot](https://img.shields.io/badge/-Spring_Boot-000?style=for-the-badge&logo=springboot)  
  ![Spring Security](https://img.shields.io/badge/-Spring_Security-000?style=for-the-badge&logo=springsecurity)  
  ![Spring Data JPA](https://img.shields.io/badge/-Spring_Data_JPA-000?style=for-the-badge&logo=spring)

- **MySQL & Maven**:  
  ![MySQL](https://img.shields.io/badge/-MySQL-000?style=for-the-badge&logo=mysql)  
  ![Maven](https://img.shields.io/badge/-Maven-000?style=for-the-badge&logo=apachemaven)

- **Socket.IO (chat real time)**:  
  ![Socket.io](https://img.shields.io/badge/-Socket.io-000?style=for-the-badge&logo=socket.io)

</details>

<details open>
<summary><strong>☁️ Others</strong></summary>
<br>

- **AWS (EC2, RDS, S3)**:  
  ![AWS](https://img.shields.io/badge/-AWS_(EC2_RDS_S3)-000?style=for-the-badge&logo=amazonaws)

- **Git & GitHub**:  
  ![Git](https://img.shields.io/badge/-Git-000?style=for-the-badge&logo=git)
  ![GitHub](https://img.shields.io/badge/-GitHub-000?style=for-the-badge&logo=github)

- **GitHub Actions (CI/CD)**:  
  ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-000?style=for-the-badge&logo=githubactions)

</details>

---

## <span id="lấy-ý-tưởng-dự-án" style="color:red;">💡 Lấy ý tưởng dự án</span>
### <span style="color:blue;">Các tính năng chính:</span>
- **Đăng ký, đăng nhập, đăng xuất tài khoản người dùng**.
- **Chat tin nhắn thời gian thực giữa người bán và người mua về sản phẩm**:
  - Tin nhắn văn bản.
  - Hỗ trợ Emoji.
  - Upload file: hình ảnh, video (<= 5MB).

---

## <span id="nguyên-tắc-làm-việc" style="color:red;">📏 Nguyên tắc làm việc</span>

> ### <span style="color:blue;">🟢 Commit Convention (Quy ước khi commit code lên GitHub):</span>
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

> ### <span style="color:blue;">🔵 Branch Naming Conventions (Quy ước đặt tên nhánh):</span>
> ```
> feature/:  dành cho phát triển tính năng mới
> bugfix/:   dành cho sửa lỗi
> 
> Quy ước:   Tên nhánh ngắn gọn, rõ ràng, không dùng ký tự đặc biệt hay viết hoa.
> Ví dụ:     feature/add-friend-functionality, bugfix/chat-not-loading
> ```

### <span style="color:blue;">🖼️ Cấu hình Prettier</span>
Cấu hình Prettier để tự động định dạng code:
```json
"editor.formatOnPaste": false,
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"prettier.singleQuote": true,
"prettier.semi": true
