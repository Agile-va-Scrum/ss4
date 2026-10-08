# BÀI LÀM: RÀ SOÁT USER STORY VÀ SẮP XẾP PRODUCT BACKLOG (FOODNOW)

---

## Bước 1. Tìm lỗi theo INVEST

| Mã | Đánh giá & Lý do |
| :--- | :--- |
| **US1** | **Đạt:** Vai trò rõ, một việc cụ thể, có lợi ích thiết thực và kiểm thử được ngay bằng cách chọn loại món rồi quan sát danh sách trả về. |
| **US2** | **Sai chữ T (Testable) và E (Estimable):** Từ ngữ "đẹp" và "dễ dùng" hoàn toàn mang tính cảm tính, không có tiêu chí đo lường cụ thể khiến đội ngũ không thể nghiệm thu (Definition of Done) hay ước lượng khối lượng công việc. |
| **US3** | **Sai chữ V (Valuable) và N (Negotiable):** Story mang tính chỉ định giải pháp kỹ thuật ("dùng React") thay vì phản ánh giá trị nghiệp vụ cho người dùng cuối; đồng thời làm mất tính linh hoạt để nhóm phát triển tự chủ thảo luận giải pháp kỹ thuật tối ưu. |
| **US4** | **Sai chữ S (Small) và E (Estimable):** Đây thực chất là một Epic chứa quá nhiều tính năng (lọc đa chiều thời gian/khu vực/nhà hàng, xuất file Excel, tự động gửi mail), phạm vi quá rộng khiến nhóm không thể ước lượng chính xác và không thể hoàn thành trong một Sprint. |

---

## Bước 2. Sửa lỗi

### a) Viết lại US2 với tiêu chí đo lường cụ thể

> **US2 (Viết lại):**  
> *Là một khách hàng, tôi muốn hoàn tất thao tác đặt món trong vòng không quá 3 bước chạm màn hình, để tiết kiệm thời gian và chốt đơn nhanh chóng.*  
> 
> * **Tiêu chí nghiệm thu (Acceptance Criteria):**  
>   1. Từ màn hình giỏ hàng đến khi hoàn tất thanh toán không vượt quá 3 lần thao tác bấm/chạm.  
>   2. Thời gian trung bình người dùng thao tác không quá 60 giây trên luồng đặt món.

---

### b) Tách US4 và xây dựng cây cấu trúc 3 cấp

* **Epic:** Quản trị và phân tích dữ liệu kinh doanh FoodNow
  * **Feature:** Báo cáo doanh thu đa chiều trên hệ thống Quản trị (Admin Dashboard)
    * **US4.1 (Xem dashboard):** *Là một admin, tôi muốn xem biểu đồ doanh thu lọc theo ngày, tuần, tháng và khu vực ngay trên trang quản trị, để nắm bắt nhanh diễn biến kinh doanh mà không cần tính toán thủ công.*
    * **US4.2 (Xuất file):** *Là một admin, tôi muốn xuất dữ liệu doanh thu chi tiết theo từng nhà hàng ra định dạng Excel, để chia sẻ số liệu đối soát định kỳ với đối tác và kế toán.*

---

## Bước 3. Xếp lại Product Backlog

### a) Thứ tự ưu tiên Product Backlog

Căn cứ vào cam kết cốt lõi của FoodNow (giao món trong 30 phút), các tính năng chạm trực tiếp đến trải nghiệm đặt món và dòng tiền được ưu tiên triển khai trước:

1. **US1 (Lọc nhà hàng theo món):** **Ưu tiên 1.** Tính năng tìm kiếm cốt lõi, giúp khách hàng chọn đồ ăn nhanh chóng ngay từ lúc mở app.
2. **US2 đã sửa (Rút gọn luồng đặt món):** **Ưu tiên 2.** Tối ưu tỷ lệ chuyển đổi, giảm thiểu tình trạng rớt đơn ngay bước chốt món.
3. **US4.1 (Dashboard doanh thu theo thời gian/khu vực):** **Ưu tiên 3.** Giúp bộ phận vận hành theo dõi số liệu tổng quan khi lượng đơn hàng bắt đầu phát sinh.
4. **US4.2 (Xuất báo cáo Excel theo nhà hàng):** **Ưu tiên 4.** Tính năng phụ trợ cho đối soát định kỳ, ở giai đoạn đầu có thể truy vấn dữ liệu thủ công trước khi tự động hóa.

---

### b) Mức độ chi tiết theo DEEP và công việc tại buổi Refinement

* **Mức độ chi tiết của story đứng đầu (US1):**
  * Theo nguyên tắc **Detailed appropriately** của DEEP, US1 nằm ở đỉnh backlog nên phải đạt mức độ chi tiết cao nhất (trạng thái **Ready**).
  * Story cần có đầy đủ: bản thiết kế giao diện (UI/UX wireframe), danh mục loại món cụ thể, logic hiển thị (ví dụ: nhà hàng bán nhiều loại món thì hiển thị ra sao), cùng bộ tiêu chí chấp thuận (Acceptance Criteria) rõ ràng cho cả trường hợp có kết quả và không có kết quả tìm kiếm.

* **Việc nhóm cần làm với US1 trong buổi Refinement:**
  1. PO giải thích rõ nghiệp vụ và trả lời các câu hỏi phát sinh từ nhóm phát triển.
  2. PO và nhóm cùng thống nhất bộ tiêu chí chấp thuận (Acceptance Criteria).
  3. Nhóm phát triển thảo luận giải pháp kỹ thuật, đánh giá các phụ thuộc hệ thống (API tìm kiếm, cơ sở dữ liệu).
  4. Cả nhóm thực hiện ước lượng (Story Point/Planning Poker) để đảm bảo story đủ nhỏ, khả thi để đưa vào Sprint Backlog kế tiếp.