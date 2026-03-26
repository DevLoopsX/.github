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

> Swiftera hiện là một hệ thống thuê thiết bị công nghệ theo mô hình khách hàng đặt thuê online, sau đó doanh nghiệp tiếp tục xử lý các bước giao nhận và vận hành thực tế. Hệ thống đã bao phủ các nhóm chức năng cốt lõi như lọc, tìm kiếm, đăng nhập, giỏ hàng, thanh toán, ảnh sản phẩm, liên hệ/hỗ trợ, khuyến mại, bản đồ, đánh giá sản phẩm, trang quản trị, quản lý hợp đồng, điều khoản và vòng đời đơn thuê.

### 4.1. Bảo mật (xác thực, phân quyền) & Tài khoản người dùng

- Hệ thống cho phép người dùng đăng ký tài khoản, xác thực email, đăng nhập, đăng xuất, làm mới phiên đăng nhập và khôi phục mật khẩu khi quên. Sau khi đăng nhập thành công, người dùng có thể xem thông tin tài khoản hiện tại, cập nhật hồ sơ cá nhân, đổi mật khẩu và yêu cầu thay đổi email.

- Hệ thống còn hỗ trợ quản lý người dùng theo vai trò và quyền hạn khác nhau. Nhờ đó khách hàng, nhân viên vận hành và quản trị viên không dùng chung một mức quyền như nhau.

### 4.2. Tìm kiếm, lọc, sắp xếp và duyệt thiết bị cần thuê

- Người dùng có thể xem danh mục sản phẩm, mở danh sách sản phẩm và duyệt cây danh mục để tìm đúng nhóm thiết bị cần thuê. Hệ thống backend hỗ trợ list có phân trang, lọc và sắp xếp nên phía frontend có thể xây dựng các trải nghiệm như tìm kiếm theo tên, lọc theo danh mục, lọc theo trạng thái hiển thị, hoặc sắp xếp theo tiêu chí phù hợp với nhu cầu người dùng.

- Ngoài việc xem danh sách, người dùng còn có thể xem chi tiết từng sản phẩm với dữ liệu đầy đủ hơn như hình ảnh, mức giá hiện tại, giá cũ tham chiếu, số lượng khả dụng và điểm đánh giá trung bình. Vì vậy, trải nghiệm duyệt thiết bị trong hệ thống hiện tại không chỉ là liệt kê tên sản phẩm, mà đã có đủ thông tin để khách đưa ra quyết định thuê. 

### 4.3. Ảnh sản phẩm và trải nghiệm hiển thị

- Mỗi sản phẩm có thể có nhiều ảnh, có ảnh chính và thứ tự hiển thị rõ ràng. Phần backend hỗ trợ tải ảnh sản phẩm lên, lưu trữ và xoá ảnh sản phẩm khi cần. Ở phía giao diện có thể hiển thị tốt trên nhiều loại thiết bị (responsive) như deskstop, mobile.

### 4.4. Hub, vị trí giao nhận và tích hợp bản đồ

- Hệ thống có phần quản lý hub, đồng thời cho phép người dùng xem danh sách hub đang hoạt động ở khu vực công khai. Frontend hiển thị điểm giao nhận hoặc điểm vận hành trên bản đồ Goong Map cho người dùng. Điểm quan trọng ở đây là hub trong Swiftera không chỉ là thông tin tham khảo mà nó còn là một phần của vận hành nội bộ, vì đơn thuê có thể được gán về hub cụ thể để xử lý.

### 4.5. Giỏ thuê thiết bị

- Hệ thống có giỏ hàng riêng cho từng người dùng. Người dùng có thể mở giỏ, thêm sản phẩm vào giỏ, sửa dòng giỏ, xóa từng dòng hoặc xóa toàn bộ giỏ. Khi thao tác với giỏ, hệ thống kiểm tra ngay những điều kiện quan trọng như sản phẩm còn đang được mở cho thuê hay không, thời gian thuê có hợp lệ hay không, số ngày thuê có đủ theo quy định tối thiểu của sản phẩm hay không, và số lượng có hợp lý hay không. 

- Đây là bước chuẩn bị dữ liệu trước khi tạo đơn thuê thật. Hệ thống còn hỗ trợ trả về hình ảnh sản phẩm đại diện và giá trị tạm tính của từng dòng để frontend hiển thị dễ hiểu hơn cho khách hàng.

### 4.6. Tạo đơn thuê và ghi nhận thông tin tại thời điểm đặt

- Khi khách hàng xác nhận đặt thuê, hệ thống tạo đơn thuê chính thức và lưu lại những thông tin quan trọng của giao dịch tại đúng thời điểm khách chốt đơn. Điều này giúp dữ liệu đơn thuê không bị thay đổi theo các cập nhật sau đó của sản phẩm hoặc chương trình ưu đãi. Đây là một chức năng rất quan trọng trong mô hình cho thuê, vì nó giúp giảm tranh chấp về sau và giữ cho đơn hàng phản ánh đúng những gì khách đã đồng ý ban đầu. 

- Ngoài ra, hệ thống hiện còn hỗ trợ xem chi tiết đơn thuê, xem danh sách đơn của bản thân và quản lý đơn ở phía nội bộ. Nhờ vậy, đơn thuê không phải một bản ghi tạo xong rồi bỏ đó, mà là trung tâm của toàn bộ vòng đời nghiệp vụ phía sau. 

### 4.7. Giữ chỗ thiết bị thực tế và chống đặt trùng

- Swiftera không chỉ quản lý theo tên sản phẩm, mà còn quản lý cả thiết bị thật theo từng serial riêng. Khi tạo đơn, hệ thống sẽ tự chọn thiết bị còn sẵn và giữ chỗ ngay để tránh việc hai khách cùng đặt trùng một món hàng vật lý. Cơ chế này là nền tảng để vận hành mô hình thuê thiết bị ngoài thực tế, nơi mỗi món hàng có vòng đời sử dụng lặp đi lặp lại qua nhiều đơn khác nhau. 

### 4.8. Thanh toán trực tuyến

- Swiftera có hỗ trợ thanh toán online qua VNPay. Hệ thống tạo giao dịch thanh toán riêng cho đơn thuê, chuyển khách sang cổng thanh toán, nhận kết quả từ VNPay và chỉ khi kiểm tra dữ liệu hợp lệ thì mới xác nhận đơn đã thanh toán.

### 4.9. Khuyến mại, giá mới và giá cũ

- Hệ thống có hỗ trợ voucher giảm giá với các điều kiện cụ thể như thời hạn còn hiệu lực, số lượt sử dụng, số ngày thuê tối thiểu và giới hạn mức giảm. Ngoài ra, dữ liệu sản phẩm còn có giá hiện tại và giá cũ tham chiếu để frontend hiển thị (thường để kích thích mua hàng).

### 4.10. Điều khoản, chính sách đổi trả, bảo hành, vận chuyển và hợp đồng

- Trong hệ thống hiện tại, phần này được hiện thực theo hướng quản lý `PolicyDocument`, cho phép công khai nội dung policy, lấy policy mới nhất theo mã, lưu việc người dùng đã đồng ý với điều khoản, và chỉ cho phép tạo hợp đồng khi các điều kiện liên quan đến policy đã đạt. Vì vậy, thay vì chỉ hiển thị các trang chính sách tĩnh, Swiftera đang quản lý điều khoản/chính sách như một phần nghiệp vụ có kiểm soát.

- Nghĩa là các nội dung như chính sách vận chuyển, điều khoản thuê, quy định xử lý sau thuê hoặc các ràng buộc liên quan có thể được quản lý tập trung theo phiên bản. Khi đi vào flow thực tế, người dùng còn cần chấp thuận điều khoản rồi hệ thống mới cho tạo hợp đồng thuê. Đây là điểm mà Swiftera vượt khỏi mức một website thương mại điện tử thông thường và tiến gần hơn đến một nền tảng giao dịch có ràng buộc rõ ràng. 

### 4.11. Quản lý vòng đời đơn thuê sau khi khách đã thanh toán

- Sau khi thanh toán thành công, hệ thống tiếp tục hỗ trợ phần vận hành: xác nhận đơn, gán hub, gán nhân sự giao/thu hồi, ghi nhận giao hàng, ghi nhận thu hồi và xử lý khoản phạt nếu có hư hại hoặc mất mát. Swiftera không chỉ giúp khách đặt thuê mà còn giúp doanh nghiệp quản lý việc cho thuê trong suốt vòng đời thực tế của món hàng. Khi món hàng đã rời kho, đang ở khách hay vừa được nhận lại, hệ thống vẫn theo dõi được trạng thái và cho phép nhân sự nội bộ xử lý đúng bước.

### 4.12. Đánh giá sản phẩm và phần phản hồi sau thuê

- Swiftera có phần đánh giá sản phẩm sau thuê. Chỉ người đã thực sự hoàn tất đơn thuê mới được đánh giá món hàng mình đã sử dụng. Nhờ đó, phần nhận xét về sản phẩm có độ tin cậy cao hơn. Về phần bình luận (feedback), hệ thống hiện thể hiện rõ nhất qua hai hướng: đánh giá sản phẩm sau khi thuê và ticket hỗ trợ/feedback gửi về doanh nghiệp.

### 4.13. Liên hệ và hỗ trợ khách hàng

- Hệ thống hỗ trợ tạo ticket liên hệ/hỗ trợ cho cả người dùng đã đăng nhập. Sau khi nhận ticket, phía vận hành có thể phản hồi và đóng ticket khi xử lý xong. Ticket có thể gắn với đơn thuê, giúp doanh nghiệp xử lý các vấn đề phát sinh sau khi giao hàng, trong quá trình khách sử dụng hoặc sau khi trả hàng.

### 4.14. Quản trị nội bộ

- Hệ thống có khu vực quản trị đủ rộng để quản lý người dùng, vai trò, quyền hạn, danh mục, sản phẩm, ảnh sản phẩm, thiết bị thực tế theo serial, hub, voucher, đơn thuê, giao dịch thanh toán, điều khoản/chính sách, hợp đồng và ticket hỗ trợ dành cho admin và nhân viên nội bộ (dashboard).

---

## <span id="5-luồng-hoạt-động--kịch-bản-chi-tiết-business-flow" style="color:red;">🔄 5. Luồng hoạt động & Kịch bản chi tiết (Business Flow)</span>

> Luồng hoạt động hiện tại của Swiftera: khách hàng thao tác online để chọn và đặt thuê thiết bị, còn doanh nghiệp tiếp tục xử lý đơn qua các bước vận hành thực tế cho đến khi món hàng được giao, sử dụng, thu hồi và hoàn tất.

### 5.1. Bước 1: Người dùng tạo tài khoản và bắt đầu phiên sử dụng

Khách hàng đăng ký tài khoản, xác thực email rồi đăng nhập vào hệ thống. Sau khi đăng nhập thành công, hệ thống trả về thông tin cần thiết để người dùng bắt đầu sử dụng nền tảng. Nếu gặp sự cố như quên mật khẩu hoặc hết phiên đăng nhập, hệ thống cũng đã có các bước hỗ trợ để người dùng tiếp tục sử dụng mà không cần tạo lại tài khoản. 

### 5.2. Bước 2: Người dùng tìm thiết bị cần thuê

Sau khi vào hệ thống, người dùng xem danh mục, duyệt danh sách sản phẩm, xem chi tiết sản phẩm và tham khảo các hub đang hoạt động. Đây là giai đoạn người dùng tìm món phù hợp với nhu cầu. Ở bước này, frontend có thể triển khai tìm kiếm, lọc và sắp xếp dựa trên dữ liệu list/filter mà backend đang cung cấp. 

### 5.3. Bước 3: Người dùng thêm thiết bị vào giỏ thuê

Khi đã chọn được món phù hợp, người dùng thêm sản phẩm vào giỏ thuê và nhập các thông tin cần thiết như thời gian thuê và số lượng. Hệ thống kiểm tra ngay các điều kiện cơ bản để chặn dữ liệu sai từ sớm. Nếu người dùng thay đổi nhu cầu, họ có thể sửa dòng giỏ, xoá từng dòng hoặc xóa toàn bộ giỏ. 

### 5.4. Bước 4: Người dùng tạo đơn thuê chính thức

Sau khi giỏ thuê đã hoàn chỉnh, người dùng gửi yêu cầu tạo đơn. Hệ thống lúc này ghi lại những thông tin quan trọng của đơn, đồng thời tính tiền thuê, tiền giảm giá nếu có voucher và các khoản liên quan khác. Đơn mới tạo sẽ ở trạng thái chờ thanh toán. Đây là bước chuyển từ ý định thuê sang giao dịch thuê chính thức. 

### 5.5. Bước 5: Hệ thống giữ chỗ món hàng thực tế cho khách

Ngay trong bước tạo đơn, hệ thống chọn và giữ chỗ món hàng thực tế còn khả dụng để tránh bị đặt trùng. Nhờ vậy, một khi khách đã tạo đơn thành công thì hệ thống đã bắt đầu bảo vệ quyền lợi booking của khách trên chính món hàng vật lý phù hợp. Đây là một bước rất quan trọng với mô hình thuê, vì nếu không có giữ chỗ, hệ thống rất dễ xảy ra trùng lịch và sai lệch tồn kho. 

### 5.6. Bước 6: Người dùng thanh toán qua VNPay

Sau khi đơn đã được tạo, khách hàng được chuyển sang bước thanh toán. Hệ thống tạo giao dịch thanh toán riêng cho đơn và chuyển người dùng tới cổng VNPay. Khi VNPay gửi kết quả về, backend sẽ kiểm tra lại rồi mới xác nhận thanh toán thành công. Nếu thanh toán chưa hợp lệ thì đơn chưa được coi là đã trả tiền.

### 5.7. Bước 7: Người dùng xác nhận điều khoản và hệ thống tạo hợp đồng

Sau khi đơn đi đến giai đoạn phù hợp, người dùng phải đồng ý với điều khoản/chính sách áp dụng cho giao dịch thuê. Chỉ khi đã có sự đồng ý hợp lệ và đơn đạt điều kiện, hệ thống mới cho phép tạo hợp đồng. Điều này giúp toàn bộ giao dịch thuê có mức ràng buộc rõ hơn so với mô hình đặt hàng thông thường. 

### 5.8. Bước 8: Doanh nghiệp chuẩn bị đơn và phân công xử lý

Khi đơn đã được thanh toán và đủ điều kiện đi tiếp, khối vận hành nội bộ bắt đầu xử lý. Hệ thống hỗ trợ gán hub, gán nhân sự giao và nhân sự thu hồi cho từng đơn. Điều này giúp chuyển flow từ phần online sang phần vận hành thực tế một cách có tổ chức, thay vì xử lý thủ công bên ngoài hệ thống. 

### 5.9. Bước 9: Giao hàng cho khách

Khi hàng được giao cho khách, hệ thống ghi nhận sự kiện giao hàng. Từ thời điểm này, món hàng được hiểu là đã ra khỏi kho và đi vào giai đoạn sử dụng thực tế của khách. TThời điểm giao hàng còn ảnh hưởng tới thời gian thuê thực tế và mốc kết thúc kỳ thuê dự kiến.

### 5.10. Bước 10: Khách sử dụng thiết bị trong thời gian thuê

Sau khi nhận hàng, khách bước vào giai đoạn sử dụng thiết bị. Trong thời gian này, đơn vẫn tiếp tục được theo dõi trên hệ thống giúp doanh nghiệp biết món hàng đang ở khách, món nào sắp đến hạn và chuẩn bị cho các bước thu hồi hoặc xử lý phát sinh nếu có. 

### 5.11. Bước 11: Gia hạn đơn thuê khi có nhu cầu

Một điểm mới rất đáng chú ý là hệ thống hiện đã có hỗ trợ gia hạn đơn thuê. Khi khách muốn gia hạn thêm thời gian, hệ thống sẽ kiểm tra xem việc kéo dài có làm xung đột với lịch sau đó hay không. Nếu serial hiện tại không còn phù hợp, hệ thống có thể tự tìm serial khác cùng loại để thay thế theo logic ưu tiên hợp lý. Điều này giúp tối ưu trải nghiệm booking mà vẫn bảo vệ quyền lợi của các đơn đã đặt sau. 

### 5.12. Bước 12: Thu hồi lại thiết bị

Khi đến hạn hoặc khi khách kết thúc thời gian thuê, nhân sự vận hành tiến hành thu hồi thiết bị và ghi nhận việc này trên hệ thống. Đây là bước đánh dấu món hàng đã rời khỏi tay khách và quay về trạng thái có thể tiếp tục được theo dõi cho các xử lý tiếp theo. 

### 5.13. Bước 13: Kiểm tra tình trạng hàng và xử lý phát sinh

Sau khi nhận lại thiết bị, doanh nghiệp tiếp tục kiểm tra tình trạng của món hàng. Nếu có hư hại, mất mát hoặc chi phí cần xử lý, hệ thống hỗ trợ cập nhật phần phạt tương ứng. Đây là bước quan trọng để mô hình thuê phản ánh được rủi ro thực tế của tài sản vật lý, chứ không chỉ coi việc nhận hàng về là xong đơn. 

### 5.14. Bước 14: Hoàn tất đơn và mở ra giai đoạn sau thuê

Khi mọi việc đã hoàn thành, đơn được đóng lại ở trạng thái kết thúc. Từ đây, khách hàng có thể để lại đánh giá cho sản phẩm, còn nếu phát sinh vấn đề chưa giải quyết xong thì có thể gửi yêu cầu hỗ trợ. Nhờ vậy, vòng đời của một đơn trong Swiftera không dừng ở bước thanh toán hay giao hàng, mà kéo dài đến cả giai đoạn sau thuê. 

---

## <span id="6-vấn-đề-pháp-lý--quản-trị-rủi-ro" style="color:red;">⚖️ 6. Vấn đề Pháp lý & Quản trị rủi ro</span>

> Swiftera không chỉ là một hệ thống có chức năng đặt thuê thiết bị, mà còn có cấu trúc kiểm soát rủi ro tương đối rõ cho một mô hình vận hành thật. Các lớp kiểm soát hiện tại thể hiện qua xác thực tài khoản, quản lý điều khoản, hợp đồng, thanh toán, quản lý tài sản theo từng món thực tế, kiểm soát vòng đời đơn và phân quyền nội bộ. 

### 6.1. Kiểm soát danh tính người dùng và quyền truy cập

Một giao dịch thuê tài sản sẽ rất rủi ro nếu không gắn với tài khoản cụ thể và không kiểm soát quyền truy cập. Hệ thống hiện yêu cầu người dùng xác thực email, hỗ trợ quản lý phiên đăng nhập, và phân chia rõ quyền của khách hàng, nhân sự vận hành và quản trị viên. Điều này giúp giảm các rủi ro như truy cập trái quyền, thao tác nhầm vai trò hoặc dữ liệu đơn hàng gắn sai người. 

### 6.2. Kiểm soát điều khoản và sự đồng ý của khách hàng

Một điểm rất quan trọng của hệ thống là không cho tạo hợp đồng tuỳ tiện. Người dùng phải có bước đồng ý với điều khoản/chính sách trước, và việc đồng ý đó được lưu lại trong hệ thống để làm cơ sở đối chiếu sau này. Trong mô hình thuê thiết bị, đây là một lớp bảo vệ rất có giá trị vì tranh chấp thường không chỉ nằm ở chuyện “đã đặt hàng chưa”, mà còn nằm ở chuyện “đã đồng ý với điều khoản xử lý trách nhiệm hay chưa”. 

### 6.3. Kiểm soát hợp đồng thuê

Hệ thống hiện chỉ cho tạo hợp đồng khi đơn đã đạt tới giai đoạn phù hợp và mỗi đơn chỉ được gắn với một hợp đồng. Điều này giúp tránh tạo hợp đồng sai thời điểm hoặc tạo chồng chéo nhiều hợp đồng cho cùng một giao dịch. Nếu nhìn dưới góc độ quản trị, đây là cách làm phù hợp để giữ cho quan hệ thuê giữa doanh nghiệp và khách hàng có cấu trúc rõ ràng hơn. 

### 6.4. Kiểm soát thanh toán và khả năng đối soát

Thanh toán là một vùng rủi ro lớn vì chỉ cần xác nhận sai là toàn bộ quy trình vận hành sau đó có thể sai theo. Hệ thống hiện tách riêng giao dịch thanh toán, kiểm tra lại dữ liệu trả về từ VNPay và chỉ khi dữ liệu hợp lệ mới xác nhận đơn đã được thanh toán. Cách tổ chức này giúp giảm sai sót và giúp doanh nghiệp dễ đối chiếu hơn về sau nếu có sự cố. 

### 6.5. Kiểm soát tài sản thực tế để tránh đặt trùng và thất thoát

Với mô hình cho thuê, rủi ro rất lớn nằm ở việc không biết chính xác món hàng nào đang ở đâu. Swiftera hiện đã đi đúng hướng khi quản lý từng món hàng vật lý riêng biệt và giữ chỗ món hàng ngay từ lúc tạo đơn. Nhờ vậy, hệ thống hạn chế được việc nhiều khách đặt trùng cùng một món thực tế, đồng thời giúp doanh nghiệp theo dõi được món nào đang rảnh, món nào đã giữ chỗ và món nào đang ở khách. 

### 6.6. Kiểm soát lịch thuê và gia hạn

Khi hệ thống bắt đầu hỗ trợ gia hạn đơn thuê, rủi ro mới xuất hiện là xung đột lịch giữa đơn hiện tại và đơn đặt sau. Tài liệu API mới cho thấy hệ thống đã xử lý theo hướng kiểm tra xung đột trước, và nếu cần thì tự tìm món khác cùng loại để thay thế. Đây là một hướng rất hợp lý vì nó vừa bảo vệ booking của khách đang thuê, vừa tránh ảnh hưởng đến các booking đã có sau đó. 

### 6.7. Kiểm soát giao hàng, thu hồi và xử lý hư hại

Hệ thống không xem việc khách đặt thuê thành công là kết thúc, mà tiếp tục theo dõi món hàng qua các bước giao, sử dụng, thu hồi và kiểm tra lại. Điều này giúp giảm rủi ro thất thoát, thất lạc hoặc “quên trạng thái” của thiết bị. Sau khi nhận lại hàng, hệ thống còn cho phép xử lý khoản phạt nếu phát sinh hư hại hoặc mất mát. Đây là điểm rất quan trọng với bài toán thuê tài sản thật. 

### 6.8. Kiểm soát khuyến mại và hạn chế sai lệch khi dùng voucher

Khuyến mại nếu không kiểm soát kỹ rất dễ gây thất thoát hoặc tạo tranh cãi với khách hàng. Swiftera hiện đã gắn voucher với các điều kiện cụ thể như còn hạn, còn lượt sử dụng, đủ điều kiện áp dụng hay không, và khi đơn bị hủy thì số lượt dùng cũng được điều chỉnh lại. Điều này giúp phần khuyến mại đi vào đúng logic vận hành thay vì chỉ là tính năng trình bày ở giao diện. 

### 6.9. Kiểm soát phản hồi, đánh giá và hỗ trợ sau thuê

Hệ thống chỉ cho khách đã hoàn tất thuê mới được đánh giá sản phẩm, giúp phần review có giá trị thực tế hơn. Đồng thời, yêu cầu hỗ trợ sau bán được đưa vào dạng ticket có phản hồi và đóng xử lý rõ ràng. Điều này giúp dữ liệu sau thuê không bị lộn xộn và tạo ra một cơ chế theo dõi phản hồi có tổ chức hơn cho doanh nghiệp. 

### 6.10. Kiểm soát phân quyền nội bộ và rủi ro thao tác sai

Một hệ thống có nhiều vai trò nội bộ rất dễ phát sinh rủi ro nếu quyền hạn không khớp với chức năng thực tế. Tài liệu hiện tại cho thấy backend đang kiểm soát quyền theo endpoint, giúp giới hạn khá rõ ai được làm gì. Điều này đặc biệt quan trọng với những thao tác nhạy cảm như quản lý đơn, thay đổi trạng thái, xử lý thanh toán, quản lý sản phẩm hoặc chỉnh sửa dữ liệu chính sách. 

### 6.11. Các rủi ro kỹ thuật vẫn cần tiếp tục hoàn thiện

Vẫn còn các vùng cần tiếp tục siết chặt thêm, như xử lý tình huống đồng thời khi nhiều thao tác cùng xảy ra, kiểm soát callback thanh toán lặp, bảo đảm đồng bộ quyền truy cập và tăng kiểm thử cho các luồng quan trọng. Điều này cho thấy hệ thống đã có tư duy nhận diện rủi ro tương đối rõ, và phần còn lại chủ yếu là làm hệ thống vững hơn khi đi vào vận hành lớn. 

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
