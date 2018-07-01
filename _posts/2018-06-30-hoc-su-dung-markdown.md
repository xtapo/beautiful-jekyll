---
layout: post
title: Học cách sử dụng Markdown
date:   2018-06-30
categories: [Markdown]
tags: [Markdown, github, website]
permalink: /hoc-cach-su-dung-markdown/
---

## Vài nét về Markdown
---

Các ngôn ngữ Markdown đã được tạo ra vào năm 2004 bởi John Gruber với sự đóng góp đáng kể từ Aaron Swartz, với mục đích cho phép người "viết sử dụng, dễ viết các định dạng văn bản đơn giản dễ đọc, và tùy chọn chuyển đổi nó thành các mã XHTML hợp lệ (hoặc HTML)".

![Markdown](http://octodex.github.com/images/octdrey-catburn.jpg)

Lấy tín hiệu từ các công ước hiện có để đánh dấu lên văn bản đơn giản trong email như setext, ngôn ngữ được thiết kế để có thể đọc như-là, mà không nhìn như nó được đánh dấu với thẻ hoặc hướng dẫn định dạng, không giống như các văn bản đã được định dạng với một ngôn ngữ Markup , chẳng hạn như HTML, trong đó có thẻ rõ ràng và hướng dẫn định dạng. Markdown là một cú pháp định dạng cho văn bản có thể được đọc bởi con người và có thể dễ dàng chuyển đổi sang HTML.

Gruber đã viết một kịch bản Perl, Markdown.pl, mà chuyển đổi đầu vào văn bản được đánh dấu để hợp lệ, cũng như hình thành XHTML hay HTML và thay thế trái chỉ dấu ngoặc vuông góc ('<') và dấu và tài liệu tham khảo với các thực thể ký tự tương ứng của họ. Nó có thể được sử dụng như là một kịch bản độc lập, như là một plugin cho Blosxom hay Movable Type, hoặc như một bộ lọc văn bản cho BBEdit.

Markdown có kể từ khi được tái thực hiện bởi những người khác như là một module Perl có sẵn trên CPAN (Text :: Markdown), và trong một loạt các ngôn ngữ lập trình khác. Nó được phân phối theo một giấy phép BSD-style và được bao gồm, hoặc có sẵn như là một plugin cho một số hệ thống quản lý nội dung.

**Các Phần mềm sử dụng ngôn ngữ Markdown:**

Markdown được sử dụng trong GitHub, GitBook, Reddit, Diaspora, Stack Overflow, OpenStreetMap và các ứng dụng khác.

**Tệp tin**

Một tài liệu Markdown là một file văn bản với phần mở rộng là ```.md```. Bạn có thể mở tệp tin markdown bằng một trình soạn thảo bất kỳ trên máy tính của bạn.

## Các thẻ tiêu đề
---
Khi chúng ta bắt đầu viết một tài liệu markdown, chúng ta cần thêm một tiêu đề cho và một vài phần tiêu đề nhỏ hơn cho tài liệu.

Markdown hỗ trợ 2 kiểu viết tiêu đề tài liệu: Setext và ATX.
* Với kiểu Setext: ta sử dụng ký tự ```=``` và ```-``` gạch chân dưới tiêu đề, sử dụng cho 2 thẻ ```<h1>``` và ```<h2>```.
  ```
  Đây là thẻ H1
  ============

  Đây là thẻ H2
  ------------
  ```
  
* Với kiểu AXT sử dụng ký tự ```#``` để biểu diễn các thẻ tiêu đề từ ```h1``` tới ```h6```.
  ```
  #h1
  ##h2
  ...
  ######h6
  ```
  
* Bạn cũng có thể sử dụng 1 thẻ đóng ```#```:
  ```
  # Đây là thẻ h1 #
  ## Đây là thẻ h2 ##
  ### Đây là thẻ h3 ######
  ```
  
## Các thẻ liên kết
---
**Markdown hỗ trợ 2 kiểu chèn liên kết là: inline và refences.**
~~~
Khai báo trong [tên liên kết](link) 
~~~

Để tạo một liên kết nội tuyến, sử dụng một tập hợp các dấu ngoặc đơn ngay sau khung vuông đóng cửa các văn bản liên kết của. bên trong ngoặc, đặt URL mà bạn muốn liên kết đến thời điểm, cùng với một tiêu đề tùy chọn cho liên kết, bao bọc trong dấu ngoặc kép.

**Ví dụ:**
``` 
    [I'm an    inline-style link](https://www.google.com)
    [I'm an    inline-style link with title](https://www.google.com "Google's    Homepage")
    [I'm a reference-style link][Arbitrary case-insensitive reference text]
    [I'm a relative    reference to a     repository file](../blob/master/LICENSE)
```

Liên kết tham khảo theo phong cách sử dụng một bộ thứ hai của dấu ngoặc vuông, bên trong đó bạn đặt một nhãn lựa chọn của bạn để xác định link:
```
This is [an example][aa] reference-style link.

[aa]:    http://example.com/    "Optional Title    Here"

[google](http://www.google.com "google")
```
This is [an example](http://example.com/) reference-style link.

## Các thẻ hình ảnh
---
sử dụng ```![tên hình ảnh](đường dẫn, "tên ảnh")```
~~~
    #    Inline ![Alternative text](/path/to/img.jpg    "Optional    title")
    #    Reference ![Alternative    text][id]
    [id]:    url/to/image "Optional    title"
~~~    
Như bạn có thể nhận thấy, hình ảnh trong Markdown là rất tương tự như liên kết.

Sự khác biệt là:
* Các dấu ngoặc vuông phải được bắt đầu bằng một dấu chấm than
* Và bên trong chúng có thể có một số văn bản thay thế. Mô tả về hình ảnh, mà được hiển thị nếu hình ảnh không thể được nạp.

## Code và blocks
---
Có nhiều cách định dạng các đoạn code như sau:

* tab vào
~~~
Đây là chú thích tab
      Tab con bên trong
          bên trong nữa
~~~          
* Dùng ```
~~~
  Đây là chú thích trên ```1 dòng```.
~~~
Đây là chú thích trên ```1 dòng```.

* Cú pháp highlightingg
  * Dùng ~~~ + tên ngôn ngữ
  * hoặc dùng ``` + tên ngôn ngữ
  
  
## Thẻ Tables
``` 
    | Tables | Cột 2 | Cột 3 |
    |--|:--:|--:|
    | 0:2 | Căn giữa :- - - -: | Căn bên phải  - - -: |
    | 0:3 | 1:3 | 2:3 |
```

| Tables | Cột 2 | Cột 3 |
|--|:--:|--:|
| 0:2 | Căn giữa :- - - -: | Căn bên phải - - - : |
| 0:2 | 1:3 | 2:3 |

```
Markdown    |    Less    |    Pretty
---    |    :---:    |    ---
*Still*    |    `renders`    |    **nicely**
1    |    2    |    3
```

Markdown  | Less  |  Pretty
--- | :---: | ---
*Still* |	`renders` |	**nicely**
1 |	2 |	3
