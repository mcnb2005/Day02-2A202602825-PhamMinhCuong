# 01.2 — Top 3 Problem Cards: FreshBox

**Phạm Minh Cương — 2A202602825**

Các card là bản phân tích đề xuất từ ý tưởng nhóm. Workflow và impact cần xác nhận với người dùng. Mọi ngưỡng số dưới đây là **mục tiêu pilot**, không phải kết quả đã đo.

## Card 1 — Không nhớ lúc cất thực phẩm

| Trường | Nội dung |
|---|---|
| Problem một câu | Người quản lý tủ lạnh không có bản ghi đáng tin về lúc cất từng hộp, nên phải tìm, nhớ hoặc hỏi lại khi cần kiểm tra. |
| Actor | Người tự chuẩn bị và quản lý thực phẩm trong một tủ lạnh gia đình/nhà ở chung; nhóm người dùng mục tiêu còn cần xác nhận. |
| Bối cảnh | Khi cất một món và khi quyết định món nào cần kiểm tra trước. |
| Current workflow | Cất hộp → ghi nhãn hoặc ghi nhớ → sau đó tìm lại → đọc nhãn/hỏi người khác → quyết định cách xử lý → cập nhật nếu có. |
| Bottleneck | Thiếu ghi nhận tại thời điểm cất; đến lúc cần dùng mới tái dựng thông tin. |
| Impact giả định | Tốn công tìm/hỏi; có thể quên món. Chưa có số đo lãng phí hoặc tần suất. |
| Success metric | ≥95% lượt cất thử nghiệm có bản ghi đúng ID và mốc; trung vị tra cứu ≤15 giây và giảm ≥30% so với cách hiện tại. Baseline chưa đo. |
| Non-AI alternative | Dán nhãn ngày giờ + một khu vực để món cần chú ý; lịch nhắc do người dùng đặt. |
| AI hypothesis | AI có thể gợi ý tên từ nhãn để giảm nhập liệu, nhưng việc ghi giờ và nhắc không cần AI. |
| Quick gut | Rule/IoT cho MVP; AI là tùy chọn được thử riêng. |
| Boundary | Không suy ra hạn dùng hay an toàn từ thời điểm cất; người dùng xác nhận món và mốc. |

## Card 2 — Lẫn thời điểm cất với thời điểm mở

| Trường | Nội dung |
|---|---|
| Problem một câu | Người dùng nhớ ngày mua hoặc ngày cất nhưng không ghi ngày mở bao bì, làm thông tin theo dõi thiếu mốc quan trọng. |
| Actor | Người dùng chai/hộp thực phẩm đóng gói nhiều lần. |
| Bối cảnh | Mở lần đầu, dùng một phần, rồi đặt lại vào tủ. |
| Current workflow | Mua/cất → mở bao bì → dùng một phần → cất lại → đọc hướng dẫn và cố nhớ lần mở. |
| Bottleneck | Thao tác mở không đồng nghĩa với sự kiện lấy/đặt vào khung; cảm biến hiện diện không xác định được lúc mở. |
| Impact giả định | Phải hỏi/đoán; nhắc việc dựa trên sai mốc. Chưa có dữ liệu người dùng. |
| Success metric | 100% hồ sơ thử có trường ngày cất/ngày mở tách biệt; khi chưa biết ngày mở phải giữ “chưa rõ”; 0 lần tự gán ngày mở từ cảm biến. |
| Non-AI alternative | Nhãn ngày mở viết tay và hướng dẫn trên bao bì. |
| AI hypothesis | OCR có thể đọc hướng dẫn trên nhãn nếu người dùng cung cấp ảnh rõ; vẫn phải xác nhận, không đoán ngày mở. |
| Quick gut | Rule + thao tác “Đã mở”; không cần Agent. |
| Boundary | Lấy ra rồi đặt lại cùng món không làm mới lịch sử ban đầu. |

## Card 3 — Ngại duy trì app nhập tay

| Trường | Nội dung |
|---|---|
| Problem một câu | Người quản lý thực phẩm có thể ngừng dùng danh sách điện tử vì mỗi lần cất/lấy phải nhập và sửa nhiều trường. |
| Actor | Người đã hoặc đang thử ghi danh sách thực phẩm trên điện thoại. |
| Bối cảnh | Cất nhiều món, lấy món ra, đổi hộp hoặc dùng chung tủ. |
| Current workflow | Mở app → thêm tên → nhập mốc → lưu → dùng/lấy món → tìm lại mục → cập nhật trạng thái. |
| Bottleneck | Công duy trì danh sách diễn ra ở mỗi lần thay đổi vật phẩm. |
| Impact giả định | Danh sách cũ, nhắc sai món, người dùng bỏ theo dõi. Cần kiểm chứng trực tiếp. |
| Success metric | Trung vị nhập/xác nhận ≤10 giây mỗi món và giảm ≥30% so với app nhập tay; ≥90% thay đổi tồn có trạng thái đúng khi kiểm cuối phiên. |
| Non-AI alternative | Nhãn đơn giản hoặc app có ít trường, không bắt nhập toàn bộ tủ. |
| AI hypothesis | OCR/tên gợi ý chỉ đáng thêm nếu tổng công nhập + sửa thấp hơn cách chọn tên thủ công. |
| Quick gut | Thử Rule trước; chỉ thêm Workflow có AI khi phép so sánh cho thấy có lợi. |
| Boundary | Không tự gán danh tính từ một thay đổi trọng lượng chung cho nhiều món. |

## Chuẩn bị trình bày

Card đề xuất trình bày là **F1**, vì phù hợp trực tiếp với concept được cung cấp. Học viên vẫn cần tự chọn, kể ví dụ thật và tự đặt câu hỏi challenge. Chưa có lời pitch hoặc phản biện nhóm được ghi nhận.

[Workflow cho ba card](03-workflows.md).
