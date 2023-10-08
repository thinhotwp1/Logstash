# Logstash
Config logstash for every service springboot
Link drive: https://drive.google.com/drive/folders/1Yj4JqtJvkBQz5C1t_mTLdkgyLyCf8w3B?usp=drive_link

## Yêu cầu đã cài đặt bộ 3 elk trên server trước

1. copy file logstash.conf vào etc/logstash/conf, có thể cấu hình dựa theo địa chỉ elasticsearch,
    tên %{appName} sẽ được cấu hình trong ứng dụng springboot
2. Thêm logback-spring.xml vào path /src/main/resources, thay đổi các cấu hình <destination>, <pattern> theo cấu hình muốn.

3. Chạy ứng dụng và kiểm tra index được thêm trên elasticsearch:
Run application kiểm tra ở cổng: http://localhost:9200/_cat/indices nếu có index "micro-%{appName}" thì đã thành công gửi log lên elasticsearch!