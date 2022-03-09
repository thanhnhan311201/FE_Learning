# Những kiến thức tổng hợp được trong khóa học **HTML, CSS từ Zero đến Hero**

## Kiến thức chung
- HTML là chữ viết tắt của Hypertext Markup Language. Nó giúp người dùng tạo và cấu trúc các thành phần trong trang web hoặc ứng dụng, phân chia các đoạn văn, heading, links, blockquotes, vv...
- CSS là ngôn ngữ tạo phong cách cho trang web - Cascading Style Sheet Language. Nó dùng để tạo phong cách và định kiểu cho những yếu tố được viết dưới dạng ngôn ngữ đánh dấu, như là HTML.

## Các bước xây dựng giao diện một website
1. Phân tích giao diện của một website (phải có một website mẫu, sau đó phân tích các thành phần của giao diện).
2. Dựng base (xây móng).
3. Xây dựng từng thành phần theo phân tích.
4. Hoàn thiện.

## Những thành phần thường có trên một giao diện website
1. **Header**: là thành phần thanh ngang nằm ở đầu trang.
2. **Navigation**: là phần điều hướng của trang, có nhiệm vụ để link tới các trang chính của trang web.
3. **Breadcrumb**: là phần hiển thị luồng đường dẫn tại giao diện trang web đó so với trang web chính.
4. **Sidebar** (subnavigation): là thành phần thanh menu nằm dọc theo giao diện trang web, thường nằm ở bên phái hoặc ở bên trái.
5. **Slider**: là thành phần để hiển thị nội dung đặc trưng của giao diện trang web, thành phần này có thể trượt qua trái hoặc trượt qua phải, nội dung thông thường là ảnh, video, chữ,...
6. **Banner**: là thành phần hiển thị ảnh đặc trưng hoặc ảnh quảng cáo của website,...
7. **Container**: là thành phần chứa các nội dung chính của website, trong trường hợp một website chứa quá nhiều content (nội dung chính) thì chúng ta cần thành phần container để bao bọc các thành phần content.
8. **Content**: là thành phần nội dung chính ở giữa trang web.
9. **Footer**: là thành phần ở cuối trang web, thông thường footer để hiển thị logo, slogan của trang web, các thông tin liên hệ, hoặc các câu hỏi thường gặp,...

## Những quy tắc cần lưu ý khi thiết kế giao diện một website
1. Từ ngoài vào trong (thiết kế từ thẻ cha vào trong thẻ con).
2. Từ trên xuống dưới (thiết kế các thành phần từ trên xuống dưới).
3. Từ tổng quan đến chi tiết.

## Những điều cần lưu ý khi thiết kế giao diện một website
1. Vị trí của thành phần đó nằm ở đâu?
2. Kích thước (width, height) của thành phần bao nhiêu?
3. Màu sắc của thành phần đó là gì?
4. Kiểu dáng (kiểu chữ, shape,...) của thành phần đó như thế nào?

## Những điều cần lưu ý khi xây dựng base cho một website

### 1. Reset CSS
- Đầu tiên khi chúng ta dựng base cho trang web, điều chúng ta nên làm đầu tiên là reset CSS.
- Cách reset đơn giản nhất là reset *padding* và *margin* bằng 0, và set box-sizing: border-box để khỏi phải tính toán kích thước content của phần tử.

### 2. Tạo các thẻ div chính
- Ứng với mỗi thành phần chính của website sẽ là một thẻ div, tuy nhiên chúng ta cần phải có thêm một thẻ div lớn để có thể chứa tất cả các thẻ div của các thành phần chính đó.
- Ứng với mỗi thẻ div của các thành phần chính, chúng ta sẽ đặt tên theo id là tên của thành phần chính.
```
vd: <div id="header"></div>
```
- Ứng với thẻ div lớn chứa các thẻ div chính thì chúng ta nên đặt tên id là wrapper (bao bọc), main hoặc app.

## Thực hành 
1. Thực hành số 1: [w3_band](https://www.w3schools.com/w3css/tryw3css_templates_band.htm)