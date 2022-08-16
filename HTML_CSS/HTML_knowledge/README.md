##### Table of Content

1. [Các thẻ HTML thông dụng](#các-thẻ-html-thông-dụng)
1. [Các dạng phần tử trong HTML](#các-dạng-phần-tử-trong-html)
1. [Attribute trong HTML](#attribute-trong-html)

# Những kiến thức HTML tổng hợp được trong khóa học **HTML, CSS từ Zero đến Hero**

## Các thẻ HTML thông dụng

### 1. html

- Thẻ _html_ dùng để chứa toàn bộ source code của giao diện website.
- Một file html chỉ chứa một thẻ _html_.

### 2. head

- Thẻ _head_ dùng để định nghĩa tiêu đề của website, link các file css, chứa source _CSS Internal_,...

### 3. body

- Thẻ _body_ để chứa toàn bộ các nội dung của giao diện website.

### 4. title

- Thẻ _title_ dùng để định nghĩa tiêu đề cho website.

### 5. meta

- Thẻ _meta_ dùng để định nghĩa nhiều thông tin cho phần _head_, mỗi thẻ _meta_ sẽ có một chức năng khác nhau.
- Một trong các cách dùng thẻ _meta_ phổ biến nhất là sử dụng thuộc tính charset="utf8" dùng để hỗ trợ tiếng việt cho website.

### 6. link

- Thẻ _link_ dùng để liên kết các file css ở bên ngoài, các font chữ,...

### 7. h1 - h6

- Thẻ _heading_ hay còn gọi là thẻ tiêu đề, nó có nhiệm vụ là tạo ra các tiêu đề của văn bản hay của của trang web.
- Trong một file html chỉ có duy nhất một thẻ _h1_.
- Từ thẻ _h2_ tới _h6_ chữ nó sẽ nhỏ dần lại.

### 8. p

- Thẻ _paragraph_ có công dụng là hiển thị các đoạn văn trong web.

### 9. img

- Thẻ _image_ dùng để hiển thị hình ảnh.
- Thuộc tính _src_ - source trong thẻ _image_ có công dụng để liên kết hình ảnh vô thẻ _image_.
- Thuộc tính _alt_ có công dụng chú thích nội dụng của hình ảnh khi ảnh bị lỗi, ảnh bị xóa hoặc đường link bị hỏng khiến cho ảnh không còn được hiển thị, thì phần chú thích trong thuộc tính _alt_ sẽ được hiển thị để thay thế.

### 10. a

- Thẻ _anchor_ có công dụng là neo liên kết, khi nhấn vô thì sẽ được dẫn tới liên kết được neo.
- Thuộc tính _href_ có công dụng là link đường dẫn liên kết.

### 11. ul, li

- Thẻ _ul_ - unordered list dùng để hiển thị các danh sách trong trang web.
- Ngoài thẻ _ul_, chúng ta có thể sử dụng thẻ ol để thay các dấu chấm trong danh sách thành số thứ tự.
- Thẻ _li_ - list item dùng để hiển thị từng mục trong danh sách thẻ _ul_.

### 12. table

- Thẻ _table_ dùng để hiển thị bảng.
- Trong thẻ _table_, có 2 thẻ quan trọng cần nhớ là thẻ _thead_ và _tbody_. Thẻ _thead_ dùng để hiển thị phần đầu (phần tiêu đề) của bảng, còn thẻ _tbody_ dùng để hiện thị nội dung của bảng.
- Trong thẻ _thead_, để định nghĩa dòng tiêu đề chúng ta sẽ sử dụng thẻ _tr_, để định nghĩa nội dung tiêu đề cho bảng chúng ta sẽ dùng thẻ _th_.
- Trong thẻ _tbody_, chúng ta có thể thêm nội dung vào bảng thẻ _tr_, mỗi thẻ _tr_ sẽ tương ứng với một dòng trong bảng, để hiển thị từng nội dung trong một dòng chúng ta sẽ dùng thẻ _td_.

### 13. input

- Thẻ _input_ cho phép chúng ta nhập nội dung vào trang web.
- Thẻ _input_ có rất nhiều type, một số type phổ biển:
  - _text_: cho phép nhập chữ vào ô input.
  - _checkbox_: tạo ra các ô check để chúng ta đánh dấu, chức năng của nó là cho phép người dùng chọn nhiều lựa chọn.
  - _radio_: về chức năng nó cũng khá tương tự với _checkbox_, tuy nhiên về hình dạng nó sẽ là hình tròn thay vì hình vuông như _checkbox_, về mặt chức năng thì chỉ cho phép người dùng chọn 1 lựa chọn duy nhất, và để thực hiện chức năng đó thì các thẻ input type _radio_ phải được đặt cùng 1 _name_.
    ...

### 14. button

- Thẻ button có công dụng là tạo ra các nút để người dùng có thể nhấn được, có chức năng để nhấn gửi hoặc nhấn submit.

### 15. div

- Thẻ div có dụng để tạo ra các khối bao quanh các phần tử khác, sẽ giúp ích trong việc css các phần tử bên trong nó.

**Tham khảo thêm tại:** https://fullstack.edu.vn/blog/tim-hieu-ve-html-va-css.html

## Các dạng phần tử trong HTML

Trong HTML, các phần tử HTML được phân loại ra thành 2 cấp độ: _block_ và _inline_.

### Phần tử HTML cấp độ block

- Là những phần tử chiếm hết không gian theo chiều ngang của phần tử cha (phần tử chứa nó), còn chiều cao được mở rộng tùy theo nội dung của phần tử này.
- Trong trình duyệt các phần tử dạng này tạo ra các dòng mới (xuống dòng) ở trước và sau phần tử.
- Các phần tử cấp độ block: body, main, header, footer, section, nav, aside, div, h1-h6, p, ul, ol, li,...etc.
- Ngoài ra chúng ta có thể style các phần tử khác thành cấp độ block bằng CSS.

```
display: block;
```

### Phần tử HTML cấp độ inline

- Là những phần tử chiếm không gian chiều ngang theo nội dung của phần tử.
- Không tạo ra dòng mới (xuống dòng) trước và sau phần tử.
- Đối với các phần tử HTML cấp độ inline, thuộc tính _height_ và _width_ sẽ không áp dụng được.
- Ngoài ra khi style css với thuộc tính _padding_ và _margin_ thì chỉ có thể style theo chiều ngang (bên trái và bên phải).
- Các phần tử cấp độ inline: a, img, strong, em, button,...etc.
- Ngoài ra chúng ta có thể style các phần tử khác thành cấp độ inline bằng CSS.

```
display: inline;
```

### Phần tử HTML cấp độ inline-block

- Ngoài ra chúng có một sự kết hợp giữa phần tử cấp độ block và phần tử cấp độ inline, đó là inline-block.
- Về mặt cơ bản, phần tử cấp độ inline-block sẽ kế thừa những đặc tính hữu ích từ 2 phần tử trên.
- Phần tử inline-block chỉ chiếm không gian chiều ngang theo nội dung của phần tử, dĩ nhiên cũng sẽ không tạo dòng mới (xuống dòng) trước và sau phần tử.
- Ngoài ra, phần tử inline-block có thể áp dụng được những thuộc tính của box-model (có thể style width và height, có thể áp dụng margin và padding theo cả chiều ngang và chiều dọc,...)
- Chúng ta có thể tạo phần tử cấp độ inline-block bằng CSS.

```
display: inline-block;
```

## Attribute trong HTML

- Attribute hay còn gọi là thuộc tính, có công dụng là thêm các thuộc tính vô trong các thẻ trong html.
- Với mỗi thẻ trong html có rất nhiều thuộc tính đi kèm theo nó, tùy vào từng mục đích chúng ta sẽ sử dụng các thuộc tính cho phù hợp. Một số thuộc tính thông dụng như: _style_, _onclick_, _title_,...
