# rc-chat
@Nam Insider Project [Dev-ngu-vl] - Realtime chat with Database, Storage, M3 and Role


# RC Chat
- Realtime message sử dụng M3 Local Storage, cho phép CDN Media, quản lý vai trò, quyền hạn, gồm các kênh chat và máy chủ IS FUCKING DISCORD CLONE

# Technologi-a
- NodeJS: v20 and up
- Engine: Vue 13
- View: Embeded JavaScript
- Web render: CSR - SSR
- Database: MongoDB

# How realtime work ?
- Sử dụng WSS --> websocket gồm client A và B kết nối giao tiếp trong đó wss cho phép tạo ra C làm đường truyền cho A và B
- Vậy ta sẽ tạo ra R làm phòng chứa A B, C làm cầu nối 2 bên giao tiếp vì giới hạn của wss là dữ liệu 1 chiều
- WSS cho A B C thực hiện lắng nghe trên event, khi A B nằm trong R, R sẽ phát ra tính hiệu gọi là boardcast kích hoạt event, lúc này A B sẽ nhận được tín hiệu và cập nhật thông tin
- Trong 1 số trường hợp, A có thể đến B mà không qua C nếu không cần B phản hồi

<img width="938" height="456" alt="image" src="https://github.com/user-attachments/assets/67b4c17d-4715-4d68-944d-eb1c023947ce" />

# Why MongoDB?
- Vì t ngu SQL, non-sql user btw

# Storage
- Chứa gồm các ảnh, video, vv, ... sử dụng M3 storage nhưng chi phí thấp hơn, sử dụng Own Host (btw chỉ phải trả tiền điện)
- Giới hạn upload tối đa 100MB cho 1 media mặc định

# Embeder
- Dựa trên mẫu Embed debugger của Discord, hoạt động y hệt, gồm 3 loại:
  + Site embed: google.com, ...
  + Extension embed: cdn.gif/mp4/mp3/png/jpg/zip

# CDN
- Đéo có tiền nên làm bản rẻ tiền mất mạng, tạo ra 1 proxy để xử lý hình ảnh/video, sử dụng Cloudflare tunnel (idk ko bt có được không)

# Chat
- Chỉ có 1 Guild duy nhất vì chỉ có bọn này dùng chứ mấy XD
- Bao gồm Role + Channel + Send message + Chat loader

---------------
Sẽ còn update thêm
