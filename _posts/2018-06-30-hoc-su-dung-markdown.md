---
layout: post
title: Học cách sử dụng Markdown
date:   2018-06-30
categories: [Markdown]
tags: [Markdown, github, website]
permalink: /hoc-cach-su-dung-markdown/
---

## Vài nét về Markdown
![Markdown](http://octodex.github.com/images/octdrey-catburn.jpg)

Các ngôn ngữ Markdown đã được tạo ra vào năm 2004 bởi John Gruber với sự đóng góp đáng kể từ Aaron Swartz, với mục đích cho phép người "viết sử dụng, dễ viết các định dạng văn bản đơn giản dễ đọc, và tùy chọn chuyển đổi nó thành các mã XHTML hợp lệ (hoặc HTML)".

Lấy tín hiệu từ các công ước hiện có để đánh dấu lên văn bản đơn giản trong email như setext, ngôn ngữ được thiết kế để có thể đọc như-là, mà không nhìn như nó được đánh dấu với thẻ hoặc hướng dẫn định dạng, không giống như các văn bản đã được định dạng với một ngôn ngữ Markup , chẳng hạn như HTML, trong đó có thẻ rõ ràng và hướng dẫn định dạng. Markdown là một cú pháp định dạng cho văn bản có thể được đọc bởi con người và có thể dễ dàng chuyển đổi sang HTML.

Gruber đã viết một kịch bản Perl, Markdown.pl, mà chuyển đổi đầu vào văn bản được đánh dấu để hợp lệ, cũng như hình thành XHTML hay HTML và thay thế trái chỉ dấu ngoặc vuông góc ('<') và dấu và tài liệu tham khảo với các thực thể ký tự tương ứng của họ. Nó có thể được sử dụng như là một kịch bản độc lập, như là một plugin cho Blosxom hay Movable Type, hoặc như một bộ lọc văn bản cho BBEdit.

Markdown có kể từ khi được tái thực hiện bởi những người khác như là một module Perl có sẵn trên CPAN (Text :: Markdown), và trong một loạt các ngôn ngữ lập trình khác. Nó được phân phối theo một giấy phép BSD-style và được bao gồm, hoặc có sẵn như là một plugin cho một số hệ thống quản lý nội dung.

**Các Phần mềm sử dụng ngôn ngữ Markdown:**

Markdown được sử dụng trong GitHub, GitBook, Reddit, Diaspora, Stack Overflow, OpenStreetMap và các ứng dụng khác.

**Tệp tin**

Một tài liệu Markdown là một file văn bản với phần mở rộng là ```.md```. Bạn có thể mở tệp tin markdown bằng một trình soạn thảo bất kỳ trên máy tính của bạn.

## Các thẻ tiêu đề

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
