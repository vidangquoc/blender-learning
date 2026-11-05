# Quy trình sản xuất một cảnh Animation Story

> **Mục tiêu:** dùng một quy trình nhất quán để dựng từng cảnh trong Roblox Animation Story/short bằng Roblox Studio và Moon Animator 2. Ưu tiên kể chuyện, diễn xuất và nhịp cảnh trước độ mượt kỹ thuật.

## Tổng quan pipeline

Quy trình tham khảo gồm các giai đoạn sau. Đây không phải đường thẳng cứng nhắc: khi phát hiện vấn đề ở giai đoạn sau, có thể quay lại giai đoạn trước để sửa.

1. **Storyboard — Phác thảo câu chuyện**
2. **Layout — Dựng bố cục cảnh**
3. **Blocking — Dựng các pose chính**
4. **Spline / Refinement — Hoàn thiện chuyển động**
5. **Polish — Tinh chỉnh diễn xuất**
6. **Camera & Lighting — Hoàn thiện hình ảnh**
7. **Rendering & Editing — Xuất và dựng hậu kỳ**

## 1. Storyboard — Phác thảo câu chuyện

**Mục đích:** xác định điều gì xảy ra trong cảnh trước khi animate.

- Chia nội dung thành các hành động hoặc beat rõ ràng.
- Xác định nhân vật nào tham gia và mục tiêu của họ.
- Phác thảo các shot/góc máy dự kiến.
- Đánh dấu điểm bắt đầu, thay đổi, cao trào và kết thúc của cảnh.
- Chú ý nhịp hài, bất ngờ, cảm xúc hoặc combat nếu có.

**Đầu ra:** chuỗi hình phác thảo hoặc shot list ngắn, đủ để hiểu cảnh sẽ kể điều gì.

## 2. Layout — Dựng bố cục cảnh

**Mục đích:** xác định không gian và vị trí trước khi làm chuyển động chi tiết.

Trong Roblox Studio:

- Đặt môi trường, nhân vật, đạo cụ và các vật thể cần thiết.
- Xác định vị trí bắt đầu/kết thúc của nhân vật.
- Xác định hướng nhìn, hướng di chuyển và khoảng cách giữa các nhân vật.
- Đặt camera thử để kiểm tra bố cục và silhouette.
- Dùng proxy/blockout đơn giản nếu môi trường hoặc đạo cụ chưa hoàn thiện.

**Đầu ra:** scene có đủ thành phần và bố cục cơ bản; người xem có thể hiểu không gian và vị trí các nhân vật.

## 3. Blocking — Dựng các pose chính

**Mục đích:** kiểm tra diễn biến và nhịp hành động bằng các pose quan trọng, chưa tập trung làm mượt.

Trong Moon Animator 2:

- Tạo các key pose thể hiện rõ ý định hành động.
- Đặt keyframe tại các thời điểm quan trọng: bắt đầu, anticipation, hành động chính, reaction, recovery và kết thúc (tùy cảnh).
- Xác định vị trí và hướng của nhân vật trong từng beat.
- Dựng timing thô và xem lại ở tốc độ thực.
- Giữ pose đủ rõ để người xem hiểu hành động.

**Đầu ra:** bản blocking thô của toàn bộ cảnh/shot. Cảnh phải đọc được về hành động, bố cục và nhịp trước khi chuyển sang tinh chỉnh.

## 4. Spline / Refinement — Hoàn thiện chuyển động

**Mục đích:** biến chuyển động thô thành chuyển động có nhịp và liên tục.

- Thêm pose trung gian khi cần.
- Điều chỉnh timing, spacing và easing.
- Kiểm tra đường chuyển động (arcs), trọng lượng và thăng bằng.
- Sửa chuyển động giật, xuyên hình và chuyển pose thiếu tự nhiên.
- Kiểm tra sự phối hợp giữa thân, đầu, tay, chân và đạo cụ.
- Với walk/run có dịch chuyển, phối hợp chu kỳ bước chân với quãng đường và tốc độ để hạn chế foot sliding.

**Đầu ra:** chuyển động rõ ràng, liên tục và có trọng lượng phù hợp với phong cách.

## 5. Polish — Tinh chỉnh diễn xuất

**Mục đích:** tăng sức biểu cảm và độ hoàn thiện sau khi cấu trúc chuyển động đã ổn.

- Thêm anticipation, follow-through và overlap ở mức phù hợp.
- Tinh chỉnh hướng nhìn, đầu, bàn tay và tư thế thân.
- Bổ sung chuyển động phụ và reaction nhỏ.
- Điều chỉnh pose hold, nhịp dừng và nhấn nhá.
- Kiểm tra đạo cụ gắn với nhân vật; tránh tạo track chuyển động độc lập gây xung đột với Weld nếu đạo cụ chỉ cần đi theo limb.

**Đầu ra:** diễn xuất có chủ đích, dễ đọc và không có lỗi phụ nổi bật.

## 6. Camera & Lighting — Hoàn thiện hình ảnh

**Mục đích:** giúp người xem tập trung vào hành động và cảm xúc quan trọng.

- Chốt khung hình, góc máy, cỡ cảnh và hướng nhìn.
- Điều chỉnh camera movement nếu cảnh cần.
- Kiểm tra nhân vật/đạo cụ không bị khuất hoặc ra khỏi khung hình ngoài ý muốn.
- Bố trí ánh sáng và màu sắc phù hợp với không khí cảnh.
- Xem lại continuity giữa các shot: hướng di chuyển, vị trí, trục nhìn và ánh sáng.

**Đầu ra:** shot có bố cục rõ, camera phục vụ câu chuyện và hình ảnh nhất quán.

## 7. Rendering & Editing — Xuất và dựng hậu kỳ

**Mục đích:** ghép các shot thành short hoàn chỉnh.

- Xuất hoặc ghi lại từng shot theo quy trình phù hợp với công cụ đang dùng.
- Sắp xếp shot theo thứ tự câu chuyện.
- Điều chỉnh nhịp cắt và thời lượng shot.
- Thêm âm thanh, thoại, nhạc, hiệu ứng và subtitle khi cần.
- Xem toàn bộ short từ đầu đến cuối để kiểm tra nhịp kể chuyện.

**Đầu ra:** bản short có thể xem liên tục, có hình ảnh và âm thanh hoàn chỉnh.

## Cách áp dụng pipeline trong dự án Roblox

| Giai đoạn | Công cụ chính | Việc cần làm |
|---|---|---|
| Storyboard | Giấy, ảnh phác thảo, shot list | Chốt hành động và nhịp câu chuyện |
| Layout | Roblox Studio | Dựng scene, nhân vật, đạo cụ và camera thử |
| Blocking | Moon Animator 2 + Roblox Studio | Dựng pose chính và timing thô |
| Refinement | Moon Animator 2 | Thêm pose trung gian, sửa timing/spacing |
| Polish | Moon Animator 2 | Hoàn thiện acting, overlap và đạo cụ |
| Camera & Lighting | Roblox Studio + Moon Animator 2 | Chốt góc máy, camera movement và ánh sáng |
| Rendering & Editing | Công cụ ghi hình/dựng video | Ghép shot, âm thanh và hậu kỳ |

## Nguyên tắc làm việc

1. **Nội dung và diễn xuất là ưu tiên.** Kỹ thuật phục vụ câu chuyện, không thay thế câu chuyện.
2. **Blocking trước, polish sau.** Đừng mất nhiều giờ làm mượt một shot khi hành động hoặc nhịp cảnh còn chưa rõ.
3. **Dựng thô toàn cảnh trước khi hoàn thiện từng chi tiết.** Xem lại toàn bộ blocking để kiểm tra nhịp và continuity.
4. **Xem lại ở tốc độ thực.** Một pose đẹp khi đứng yên chưa chắc hoạt động tốt khi phát liên tục.
5. **Pipeline có thể lặp lại.** Nếu camera, layout hoặc hành động chưa ổn, quay lại sửa đúng giai đoạn liên quan.
6. **Lưu source riêng.** Giữ project Moon Animator và bản scene gốc; Animation ID đã publish không thay thế file nguồn có thể chỉnh sửa.

## Checklist hoàn thành một cảnh

- [ ] Người xem hiểu mục tiêu và hành động của cảnh.
- [ ] Layout, vị trí và hướng di chuyển nhất quán.
- [ ] Các pose chính đọc được và timing hợp lý.
- [ ] Chuyển động không giật hoặc trượt chân ngoài ý muốn.
- [ ] Nhân vật và đạo cụ không xuyên hình hoặc xung đột.
- [ ] Camera giữ được hành động quan trọng trong khung hình.
- [ ] Các shot nối với nhau hợp lý.
- [ ] Âm thanh và nhịp hậu kỳ hỗ trợ câu chuyện.
