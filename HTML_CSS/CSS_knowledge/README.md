##### Table of Content

1. [Các cách sử dụng CSS](#các-cách-sử-dụng-css)
1. [Các trường hợp sử dụng](#các-trường-hợp-sử-dụng)
1. [Lưu ý khi sử dụng CSS](#lưu-ý-khi-sử-dụng-css)
1. [CSS Selector](#css-selector)
1. [CSS Selector cơ bản](#css-selector-cơ-bản)
1. [CSS Priority](#css-priority)
1. [CSS Variable](#css-variable)
1. [CSS Units](#css-units)
1. [CSS Functions](#css-functions)
1. [CSS Pseudo-Classes](#css-pseudo-classes)
1. [CSS Pseudo-Elements](#css-pseudo-elements)
1. [CSS Box Model](#css-box-model)
1. [Background Attributes](#background-attributes)
1. [Position Attributes](#position-attributes)
1. [Các cách căn giữa item](#các-cách-căn-giữa-item)


# Những kiến thức CSS tổng hợp được trong khóa học **HTML, CSS từ Zero đến Hero**


## Các cách sử dụng CSS

### 1. Internal

- Là cách CSS trong cặp thẻ style, và chúng ta có thể đặt cặp thẻ style đó ở bất kì vị trí nào ngoại trừ giữa thẻ head và body.
- Khuyến khích CSS trong thẻ head.

### 2. External

- Là cách CSS ở ngoài file html, tức là chúng ta sẽ CSS ở trong một file CSS ở bên ngoài (có thể là trong cùng thư mục project hoặc ở trên mạng).
- Để sử dụng được *CSS External* chúng ta sẽ sử dụng một cặp thẻ link để dẫn tới file CSS đó.
```
vd: <link rel="stylesheet" href="{đường dẫn file CSS}">
```

### 3. Inline
- Là cách CSS trong thuộc tính style trong thẻ mở của html.


## Các trường hợp sử dụng

### 1. External
- Trong thực tế hầu hết chúng ta sử dụng cách này. Viết CSS riêng ra một file giúp code được gọn gàng và tách bạch hơn. Giúp dễ dàng trong việc sử dụng lại giữa nhiều trang khác nhau.

### 2. Internal
- Có thể sử dụng trong trường hợp CSS cho một trang có style khác biệt hoàn toàn so với các trang còn lại. Bạn cần đủ kinh nghiệm để chắc chắn vào điều đó, đôi khi có những thành phần tại thời điểm đó là duy nhất, nhưng trong tương lai nó sẽ được sử dụng ở mọi nơi.
- Khi một trang xuất hiện một thành phần chỉ sử dụng duy nhất trong trang này bạn cũng có thể sử dụng *CSS Internal*. Tuy nhiên cũng cần nhiều kinh nghiệm để có thể đánh giá một cách đúng đắn.
- Ngoài ra một số tips để tối ưu tốc độ tải của website người ta cũng sử dụng *CSS Internal*.

### 3. Inline
- Trường hợp sử dụng phổ biến nhất có lẽ là khi tạo email HTML, có khi nào bạn nhận được email quảng cáo với giao diện khá bắt mắt. Đó chính là những email HTML được sử dụng *CSS Inline*. Tại sao email HTML lại sử dụng *CSS Inline*? Đơn giản vì để đáp ứng được các tiêu chuẩn, các vấn đề bảo mật khi gửi email HTML của các nhà cung cấp dịch vụ mail.
- Trường hợp khác là *CSS Inline* dùng để thay đổi giá trị *url* của thuộc tính *background-image* trong danh sách sản phẩm (đại loại là một danh sách có hình ảnh). Thực tế một website khi hoàn thiện cần có bước lấy dữ liệu từ database để hiển thị ra. Trong trường hợp bạn hiển thị ảnh với *background-image* mà ảnh đó được lấy từ database thì bạn phải sử dụng *CSS Inline*.
- Và khi làm việc với DOM (sẽ học trong khóa Javascript) chúng ta thường thay đổi giá trị của các thuộc tính CSS trên mỗi thành phần HTML qua thuộc tính style. Thay đổi này sẽ tạo nên các thay đổi *CSS Inline*.
- Trong thực tế mọi thứ đều có thể xảy ra, sẽ có rất nhiều các trường hợp diễn ra trong quá trình các bạn làm việc. Quan trọng là bạn hãy học thật chắc kiến thức cơ bản để sau này làm việc có thể Thiên biến vạn hóa để giải quyết vấn đề.


## Lưu ý khi sử dụng CSS
- Khi kết thúc CSS một thuộc tính thì phải có dấu ";".
- Khi chưa đủ kinh nghiệm để thực sự hiểu khi nào nên dùng *CSS Internal* và *CSS Inline* thì tốt nhất là hãy sử dụng *CSS External*.


## CSS Selector
Trong CSS, CSS selectors là các cách chúng ta sử dụng để chọn ra các phần tử (elements) mà chúng ta muốn “style” cho chúng. Có rất nhiều cách để chúng ta có thể select các phần tử để CSS.

### 1. CSS bằng cách gọi trực tiếp các thẻ trong html
- Đối với cách này nó sẽ gặp một hạn chế là nó sẽ ảnh hưởng toàn bộ các thẻ còn lại trong html. Ví dụ khi ta CSS thẻ h1 thì toàn bộ tất cả các thẻ h1 sẽ đều bị CSS, tuy nhiên trong khi đó chúng ta chỉ cần CSS 1 thẻ h1 thôi thì cách này không hiệu quả.
- Để khắc phục vấn đề này chúng ta cần đặt ID và Class cho từng thẻ html để CSS hiệu quả hơn, tránh CSS nhầm các thẻ trong html.

### 2. CSS bằng ID
- Với việc đặt id riêng biệt cho từng thẻ trong html sẽ giúp chúng ta CSS dễ dàng hơn và tránh bị nhầm lẫn. Một điều lưu ý khi CSS bằng id là khi chúng ta select đối tượng thì phải có dấu "#".
```
vd: khi chúng ta đặt thẻ h1 với id là "first-heading" thì khi chúng ta gọi thẻ h1 để css thì chúng ta phải gọi bằng "#first-heading".
```
- Ngoài ra bản thân id nó mang nghĩa là *identify*, có nghĩa là định danh duy nhất nên chỉ xuất hiện duy nhất một lần, cho nên trong một project không được phép đặt trùng id cho nhiều thẻ html điều này dễ bị lỗi trong javascript.
- Cho nên để có thể CSS cho nhiều đối tượng cùng lúc thì chúng ta sẽ sử dụng class.

### 3. CSS bằng class
- Về công dụng thì tương tự như id, nhưng về mặt ý nghĩa thì chúng ta được phép đặt tên cùng class cho nhiều thẻ html để tái tận dụng CSS, tránh lặp lại mã. Về cách sử dụng thì khi chúng ta select thì phải dùng dấu ".". 
- Có thể đặt nhiều class cho một thẻ html.
```
vd: <div class="class1 class2"></div>
```


## CSS Selector cơ bản

### 1. .class
- Cách sử dụng:
```
.intro {

}
```
- Ý nghĩa: chọn tất cả các thẻ có class="intro".

### 2. .class1.class2
- Cách sử dụng:
```
.name1.name2 {

}
```
- Ý nghĩa: chọn tất cả các thẻ có cả name1 và name2 được đặt trong thuộc tính class của nó.

### 3. .class1 .class2
- Cách sử dụng:
```
.name1 .name2 {

}
```
- Ý nghĩa: chọn tất cả các thẻ có class="name2" là con của phần tử có class="name1".

### 4. *
- Cách sử dụng: 
```
* {

}
```
- Ý nghĩa: chọn tất các thẻ.

### 5. element
- Cách sử dụng:
```
h2 {

}
```
- Ý nghĩa: chọn tất cả các thẻ h2.

### 6. element.class
- Cách sử dụng:
```
div.box {

}
```
- Ý nghĩa: chọn tất cả các thẻ div có class="box".

### 7. element, element
- Cách sử dụng:
```
div, h2 {

}
```
- Ý nghĩa: chọn tất cả các thẻ div và thẻ h2.

### 8. element element 
- Cách sử dụng:
```
div p {

}
```
- Ý nghĩa: chọn tất cả các thẻ p có trong thẻ div.

### 9. element > element
- Cách sử dụng:
```
div > p {

}
```
- Ý nghĩa: chọn tất cả thẻ p là con trực tiếp của thẻ div.

### 10. element + element
- Cách sử dụng:
```
div + p {

}
```
- Ý nghĩa: chọn tất cả thẻ p đứng liền kề sau thẻ div.

### 11. element ~ element
- Cách sử dụng:
```
div ~ p {

}
```
- Ý nghĩa: chọn tất cả thẻ p đứng sau thẻ div.

**Tham khảo thêm tại:** https://www.w3schools.com/cssref/css_selectors.asps


## CSS Priority
- Khi chúng ta so sánh giữa *CSS Internal* và *CSS External* thì không có cách nào ưu tiên hơn cách nào, thằng nào gọi sau thì thằng đó sẽ ưu tiên. Tức nếu chúng ta *CSS Internal* sau *CSS External* thì *CSS Internal* sẽ được ưu tiên và ngược lại.
- Khi xét về thứ tự ưu tiên khi select các phần tử thì chúng ta sẽ có thứ tự như sau: *CSS Inline* > *id* > *class* > *tag*.
- Khi chúng ta select phần tử nhiều lần cùng lúc (select nhiều lần với độ ưu tiên bằng nhau) thì lần select cuối cùng sẽ được ưu tiên cao hơn.
```
vd: khi chúng ta thực hiện CSS internal cho thẻ h1, lần đầu chúng style thuộc tính color là màu đỏ, còn lần sau thì style thuộc tính color là màu xanh, thì thẻ h1 sẽ bị ảnh hưởng thuộc tính color màu xanh thì nó sẽ ưu tiên cho lần CSS sau cùng (select cuối cùng).
```
- Trong trường hợp khi chúng select nhiều thành phần cùng một lúc (h1.heading-class#headingid) thì chúng ta cứ mặc định tính độ ưu tiên các thành phần như sau:  *CSS Inline* - 1000, *id* - 100, *class* - 10,  *tag* - 1. Dựa vào số điểm ưu tiên chúng ta sẽ biết được select nào có độ ưu tiên cao hơn.
```
vd: h1#heading-id.heading-class > #heading-id.heading-class (111 > 110)
```
- Khi chúng CSS mà có thuộc tính *!important* thì nó sẽ có độ ưu tiên vượt trội, cao hơn tất cả. Trong trường hợp có nhiều select đều có thuộc tính *!important* thì nó sẽ tính độ ưu tiên lại theo thứ tự từ ban đầu (như ý 2).


## CSS Variable
- Trong html, khi chúng ta cần tái sử dụng một thuộc tính CSS nào đó (ví dụ: color, width, height,...) cho nhiều phần tử cùng lúc thì chúng ta nên sử dụng biến để CSS.
- Điều đó sẽ giúp ích cho việc tái sử dụng nhiều lần và dễ dàng nâng cấp, thay đổi. 
```
vd: khi chúng ta thiết kế một giao diện cho một trang web, chúng ta xác định màu chủ đạo của trang web là màu cam và cần áp màu cam cho nhiều phần tử trong html, thì với việc đặt một biến màu cam sẽ giúp ta dễ dàng trong việc tái sử dụng. Khi chúng ta muốn nâng cấp hoặc thay đổi màu chủ đạo sang màu xanh thì chúng ta chỉ cần thay đổi giá trị màu của biến đó chứ không nhất thiết phải thay đổi thủ công từng thuộc tính màu trong các thẻ html.
```
- Cách sử dụng:
    - Khi đặt tên biến chúng ta sẽ cần thêm dấu "--"
        ```
        --myVariable
        ```
    - Khi đặt biến toàn cục, thì chúng ta có thể sử dụng tại bất kì đâu trong html hoặc trong file *CSS External*. Ví dụ mẫu khi khai báo biến toàn cục:
        ```
        :root {
            --myColor: orange;
        }
        h1 {
            color: var(--myColor);
        }
        ```
    - Khi đặt tên biến cục bộ, thì chúng ta chỉ có thể khai báo bên trong selector cụ thể và chỉ có thể được sử dụng bên trong selector đó, không thể sử được cho các selector khác. Ví dụ khi khai báo biến cục bộ trong selector thẻ h1:
        ```
        h1 {
            --myColor: orange;
            color: var(--myColor);
        }
        ```


## CSS Units
Trong CSS chúng ta sẽ có 2 nhóm đơn vị: Absolute Units và Relative Units.

### 1. Absolute Units
- Các đơn vị trong Absolute Units sẽ luôn luôn cố định, không thay đổi khi các yếu tố xung quanh thay đổi (giao diện thay đổi,...).
- Trong Absolute Units chúng ta có các đơn vị như sau: *px*, *pt*, *cm*, *mm*, *inch*, *pc*.
- Trong tất cả các đơn vị ở trên thì *px* là đơn vị được sử dụng phổ biến nhất.
- Tùy vào độ phân giải của mỗi màn hình mà số lượng *px* hiển thị sẽ khác nhau, đối với màn hình độ phân giải cao thì 1px sẽ tương đương với nhiều pixel trên màn hình, còn đối với màn hình độ phân giải thấp thì 1px sẽ tương đương với 1px trên màn hình.

### 2. Relative Units
- Ngược lại với Absolute Units, các đơn vị trong Relative Units sẽ thay đổi phụ thuộc vào yếu bên xung quanh (kích thước của thẻ cha bị thay đổi, chiều dài và chiều ngang của giao diện bị thay đổi,...).
- Các đơn vị trong Relative Units: *%*, *rem*, *em*, *vw*, *vh*, *vmin*, *vmax*, *ex*, *ch*.
- Các đơn vị được sử dụng phổ biến: *%*, *rem*, *em*, *vw*, *vh*.
- Ứng với mỗi đơn vị sẽ có cách phụ thuộc khác nhau:
    - *%*: phụ thuộc vào thẻ cha chứa nó, kích thước của nó sẽ thay đổi dựa vào kích thước của thẻ cha chứa nó.
        ```
        vd: thẻ body là thẻ cha chứa thẻ div, thẻ div có width là 50% => width của thẻ div sẽ bằng 50% của thẻ body, nếu thẻ body có width là 500px thì thẻ div sẽ có width là 250px.
        ```
    - *rem*: phụ thuộc vào thẻ html. Quy luật: 1rem = 1 * giá trị.
        ```
        vd: thẻ html có thuộc tính font-size là 20px, thì khi thẻ h1 style thuộc tính font-size có giá trị là 1rem thì tương đồng với giá trị 20px, nếu 2rem thì là 40px => mọi giá trị thuộc tính của các thẻ khác sẽ phụ thuộc vào thuộc tính tương đồng trong thẻ html.
        ```
    - *em*: về chức năng thì tương tự như rem, nhưng nó sẽ phụ thuộc vào thẻ chứa nó gần nhất có thuộc tính tương đồng.
        ```
        vd: khi chúng ta style thẻ h1 font-size=2em, thì nó sẽ tìm thẻ chứa thẻ h1 đó gần nhất có thuộc tính font-size. Về quy luật cũng tương tự như rem: 1em = 1* giá trị.
        ```
    - *vw*, *vh*: cả 2 đơn vị này sẽ phụ thuộc vào kích thước giao diện hiện tại, *vw* sẽ phụ thuộc vào chiều ngang, *vh* sẽ phụ thuộc vào chiều dọc.

- Trong thực tế, dev sẽ thường dùng đơn vị *rem* hơn *em*, vì *rem* dễ kiểm soát vì nó luôn phụ thuộc vào thẻ html. Trong thực tế của des một trang web, dev sẽ cho thẻ html có font-size=100% (16px), sau đó sẽ cho các thẻ khác sử dụng đơn vị *rem* để kế thừa, giúp ích cho việc thay đổi kích thước toàn bộ chữ trong trang web, thường được sử dụng trong kĩ thuật responsive.
- Các đơn vị *%* rất quan trọng trong việc thiết kế giao diện, vì nó giúp chúng ta phân phối layout một cách hợp lý.
- Lưu ý về thuộc tính width và height, khi đặt theo *%* sẽ tỉ lệ vào thẻ mà nó phụ thuộc, mặc định là thẻ cha trực tiếp của nó. Vì vậy, thẻ cha của nó phải có kích thước cho width hoặc height thì thẻ con đặt theo *%* mới có tác dụng.


## CSS Functions
- Các functions thông dụng:
    - *var()*: dùng để đặt biến.
    - *linear-gradinet()*: tạo ra một dải màu chuyển đổi từ màu thứ nhất sang màu thứ hai.
        ```
        vd: linear-gradinet(0, #333, #fff): tham số đầu tiên là hướng đổi màu (trong ví dụ là 0 độ, tức là từ dưới lên trên), tham số thứ hai màu thứ nhất và tham số thứ ba là màu thứ hai.
        ```
    - *rgba()*: tương tự rgb nhưng có thể giá trị alpha, alpha dùng để pha độ trong suốt.
    - *rgb()*: dùng để tạo màu rgb, có thể pha màu dựa vào 3 giá trị R-G-B.
    - *calc()*: dùng để tính toán các đơn vị trong css, có thể tính toán giữa 2 giá trị tương đối và tuyệt đối.
    - *attr()*: dùng để lấy giá trị thuộc tính, thường được sử dụng chung với lớp giả.


## CSS Pseudo-Classes
- Khi chúng ta CSS thuộc tính vào các thẻ, tùy vào từng lớp giả sẽ có cách kích hoạt hiển thị các CSS đó khác nhau:
- Các lớp giả thông dụng:
    + *:root*:
    + *:hover*: được kích hoạt khi di chuyển vào.
    + *:active*: được kích hoạt khi click vào.
    + *:first-child*: lấy thẻ con đầu tiên để CSS.
    + *:last-child*: lấy thẻ con cuối cùng để CSS.
- Cách sử dụng: 
```
h1:hover {

}
```


##  CSS Pseudo-Elements
- Các Pseudo-Elements được sử dụng khi chúng ta cần tạo ra các phần tử để hiển thị mà không cần viết mã html, chỉ cần viết mã css.
- Các phần tử giả thông dụng:
    - *::before*: tạo ra phần tử nằm trong thẻ được chọn, vẫn có thể style các thuộc tính bình thường, mỗi element chỉ tồn tại duy nhất một element giả *::before*.
    - *::after*: về chức năng thì y chang *::before*, mỗi element cũng chỉ tồn tại duy nhất một element giả *::after*. Về vị trí element *::before* sẽ là element đầu tiên trong tất cả các element của thẻ được chọn, còn element *::after* sẽ là element cuối cùng.
        ```
        vd: khi chúng ta tạo một thẻ div cha có 10 thẻ div con, khi chúng ta chọn thẻ div cha để tạo element giả before và after, thì element before sẽ là phần tử đầu tiên còn element after sẽ là phần tử cuối cùng.
        ```
        - Mỗi element before và after đều có thuộc tính content, một thuộc tính rất quan trọng.
    + *::first-letter*: được dùng để chọn chữ cái đầu tiên để CSS.
    + *::first-line*: được dùng để chọn dòng đầu tiên để CSS, lưu ý là dòng đầu tiên khi có thẻ br.
    + *::selection*: mọi thuộc tính khi style sẽ được hiển thị khi chúng ta bôi chuột vào vùng mà chúng ta đã CSS.
- Cách sử dụng:
```
h1::first-letter {

}
```


## CSS Box Model

## 1. CSS padding
- *Padding* là đệm thêm một phần kích thước của phần tử, nó sẽ khiến cho kích thước tổng thể của phần tử sẽ bị tăng lên.
- Cách sử dụng:
    - 1 giá trị: đệm cả 4 hướng.
    - 2 giá trị: giá trị thứ nhất là bên trên và bên dưới, giá trị thứ hai là bên trái và bên phải.
    - 3 giá trị: giá trị thứ nhất sẽ là bên trên, giá trị thứ hai là bên trái và bên phải, giá trị thứ ba sẽ là bên dưới.
    - 4 giá trị: theo thứ tự từng giá trị một sẽ là trên, phải, dưới, trái.
    ```
    vd: padding: 10px 12px 14px 16px;
    ```

### 2. CSS border
- *Border* được hiểu là một lớp viền ngoài cùng ôm trọn element được chọn.
- Khi chúng ta thêm *border* vào element, nó sẽ khiến kích thước tổng thể của element tăng lên, ngoài ra chúng ta có thể style thêm thuộc tính hình dạng và màu cho lớp viền này.
- Trong thực tế thì người ta sẽ cho kích thước của viền này là 1px.
- Mặc định kiểu *border* solid (viền liền) sẽ có kích thước mặc định là 3px.
```
vd: border: 1px solid #333;
```

### 3. CSS margin
- *Margin* sẽ khác biệt so với *Padding*, vì nó sẽ không tăng lên kích thước tổng thể của element.
- Thông thường người ta sử dụng *margin* để tạo khoảng cách cho các element, ví dụ khi người ta cần tách 2 element đứng gần nhau thì người ta tạo *margin* để tách 2 vật thể đó ra, vầ tất nhiên *margin* nó sẽ không làm tăng kích thước tổng thể của 2 element đó.
- Về cách sử dụng thì nó tương tự như *padding*.

### 4. CSS box-sizing
- Thuộc tính *box-sizing* có chức năng sẽ tự động, căn chỉnh kích thước content của element sao cho kích thước khai báo tổng thể của element đó không bị tăng lên khi có thêm *padding* và *border*.
    ```
    vd: khi chúng ta tạo một div box có kích thước 100px, và chúng ta cho thêm padding 10px và *border 1px thì sẽ làm cho kích thước tổng thể của box đó tăng thêm 22px. Thì để vẫn giữ *padding* và border và vẫn muốn giữ kích thước tổng thể là 100px thì buộc lòng chúng ta phải trừ kích thước của box đi 22px, nhưng làm việc đó thì rất là tốn công, chúng ta chỉ cần việc thêm thuộc tính box-sizing: border-box thì nó tự động tính toán làm giảm đi kích thước content sao cho kích thước tổng thể vẫn còn là 100px.
- Một điều lưu ý là nếu chúng ta cố tình đặt kích thước *padding* vô cùng lớn thì nó vẫn làm tăng kích thước tổng thể của element.
- Mặc định thuộc tính *box-sizing* sẽ mang giá trị là *content-box*, tức là vẫn giữ nguyên.
- Cách sử dụng:
```
box-sizing: border-box;
```


## Background Attributes

## 1. CSS background-clip
- Thuộc tính *background-clip* có chức năng là đổ màu từ thành phần nào. Tức là ví dụ khi chúng ta cho thuộc tính *background-clip* mang giá trị là *border-box* thì màu nền sẽ được đổ từ *border* (nếu có và dạng *dashed*) vô *padding* (nếu có) rồi vô tới *content*; tức là cả màu *border*, màu *padding* và màu *content* đều mang cùng một màu của *background-color*.
```
vd: nếu chúng ta chỉ cần đổ màu từ padding thì chỉ cần style giá trị là padding-box thì chỉ có màu padding và màu content là chung, còn màu border sẽ không có.
```
- Giá trị mặc định của thuộc tính *background-clip* là *border-box*.
- Trong thực tế, khi chúng ta chỉ cần đổ màu cho *content* thôi mà hong cần đổ màu cho *border* và *padding*, thì chúng ta sẽ style thuộc tính *background-clip* giá trị là *content-box*.

## 2. CSS background-image
- Thuộc tính *background-image* cho phép chúng ta chèn hình ảnh vào nền. Chúng ta có thể kết hợp đan xen nhiều ảnh với nhau, và mỗi hình ảnh sẽ cách nhau bằng dấu ",", hoặc chúng ta có thể kết hợp dải màu chuyển đổi *linear-gradient* với hình ảnh.
- Cách sử dụng:
```
background-image: url({đường dẫn hình ảnh});
```
- Ngoài ra chúng ta có thêm 2 thuộc tính để có thể chỉnh sửa hình ảnh là *background-size* và *background-repeat*:
    - *Background-size* cho phép chúng ta điều chỉnh kích thước của hình ảnh nền, khi chúng ta chỉ cho 1 giá trị thì mặc định nó sẽ hiểu giá trị đó giá trị đó là *width*, còn giá *height* thì nó sẽ để auto để vẫn giữ tỉ lệ của hình ảnh không làm méo hình.
    - *Background-repeat* có chức năng giúp ta điều chỉnh sự *repeat*, nếu chúng ta không mong muốn hình bị lặp lại thì chúng ta sẽ set giá trị là *no-repeat*, còn nếu chúng ta cần *repeat* thì chúng ta set giá trị là *repeat* hoặc chúng ta có thể xóa luôn thuộc tính *background-repeat* vì mặc định khi chèn hình vào nên nó tự động lặp lại để fit với kích thước tổng thể của element.

### 3. CSS background-size keywords
- Trong thuộc tính *background-size* ngoài chúng ta có thể style bằng các kích thước tương đối và tuyệt đối, chúng ta còn có thể style theo keyword.
- Có 2 keyword thông dụng được dùng trong *background-size* đó chính là *contain* và *cover*.
- Keyword *contain* nó sẽ lấy tùy biến lấy kích thước dài nhất của thẻ cha chứa nó để làm kích thước cố định, còn kích thước còn lại sẽ được set auto để không làm méo ảnh. Tuy nhiên *contain* thì nó sẽ cố gắng để có thể hiển thị đầy đủ bức ảnh, nó chấp nhận sẽ bị dư ra một khoảng hở để có thể hiển thị được đầy đủ của bức ảnh.
- Ngược lại với *contain*, keyword *cover* nó cũng sẽ lấy kích thước dài nhất của thẻ cha chứa nó để làm kích thước cố định, tuy nhiên *cover* nó chấp nhận hiển thị không đầy đủ hình ảnh, nó sẽ cố gắng làm cho hình ảnh được bao trọn hết thẻ cha chứa nó, nó không chấp nhận có khoảng hở.
- Đối với *cover* thì nó sẽ làm hình ảnh nền bị mất một phần để có thể fit nguyên vẹn với thẻ cha chứa nó, còn *containt* nó sẽ cố gắng hiển thị đầy đủ hình ảnh và chấp nhận bị hở một khoảng trống.

### 4. CSS background-origin
- Cũng tương tự như *background-color*, chúng ra có thuộc tính *background-clip* để quyết định nơi đổ màu; còn đối với *background-image* chúng ta sẽ có thuộc tính *background-origin* để quyết nơi bắt đầu hiển thị hình ảnh.
- Về công dụng nó cũng tương tự như *background-clip*.
- Giá trị mặc định của thuộc tính *background-origin* là *padding-box*.
- Trong thực tế khi chúng ta des một trang web, chúng ta cần phải style để hình ảnh nó không bị ảnh hưởng với *border* và *padding* thì chúng ta sẽ cần sử dụng tới thuộc tính *background-origin* để căn chỉnh.

### 5. CSS background-position
- Thuộc tính *background-position* có công dụng giúp chúng ta căn chỉnh vị trí của ảnh nền.

### 6. CSS background shorthand
- Thay vì chúng ta phải viết rõ ràng từng thuộc tính một, thì chúng ta thể thực hiện các câu lệnh viết tắt.
- Một điều lưu ý khi viết shorthand là thuộc tính *background-position* phải đi chung với thuộc tính *background-size*, và trước thuộc tính *background-image* phải có dấu "/".
- Cách sử dụng:
```
background: no-repeat url("đường dẫn ảnh") center / contain;
```
hoặc
```
background: url("đường dẫn ảnh") no-repeat center / contain;
```

## Position Attributes
Các thuộc tính position sẽ cho phép chúng ta thiết lập các vị trí đặc biệt, nó cho phép các element có thể đè lên nhau. Khi chúng ta style thuộc tính position thì element đó sẽ có thêm các thuộc tính *top* *bottom* *right* *left* để chúng có thể thiết lập vị trí cho element đó.

### 1. CSS Position: Relative
- *Relative* là vị tí tương đối, nó phụ thuộc vào chính mình, nó sẽ lấy vị trí của chính bản thân nó làm gốc, nó sẽ không phụ thuộc vào bất kì một element nào cả.

### 2. CSS Position: Absolute
- *Absolute* là vị trí tuyệt đối, nó sẽ phụ thuộc vào thẻ cha chứa nó gần nhất có thuộc tính position để làm gốc.
- Trong thực tế, người ta thường sẽ sử dụng thuộc tính position *absolute* khi chúng ta cần di chuyển một thẻ con xung quanh vị trí của thẻ cha, khi đó chúng ta sẽ set thuộc tính position bất kỳ cho thẻ cha, rồi sau đó chúng ta sẽ set thuộc tính position *absolute* cho thẻ con đó, sau đó chúng ta sẽ sử dụng các thuộc tính *top* *left* *bottom* *right* để thiết lập vị trí của thẻ con theo vị trí gốc của thẻ cha.

### 3. CSS Position: Fixed
- Cũng tương tự như *Absolute*, vị trị *Fixed* nó sẽ phụ thuộc vào cửa sổ trình duyệt làm gốc.
- Trong thực tế người ta hay sử dụng vị trí *fixed* để thiếp lập vị trí của header và footer của trang web.

### 4. CSS Position: Sticky
- Thuộc tính ít thông dụng, vì nó ít được hỗ trợ nhiều trình duyệt.
- Nó sẽ không phụ thuộc vào bất kỳ ai, nó sẽ lấy vị trí hiện tại của nó làm gốc.
- Tuy nhiên có một công năng thú vị, đó là khi chúng ta style thuộc tính top=0, thì khi chúng ta cuộn trang web nếu element đó mà cách top của trình duyệt bằng 0 thì nó sẽ bám dính, nó khá tương đồng với vị trí *fixed*.

## Các cách căn giữa item

### 1. text-align: center
- Cách sử dụng:
```
h1 {
    text-align: center;
}
```
hoặc
```
div .box {
    background-color: orange;
    height: 100px;
    text-align: center;
}

h1 {

}
```
- Thuộc tính *text-align: center;* dùng để căn giữa item theo trục ngang.
- Đây là thuộc tính có tính thừa kế, cho nên có thể sử dụng trực tiếp vào thẻ con hoặc áp dụng vào thẻ cha để thẻ con thừa kế.
- Trong trường hợp chỉ có một thẻ con cần căn giữa thì nên dùng thuộc tính này vào trực tiếp thẻ con đó, còn trường hợp có nhiều thẻ con thì nên áp dụng thuộc tính này vào chính thẻ cha chứa các thẻ con đó để các thẻ con được căn giữa.

### 2. line-height
- Cách sử dụng:
```
div .box {
    background-color: orange;
    height: 100px;
}

h1 {
    line-height: 100px;
}
```
hoặc
```
div .box {
    background-color: orange;
    height: 100px;
    line-height: 100px;
}

h1 {

}
```
hoặc
```
div .box {
    --height: 100px;
    background-color: orange;
    height: var(--height);
}

h1 {
    line-height: var(--height);
}
```
- Thuộc tính *line-height* dùng để thiết lập chiều cao cho dòng của item. Tuy nhiên chúng ta có thể sử dụng thuộc tính này để căn giữa item theo trục dọc bằng cách chúng ta thiết lập thuộc tính *line-height* bằng với chiều cao của thẻ cha chứa item đó.
- Đây là thuộc tính có tính thừa kế, nên cách sử dụng cũng tương tự như thuộc tính *text-align*.

### 3. Căn giữa với thuộc tính display: flex
- Cách sử dụng:
```
div .box {
    background-color: orange;
    height: 100px;
    display: flex;
}

h1 {
    margin: auto;
}
```
hoặc
```
div .box {
    background-color: orange;
    height: 100px;
    display: flex;
    align-item: center;
    justify-content: center;
}

h1 {

}
```
- Cả 2 cách trên đều được sử dụng để căn giữa các item theo trục dọc và trục ngang.
- Một điều lưu ý khi sử dụng 2 cách trên để căn giữa các item là bắt buộc phải có thuộc tính *display: flex;*.
- Đối với cách thứ hai, thuộc tính *align-item: center;* dùng để căn giữa các item theo trục dọc, còn thuộc tính *justify-content: center;* dùng để căn giữa các item theo trục ngang.

### 4. Căn giữa với thuộc tính position
- Cách sử dụng:
```
div .box {
    background-color: orange;
    height: 100px;
    position: relative;
}

h1 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateY(-50%) translateX(-50%);
}
```
hoặc
```
div .box {
    background-color: orange;
    height: 100px;
    display: flex;
}

h1 {
    position: absolute;
    tmargin: auto;
}

h1::after {
    position: absolute;
    left: -10px;
    content: "";
    border-left: 3px solid #333;
    height: 20px;
    top: 50%;
    transform: translateY(-50%);
}
```
- Trong trường hợp khi chúng ta không thể sử dụng các cách ở trên để căn giữa item, thì chúng ta có thể sử dụng thuộc tính *position* để căn giữa item.
- Để hiểu thêm cách sử dụng thuộc tính *position* để căn giữa item, vui lòng tham khảo thêm tại: [Căn giữa item với thuộc tính position](https://youtu.be/I2-m_kWZp_Y?t=364)