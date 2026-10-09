# Giáo trình mới: Làm phim hoạt hình phong cách Roblox bằng Blender

## Mục tiêu cuối cùng

Tự sản xuất video hoạt hình hoàn chỉnh để đăng YouTube bằng Blender: lấy nhân vật/cảnh/đạo cụ phong cách Roblox, chuẩn bị tài nguyên, làm animation, dựng cảnh, đặt camera, ánh sáng, âm thanh và render video. **Không học quy trình đưa animation trở lại Roblox Studio**, vì mục tiêu là làm phim chứ không phát triển game.

## Nguyên tắc học

- Học đến đâu tạo sản phẩm dùng được đến đó; ưu tiên thực hành trực tiếp trên nhân vật và cảnh thật.
- Không làm bài tập lý thuyết riêng nếu có thể học ngay trong một cảnh thực tế.
- Mỗi lượt chỉ hướng dẫn một bước ngắn; chờ người học xác nhận đã xong rồi mới tiếp tục.
- Ưu tiên quy trình nhẹ máy: low-poly/stylized assets, Eevee khi phù hợp, preview độ phân giải thấp, render thử từng đoạn.
- Không mặc định mọi tài nguyên tìm thấy trong Roblox đều được phép dùng để kiếm tiền. Chọn tài nguyên có quyền sử dụng phù hợp và tạo câu chuyện/animation nguyên bản.
- Chỉ đánh dấu bài DONE khi đã làm xong sản phẩm và đạt tiêu chí PASS.

## Roadmap

Trạng thái: 🟢 DONE · 🟡 IN PROGRESS · ⚪ TODO

### Giai đoạn A — Nền tảng Blender

1. 🟢 Làm quen giao diện, viewport và Timeline
2. 🟢 Transform, keyframe và playback
3. 🟢 Dope Sheet, Graph Editor cơ bản
4. 🟡 Rig/Bone/IK — đã thực hành skeleton cơ bản, constraint, IK target và pole; chỉ học bổ sung khi rig thực tế yêu cầu

### Giai đoạn B — Chuẩn bị tài nguyên Roblox

5. 🟡 Import character Roblox vào Blender
   - Xác định nguồn character và quyền sử dụng.
   - Chọn cách export phù hợp với nguồn tài nguyên.
   - Import file vào Blender và kiểm tra mesh, texture, scale, hướng và hierarchy.
   - Kiểm tra xem rig/Armature có được giữ lại hay không; không giả định file model nào cũng có rig.
6. ⚪ Import map, môi trường và đạo cụ
   - Đưa cảnh vào Blender, chia collection, đặt origin/scale và dọn object thừa.
   - Kiểm tra texture/material và sửa lỗi hiển thị.
   - Tối ưu scene để viewport và render không quá nặng.
7. ⚪ Chuẩn bị rig để animate
   - Xác định rig có thể dùng trực tiếp hay cần sửa/rig lại.
   - Kiểm tra bone hierarchy, pose, IK và mesh deformation.
   - Tạo bản sao dự phòng trước khi chỉnh rig.

### Giai đoạn C — Làm chuyển động

8. ⚪ Nguyên tắc animation thực dụng: pose, timing, spacing, silhouette
9. ⚪ Tạo pose key chính và chuyển động thử 3–5 giây
10. ⚪ Idle và reaction: đứng, nhìn, giật mình, ngã
11. ⚪ Walk/run và chuyển động di chuyển trong cảnh
12. ⚪ Action/combat: wind-up, anticipation, impact, recovery
13. ⚪ Follow-through, overlap và polish bằng Graph Editor
14. ⚪ Animate nhiều nhân vật và giữ đúng vị trí tương đối trong cảnh

### Giai đoạn D — Kể chuyện bằng hình ảnh

15. ⚪ Blocking một cảnh: nhân vật, đạo cụ và hành động đọc rõ trong silhouette
16. ⚪ Camera: shot size, góc máy, chuyển động camera và continuity
17. ⚪ Ánh sáng, màu sắc và vật liệu phong cách Roblox
18. ⚪ Hiệu ứng đơn giản: bụi, hit flash, trail, vật thể bay; chọn cách nhẹ máy
19. ⚪ Âm thanh: thoại, SFX, nhạc và đồng bộ với hành động

### Giai đoạn E — Render và xuất bản

20. ⚪ Tối ưu render cho máy cấu hình vừa/nhẹ
21. ⚪ Render preview, kiểm tra lỗi và render bản cuối
22. ⚪ Dựng hậu kỳ, thêm âm thanh/tiêu đề và xuất video
23. ⚪ Làm pilot YouTube 30–60 giây từ đầu đến cuối
24. ⚪ Hoàn thiện pipeline lặp lại cho các tập tiếp theo

## Sản phẩm cuối khóa

Một video pilot hoạt hình phong cách Roblox dài 30–60 giây, có:
- Ít nhất một nhân vật được animate.
- Một môi trường và một đạo cụ.
- Một hành động có mở đầu, điểm nhấn và kết thúc.
- Camera, ánh sáng và âm thanh cơ bản.
- File Blender có tổ chức và video đã render.

## Bài hiện tại

**Bài 5 — Import character Roblox vào Blender.**

Trước khi hướng dẫn export, cần biết character nằm ở đâu (trong project Roblox Studio của người học hay ở một game có sẵn) và kiểm tra định dạng/rig thực tế. Không yêu cầu người học làm lại bài R6/R15; chỉ giải thích khái niệm khi cần để chọn đúng quy trình.

## Tiêu chí PASS cho Bài 5

- Character xuất hiện đúng trong Blender.
- Scale và hướng nhìn hợp lý.
- Mesh/material hiển thị đủ để tiếp tục làm việc.
- Đã kiểm tra rõ rig có được giữ lại hay chưa.
- File Blender được lưu thành một project có thể mở lại.

## Ghi chú tiến độ

Các bài Blender cơ bản 1–3 đã hoàn thành. Người học đã thực hành skeleton thủ công, Pose Mode, keyframe, Copy Rotation, IK Target và Pole Target. Không cần lặp lại các bài này nếu chúng không trực tiếp giải quyết vấn đề của rig character thật.
