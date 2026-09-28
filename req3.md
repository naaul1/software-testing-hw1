# Requirement 3 - 15 test cases cho ấm đun nước Happy Cook HEK-17WF (đã chạy 14/15, TC03 Blocked)

## 0. Thông tin thiết bị

- Nhãn hiệu: Happy Cook
- Model: HEK-17WF
- Dung tích: 1,7 lít
- Năm mua: 2020 (đối chiếu lại năm sản xuất trên tem khi chụp ảnh)
- Số serial (che 4 ký tự giữa): sinh viên tự điền từ tem dưới đáy ấm
- Ảnh: 1 ảnh ấm + thẻ sinh viên trong cùng khung hình (sinh viên tự chụp, không dùng AI).

## 1. Bảng 15 test cases

| ID | Mục tiêu (Objective) | Đầu vào (Input) | Các bước (Steps) | Kết quả mong đợi (Expected) | Thực tế (Actual) | Verdict |
|----|----------------------|-----------------|------------------|-----------------------------|------------------|---------|
| TC01 | Đun sôi lượng nước định mức thì tự ngắt | Nước đến vạch MAX, nắp đóng, đặt đúng đế, cắm điện | 1. Đổ nước đến MAX. 2. Đóng nắp. 3. Đặt lên đế. 4. Bật công tắc. | Nước sôi, công tắc tự ngắt, đèn tắt. | Đúng như mong đợi. | Pass |
| TC02 | Tắt thủ công giữa chừng | Ấm đang đun | 1. Bật đun. 2. Gạt công tắc về OFF khi chưa sôi. | Dừng đun ngay, đèn tắt. | Đúng như mong đợi. | Pass |
| TC03 | Bảo vệ khi đun không có nước | Ấm rỗng, nắp đóng (có người giám sát, tắt ngay nếu quá nóng) | 1. Để ấm rỗng. 2. Bật công tắc. 3. Quan sát và tắt ngay. | Tự ngắt chống cháy, không chảy nhựa, không khét. | Không thực hiện vì nguy hiểm (không đun ấm rỗng). | Blocked |
| TC04 | Châm quá vạch MAX | Nước trên vạch MAX, nắp đóng | 1. Đổ quá MAX. 2. Đun đến sôi. 3. Quan sát vòi và nắp. | Ghi nhận nước có trào qua vòi/nắp hay không; trào vào đế điện là không đạt an toàn. | Đúng như mong đợi. | Pass |
| TC05 | Đun khi nắp mở | Nước định mức, nắp mở | 1. Đổ nước. 2. Mở nắp. 3. Bật đun và quan sát. | Ghi nhận hơi thoát và thời điểm tự ngắt (nắp mở có thể ngắt chậm hoặc không ngắt). | Đúng như mong đợi. | Pass |
| TC06 | Đun lại ngay sau khi vừa sôi | Ấm vừa tự ngắt, nước còn nóng | 1. Chờ ấm tự ngắt. 2. Bật lại công tắc ngay. | Công tắc không giữ (khóa nhiệt) hoặc ngắt lại rất nhanh. | Đúng như mong đợi. | Pass |
| TC07 | Đun với lượng nước ít (0,5 lít) | 0,5 lít nước đong bằng cốc, nắp đóng | 1. Đong 0,5 lít. 2. Đổ vào ấm. 3. Đun đến sôi. | Sôi và tự ngắt bình thường, không cạn nước. | Đúng như mong đợi. | Pass |
| TC08 | Đặt ấm lệch khỏi tâm đế | Ấm đặt lệch tâm đế 360, có nước | 1. Đặt ấm lệch. 2. Bật công tắc. | Không vào điện hoặc đèn không sáng (tiếp xúc kém thì không đun). | Đúng như mong đợi. | Pass |
| TC09 | Rót nước sau khi sôi | Ấm vừa sôi | 1. Nhấc ấm khỏi đế. 2. Rót ra cốc. | Vòi chảy đều, thân không rò, tay cầm cầm được để rót. | Đúng như mong đợi. | Pass |
| TC10 | Tay cầm và vỏ khi sôi | Ấm vừa sôi | 1. Quan sát và chạm vào tay cầm. 2. Chạm nhanh vỏ. | Tay cầm cầm được bình thường, vỏ nóng nhưng không gây bỏng khi chạm nhanh. | Đúng như mong đợi. | Pass |
| TC11 | Dây điện và phích cắm | Quan sát + sau 1 lần đun | 1. Kiểm tra dây và phích. 2. Sờ dây/phích sau khi đun. | Dây nguyên vẹn, phích và dây không nóng bất thường. | Đúng như mong đợi. | Pass |
| TC12 | Đèn báo trạng thái | Các trạng thái đun/ngắt/nhấc | 1. Quan sát đèn khi bật. 2. Khi sôi ngắt. 3. Khi nhấc khỏi đế. | Đèn sáng khi đun, tắt khi ngắt và khi nhấc ra. | Đúng như mong đợi. | Pass |
| TC13 | Nhấc ấm khỏi để giữa chừng | Ấm đang đun | 1. Bật đun. 2. Nhấc ấm khỏi đế khi chưa sôi. | Dừng đun ngay, đèn tắt. | Đúng như mong đợi. | Pass |
| TC14 | Dung tích thực tế tại vạch MAX duy nhất | Thể tích nước 1,7 lít (bằng dung tích danh định trên tem) | 1. Đong đúng 1,7 lít. 2. Đổ vào ấm. 3. Đối chiếu mực nước với vạch MAX. | Mực nước ngang đúng vạch MAX, sai lệch không đáng kể. | Đúng như mong đợi. | Pass |
| TC15 | Độ bền khớp nắp và lòng ấm | Thao tác tay, quan sát mắt thường | 1. Mở/đóng nắp 10 lần. 2. Mở nắp hết cỡ xem có giữ được không, đóng có khớp chắc không. 3. Kiểm tra bản lề và mép nắp. 4. Kiểm tra lòng ấm (rỉ, sứt, cặn, đổi màu). | Nắp đóng mở trơn, khớp chắc, không lỏng và không bung; lòng ấm không rỉ và không sứt. | Đúng như mong đợi. | Pass |

## 2. Ghi chú

- Các case [edge] (TC04, TC05, TC06, TC08) là ứng viên cho mục ">=3 edge case AI bỏ sót" (G9.3); đối chiếu với output AI trong biểu mẫu [AI-02] rồi chốt.
- Đã chạy 14/15 case, mọi chức năng đúng như mong đợi. TC03 Blocked: không thực hiện vì nguy hiểm, không bịa kết quả.
- Quay >=5 video (mỗi video <=60s) có giọng thuyết minh của chính sinh viên; tải lên YouTube unlisted rồi dán link vào report.
