---
title: "Hệ Thống Phân Tán"
date: "2025-04-28"
updated: "2025-04-28"
categories:
  - "Ứng dụng phân tán"
  - "Tìm hiểu"
  - "Phạm Kim Thành"
coverImage: "/4k.jfif"
coverWidth: 16
coverHeight: 9
excerpt:
---

## 1. Hệ thống phân tán là gì?

Hệ thống phân tán (**Distributed System**) là tập hợp nhiều máy tính độc lập được liên kết với nhau, phối hợp hoạt động như một hệ thống duy nhất đối với người dùng. Mỗi máy tính trong hệ thống có thể thực hiện các nhiệm vụ riêng biệt, nhưng chung quy lại nhằm mục tiêu tối ưu hóa hgitiệu năng, độ tin cậy và khả năng mở rộng.

**Ví dụ:**  
- Hệ thống máy chủ Google Search: dữ liệu được lưu trữ và xử lý phân tán trên hàng triệu máy chủ.  
- Ứng dụng lưu trữ đám mây như Dropbox, Google Drive.

## 2. Các ứng dụng của hệ thống phân tán

Hệ thống phân tán được ứng dụng rộng rãi trong rất nhiều lĩnh vực như:
- **Công nghệ thông tin:** Cloud Computing (AWS, Azure), Blockchain, Microservices.
- **Viễn thông:** Hệ thống mạng điện thoại di động.
- **Tài chính:** Giao dịch ngân hàng trực tuyến, hệ thống thanh toán toàn cầu.
- **Giải trí:** Netflix, Spotify - truyền phát nội dung đa phương tiện.
- **Sản xuất công nghiệp:** Điều khiển nhà máy thông qua các mạng cảm biến.


## 3. Các khái niệm chính của hệ thống phân tán

### Giải thích các thuật ngữ:

- **Scalability (Khả năng mở rộng):**  
  Khả năng hệ thống tiếp tục hoạt động hiệu quả khi quy mô tăng (nhiều người dùng, nhiều dữ liệu hơn).

- **Fault Tolerance (Khả năng chịu lỗi):**  
  Khả năng hệ thống tiếp tục hoạt động ngay cả khi một hoặc nhiều thành phần gặp sự cố.

- **Availability (Độ sẵn sàng):**  
  Xác suất hệ thống luôn sẵn sàng để phục vụ người dùng tại mọi thời điểm.

- **Transparency (Tính trong suốt):**  
  Người dùng không cần biết hệ thống vận hành ra sao, chỉ cần trải nghiệm dịch vụ như một hệ thống duy nhất.

- **Concurrency (Tính đồng thời):**  
  Nhiều tiến trình có thể được thực thi cùng lúc mà không làm sai lệch kết quả cuối cùng.

- **Parallelism (Tính song song):**  
  Các tác vụ được chia nhỏ và xử lý đồng thời trên nhiều máy khác nhau.

- **Openness (Tính mở):**  
  Hệ thống cho phép tích hợp, mở rộng dễ dàng với các thành phần mới.

- **Vertical Scaling (Mở rộng theo chiều dọc):**  
  Tăng cường khả năng xử lý của một máy (nâng cấp CPU, RAM).

- **Horizontal Scaling (Mở rộng theo chiều ngang):**  
  Thêm nhiều máy mới vào hệ thống để xử lý khối lượng công việc.

- **Load Balancer (Cân bằng tải):**  
  Phân phối đều yêu cầu công việc giữa các máy chủ để tránh quá tải.

- **Replication (Sao lưu nhân bản):**  
  Tạo nhiều bản sao của dữ liệu nhằm tăng độ tin cậy và giảm thời gian truy xuất.

### Ví dụ minh họa:

Giả sử hệ thống bán hàng trực tuyến như Shopee, Lazada:  
- Khi nhiều người cùng truy cập đặt hàng (Concurrency), hệ thống cần mở rộng bằng cách thêm máy chủ mới (Horizontal Scaling).  
- Các đơn hàng được lưu nhiều bản sao ở nhiều địa điểm (Replication) để bảo vệ dữ liệu.  
- Nếu một server lỗi (Fault Tolerance), hệ thống sẽ chuyển yêu cầu sang server khác thông qua Load Balancer.


## 4. Kiến trúc của hệ thống phân tán

### Các mô hình kiến trúc phổ biến:

1. **Client-Server Architecture:**  
   Người dùng gửi yêu cầu từ client và server phản hồi. Ví dụ: Gmail, Facebook.

2. **Three-tier Architecture:**  
   Gồm 3 tầng: giao diện người dùng (client) - xử lý logic (application server) - lưu trữ dữ liệu (database server).

3. **Peer-to-Peer (P2P) Architecture:**  
   Các máy vừa là client vừa là server cho nhau. Ví dụ: mạng BitTorrent.

4. **Microservices Architecture:**  
   Các thành phần dịch vụ nhỏ, độc lập được triển khai và vận hành riêng biệt. Ví dụ: hệ thống Netflix, Amazon.

### Ví dụ minh họa:

![Ví dụ kiến trúc hệ thống phân tán](https://upload.wikimedia.org/wikipedia/commons/9/97/Distributed_computing.svg)  
*(Hình ảnh: Mô hình hệ thống phân tán với nhiều máy chủ xử lý song song và đồng bộ dữ liệu.)*

