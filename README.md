# Graphhopper-Tollbooth
Tài liệu này dùng để hướng dãn viết các Tag trạm thu phí trong OSM
## Cấu trúc của 1 tag:
- Cấu trúc của tag gồm 2 phần key và value. Key là phần đứng trước dấu `=`. Value là phần đứng sau dấu `=`
```
toll:<transportation mode> = <toll-value>
```
## Key:
- Là phần xác định loại xe bị thu phí khi qua trạm
- Luôn bắt đầu với `toll:` và ngay sau đó ( phần <transportation mode> ) là các phương tiện được liệt kê dưới dây:
+ Để trống : Tất cả các loại phương tiện, kể cả đi bộ.
+ `hgv` : Các loại xe tải, xe bán tải. Chưa có profile cho loại xe này.
+ `N2` : Các loại xe container nặng. Chưa có profile cho loại xe này.
+ `N3` : Các loại xe container nặng. Chưa có profile cho loại xe này.
+ `car` : Xe ôtô.
## Value:
- Chỉ có thể là `yes/no`.
- `yes` : Xe bị thu phí.
- `no` : Xe không bị thu phí, là mặc định cho tất cả các loại xe.
* Lưu ý, mỗi tag chỉ cho 1 loại xe.
## Sử dụng trên Map4dSDK:
- Sử dụng tương tự như tránh cầu,... với từ khóa `TOLL`.
## Ví dụ của tag:
- toll=yes : Thu phí tất cả các phương tiện đi qua kể cả đi bộ.
- toll:car=yes : Thu phí tất cả các xe ô tô đi qua.
