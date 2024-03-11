### thẻ <pre></pre>
Thẻ <pre> trong HTML được sử dụng để hiển thị nội dung văn bản với định dạng nguyên thủy, giữ nguyên các khoảng trắng, xuống dòng và các ký tự không được mã hóa HTML


### thẻ <hr/>
Thẻ <hr> trong HTML là viết tắt của "horizontal rule" (đường ngang), và nó được sử dụng để tạo một đường ngang ngăn cách các phần khác nhau trên trang web của bạn.

## Thẻ chèn liên kết (a = anchor)

<a href="link">Text</a>

`#` => Hash => Phía client

target

- `_blank` => mở tab mới
- `_self` => mở tab hiện tại

## Thẻ chèn hình ảnh (img = image)

- <img src="link ảnh" width="chiều rộng" height="chiều cao"  title="Tiêu đề" alt="Chữ thay thế"/>

Đường dẫn tương đối (relative path): Chỉ ở cấp folder con

Đường dẫn tuyệt đối (absolute path): Đầy đủ cả giao thức và đường dẫn

http://tenmien/duong-dan

protocol + domain:port/path

## cách back về file cha khi dùng liên kết là dung  ../

## Table

- Vẽ theo hàng ngang
- Vẽ hàng trước, cột sau

Thẻ table => Tạo bảng

- width: Chiều rộng
- border: Viền
- cellpadding: Khoảng cách giữa viền tới nội dung của các ô
- cellspacing: Khoảng cách giữa các ô (lề)

Thẻ tr => Tạo hàng cho bảng

Thẻ td => tạo cột cho bảng (Nằm trong thẻ tr)


## mindset khi tạo table có cấu trúc chia cột và hàng phức tạp
b1: tạo thẻ <table border="1" width="100%" cellpadding="10">
b2: đếm số hàng nhiều nhất(cộng thêm cả hàng con) và thêm đủ số thẻ <tr> </tr> tương ứng tr*n (n là số hàng) và ấn phím tab
b3: tạo ô, gộp ô từ những hàng phúc tạp cho đến đơn giản. liên tục check sản phẩm đúng theo ý tưởng hay chưa và tự điều chỉnh (dùng thuộc tính colspan và rolspan)

lưu ý: trong thẻ tr nhất định ít nhất phải có một thẻ td hoặc th(dùng cho thead), nếu không có sẽ không tạo ra ô. và thuộc tính colspan,rolspan chỉ dùng được cho td,th.

## Form: Biểu mẫu

- 1 trang web sẽ có nhiều form
- form đứng ngang hàng, không lồng nhau
## - 1 form bao gồm nhiều thành phần(element) ví dụ: input, label, button, select, option.
- 1 form thường có 2 thuộc tính: method và action:

`<form method="phuong-thuc(post,get)" action="duong-dan">
Các trường

</form>`

## Các trường(thành phần - element) trong form

### 1. Thẻ input - cho phép người dùng nhập thông tin từ đó dùng để thu thập và gửi dữ dữ liệu lên server của một trang web(ví dụ như tạp tài khoản, đăng nhập...)
- cú pháp cơ bản của thẻ: <input type="loại_dữ_liệu" name="tên" value="giá_trị" />

 ##các attributes của input
cơ bản:
- type: Kiểu dữ liệu (Default = text): phổ biến gồm các type sau: text, password, email, number, date, checkbox, radio, file, submit, button.
- name: Tên trường để lấy dữ liệu (back-end)
- value: Giá trị của input


- placeholder: Văn bản hiển thị như gợi ý cho người dùng về dữ liệu cần nhập. Thường là một mô tả ngắn về loại dữ liệu mong đợi.
- required: Đánh dấu input là bắt buộc phải điền trước khi submit form.
- readonly: Cho phép input chỉ có thể đọc mà không thể chỉnh sửa.
- disabled: Vô hiệu hóa input, ngăn người dùng tương tác với nó.
- maxlength: Xác định số ký tự tối đa được phép nhập vào input.
- min và max: Áp đặt giá trị tối thiểu và tối đa cho các loại số như number hoặc date.
- pattern: Sử dụng regex để kiểm tra dữ liệu người dùng nhập vào với mẫu cụ thể.
- autofocus: Tự động focus vào input khi trang được tải.

## 2. Thẻ label - ược sử dụng để xác định nhãn cho phần tử input, select, textarea

- Thể hiện 1 dòng chữ mô tả cho trường, 
- có 3 thuộc tính thường dùng cho thẻ label: for, form
- form: Chỉ định một hoặc nhiều biểu mẫu mà nhãn thuộc về
- for: Thuộc tính này liên kết nhãn với một phần tử biểu mẫu cụ thể bằng cách chỉ định ID của phần tử biểu mẫu. 
cú pháp:
- <label for="id của element form(input,select, button, textarea)" form="">Nội dung</label>

vídu:
<form id="loginForm">
  <label for="username" form="loginForm">Tên người dùng:</label>
  <input type="text" id="username" name="username">
</form>

## 3. thẻ button -  để tạo ra một nút trong một biểu mẫu hoặc bất kỳ nội dung tĩnh nào cần thực hiện hành động nào đó khi người dùng click vào.
cú pháp: <button>Click me</button>

attribute button:
type: Xác định loại nút, như submit, reset, hoặc button. Nếu không được chỉ định, giá trị mặc định là submit.
name: Xác định tên của nút, thường được sử dụng khi gửi dữ liệu từ biểu mẫu.
value: Xác định giá trị được gửi khi nút được nhấn, thường được sử dụng trong các biểu mẫu gửi dữ liệu.
form: Xác định biểu mẫu mà nút thuộc về, khi nó không nằm trong phần tử <form> trực tiếp.

ví dụ về form attribute: 
<form id="myForm">
  <!-- ... -->
</form>
<button type="submit" form="myForm">Submit Form</button>


