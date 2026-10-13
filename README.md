# Bài 4 : Xây dựng quy trình lưu nhật ký hệ thống


## 1. So sánh

- > ghi đè tệp cũ. Dùng khi muốn tạo báo cáo mới, ví dụ báo cáo riêng cho ca sáng.
  > 
- >> ghi thêm vào cuối tệp, giữ lại nội dung cũ. Dùng khi muốn lưu nhật ký liên tục.
  >> 
Nếu An dùng nhầm > cuối tháng, báo cáo 30 ngày trước sẽ bị ghi đè và mất.


## 2. Lựa chọn

Để theo dõi lỗi mới phát sinh, có thể dùng lệnh:

- Get-Content server.log -Tail 0 -Wait | Where-Object { $_ -match "ERROR" } | Add-Content daily_report.txt 
