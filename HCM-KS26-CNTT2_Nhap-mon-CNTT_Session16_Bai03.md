### **Bài 3 : Xử lý Sự cố Giao diện Website Doanh nghiệp** 

### **PHẦN 1: BÁO CÁO PHÂN TÍCH BOX MODEL (I/O)**

 Box Model có:
- Content: kích thước 840 × 600 px.
- Padding (Vùng đệm): Có giá trị là 12 (trên) và 10 ở (dưới/trái/phải)
- Border (Đường viền): là 1px ở  (trên/trái/phải) và 15 px ở dưới
- Margin (Lề bên ngoài): có 0 px ở (dưới/trái) và 1 px ở bên phải và 10 px ở trên

Và xem Rendering Engine, ta thấy:
- Nguyên nhân bị đè màn hình:  ở div#lesson-content do sử dụng các giá trị Margin âm quá lớn -28px, -20px và kèm xung đột Float cả hai phần tử div#lesson-content và div#video-list đều dùng float: left

**2\. Giải pháp khắc phục**

- Tại bảng Styles chọn div.lesson-content, chỉnh sửa các thuộc tính sau:  
1. Bỏ margin âm:  
- Đổi margin-right: \-20px thành margin-right: 20px   
2. Kiểm soát lại độ rộng   
- Giảm độ rộng width: 65% \!important; xuống khoảng 55% \- 60% để chừa đủ không gian cho khung bên phải.  
   

