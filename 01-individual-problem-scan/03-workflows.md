# 01.3 — Workflow trước và sau: FreshBox

**Phạm Minh Cương — 2A202602825**

Đây là workflow giả thuyết để quan sát và thử nghiệm. Chưa có thời gian thực đo.

## Card 1 — Ghi nhớ lúc cất

**Trước:**

```text
Cất hộp → Ghi nhãn hoặc ghi nhớ
→ Cần kiểm tra → Tìm hộp, đọc nhãn/hỏi lại [điểm nghẽn]
→ Quyết định xử lý → Cập nhật ghi chú nếu có
```

**Sau, MVP một vật phẩm trong một vùng theo dõi:**

```text
Đặt hộp → Cảm biến tạo sự kiện dự kiến và ghi thời điểm
→ Người dùng chọn/xác nhận ID món và lịch sử liên quan
→ Lưu bản ghi + lịch nhắc do người dùng xác nhận
→ Nhận nhắc kiểm tra → Xem thông tin và hướng dẫn phù hợp
→ Xác nhận đã lấy/đã dùng/đã bỏ hoặc tiếp tục theo dõi
```

Fallback: sự kiện thiếu hoặc mơ hồ → nhập tay; không nhận diện được món → giữ “chờ xác nhận”. Mốc “đặt vào” chỉ là quan sát của thiết bị; người dùng có thể cần bổ sung ngày nấu/mở trước đó.

## Card 2 — Theo dõi ngày mở

**Trước:**

```text
Mua và cất chai → Mở và dùng một phần → Đặt lại
→ Lần sau đọc hướng dẫn → Cố nhớ đã mở lúc nào [điểm nghẽn]
```

**Sau:**

```text
Chọn hồ sơ chai → Người dùng bấm “Đã mở” và xác nhận thời điểm
→ Lưu ngày mở riêng với ngày cất và thông tin nhãn
→ Rule nhắc theo mốc đã được người dùng chọn
→ Lấy/đặt lại vẫn dùng hồ sơ cũ
```

Fallback: không nhớ thời điểm mở → ghi “chưa rõ”, không tự lấy ngày hiện tại để thay thế. Xác nhận thay món mới mới được tạo hồ sơ mới.

## Card 3 — Giảm công cập nhật danh sách

**Trước:**

```text
Mở app → Tạo tên món → Nhập mốc → Lưu
→ Lấy món → Tìm mục tương ứng → Sửa trạng thái [công lặp lại]
```

**Sau:**

```text
Cảm biến phát hiện thay đổi → Gợi ý sự kiện
→ Người dùng xác nhận thêm/lấy/đặt lại/thay món
→ Cập nhật danh sách và lịch nhắc
→ Sự kiện không rõ → Chọn thủ công trước khi sửa lịch sử
```

AI OCR là nhánh thử nghiệm thêm khi đặt món: người dùng chụp nhãn → AI gợi ý tên/nội dung nhãn → người dùng kiểm tra. Nhánh này không cần thiết để MVP ghi giờ hoạt động.

## Trường hợp phải kiểm tra

| Tình huống | Cách thiết kế xử lý |
|---|---|
| Hai món vào cùng lúc | Báo cần xác nhận; không tự chia một sự kiện thành hai hồ sơ chắc chắn |
| Lấy rồi đặt lại cùng món | Giữ mốc gốc, thêm sự kiện; không làm mới thời gian đã lưu |
| Thay bằng món khác cùng trọng lượng | Người dùng xác nhận; không coi trọng lượng là định danh |
| Mất mạng | Lưu sự kiện cục bộ nếu phần cứng hỗ trợ; hiển thị lần đồng bộ cuối; không hứa đã nhận nhắc trên điện thoại |
| Mất nguồn/đồng hồ không đáng tin | Đánh dấu khoảng dữ liệu chưa biết; không dựng lại thời gian bị mất |
| Bỏ món khỏi khung nhưng vẫn trong tủ | Ghi “ra khỏi vùng theo dõi”, không tự kết luận đã ăn |
