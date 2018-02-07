# Ghi chép cách cấu hình cơ bản để sử dụng osTicket.

## 1. Quản lý thông tin về các đầu mục hỗ trợ trong osTicket.

Để xem thông tin về các đầu mục và quản lý thông tin về các đầu mục hỗ trợ chúng ta làm như sau. Lưu ý quản lý thông 
tin về các đầu mục hỗ trợ cần được đăng nhập dưới quyền admin.

- Đăng nhập osTicket với quyền admin sau đó chọn `Admin Panel ` :

![admin-panel](/images/admin-panel.png)

- Chọn mục `Manage` :

![manage](/images/manage.png)

- Tại đây chúng ta có thể thấy được các thông tin về những đầu mục hỗ trợ , trạng thái của các đầu mục này, độ ưu tiên cũng như bộ phận đảm nhiệm giải quyết các ticket.

### 1.1. Thêm một đầu mục hỗ trợ mới.

- Để thêm thông tin về một đầu mục hỗ trợ mới chúng ta chọn `Add new help topic` :

![add-help-topic](/images/add-help-topic.png)

- Sau đó điền thông tin cần thiết như sau :

![add-help-topic-1](/images/add-help-topic-1.png)

- Chọn team sẽ giải quyết các vấn đề liên quan đến đầu mục này (Phần này sẽ nói rõ hơn ở phần 1.2. Có thể tạm hiểu ở đây chúng ta cần chọn team giải quyết, 
trong team này có thể có một hoặc nhiều user dành cho nhiều người hỗ trợ được nhận các tiket từ đầu mục này) :

![add-help-topic-2](/images/add-help-topic-2.png)

### 1.2. Thêm một team/group mới để hỗ trợ khách hàng.

- Chọn `Admin Panel` :

![admin-panel](/images/admin-panel.png)

- Sau đó chọn phần `Agents` rồi chọn `Teams` :

![1-2-1](/images/1-2-1.png)

- Chọn Add New Team :

![1-2-2](/images/1-2-2.png)

- Điền các thông tin như sau :

![1-2-3](/images/1-2-3.png)

=> Như thế đẫ tạo thành công một team để support , bây giờ chúng ta cần tạo các user dành cho các nhân viên trong công ty và thêm vào từng team cụ thể để hỗ trợ người dùng một cách hiệu quả nhất.

### 1.3. Thêm bộ phận để hỗ trợ khách hàng.

- Chọn `Admin Panel` :

![admin-panel](/images/admin-panel.png)

- Chọn `Agents` sau đó chọn `Departments` :

![1-3-1](/images/1-3-1.png)

- Chọn `Add new Department` :

![1-3-2](/images/1-3-2.png)

- Điền thôn tin cấu hình :

![1-3-3](/images/1-3-3.png)


### 1.4. Thêm user mới và thêm vào group để nhận ticket từ khách hàng.

- Chọn `Admin Panel` :

![admin-panel](/images/admin-panel.png)

- Sau đó chọn `Agents` rồi chọn `Add new agent` :

![1-4-1](/images/1-4-1.png)

- Cấu hình tài khoản như sau :

![1-4-2](/images/1-4-2.png)

- Cấu hình password cho tài khoản như sau :

![1-4-3](/images/1-4-3.png)

- Cấu hình Department :

![1-4-5](/images/1-4-5.png)

- Thêm User vào Team tương ứng :

![1-4-4](/images/1-4-4.png)

=> Như thế là đã cấu hình thành công đối với người quản trị , phần tiếp theo sẽ là bài hướng dẫn tạo user cho khách hàng, tạo mới ticket và cách reply khách hàng từ bộ phận hoox trợ.