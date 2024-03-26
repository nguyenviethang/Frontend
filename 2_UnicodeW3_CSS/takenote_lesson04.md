## với color css

khi tác động thành phần cha thì các thành phần con sẽ bị tác đông(trừ một số thẻ đậc biệt: như thẻ a)

- thẻ a không bị tác động khi dùng color câ cho HTML thành phần cha, bắt buộc phải css riêng cho thẻ a nếu muốn dùng css color

# với font-size css

## các đơn vị trong css

### nhóm tuyệt đối:

- px (pixel) = diểm ảnh
- pt (point) = 1.3 x pixel

note: tác động vào kích thước thành phần cha lớn nhất(thường là body HTML), tránh dùng vì web chạy trên nhiều thiết bị, dễ bị vỡ reponsive khi dùng giá trị tuyệt đối

- đa số các trình duyệt hiện nay setting fontsize là 16px

### nhóm tương đối

- em : tỷ lệ với font-size của các thành phần cha
  => 1 em = font-size của thành phần cha
- rem: tỷ lệ với font-size cảu trình duyệt (có thay đổi bằng selector)
  => 1 rem = font-size của selector html
- %: giống rem (khác vê tỷ lệ)
  => 100 % = font-size cau thành phần cha

note: em phụ thuộc vào cha gần nhất, rem phụ thuộc vào thẻ HTML(thẻ cha lớn nhất) --> nên ưu tiên dùng rem, chỉ dùng em vào một số tình huống cố định phụ thuộc vào thằng cha gần nhất của thuộc tính con.

Các đơn vị bên kích thước:

- vw
- vh

### với font-family css

một số font chữ đã đươc cài đặt sẵn trên wndow, ta có thể dùng ngay, ví dụ như tahoma, times new roman, Arial....

- với những tên font-family có khoảng trắng thì nên đặt trong nháy kép
  ví du: font-family: "Times New Roman";
- một font-family chữ thêm vào có thể ảnh hưởng đến font-size, font-weight vì kích thước, độ đậm nhật mỗi font khác nhau --> font chữ PHẢI setup trước
- với font-family, ta có thể để nhiều font trên một đoạn text
  ví dụ: font-family: "Times New Roman", Verdana, Tahoma, sans-serif; --> nếu không tìm thấy font times new roman trong file code thì chuyển sang áp dụng font verdana và tương tự cho đến hết.
- bất kì font nào chúng ta chọn thì cũng phải có đuôi san-serif(chữ không chân - 99%) hoặc serif(chữ có chân)
- chúng ta có thể vào https://fonts.google.com/ để chọn font đẹp cho web đang làm

- những css có chữ cái ban đầu bắt đầu bằng @ thì gọi chung là at-rule css
- để import font vào file css dùng
  @font-face {
  font-family: ; (tên có thể dùng bất cứ tên gì, nhưng nên dùng đúng tên font của đúng file font đang dùng)
  src: url('') (link đúng file font-family cần dùng)
  }

define nhiều kiểu font nhưng cùng tên font đó để dùng font weight chuẩn nhất của font giúp font có độ đậm nhât kiểu chữ ăn khớp nhất với font.
ví dụ: đặt tên font-family ở mỗi @font-face cùng một tên là "Open Sans"
@font-face {
font-family: "Open Sans";
src: url('../fonts/OpenSans-Light.ttf');
font-weight: normal;
}

@font-face {
font-family: "Open Sans";
src: url('../fonts/OpenSans-Regular.ttf');
font-weight: 500;
}

@font-face {
font-family: "Open Sans";
src: url('../fonts/OpenSans-Bold.ttf');
font-weight: bold;
}

và ta css:
body{
font-weight: bold
}
khi css cho body: chọn bold--> css sẽ chọn font-face thứ 3, khi chọn 500--> css sẽ chọn font-face thứ 2, nếu nhích lên 600 thì nó sẽ chọn font-face có fint-weight cao hơn(chính là font-face thứ 3)

độ đâmh nhật kéo dài từ 100 đên 900, độ đậm nhật tùy thuộc dèine của font chữ

## font-weight: độ đậm nhạt của nét chữ

giá trị trải từ 100 - 900, normal=100, bold=900

## font-style: nghiêng chữ

các giá trị: normal- bình thường, italic- nghiêng

## text-decoration: gạch chân chữ

các giá trị: none- bỏ gạch chân(hay dùng cho thẻ a), underline- gạch chân, overline- gạch trên, line-through: gạch giữa.

## line-height: độ giãn dòng của font-size:

ví dụ:  
line-height: 1.5;
font-size: 25px;

độ giãn dòng ở văn bản là 1.5 nhân cho 25px bằng 37.5px

## letter-spacing: khoảng cách giữa các ký tự

ví dụ: letter-spacing: 5px;

## word-spacing: khoảng cachs giữ các chữ

ví dụ: word-spacing: 2px;

## text-transform: chuyển sang chữ hoa
giá trị: lowercase- chuyến sang chữ thường, uppercase- chuyển sang chữ hoa, capitalize- viết hoa chữ cái đầu mỗi chữ
## text-indent: thụt dòng khi bắt đầu 1 đoạn văn bản
ví dụ: text-indent: 10px;


### chuyên đề backgound
## background-color: set màu nền
## background-image: set hinh nền
giá trị: url('link_local') 
ví dụ:
background-image: url('../images/ex01.jpg');

+ về độ ưu tiên: background-image > background-color, khi set thì nên set cả hai vì nếu bị lỗi hay web chưa load kip thì nó sẽ hiện thị background-color để tránh để người dùng hiểu là web bị lỗi
## background-repeat: tránh bị lặp ảnh
giá trị: no-repeat(99%)- không lặp ảnh nếu kích thước ảnh nhỏ hơn khung nhìn của web
repeat- lặp ảnh
repeat-x: lặp theo trục x
repeat-y: lặp theo trục y
## background-size: chỉnh kích thước của ảnh
các giá trị mặc đinh
100%: width=100%, height=auto
100% 100%: width=100%, height=100% theo đến phần tử html cuối cùng.
cover(99%): thường set nền cho khối nào đấy thì thường dùng giá trị này, ảnh sẽ nét và full 
contain: witdth=auto, height=100% (trường hợp này dùng cho lúc ảnh nền chúng ta quá dài)

## background-position: căn chỉnh background theo trục Oxy,
ví dụ: background-position: center center;
các giá trị: right, left, center, bottom, %
## background-attachment: Thuộc tính CSS đặt xem vị trí của hình nền được cố định trong khung nhìn hay cuộn với khối chứa nó
giá trị thường dùng: fixed
 ### lưu ý: ta có thể dùng mỗi background css để css cho thuộc tính html, không cần dùng các dạng backgroud có hậu tố như trên(trừ backgroud-size): 
 ví dụ:
    background: gold url('../images/ex01.jpg') no-repeat fixed;
    background-size: center;

### chuyên đề border
## border-width: độ dày của viền
ví dụ:     border-width: 1px;

## border-style: đặt kiểu nét đường viền cho bốn cạnh của phần tử(nết đứt, nết chấm)
ví dụ:
border-style: solid;

## border-color: đặt màu cho viền,
ví dụ: border-color: red;

## border-radius: bo góc cho viền
ví dụ: border-radius: 10px;

### lưu ý: ta có thể dùng mỗi border css để css cho thuộc tính html, không cần dùng các dạng border có hậu tố như trên:
ví dụ: border: 3px double;
