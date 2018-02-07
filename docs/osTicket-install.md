# Hướng dẫn cài đặt osTicket.

## 1. Yêu cầu máy chủ và phân hoạch IP.

- Ở bài này mình chỉ nêu ra các bước thực hiện cài đặt trên máy chủ CentOS 7.

![ip-planning](/images/ip-planning.png)

## 2. Các bước cài đặt.

- Cài đặt gói `epel-release`

    ```sh
    yum -y install epel-release
    ```

- Cài đặt httpd, mysql và các gói cần thiết khác :

    ```sh
    yum -y install firewalld mariadb mariadb-server httpd php unzip php-mysql php-imap php-xml php-mbstring php-pecl-apcu php-pecl-zendopcache php-intl php-gd
    ```

- Tải bản osTicket (osTicket Core, v1.10.1) tại [đây](http://osticket.com/download)

- Dùng sFTP để chuyển file vừa tải đến thư mục `/opt` .

- Sau đó dùng `unzip` để giải nén :

    ```sh
    cd /opt
    unzip osTicket-v1.10.zip
    ```

- Coppy thư mục `upload` tới `/var/www/html` :

    ```sh
    cp -rp upload /var/www/html/helpdesk
    ```

- Phân quyền cho thư mục `helpdesk` :

    ```sh
    chown -R apache:apache /var/www/html/helpdesk
    ```

- Chuyển đến thư mục helpdesk và cấu hình file config :

    ```sh
    cd /var/www/html/helpdesk
    cp include/ost-sampleconfig.php include/ost-config.php
    ```

- Phân quyền cho file config :

    ```sh
    chmod 0666 include/ost-config.php
    ```

- Khởi động `httpd` và `mariadb` :

    ```sh
    systemctl start httpd
    systemctl enable httpd
    systemctl start mariadb
    systemctl enable mariadb
    ```

- Tạo db lưu trữ :

    ```sh
    mysql -uroot -p
    mysql> CREATE DATABASE ost;
    mysql> GRANT ALL PRIVILEGES ON ost.* TO "ostusr"@"localhost" IDENTIFIED BY "password";
    mysql> FLUSH PRIVILEGES;
    mysql> exit
    ```

- Tắt firewalld :

    ```sh
    systemctl stop firewalld
    ```

- Truy cập vào đường dẫn http://192.168.30.121/helpdesk để điền các thông số về DB .

-  Hết - good luck for you.

# Tham khảo :

- https://mangolassi.it/topic/11624/installing-osticket-1-10-on-centos-7/2