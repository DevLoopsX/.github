# <span style="color:red;">⚡ Swiftera - Nền tảng Thương mại điện tử cho thuê thiết bị công nghệ</span>

## <span style="color:red;">📚 Mục lục</span>

1. [Tên dự án và chủ đề](#1-tên-dự-án-và-chủ-đề)
2. [Lý do lựa chọn dự án](#2-lý-do-lựa-chọn-dự-án)
3. [Công nghệ sử dụng](#3-công-nghệ-sử-dụng)
4. [Các tính năng chính (Bám sát Yêu cầu Đề bài)](#4-các-tính-năng-chính-bám-sát-yêu-cầu-đề-bài)
5. [Vấn đề Pháp lý & Quản trị rủi ro](#5-vấn-đề-pháp-lý--quản-trị-rủi-ro)
6. [Hướng dẫn sử dụng & Demo](#6-hướng-dẫn-sử-dụng--demo)
7. [Nguyên tắc làm việc](#7-nguyên-tắc-làm-việc)

---

## <span id="1-tên-dự-án-và-chủ-đề" style="color:red;">🚀 1. Tên dự án và chủ đề</span>

### 📌 Ý nghĩa tên **Swiftera**

**Swiftera** là từ ghép mang ý nghĩa về tốc độ và xu hướng thời đại:

- **Swift**: Nhanh chóng, tốc độ, linh hoạt.
- **Era**: Kỷ nguyên, thời đại.

**Swift + Era = Swiftera** → _"Kỷ nguyên tiếp cận và sử dụng công nghệ nhanh chóng mà không cần sở hữu"_.

### 🎯 Sơ lược về dự án

**Swiftera** là nền tảng thương mại điện tử hoạt động theo mô hình **Cho thuê (Rental E-commerce)**, tập trung vào đồ công nghệ (B2C và C2C):

- Người cho thuê (**Lessor**) đăng tải thiết bị (máy ảnh, flycam, laptop, console game) với giá thuê theo ngày và tiền cọc thế chấp.
- Người thuê (**Renter**) chọn ngày rảnh trên lịch, thanh toán tiền thuê và đặt cọc qua ví trung gian (Escrow) để nhận đồ.
- Ứng dụng tích hợp **Goong Maps / Google Maps** để tìm kiếm đồ cho thuê quanh khu vực và **AI Computer Vision** để soi tình trạng xước xát của máy lúc giao/nhận nhằm bảo vệ tài sản hai bên.

---

## <span id="2-lý-do-lựa-chọn-dự-án" style="color:red;">🔥 2. Lý do lựa chọn dự án</span>

- **Đón đầu xu hướng Rental Economy**: Giải quyết nhu cầu sử dụng đồ công nghệ đắt tiền trong thời gian ngắn của sinh viên, freelancer mà không cần bỏ số tiền lớn mua đứt.
- **Giải quyết rủi ro bằng công nghệ sâu**: Giải quyết triệt để bài toán mất cắp hoặc tranh chấp hỏng hóc bằng e-KYC định danh, ví trung gian giữ cọc và AI soi vết xước.
- **Rèn luyện Tech Stack hiện đại**: Xử lý logic Booking phức tạp, Quản lý State tối ưu với Zustand trên nền tảng Next.js (App Router) kết hợp UI components từ shadcn/ui.

---

## <span id="3-công-nghệ-sử-dụng" style="color:red;">🛠️ 3. Công nghệ sử dụng</span>

### <span style="font-size:18px;">✨ Front-end</span>

<div align="left" style="margin: 15px 0 20px 0; display: flex; flex-wrap: wrap;">
  <img src="https://img.shields.io/badge/-TypeScript-000?style=for-the-badge&logo=typescript" alt="TypeScript" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Next.js-000?style=for-the-badge&logo=next.js" alt="Next.js" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-shadcn%2Fui-000?style=for-the-badge&logo=uiomatic" alt="shadcn/ui" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Tailwind_CSS-000?style=for-the-badge&logo=tailwind-css" alt="Tailwind CSS" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Zustand-000?style=for-the-badge&logo=react" alt="Zustand" style="margin-right: 19px; margin-bottom: 12px;"/>
</div>

---

### <span style="font-size:18px;">🔧 Back-end & AI</span>

<div align="left" style="margin: 15px 0 20px 0; display: flex; flex-wrap: wrap;">
  <img src="https://img.shields.io/badge/-Java_25-000?style=for-the-badge&logo=openjdk" alt="Java" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Spring_Boot_4-000?style=for-the-badge&logo=springboot" alt="Spring Boot" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Spring_Security_6-000?style=for-the-badge&logo=springsecurity" alt="Spring Security" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-MySQL_8.4-000?style=for-the-badge&logo=mysql" alt="MySQL" style="margin-right: 19px; margin-bottom: 12px;"/>
</div>

---

### <span style="font-size:18px;">🌐 Others & Deploy</span>

<div align="left" style="margin: 15px 0 20px 0; display: flex; flex-wrap: wrap;">
    <img src="https://img.shields.io/badge/-Goong_Maps-000?style=for-the-badge&logo=googlemaps" alt="Goong Maps" style="margin-right: 19px; margin-bottom: 12px;"/>
    <img src="https://img.shields.io/badge/-GitHub_Actions-000?style=for-the-badge&logo=githubactions" alt="GitHub Actions" style="margin-right: 19px; margin-bottom: 12px;"/>
    <img src="https://img.shields.io/badge/-Nginx-000?style=for-the-badge&logo=nginx" alt="Nginx" style="margin-right: 19px; margin-bottom: 12px;"/>
    <img src="https://img.shields.io/badge/-AWS_S3-000?style=for-the-badge&logo=AmazonWebServices" alt="AWS S3" style="margin-right: 19px; margin-bottom: 12px;"/>
    <img src="https://img.shields.io/badge/-AWS_EC2-000?style=for-the-badge&logo=AmazonWebServices" alt="AWS EC2" style="margin-right: 19px; margin-bottom: 12px;"/>
    <img src="https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white" style="margin-right: 19px; margin-bottom: 12px;"/>
</div>

---

## <span id="4-các-tính-năng-chính-bám-sát-yêu-cầu-đề-bài" style="color:red;">🎮 4. Các tính năng chính (Bám sát Yêu cầu Đề bài)</span>

Dự án đáp ứng 100% các yêu cầu chức năng từ đề cương môn học:

### 1. 🔐 Đăng nhập, đăng xuất & e-KYC

- Hỗ trợ đăng nhập bằng Email/SĐT kèm JWT token.
- Bắt buộc xác thực **e-KYC** (tải lên CCCD 2 mặt) trước khi thuê hoặc cho thuê đồ để đảm bảo định danh người dùng theo quy định pháp luật.

### 2. 🎛️ Trang quản trị (Admin Panel)

- Phân quyền Role-based Access Control (Admin / Renter / Lessor).
- Admin quản lý danh sách người dùng, phê duyệt bài đăng (Listing) để tránh hàng cấm, theo dõi doanh thu phí sàn và giải quyết các tranh chấp hư hỏng thiết bị.

### 3. 🔍 Lọc, tìm kiếm & Sắp xếp (Filter, Search, Sort)

- **Tìm kiếm:** Theo tên thiết bị (VD: "Sony A6000", "MacBook Pro").
- **Lọc:** Theo danh mục (Máy ảnh, Gaming, PC), khoảng giá thuê, và **lọc theo ngày rảnh (Date Range Picker)** trên lịch.
- **Sắp xếp:** Giá từ thấp đến cao, thiết bị gần vị trí người dùng nhất, và đánh giá cao nhất.

### 4. 🖼️ Ảnh sản phẩm & 📱 Responsive

- Hỗ trợ tải lên nhiều ảnh cho một sản phẩm (Slider ảnh chi tiết mặt trước, sau, cạnh máy) nhằm minh bạch tình trạng xước xát.
- Giao diện xây dựng bằng **Tailwind CSS + shadcn/ui** đảm bảo **Responsive 100%**, tương thích hoàn hảo trên cả Mobile, Tablet và Desktop.

### 5. 🛒 Giỏ hàng, thanh toán (Escrow Wallet)

- Cho phép Renter gom nhiều món đồ (thuê cùng thời gian) vào chung một giỏ hàng.
- Tích hợp thanh toán VNPAY. Hoạt động theo cơ chế **Ví trung gian (Escrow)**: Khách thanh toán Tổng tiền (Tiền thuê + Tiền cọc). Sàn giữ Tiền cọc để làm tài sản bảo đảm, chỉ trả Tiền thuê cho Lessor sau khi giao dịch hoàn tất.

### 6. 🗺️ Google Maps / Goong Maps

- Tích hợp bản đồ để định vị các món đồ cho thuê quanh bán kính 5-10km.
- Giúp Renter tìm đồ gần nhà để tự đến lấy (**Pickup**), tiết kiệm chi phí vận chuyển 2 chiều đắt đỏ của thiết bị cồng kềnh.

### 7. 🎁 Khuyến mại, giá mới, giá cũ

- Lessor có thể thiết lập chương trình giảm giá nếu thuê dài ngày (VD: Thuê > 7 ngày giảm 20%).
- UI sẽ hiển thị **Giá cũ (Bị gạch chéo)** và **Giá mới (In đậm, màu đỏ)** trên trang chi tiết sản phẩm. Có hỗ trợ nhập mã Voucher khi thanh toán.

### 8. 📜 Chính sách đổi trả, bảo hành, vận chuyển

- Tích hợp tự động sinh **Hợp đồng điện tử (E-contract)** trước khi thanh toán.
- Hiển thị minh bạch trang CMS các chính sách: Quy định bồi thường (nếu xước xát/rơi vỡ), Chính sách hoàn cọc tự động, Miễn trừ trách nhiệm dữ liệu.

### 9. ⭐ Đánh giá sản phẩm, bình luận & Liên hệ

- **Đánh giá:** Renter chấm điểm uy tín (Rating 5 sao) và để lại review sau khi trả đồ.
- **Bình luận & Liên hệ:** Khung hỏi đáp trực tiếp dưới bài đăng hoặc tính năng Chat nội bộ để Renter hỏi Lessor các vấn đề kỹ thuật (VD: "Máy này quay 4K bị quá nhiệt không?"). Có form Contact Admin để báo lỗi.

---

## <span id="5-vấn-đề-pháp-lý--quản-trị-rủi-ro" style="color:red;">⚖️ 5. Vấn đề Pháp lý & Quản trị rủi ro</span>

Do đặc thù giá trị hàng hóa lớn, dự án **Swiftera** được thiết kế tuân thủ nghiêm ngặt **Luật Thương mại điện tử Việt Nam (Luật số: 122/2025/QH15)** và các quy định liên quan:

### 5.1. Giấy phép hoạt động (Điều 14 - Luật TMĐT 2025)

- Hệ thống hoạt động dưới mô hình **Sàn giao dịch TMĐT** (trung gian kết nối người cho thuê và người thuê).
- Chủ quản nền tảng tuân thủ quy định đăng ký và khai báo pháp nhân với Bộ Công Thương (gắn logo xanh "Đã đăng ký Bộ Công Thương").

### 5.2. Giải quyết Tranh chấp & Trách nhiệm Chủ sàn (Điều 15 & 17)

- Sàn cung cấp cơ chế tiếp nhận khiếu nại trực tuyến.
- Tích hợp **AI Computer Vision**: Chụp ảnh máy trước và sau khi thuê. Nếu xảy ra tranh chấp xước xát/hỏng hóc, AI sẽ so sánh ảnh làm bằng chứng điện tử để Admin quyết định trừ tiền cọc đền bù (tranh chấp dân sự), đảm bảo tính công bằng và miễn trừ trách nhiệm pháp lý liên đới cho chủ sàn.

### 5.3. Ngăn chặn Lạm dụng tín nhiệm chiếm đoạt tài sản (Hình sự)

- Để phòng chống việc Renter thuê đồ rồi mang đi cầm đồ/bán trộm, hệ thống yêu cầu bắt buộc **e-KYC (Xác thực Căn cước công dân)** liên kết dữ liệu định danh.
- Tích hợp cơ chế **Đặt cọc (Deposit)** qua cổng thanh toán/thẻ tín dụng thay vì niềm tin thông thường, tạo rào cản tài chính đối với các hành vi gian lận.

### 5.4. Bảo vệ dữ liệu cá nhân (Nghị định 13/2023/NĐ-CP)

- Hệ thống bắt buộc người dùng tick chọn _"Đồng ý với chính sách xử lý dữ liệu cá nhân"_ khi thu thập CCCD.
- Có hợp đồng điện tử yêu cầu Renter cam kết **Tự sao lưu và Xóa dữ liệu** (trên máy ảnh, laptop) trước khi trả máy; Sàn và Lessor được miễn trừ trách nhiệm về lộ lọt dữ liệu hậu giao dịch.

---

## <span id="6-hướng-dẫn-sử-dụng--demo" style="color:red;">📽️ 6. Hướng dẫn sử dụng & Demo</span>

Xem ngay video hướng dẫn sử dụng và Demo hệ thống Swiftera: [https://www.youtube.com/watch?v=SwifteraDemo](https://www.youtube.com/watch?v=SwifteraDemo)

---

## <span id="7-nguyên-tắc-làm-việc" style="color:red;">📏 7. Nguyên tắc làm việc</span>

### 🟢 **Commit Convention (Quy ước khi commit code lên GitHub)**

- `feat`: thêm một feature mới
- `fix`: sửa lỗi trong hệ thống
- `refactor`: sửa code mà không thêm tính năng hoặc fix bug
- `docs`: cập nhật hoặc thay đổi tài liệu
- `chore`: thay đổi nhỏ, không liên quan đến logic code
- `style`: thay đổi về giao diện, CSS/UI
- `perf`: cải thiện hiệu năng xử lý
- `vendor`: cập nhật phiên bản dependencies, packages

### 🔵 **Branch Naming Conventions (Quy ước đặt tên nhánh)**

- `feature/`: dành cho phát triển tính năng mới
- `bugfix/`: dành cho sửa lỗi

**Quy ước**: Tên nhánh ngắn gọn, rõ ràng, không dùng ký tự đặc biệt hay viết hoa.

**Ví dụ**: `feature/add-zustand-store`, `bugfix/calendar-conflict`

### 🎨 **Cấu hình Prettier**

```json
{
    "editor.formatOnPaste": false,
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "prettier.singleQuote": true,
    "prettier.semi": true
}
```
