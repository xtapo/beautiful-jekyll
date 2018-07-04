---
layout: post
title: Cài đặt Git và thiết lập ban đầu
image: /img/git-logo.png
date:   2018-07-02 03:00:00
categories: [github]
tags: [git, github]
permalink: /cai-dat-git-va-thiet-lap-ban-dau/
---

Để có thể sử dụng được Git, bạn phải cài ứng dụng Git vào máy tính để có thể sử dụng các dòng lệnh của Git vì toàn bộ quy trình làm việc với Git đều diễn ra các dòng lệnh (mặc dù ở Windows có một  số phần mềm sử dụng Git với GUI nhưng mình không đề cập ở serie này).

### Cài Git vào Linux
---
Nếu bạn đang sử dụng hệ điều hành Ubuntu/Debian thì có thể sử dụng lệnh sau để cài Git.

```$ sudo apt-get install git```

Hoặc lệnh sau để cài trên CentOS/Fedora/RHEL.

```$ yum install git```

### Cài Git vào Mac OS
---
Đối với Mac, bạn có thể sử dụng file installer tải tại địa chỉ http://git-scm.com/download/mac để cài đặt.

Sau khi cài đặt Git vào Windows, bạn sẽ cần mở ứng dụng Git Bash lên để bắt đầu sử dụng các dòng lệnh của Git.

### Thiết lập chứng thực cá nhân
---
Sau khi cài Git xong, việc đầu tiên bạn nên làm là khai báo tên và địa chỉ email vào trong file cấu hình của Git trên máy. Để làm điều này bạn sẽ cần sử dụng hai lệnh sau đây để thiết lập tên và email.

```
$ git config --global user.name "Quang Nhan"
$ git config --global user.email "contact@quangnhan.com"
```

Sau khi thiết lập xong, bạn có thể kiểm tra thông tin chứng thực trên user của bạn bằng cách xem tập tin `~/.gitconfig` (nhắc lại rằng dấu ~ nghĩa là thư mục gốc của user).

```
$ cat ~/.gitconfig
[user]
 name = Quang Nhan
 email = contact@quangnhan.com
```

Hoặc bạn cũng có thể dùng lệnh `git config --list` để ghi danh sách các thiết lập hiện tại mà bạn đã làm.

Như vậy là bạn đã xong bước ban đầu đó là cài đặt Git và thiết lập tên và email của mình vào Git để bắt đầu làm việc. Ở phần sau, mình sẽ hướng dẫn cách bạn tạo ra một local repository (kho chứa trên máy cá nhân) để xem Git hoạt động thế nào.

Nguồn: thachpham