# học vè css

có 3 cách để nhứng css vào file html là inline, intenal, extenal

- chủ yếu(99%) dev dùng extenal, tức là tạo là một file style.css và link vào file html --> dễ maintain

cách viêt comment trong css: /\* \*/

- cụ thể là dùng tổ hợp phím Ctrl + / để biết một dòng css đang dùng thành comment
- nên comment nhiều để dễ maintain
  cấu trúc cú pháp:
  selector {
  property1: value1;
  property2: value2;
  }
  lưu ý:
- CSS có tính chất "Cascading", tức là các quy tắc có thể được ghi đè theo thứ tự ưu tiên.
- cách đặt tên id: class
  - tường minh(theo chức năng nhiệm vụ)
  - tiếng anh(đúng chính tả, dùng số ít và nhiều)
  - Viết thường, sử dụng gạch ngang, không nên dùng số
  - Nên bắt đầu bằng chữ cái
  - Cháp nhận: chữ cái thường, dấu gạch dưới, gạch ngang, số
  - Không được phép bắt đầu bằng số
  - Sử dụng danh từ
  - id trong 1 thẻ chỉ có 1, id rất ít khi dự dụng, vì nó không đẹp
  - class trong 1 thẻ html sẽ có nhiều (Mỗi class sẽ cách nhau bởi khoảng trắng)
  * inline > id > class > element HTML in css, NHƯNG tát cả điều này sẽ bị đánh bật bởi !important

take note: searching "cách dùng emmet html" để có những cách gõ nhanh html.

Nguyên tắc với selector ~

- Cùng cấp
- Nằm trong 1 cha
- Không phân biệt thứ tự liền sau

## tìm hiểu cách sự dung selector phổ biến

### cách 1: id, class, element HTML,

    Selector của lớp (Class Selector): .class-name { }
    Selector của ID: #id-name { }
    Selector phần tử HTML: element { }
    Selector kết hợp: element.class { }, element#id { }, elementA elementB { }, v.v.


    vi du về selector ket hợp:
    /* Selector phần tử kết hợp với class */
    element.class-name { /* Áp dụng cho các phần tử có class "class-name" là con của phần tử element */
    /* CSS properties */
    }

    /* Selector phần tử kết hợp với ID */
    element#id-name { /* Áp dụng cho phần tử có ID là "id-name" là con của phần tử element */
        /* CSS properties */
    }

.wrapper .container .content  /* dich: thằng container nằm trong wrapper, thằng content nằm trong thằng container và thằng wrapper*/

selector càng chi tiết thì độ ưu tiên càng cao
### cách 2: Selector con, người em, người anh:

    Chọn tất cả các phần tử: * { }
    Chọn tất cả các phần tử con của một phần tử: parent > child { }
    Chọn phần tử ngay kế tiếp: element + next-element { }
    Chọn phần tử cùng loại: element ~ sibling-element { }

ví dụ:

/_ Lựa chọn tất cả các phần tử <a> là con của các phần tử <li> _/
li > a {
/_ CSS properties _/
}

/_ Lựa chọn phần tử ngay kế tiếp sau phần tử <h2> _/
h2 + p {
/_ CSS properties _/
}

/_ Lựa chọn tất cả các phần tử em (siblings) của phần tử _/
h2 ~ p {
/_ CSS properties _/
}

### cách 3: Selector thuộc tính: chọn các element html có attribute cụ thẻ

ví dụ :

/_ Chọn tất cả các phần tử có thuộc tính "target" _/
[target] {
/_ CSS properties _/
}

/_ Chọn các phần tử có thuộc tính "target" với giá trị "blank" _/
[target="_blank"] {
/_ CSS properties _/
}

### cách 4: Selector pseudo-class và pseudo-element: Chọn các trạng thái hoặc phần tử cụ thể:

ví dụ:
/_ Selector pseudo-class cho phần tử khi rê chuột qua _/
a:hover {
/_ CSS properties _/
}

/_ Selector pseudo-element chọn phần tử đầu tiên trong một loại phần tử _/
p:first-of-type {
/_ CSS properties _/
}


###### - HOC VE TEXT
## cac gia tri mac dinh trong css
initial: mỗi thuộc tính đều có style gốc của nó, thì từ khóa này sẽ yêu cầu trình duyệt sử dụng style gốc của nó(thường là style gốc của trình duyệt).
Ví dụ: Style gốc của thuộc tính display là inline, cho mọi phần tử, còn style của trình duyệt set cho thẻ <div> là display: block. Nếu thẻ <div> được gán giá trị initial, thì nó sẽ nhận giá trị inline thay vì block.

inherit : Giống như tên gọi của nó là kế thừa, từ khóa này sẽ yêu cầu trình duyệt tìm kiếm giá trị của phần tử cha gần nó nhất, và sử dụng lại cái đó. Nếu như phần tử cha gần nhất của nó cũng có giá trị inherit thì nó sẽ tiếp tục tìm đi lên cho đến khi thấy giá trị nào đó. Nếu vẫn không có giá trị nào, nó sẽ sử dụng style của trình duyệt, nếu cũng không có, nó sẽ sử dụng style gốc của thuộc tính

unset : https://viblo.asia/p/ban-da-that-su-hieu-gia-tri-initial-inherit-va-unset-trong-css-RQqKLPwOK7z

tổng kết:
học selector, pseudo class+ pseudo element, text
