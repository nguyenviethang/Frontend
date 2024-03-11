### lap trinh fron end
lo trinh:
HTML-> CSS -> SCSS -> responsive -> Bootstrap -> Cut Templates -> Js -> React JS.
### lo trinh back end
PHP basic -> PHP OOP -> MySQL -> PHP+ MySQL -> Mock Project MVC -> Laravel -> Magento -> Git.

### so sánh SSR và CSR

SSR (Server-Side Rendering) và CSR (Client-Side Rendering) là hai phương pháp chính để hiển thị nội dung web trong ứng dụng phía máy khách.

Server-Side Rendering (SSR): Khi sử dụng SSR, trình duyệt không cần chờ đợi cho toàn bộ mã HTML được tạo ra. Thay vào đó, máy chủ tạo ra HTML từ phía máy chủ và gửi nó trực tiếp đến trình duyệt. Điều này có nghĩa là người dùng sẽ thấy nội dung ngay khi họ truy cập trang, vì không có thời gian chờ đợi lâu để tải dữ liệu.

Client-Side Rendering (CSR): Trong trường hợp CSR, trình duyệt tải một trang trống ban đầu và sau đó sử dụng JavaScript để tải dữ liệu và tạo ra nội dung của trang. Điều này có thể tạo ra trải nghiệm trực quan tốt hơn sau khi tải xong, vì nó cho phép các tương tác động và cập nhật nhanh chóng. Tuy nhiên, thời gian ban đầu để tải trang có thể lâu hơn do phải tải mã JavaScript và dữ liệu từ máy chủ.

So sánh:

Hiệu suất ban đầu: SSR có thể cung cấp trang web nhanh hơn ban đầu vì nó trả về nội dung ngay từ phía máy chủ. CSR thì thường cần thời gian để tải mã JavaScript và dữ liệu trước khi hiển thị nội dung.
Tương tác và động cơ của trang web: CSR cho phép tương tác nhanh chóng sau khi trang đã tải xong, vì việc cập nhật chỉ cần xử lý phía máy khách. SSR cần phải gửi yêu cầu đến máy chủ để cập nhật nội dung, có thể làm chậm quá trình này.
Tùy thuộc vào yêu cầu cụ thể của ứng dụng, lựa chọn giữa SSR và CSR có thể được thực hiện để đạt được trải nghiệm người dùng tốt nhất. Một số ứng dụng sử dụng cả hai kỹ thuật, được gọi là "Hybrid Rendering", để tận dụng lợi ích của cả hai phương pháp
### cac loai the HTML
- thẻ đủ và thẻ rỗng
- thẻ block và inline

 + thẻ đủ: có thẻ mở và thẻ đóng
 + thẻ rỗng: chỉ có thẻ mở

#### thẻ block
+ width: 100%
+ mỗi thẻ block nằm trên 1 dòng, 2 thẻ block không thể nằm chung một dòng.

#### the inline
+ width = nội dung thẻ
+ mỗi thẻ inline liên kề các thẻ inline khác được xếp sát nhau, hai thẻ inline có thể nằm chung 1 dòng.

### cáu tạo thẻ HTML
< tagname atributes="values"> content </ tagname >  -> thẻ đủ
< tagname atributes="values">

### XHTML ( nói đơn giản là bộ quy tắc viết HTML trở nên chặt chẽ)
XHTML (Extensible Hypertext Markup Language) là một ngôn ngữ đánh dấu dựa trên HTML, nó kết hợp các tính năng của HTML với cú pháp XML (eXtensible Markup Language). XHTML được thiết kế để làm cho HTML trở thành một ứng dụng của XML, cho phép nó có cấu trúc nghiêm ngặt hơn và dễ dàng phân tích hơn.

Cú pháp của XHTML tương tự HTML, nhưng nó yêu cầu các quy tắc nghiêm ngặt hơn về cú pháp, bao gồm:

Viết hoa chữ cái: Tất cả các thẻ và thuộc tính phải viết hoa chữ cái.

Thẻ phải được đóng: Mọi thẻ mở phải có thẻ đóng tương ứng.

Thuộc tính phải có giá trị: Tất cả các thuộc tính phải có giá trị, và giá trị phải được đặt trong dấu nháy kép.



 ### HTML semantic
 Semantic HTML là việc sử dụng các thẻ HTML để tạo ra cấu trúc của trang web một cách có ý nghĩa, mô tả được ý nghĩa của nội dung. Các thẻ semantic giúp cho việc hiểu cấu trúc và nội dung của trang web trở nên rõ ràng hơn cho cả người đọc và các công cụ máy tính (như công cụ tìm kiếm, trình đọc màn hình cho người khuyết tật, vv.).

Một số ví dụ về thẻ semantic HTML:

<header>: Định nghĩa phần đầu của trang web hoặc phần đầu của một phần tử con.
<nav>: Chứa các liên kết điều hướng trang web hoặc một phần của nó.
<main>: Chứa nội dung chính của trang.
<section>: Định nghĩa các phần khác nhau của nội dung trong một trang.
<article>: Đánh dấu một phần tử chứa một bài viết hoặc một nội dung độc lập.
<aside>: Định nghĩa một phần của trang web không liên quan trực tiếp đến nội dung chính.
<footer>: Chứa thông tin cuối trang như thông tin liên hệ hoặc thông tin về tác giả.
Sử dụng các thẻ semantic giúp trình duyệt và các công cụ khác có thể hiểu và diễn giải nội dung của trang web một cách chính xác hơn. Điều này có thể cải thiện trải nghiệm người dùng và tối ưu hóa SEO bởi vì công cụ tìm kiếm có thể hiểu được cấu trúc và nội dung của trang web một cách tốt hơn.


## cấu tạo chung của thẻ HTML
- thẻ block không cần quan tâm đến thuộc tính(không phải là tất cả) ví dụ: <div></div>, <h1></h1>, <header>, <nav>...
- tất cả các thẻ html đều sẽ có 2 thuộc tính: class(90% dùng thẻ này), id ->dùng để css
- Mỗi thẻ HTML sẽ có css mặc định của trình duyệt nhưng độ ưu tiên thấp

### cach viet nhanh nhieu the giong nhau:
ví dụ yêu cầu tạo 5 thẻ h5 có nội dung giống nhau
#### Cách 1:
B1: h5*5 --> ấn phím tab
B2: di chuyển con trỏ đến phần content và ấn tổ hợp phím ctrl + alt + mũi tên xuống --> ghi nội dung
#### cách 2:
B1: tạo ra thẻ 1 thẻ h5 với nội dung
B2: ấn 4 LẦN tổ hơp phím shift + alt + mũi thên xuống để nhân bản 4 thẻ nàm ngày phía dưới

## Các thẻ html 5

- header
- footer
- main
- nav
- section
- article
- aside
- figure và figcaption
- time

## Thẻ chèn liên kết (a = anchor)

<a href="link">Text</a>

`#` => Hash => Phía client

target

- `_blank` => mở tab mới
- `_self` => mở tab hiện tại




