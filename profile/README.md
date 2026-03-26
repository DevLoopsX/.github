# <span style="color:red;">⚡ Swiftera - Nền tảng Thương mại điện tử cho thuê thiết bị công nghệ</span>

## <span style="color:red;">📚 Mục lục</span>

1. [Tên dự án và chủ đề](#1-tên-dự-án-và-chủ-đề)
2. [Lý do lựa chọn dự án](#2-lý-do-lựa-chọn-dự-án)
3. [Công nghệ sử dụng](#3-công-nghệ-sử-dụng)
4. [Các tính năng chính (Bám sát Yêu cầu Đề bài)](#4-các-tính-năng-chính-bám-sát-yêu-cầu-đề-bài)
5. [Luồng hoạt động & Kịch bản chi tiết (Business Flow)](#5-luồng-hoạt-động--kịch-bản-chi-tiết-business-flow)
6. [Vấn đề Pháp lý & Quản trị rủi ro](#6-vấn-đề-pháp-lý--quản-trị-rủi-ro)
7. [Hướng dẫn sử dụng & Demo](#7-hướng-dẫn-sử-dụng--demo)
8. [Nguyên tắc làm việc](#8-nguyên-tắc-làm-việc)

---

## <span id="1-tên-dự-án-và-chủ-đề" style="color:red;">🚀 1. Tên dự án và chủ đề</span>

### 📌 Ý nghĩa tên **Swiftera**

**Swiftera** là từ ghép mang ý nghĩa về tốc độ và xu hướng thời đại:

- **Swift**: Nhanh chóng, tốc độ, linh hoạt.
- **Era**: Kỷ nguyên, thời đại.

**Swift + Era = Swiftera** → _"Kỷ nguyên tiếp cận và sử dụng công nghệ nhanh chóng mà không cần sở hữu"_.

### 🎯 Sơ lược về dự án

**Swiftera** là nền tảng thương mại điện tử hoạt động theo mô hình **Cho thuê (Rental E-commerce) thuần B2C kết hợp O2O (Online to Offline)**:

- **Công ty tự đầu tư và sở hữu 100% kho thiết bị** (máy ảnh, flycam, laptop, console game) để cho khách hàng cá nhân thuê.
- Khách hàng (**Renter**) thao tác Online: Chọn ngày rảnh, thanh toán tiền thuê, đặt cọc và thực hiện e-KYC (Tải ảnh CCCD).
- Khách hàng đến nhận máy trực tiếp Offline tại các **Trạm giao dịch (Tech Hubs)** của Swiftera. Tại đây, **Nhân viên (Staff)** thao tác trên hệ thống để đối chiếu danh tính, chụp ảnh đồng kiểm và ký hợp đồng bằng mã OTP.

---

## <span id="2-lý-do-lựa-chọn-dự-án" style="color:red;">🔥 2. Lý do lựa chọn dự án</span>

* **Đề tài mới lạ, đột phá tại Việt Nam (Thoát khỏi lối mòn đồ án):** Hầu hết các đồ án môn học Thương mại điện tử hiện nay đều tập trung vào mô hình Bán lẻ truyền thống (Bán quần áo, giày dép, thức ăn...). Việc lựa chọn mô hình **Cho thuê trực tuyến (Rental E-commerce)** mang lại sự mới mẻ, độc đáo. Đề tài này không chỉ giải quyết nhu cầu thực tế của giới trẻ (thích trải nghiệm đồ xịn mà không cần mua đứt) mà còn giúp đồ án trở nên thú vị, nổi bật và ít "nhàm chán" hơn trước hội đồng đánh giá.

* **Thử thách kỹ thuật & Tư duy thiết kế hệ thống (System Design):** Khác với bán đứt, quy trình cho thuê đòi hỏi giải quyết những bài toán logic phức tạp hơn gấp nhiều lần. Nhóm sẽ có cơ hội rèn luyện kỹ năng xử lý: Thuật toán chặn lịch (Block Calendar) để tránh trùng lặp ngày thuê, quản lý dòng tiền đa chiều (Thanh toán tiền thuê + Giữ tiền cọc + Gọi API Hoàn cọc tự động), và đồng bộ trạng thái phức tạp giữa 3 nền tảng (User, Staff, Admin) bằng **Next.js** và **Zustand**.

* **Tính ứng dụng thực tiễn & Quản trị rủi ro doanh nghiệp (O2O):** Dự án không chỉ dừng lại ở việc "code cho web chạy", mà còn thể hiện tư duy kinh doanh và am hiểu pháp luật. Việc áp dụng mô hình O2O (Online to Offline), định danh e-KYC và sử dụng Hợp đồng điện tử OTP giúp giải quyết triệt để "nỗi đau" lớn nhất của ngành cho thuê: Rủi ro mất cắp và Tranh chấp bồi thường, biến Swiftera thành một dự án có tính khả thi cực cao để khởi nghiệp thực tế.

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

### <span style="font-size:18px;">🔧 Back-end</span>

<div align="left" style="margin: 15px 0 20px 0; display: flex; flex-wrap: wrap;">
  <img src="https://img.shields.io/badge/-Java-000?style=for-the-badge&logo=openjdk" alt="Java" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Spring_Boot-000?style=for-the-badge&logo=springboot" alt="Spring Boot" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Spring_Security-000?style=for-the-badge&logo=springsecurity" alt="Spring Security" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-Spring_Data_JPA-000?style=for-the-badge&logo=spring" alt="Spring Data JPA" style="margin-right: 19px; margin-bottom: 12px;"/>
  <img src="https://img.shields.io/badge/-MySQL-000?style=for-the-badge&logo=mysql" alt="MySQL" style="margin-right: 19px; margin-bottom: 12px;"/>
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

## <span id="4-các-tính-năng-chính-bám-sát-yêu-cầu-đề-bài" style="color:red;">🎯 4. Các tính năng chính</span>

Swiftera  triển khai đầy đủ các nhóm chức năng cốt lõi cho một nền tảng thuê thiết bị công nghệ theo mô hình B2C kết hợp O2O, gồm quản lý danh mục sản phẩm, tồn kho theo serial, giỏ hàng, đơn thuê, thanh toán online, hợp đồng, policy/consent, đánh giá sản phẩm, ticket hỗ trợ và IAM nội bộ. :contentReference[oaicite:0]{index=0}

### 4.1. Quản lý tài khoản, xác thực và phân quyền
- Hỗ trợ đăng ký tài khoản, xác thực email, đăng nhập, refresh token, quên mật khẩu và đăng xuất.
- Hệ thống dùng JWT cho xác thực và quản lý refresh token ở DB.
- Phân quyền nội bộ theo mô hình **User - Role - Permission**, trong đó permission được quản lý theo `apiPath + httpMethod + module`.
- `PermissionInterceptor` kiểm tra quyền truy cập endpoint ở runtime. 

### 4.2. Quản lý danh mục, sản phẩm, hình ảnh và hub
- Quản lý cây danh mục nhiều cấp (`Category`).
- Quản lý sản phẩm cho thuê (`Product`) với các thông tin như tên, mô tả, giá thuê ngày, tiền cọc, số ngày thuê tối thiểu, trạng thái active.
- Quản lý nhiều ảnh cho mỗi sản phẩm (`ProductImage`), có `sortOrder` và `isPrimary`.
- Quản lý các hub vận hành/kho hàng (`Hub`) với mã hub, địa chỉ, tọa độ và trạng thái hoạt động. 

### 4.3. Quản lý tồn kho vật lý theo serial
- Mỗi tài sản vật lý được quản lý dưới dạng `InventoryItem` riêng theo serial number.
- Mỗi item gắn với một product và một hub cụ thể.
- Item có trạng thái vận hành như `AVAILABLE`, `RESERVED`, `RENTED` và các thông tin đánh giá tình trạng.
- Đây là nền tảng để hệ thống chống overbooking và theo dõi vòng đời từng món hàng thực tế. 

### 4.4. Giỏ hàng thuê thiết bị
- Mỗi user có một giỏ hàng (`Cart`) riêng.
- User có thể thêm dòng giỏ (`CartLine`), cập nhật, xóa từng dòng hoặc xóa toàn bộ giỏ.
- `CartLine` hiện lưu sản phẩm, khoảng ngày thuê và số lượng.
- Hệ thống kiểm tra nghiệp vụ khi thêm/cập nhật giỏ:
  - sản phẩm phải còn active,
  - khoảng ngày thuê phải hợp lệ,
  - số ngày thuê phải lớn hơn hoặc bằng `minRentalDays`,
  - `quantity >= 1`.
- Response giỏ hàng trả thêm `productImageUrl` và `lineTotal` để frontend hiển thị thuận tiện. 

### 4.5. Tạo đơn thuê và snapshot dữ liệu nghiệp vụ
- Từ line items ở frontend, hệ thống tạo `RentalOrder` và `RentalOrderLine`.
- Khi tạo đơn, backend snapshot các thông tin quan trọng để bảo toàn dữ liệu nghiệp vụ tại thời điểm đặt thuê, gồm:
  - thông tin giao hàng,
  - `voucherCodeSnapshot`,
  - `productNameSnapshot`,
  - `dailyPriceSnapshot`,
  - `depositAmountSnapshot`.
- Hệ thống tính các giá trị tiền thuê, giảm giá voucher và tiền cọc ngay tại bước tạo đơn. 

### 4.6. Chống overbooking và giữ chỗ tồn kho
- Khi tạo đơn, hệ thống tự chọn `InventoryItem` đang khả dụng theo thứ tự FIFO (`createdAt ASC`).
- Việc lấy inventory khả dụng có dùng lock pessimistic để giảm race condition.
- Hệ thống reserve inventory ngay khi tạo order để tránh nhiều khách đặt trùng cùng một serial vật lý.
- Nếu hủy đơn ở trạng thái cho phép, inventory sẽ được release về trạng thái khả dụng. 

### 4.7. Thanh toán online qua VNPay
- Hệ thống khởi tạo `PaymentTransaction` riêng cho từng đơn thuê.
- FE gọi API initiate payment để nhận URL thanh toán VNPay.
- Backend xử lý callback IPN từ VNPay:
  - verify checksum,
  - đối chiếu số tiền,
  - cập nhật transaction `SUCCESS` hoặc `FAILED`,
  - cộng dồn `grandTotalPaid`,
  - nếu đủ tiền thì chuyển đơn sang `PAID`.
- Browser sau thanh toán được redirect về frontend qua endpoint return. 

### 4.8. Vận hành vòng đời đơn thuê
- Hệ thống quản lý vòng đời đơn bằng state machine.
- Các thao tác vận hành chính đã có endpoint chuyên biệt:
  - đổi trạng thái đơn,
  - gán hub,
  - gán nhân sự giao/thu hồi,
  - ghi nhận giao hàng,
  - ghi nhận thu hồi,
  - set penalty khi có hư hại hoặc mất mát.
- Khi giao hàng, inventory chuyển từ `RESERVED` sang `RENTED`.
- Khi thu hồi, inventory chuyển từ `RENTED` hoặc `RESERVED` về `AVAILABLE`. 

### 4.9. Quản lý voucher và khuyến mại
- Hệ thống hỗ trợ voucher giảm giá theo phần trăm hoặc cố định.
- Voucher có các ràng buộc như:
  - trạng thái active,
  - thời hạn hiệu lực,
  - giới hạn số lượt sử dụng,
  - số ngày thuê tối thiểu,
  - mức trần giảm giá nếu là dạng phần trăm.
- `usedCount` của voucher được tăng/giảm theo lifecycle đơn thuê. 

### 4.10. Policy, consent và hợp đồng thuê
- Admin quản lý `PolicyDocument` theo `code` và `version`.
- User phải consent policy trước khi tạo hợp đồng.
- Hệ thống chỉ cho tạo `RentalContract` khi:
  - order ở trạng thái `PAID` hoặc `PREPARING`,
  - policy đang active và là bản latest theo code,
  - user của order đã có consent `ACCEPTED`.
- Mỗi order chỉ có một contract.
- Khi tạo contract, backend tự sinh `contractNumber` và lưu metadata xác nhận như IP/User-Agent. 

### 4.11. Đánh giá sản phẩm và hỗ trợ khách hàng
- Sau khi đơn `COMPLETED`, user có thể tạo review cho sản phẩm đã thuê.
- Rule nghiệp vụ:
  - chỉ owner của order được review,
  - product phải thuộc order,
  - chặn duplicate review trên cùng cặp `(order, user, product)`.
- Hệ thống cũng hỗ trợ `ContactTicket` cho user hoặc guest, cho phép Staff/Admin phản hồi và đóng ticket khi xử lý xong. 

### 4.12. Quản trị nội bộ cho Admin/Staff
- Admin/Staff có thể quản lý:
  - users, roles, permissions,
  - categories, hubs, products, product images,
  - inventory items,
  - vouchers,
  - rental orders,
  - payment transactions,
  - policy documents,
  - contact tickets.
- Đây là lớp vận hành nội bộ chính của hệ thống hiện tại. 

---

## <span id="5-luồng-hoạt-động--kịch-bản-chi-tiết-business-flow" style="color:red;">🔄 5. Luồng hoạt động & Kịch bản chi tiết (Business Flow)</span>

Luồng hoạt động hiện tại của hệ thống được thiết kế theo hướng: khách hàng duyệt sản phẩm và tạo đơn trên nền tảng online, sau đó khối vận hành nội bộ tiếp tục xử lý vòng đời đơn thuê theo state machine cho đến khi hoàn tất. 

### 5.1. Giai đoạn 1: Khách hàng đăng ký, xác thực và đăng nhập
1. Người dùng đăng ký tài khoản.
2. Hệ thống gửi email xác thực.
3. Sau khi verify email thành công, user có thể đăng nhập.
4. Hệ thống cấp access token và refresh token để sử dụng các endpoint cần xác thực. 

### 5.2. Giai đoạn 2: Duyệt sản phẩm và chuẩn bị thuê
1. User xem danh sách sản phẩm và danh mục.
2. User xem chi tiết sản phẩm theo ID hoặc slug.
3. User có thể xem hub công khai để tham khảo điểm vận hành/giao nhận.
4. Từ dữ liệu sản phẩm và ảnh, frontend hiển thị thông tin cần thiết cho quyết định thuê. 

### 5.3. Giai đoạn 3: Tạo và quản lý giỏ hàng
1. User mở giỏ bằng `GET /cart`; hệ thống sẽ lấy giỏ hiện có hoặc tự tạo mới nếu chưa tồn tại.
2. User thêm dòng giỏ bằng `POST /cart/lines` với sản phẩm, khoảng ngày thuê và số lượng.
3. User có thể cập nhật line bằng `PATCH /cart/lines/{cartLineId}` khi đổi lịch hoặc số lượng.
4. User có thể xóa từng dòng hoặc clear toàn bộ giỏ. 

### 5.4. Giai đoạn 4: Tạo đơn thuê và giữ chỗ inventory
1. FE gửi `POST /rental-orders` từ danh sách line items cùng thông tin giao hàng và voucher code nếu có.
2. Backend kiểm tra điều kiện nghiệp vụ của line items.
3. Service snapshot dữ liệu quan trọng của order và order line.
4. Hệ thống tính:
   - số ngày thuê,
   - subtotal,
   - discount,
   - tiền cọc,
   - tổng tiền cần thanh toán.
5. Backend chọn `InventoryItem` `AVAILABLE` theo FIFO và reserve hàng ngay khi tạo order.
6. Đơn được tạo ở trạng thái `PENDING_PAYMENT`. 

### 5.5. Giai đoạn 5: Thanh toán qua VNPay
1. FE gọi `POST /payments/{rentalOrderId}/initiate`.
2. Backend tạo `PaymentTransaction` ở trạng thái `PENDING` và trả về payment URL.
3. User thanh toán trên giao diện VNPay.
4. VNPay gọi `GET /payments/vnpay/ipn` về backend.
5. Backend:
   - verify checksum,
   - tìm transaction theo `vnp_TxnRef`,
   - kiểm tra amount khớp,
   - cập nhật transaction `SUCCESS` hoặc `FAILED`.
6. Nếu giao dịch thành công và số tiền đã trả đủ, order chuyển sang `PAID`.
7. Browser của user được redirect về frontend qua `GET /payments/vnpay/return`. 

### 5.6. Giai đoạn 6: Consent chính sách và tạo hợp đồng
1. Admin tạo `PolicyDocument` theo `code` và `version`.
2. User đọc policy latest theo code.
3. User thực hiện consent qua `POST /policies/{policyId}/consent`.
4. Khi order ở trạng thái `PAID` hoặc `PREPARING`, hệ thống cho phép tạo hợp đồng bằng `POST /contracts/rental-order/{rentalOrderId}`.
5. Backend kiểm tra:
   - policy đang active và là bản latest,
   - user đã có consent `ACCEPTED`,
   - order chưa có contract trước đó.
6. Sau khi đạt điều kiện, hệ thống sinh `contractNumber` và lưu `RentalContract`. 

### 5.7. Giai đoạn 7: Vận hành đơn sau thanh toán
1. Sau khi thanh toán xong, đơn đi vào flow vận hành nội bộ.
2. Trạng thái chính của flow:
   - `PENDING_PAYMENT -> PAID/CANCELLED`
   - `PAID -> PREPARING -> DELIVERING -> DELIVERED -> IN_USE/PENDING_PICKUP -> PICKING_UP -> PICKED_UP -> INSPECTING -> COMPLETED`
3. Admin/Staff có thể gán hub và gán nhân sự giao/thu hồi cho đơn.
4. Khi bắt đầu giao hàng, đơn được đưa vào giai đoạn giao thực tế.
5. Khi gọi `record-delivery`, inventory item của đơn chuyển từ `RESERVED` sang `RENTED`.
6. Trong thời gian khách sử dụng, đơn có thể ở trạng thái `IN_USE`.
7. Khi đến giai đoạn thu hồi, đơn chuyển qua `PENDING_PICKUP` và `PICKING_UP`.
8. Khi gọi `record-pickup`, inventory item chuyển từ `RENTED` hoặc `RESERVED` về `AVAILABLE`.
9. Sau đó đơn đi qua bước `INSPECTING`, có thể set penalty nếu phát sinh tổn thất, rồi kết thúc ở `COMPLETED`. 

### 5.8. Giai đoạn 8: Hủy đơn
1. Hệ thống chỉ cho phép hủy đơn ở trạng thái `PENDING_PAYMENT`.
2. Khi hủy đơn:
   - inventory đã reserve sẽ được release từ `RESERVED` về `AVAILABLE`,
   - nếu có voucher thì `usedCount` được giảm lại,
   - order chuyển sang `CANCELLED`. 

### 5.9. Giai đoạn 9: Đánh giá và hỗ trợ sau thuê
1. Sau khi order `COMPLETED`, user có thể tạo review cho sản phẩm đã thuê.
2. Hệ thống chặn review sai quyền hoặc review trùng.
3. Nếu cần hỗ trợ, user hoặc guest có thể tạo `ContactTicket`.
4. Staff/Admin phản hồi ticket qua endpoint reply.
5. Khi xử lý xong, ticket được đóng; ticket đã đóng không thể reply/close tiếp. 

### 5.10. Giai đoạn 10: Quản trị nội bộ và vận hành hệ thống
1. Admin quản lý user, role, permission.
2. Admin/Staff quản lý catalog, hub, product, inventory, voucher, policy, order, payment transaction và ticket.
3. Toàn bộ quyền truy cập endpoint protected được authorize theo permission trong DB. 

---

## <span id="6-vấn-đề-pháp-lý--quản-trị-rủi-ro" style="color:red;">⚖️ 6. Vấn đề Pháp lý & Quản trị rủi ro</span>

Hệ thống hiện tại đã có nhiều ràng buộc pháp lý và kiểm soát rủi ro được suy ra trực tiếp từ code, đặc biệt ở các lớp xác thực tài khoản, consent policy, hợp đồng thuê, thanh toán, tồn kho theo serial, trạng thái đơn thuê và phân quyền endpoint. Nội dung dưới đây bám theo bộ docs hiện tại của backend. 

### 6.1. Xác thực danh tính và bảo mật truy cập
- Tài khoản phải verify email trước khi có thể sử dụng đầy đủ luồng nghiệp vụ.
- Mật khẩu bị ràng buộc bởi regex độ mạnh tối thiểu.
- Access token có hạn sử dụng; logout sẽ blacklist token ở Redis theo TTL còn lại.
- Refresh token được lưu ở DB và đi kèm cookie HttpOnly/Secure/SameSite=None.
- Các endpoint protected yêu cầu JWT hợp lệ. 

### 6.2. Ràng buộc dữ liệu người dùng
- Email và phone được kiểm soát unique ở tầng service và DB.
- Số điện thoại đi theo chuẩn VN.
- Profile có ràng buộc độ dài và kiểm soát cập nhật.
- Một số account hệ thống có rule bảo vệ không cho cập nhật/xóa tùy ý. :contentReference[oaicite:26]{index=26}

### 6.3. Consent policy và cơ sở ràng buộc điều khoản
- `PolicyDocument` quản lý chính sách theo `code/version` và trạng thái active.
- `UserConsent` là bằng chứng user đã chấp thuận policy.
- Muốn tạo hợp đồng, user phải consent policy latest đang active.
- `UserConsent` hiện lưu `ipAddress` và `userAgent`, tạo cơ sở chứng minh việc đồng ý điều khoản trước khi phát hành contract. 

### 6.4. Hợp đồng thuê và ràng buộc ký kết
- Hợp đồng chỉ được tạo khi order ở trạng thái `PAID` hoặc `PREPARING`.
- Mỗi order chỉ có một contract.
- Contract gắn với policy đang hiệu lực và user đã consent hợp lệ.
- Contract lưu metadata xác nhận như IP/User-Agent và định danh nghiệp vụ `contractNumber`. 

### 6.5. Kiểm soát thanh toán và đối soát giao dịch
- Mọi thanh toán được tách riêng khỏi order thông qua `PaymentTransaction`.
- Callback VNPay phải verify checksum và amount trước khi xác nhận thành công.
- Chỉ khi transaction thành công và đủ tiền thì order mới được đẩy sang `PAID`.
- Các mã giao dịch từ gateway được lưu để audit và reconcile. 

### 6.6. Kiểm soát vòng đời đơn thuê
- State machine kiểm soát việc chuyển trạng thái order.
- Chỉ cho phép hủy đơn ở `PENDING_PAYMENT`.
- Các thao tác giao/nhận tác động trực tiếp đến trạng thái inventory.
- Có cơ chế `set-penalty` để xử lý tình huống hư hại, mất mát hoặc chi phí bồi thường. 

### 6.7. Kiểm soát tài sản và chống overbooking
- Tài sản vật lý được quản lý theo từng serial inventory item.
- Inventory được reserve ngay khi tạo đơn để tránh trùng lịch cùng một serial.
- Khi hủy đơn, inventory được release.
- Khi giao/thu hồi, trạng thái item được cập nhật tương ứng giữa `RESERVED`, `RENTED` và `AVAILABLE`.
- Đây là lớp kiểm soát nghiệp vụ rất quan trọng đối với mô hình cho thuê tài sản vật lý. 

### 6.8. Ràng buộc voucher và khuyến mại
- Voucher có thời gian hiệu lực, usage limit, min rental days và giới hạn mức giảm.
- Voucher được validate theo bối cảnh đơn thuê, gồm ngày thuê và subtotal.
- `usedCount` tăng/giảm theo lifecycle đơn để giảm sai lệch số lượt sử dụng. 

### 6.9. Ràng buộc review, ticket và quyền thao tác
- Chỉ user sở hữu order hoàn tất mới được review sản phẩm.
- Mỗi tổ hợp `(order, user, product)` chỉ được một review.
- Ticket đã đóng không thể reply/close lại.
- Đây là các ràng buộc giúp hạn chế spam, thao tác sai quyền và dữ liệu phản hồi không hợp lệ. 

### 6.10. Ràng buộc phân quyền nội bộ
- Endpoint protected yêu cầu JWT hợp lệ và permission phù hợp theo DB.
- Role là tập permission, không hard-code toàn bộ quyền trực tiếp vào role ở code.
- Một số endpoint public được allowlist cho browse, auth và callback thanh toán.
- Nếu `Permission.apiPath` không khớp route thực tế, quyền hợp lệ có thể vẫn bị từ chối, nên đây là một điểm cần kiểm soát rất kỹ khi vận hành. 

### 6.11. Ràng buộc validation đầu vào
- Request DTO áp dụng Jakarta Validation.
- Global exception handler trả lỗi field-level thống nhất.
- Ngoài validation annotation, tầng service còn kiểm tra thêm các rule nghiệp vụ như:
  - duplicate,
  - ownership,
  - state transition,
  - điều kiện hợp đồng,
  - điều kiện voucher,
  - điều kiện review/ticket. 

### 6.12. Rủi ro kỹ thuật và kiểm soát vận hành cần lưu ý
- Có rủi ro race condition khi reserve/release inventory nếu tải cao hoặc nhiều request đồng thời.
- Callback VNPay cần idempotent và chống replay tốt hơn để tránh ghi nhận trùng.
- Việc mapping permission path không khớp route có thể gây lỗi 403 ngoài kỳ vọng.
- Cần rà soát kỹ các mapper ignore field để tránh frontend thiếu dữ liệu cần thiết.
- Cần kiểm tra lại đường dẫn Liquibase changelog và changesets giữa các thư mục resources để tránh mismatch khi chạy migration. 

### 6.13. Hướng hoàn thiện để tăng mức pháp lý và audit
- Tăng độ tin cậy metadata IP trong `UserConsent` bằng cơ chế trusted proxy rõ ràng hơn.
- Chuẩn hóa render/hash tài liệu policy để tăng khả năng chống tranh chấp phiên bản.
- Cân nhắc bổ sung audit trail chi tiết hơn cho thay đổi trạng thái order/inventory.
- Có thể bổ sung idempotency key cho các endpoint nhạy cảm liên quan thanh toán hoặc thao tác nghiệp vụ quan trọng. :contentReference[oaicite:37]{index=37}

---

## <span id="7-hướng-dẫn-sử-dụng--demo" style="color:red;">📽️ 7. Hướng dẫn sử dụng & Demo</span>

Xem ngay video hướng dẫn sử dụng và Demo hệ thống Swiftera: [https://www.youtube.com/watch?v=SwifteraDemo](https://www.youtube.com/watch?v=SwifteraDemo)

---

## <span id="8-nguyên-tắc-làm-việc" style="color:red;">📏 8. Nguyên tắc làm việc</span>

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

**Ví dụ**: `feature/add-staff-portal`, `bugfix/calendar-conflict`

### 🎨 **Cấu hình Prettier**

```json
{
    "editor.formatOnPaste": false,
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "prettier.singleQuote": true,
    "prettier.semi": true
}
