---
layout: post
title: Các đoạn mã Jekyll - Chỉ việc Copy và Paste!
image: /img/jekyll-logo.png
date:   2018-07-26 08:55:00
categories: [jekyll, thiết kế website]
tags: [thiết kế web, jekyll]
permalink: /cac-doan-ma-jekyll-chi-viet-copy-paste/
---
Jekyll có các đoạn mã trên website chính thức, nhưng không có sự phong phú. Đây là những đoạn mã mà bạn chỉ việc copy nó vào trang web jekyll của bạn là nó sẽ hoạt động ngay.

Tôi sẽ tạo một số đoạn mã Jekyll quan trọng để có thể chèn trực tiếp vào website Jekyll mà không cần phải chỉnh sửa hoặc chỉnh sửa một ít để chúng có thể hoạt động được.

### Jekyll Pagination
```
<!--
     Before implementing this Jekyll snippet make sure
     1. "plugins: jekyll-paginate" is added in the _config.yml file.
     2. for loop has "paginator.post" instead of "site.posts".
-->

{% if paginator.total_pages > 1 %}
<div class="wj-pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&laquo; Prev</a>
  {% else %}
    <span>&laquo; Prev</span>
  {% endif %}

  {% for page in (1..paginator.total_pages) %}
    {% if page == paginator.page %}
      <span class="active">{{ page }}</span>
    {% elsif page == 1 %}
      <a href="/">{{ page }}</a>
    {% else %}
      <a href="{{ site.paginate_path | prepend: site.baseurl | replace: '//', '/' | replace: ':num', page }}">{{ page }}</a>
    {% endif %}
  {% endfor %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Next &raquo;</a>
  {% else %}
    <span>Next &raquo;</span>
  {% endif %}
</div>
{% endif %}

<style>
.wj-pagination {
    text-align: center;
}
.wj-pagination a, .wj-pagination span {
    padding: 7px 18px;
    border: 1px solid #eee;
    margin-left: -2px;
    margin-right: -2px;
    background-color: #ffffff;
    display: inline-block;
}
.wj-pagination a:hover {    
    background-color: #f1f1f1;
    color: #333;
}
</style>
```
<script src="https://gist.github.com/sharu725/3c3a3971955d02e24f45edc864bf8172.js"></script>
