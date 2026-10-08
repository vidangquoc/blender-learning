# Lesson 01 — Làm quen Blender & Timeline

**Status:** 🟡 IN PROGRESS

## Mục tiêu
- Hiểu Blender viewport.
- Biết Object Mode/Edit Mode.
- Điều hướng viewport.
- Hiểu Timeline và frame.
- Tạo animation đơn giản bằng keyframe.

## Các bước học

### Bước 1 — Làm quen giao diện
1. Mở Blender.
2. Xác định **3D Viewport**, **Outliner**, **Properties**, **Timeline**.
3. Chọn Cube mặc định.

### Bước 2 — Transform cơ bản
- Move: `G`
- Rotate: `R`
- Scale: `S`
- Ví dụ:
  - `G X 3`
  - `R Z 45`
  - `S 1.5`
- Undo: `Ctrl + Z`
- Redo: `Ctrl + Shift + Z`

### Bước 3 — Object Mode / Edit Mode
- Nhấn `Tab` để chuyển giữa Object Mode và Edit Mode.
- Object Mode: thao tác với cả object.
- Edit Mode: chỉnh mesh/vertex/edge/face của object.

### Bước 4 — Timeline & Frame
- Timeline dùng để điều khiển thời gian animation.
- Mỗi frame là một mốc thời gian.
- Ví dụ 30 FPS: khoảng 30 frame ≈ 1 giây.

### Bước 5 — Keyframe đầu tiên
1. Ở **frame 1**, đặt Cube ở vị trí ban đầu.
2. Insert **Location keyframe**.
3. Chuyển tới **frame 40**.
4. Di chuyển Cube sang vị trí mới, ví dụ X +5.
5. Insert **Location keyframe** lần nữa.
6. Bấm **Play** trên Timeline và quan sát Cube di chuyển.

### Bước 6 — Hiểu 3 khái niệm cốt lõi
- **Frame:** một mốc thời gian trong animation.
- **Keyframe:** lưu trạng thái của object tại một frame.
- **Interpolation:** Blender tự tính chuyển động giữa các keyframe.

## Checkpoint
Trước khi sang phần tiếp theo, phải làm được:
- [ ] Chọn Cube
- [ ] Move bằng G
- [ ] Rotate bằng R
- [ ] Scale bằng S
- [ ] Object Mode ↔ Edit Mode bằng Tab
- [ ] Xác định Timeline
- [ ] Tạo 2 keyframe Location
- [ ] Chạy animation Cube từ A → B
- [ ] Lưu file .blend vào thư mục học tập

## Exercise 01 — Transform cơ bản
Dùng Cube mặc định:
1. Chọn Cube.
2. Thử Move, Rotate, Scale.
3. Dùng Undo/Redo để luyện kiểm soát thao tác.

## Exercise 02 — Animation A → B
Tạo animation cho Cube từ vị trí A ở frame 1 tới vị trí B ở frame 40 bằng Location keyframe.

## PASS
Chỉ đánh dấu DONE khi mày:
1. Tự tạo được animation Cube từ A → B.
2. Giải thích được frame, keyframe và interpolation.
3. Lưu được file `.blend` vào thư mục học tập.
4. Hoàn thành toàn bộ checkpoint.

Nếu bị kẹt, gửi screenshot/video để xử lý cùng.
