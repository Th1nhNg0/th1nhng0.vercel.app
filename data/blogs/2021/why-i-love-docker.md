---
title: Lý do mình yêu Docker
date: "2021-11-30"
tags: ["programming", "chatchit"]
draft: false
summary: Docker là một dự án mã nguồn mở giúp tự động triển khai các ứng dụng Linux và Windows vào trong các container ảo hóa.
images: ["static/images/2021/why-i-love-docker.jpg"]
layout: PostLayout
---

Có bao giờ các bạn chật vật với việc cài đặt các công cụ và service trên máy tính cá nhân hay server chưa? Ví dụ như: mysql, mongodb, redis, nginx, elasticsearch...

Nhớ hồi mới học lập trình, để cài được mysql database mình phải trải qua 7749 bước. Cài nhầm phiên bản làm mình phải uninstall cài lại tự đầu =)).

![mysql_step](/static/images/2021/mysql_step.png)

Với Docker, chỉ cần 2 dòng lệnh đơn giản là chúng ta đã có 1 server mysql chạy ngon lành

```bash
docker pull mysql
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql
```

**Vậy Docker là gì?**

> Docker là một dự án Open source giúp tự động triển khai các ứng dụng Linux và Windows vào trong các container ảo. (theo Wiki)

Để tìm hiểu thêm các bạn có thể search Google với từ khóa: [Docker](https://www.google.com/search?q=docker). Ở bài viết này, mình chỉ nói về những lợi ích của Docker đối với mình.

1. Chạy bất cứ ứng dụng, service nào, kể cả nó không hỗ trợ hệ điều hành bạn đang sử dụng.
2. Môi trường dev và môi trường production là như nhau. Sẽ không có trường hợp: máy em chạy được nhưng sao em deploy lên server nó lại lỗi =)).
3. Tiết kiệm thời gian. VD: khi máy tính gặp vấn đề, ta cài lại máy thì phải setup lại môi trường dev, rất tốn thời gian. Với Docker thì chỉ cần 1 lệnh.
4. Nhờ chạy cô lập trong container, các service sẽ không bị xung đột với nhau, tránh tính trạng lỗi là sập cả hệ thống.

Nói tóm lại, biết sử dụng Docker là điểm cộng rất lớn khi là một lập trình viên.