# Lesson 04 — Roblox Character: R6/R15, Rig & Bone

**Trạng thái:** 🟡 IN PROGRESS  
**Phần đã thực hành:** Rig & Bone cơ bản, Constraint, IK, Pole Target.  
**Phần tiếp theo:** Tìm hiểu cấu trúc nhân vật Roblox R6/R15 và hoàn thành checkpoint tổng.

## Mục tiêu

- Hiểu Bone, Armature, Skeleton và Rig.
- Tạo và chỉnh skeleton đơn giản trong Blender 5.2.
- Hiểu Parent/Child hierarchy.
- Dùng Pose Mode và keyframe để tạo chuyển động.
- Phân biệt Bone Constraint và Object Constraint.
- Thiết lập và kiểm tra IK cùng Pole Target.
- Chuẩn bị kiến thức để học cấu trúc nhân vật Roblox R6/R15.

## Bài 1 — Bone, Armature, Skeleton và Rig

- **Bone:** một xương riêng lẻ, có Head và Tail.
- **Armature:** object Blender chứa các bone.
- **Skeleton:** cấu trúc các bone và quan hệ giữa chúng.
- **Rig:** hệ thống điều khiển character; có thể gồm skeleton, controls, constraints và cách mesh gắn với skeleton.
- **Mesh:** hình học nhìn thấy được của nhân vật; không phải là bone.

Nhớ nhanh: Mesh = hình thể; Bone/Skeleton = cấu trúc xương; Rig = hệ thống điều khiển.

## Bài 2 — Edit Mode và Pose Mode

### Edit Mode
- Xây dựng skeleton, chỉnh Head/Tail, tạo bone mới và thiết lập hierarchy.
- Chọn bone hoặc đầu bone rồi nhấn `E` để extrude bone mới.

### Pose Mode
- Tạo tư thế và chuyển động cho các bone.
- `R` để xoay bone; `G` để di chuyển bone/điều khiển khi phù hợp.
- Di chuyển đến frame khác, thay đổi pose và nhấn `I` để tạo keyframe.

**Quy tắc:** Edit Mode = xây bộ xương; Pose Mode = điều khiển tư thế/chuyển động.

## Bài 3 — Parent và Child

Khi bone B là Child của bone A, chuyển động của A có thể ảnh hưởng đến B theo hierarchy. Xoay Child không tự động làm Parent xoay theo.

Thực hành:
1. Vào Pose Mode.
2. Xoay `UpperArm.L` bằng `R` và quan sát cẳng tay.
3. Chọn `Forearm.L`, xoay thử và quan sát cánh tay trên.

## Bài 4 — Tạo skeleton đơn giản

Tạo một skeleton có cột sống, pelvis, hai tay, cẳng tay, bàn tay, hai chân và bàn chân. Mục tiêu là hiểu hierarchy, không cần làm đẹp hoặc gắn mesh ngay.

Đặt tên trái/phải nhất quán, ví dụ `UpperArm.L`, `Forearm.L`, `UpperArm.R`, `Forearm.R`. Hậu tố `.L` và `.R` giúp nhận diện bên trái/phải trong nhiều workflow Blender.

## Bài 5 — Bone và keyframe

1. Chọn Armature và vào Pose Mode.
2. Chọn một bone.
3. Ở frame 1, đặt pose ban đầu và nhấn `I` để tạo keyframe.
4. Chuyển sang frame 20, thay đổi pose và nhấn `I` lần nữa.
5. Phát animation bằng `Space` để xem chuyển động nội suy.

## Bài 6 — Constraint

Constraint là một quy tắc bổ sung để điều khiển một bone hoặc object. Ví dụ **Copy Rotation** có thể làm bone nhận hướng xoay từ bone/object khác.

- **Parent/Child:** quan hệ phân cấp trong skeleton.
- **Constraint:** quy tắc điều khiển bổ sung giữa các bone/object hoặc theo một điều kiện.

Để tạo constraint cho bone:
1. Chọn Armature chính.
2. Vào Pose Mode và chọn bone cần điều khiển.
3. Mở **Bone Constraints Properties** (không phải Object Constraints).
4. Thêm constraint mong muốn và thiết lập target nếu cần.

Thực hành đã hoàn thành: thêm Copy Rotation và xác nhận constraint hoạt động.

## Bài 7 — Inverse Kinematics (IK)

**IK (Inverse Kinematics)** cho phép đặt target ở vị trí mong muốn để Blender tự tính góc xoay của chuỗi bone nhằm đưa phần cuối chuỗi về phía target.

### Thiết lập đã thực hành
1. Tạo một Armature riêng tên `IK_Target`.
2. Chọn bone cẳng tay (`Forearm.L`) trong Armature chính, ở Pose Mode.
3. Thêm **Inverse Kinematics** trong Bone Constraints Properties.
4. Đặt **Target** là object `IK_Target`; nếu target là Armature, chọn bone điều khiển tương ứng ở ô **Bone**.
5. Đặt **Chain Length = 2** để chuỗi IK tính cẳng tay và cánh tay trên.
6. Chọn `IK_Target`, vào Pose Mode của nó và di chuyển bone target bằng `G`.
7. Xác nhận cánh tay tự xoay theo vị trí target.

**Lưu ý:** Constraint phải nằm trên bone của Armature chính. Trong Pose Mode, ta điều khiển bone thuộc Armature đang hoạt động; target được chọn trong ô Target của constraint, không cần chọn hai Armature cùng lúc trong Viewport.

## Bài 8 — Pole Target

Pole Target giúp kiểm soát hướng gập của chuỗi IK, chẳng hạn khuỷu tay hoặc đầu gối.

### Thiết lập đã thực hành
1. Tạo bone điều khiển riêng tên `Pole.L` trong Armature `IK_Target`.
2. Đặt bone Pole lệch khỏi đường nối vai → khuỷu tay → bàn tay, về phía muốn khuỷu tay hướng tới.
3. Chọn Armature chính, vào Pose Mode và chọn bone có IK Constraint.
4. Trong IK Constraint, đặt **Pole Target** là object `IK_Target` và **Pole Bone** là `Pole.L`.
5. Giữ Pole Angle mặc định ban đầu; chỉ điều chỉnh nếu khuỷu tay xoay sai hướng.
6. Di chuyển IK target để đổi vị trí bàn tay.
7. Di chuyển `Pole.L` để đổi hướng gập khuỷu tay.

### Kết quả đã xác nhận
- Di chuyển IK target làm chuỗi cánh tay tự xoay theo target.
- Di chuyển `Pole.L` làm thay đổi hướng gập khuỷu tay.
- Đã thử xoay `UpperArm.L` và bật/tắt IK Constraint để quan sát ảnh hưởng lên chuỗi.

## Bài 9 — Roblox R6 và R15 (chưa hoàn thành)

- **R6:** rig tiêu chuẩn đơn giản hơn, gồm sáu phần cơ thể chính; ít phân đoạn tay/chân hơn.
- **R15:** rig tiêu chuẩn có nhiều phân đoạn cơ thể hơn, cho phép chuyển động linh hoạt và chi tiết hơn.

R6/R15 là tên rig Roblox; không nên hiểu rằng Armature trong Blender chỉ có đúng 6 hoặc 15 bone. Khi học phần này, cần xem cấu trúc các bộ phận, khớp/joint và cách chúng ảnh hưởng đến animation.

Phần tiếp theo: xem cấu trúc R6 và R15, so sánh tay/chân/khớp, rồi mới chuẩn bị hoặc import character vào Blender.

## Hotkey đã dùng

| Hotkey | Chức năng |
|---|---|
| `Shift + A` | Mở Add menu trong 3D Viewport |
| `Tab` | Chuyển Object Mode ↔ Edit Mode (tùy context) |
| `Ctrl + Tab` | Mở menu chuyển mode; dùng để vào Pose Mode với Armature |
| `E` | Extrude bone trong Armature Edit Mode |
| `G` | Di chuyển object/bone/IK target tùy mode |
| `R` | Xoay object hoặc bone tùy mode |
| `I` | Chèn keyframe trong context animation phù hợp |
| `Space` | Play/Pause animation |

Xem thêm danh sách hotkey tại [HotKeys.md](../HotKeys.md).

## Checkpoint tổng

Đánh dấu Lesson 04 hoàn thành sau khi có thể tự giải thích hoặc thực hiện:

- [x] Giải thích Bone, Armature, Skeleton và Rig.
- [x] Chỉnh bone trong Edit Mode và điều khiển bone trong Pose Mode.
- [x] Giải thích Parent/Child hierarchy.
- [x] Tạo keyframe cho bone và phát animation.
- [x] Thử Copy Rotation Constraint.
- [x] Thêm IK Constraint, di chuyển target và quan sát chuỗi xương.
- [x] Thêm Pole Target và điều khiển hướng gập khuỷu tay.
- [ ] So sánh cấu trúc R6 và R15.
- [ ] Hoàn thành checkpoint về cấu trúc Roblox R6/R15.

**Trạng thái hiện tại:** Phần Rig/Bone, Constraint, IK và Pole Target đã thực hành. Lesson 04 vẫn IN PROGRESS vì phần R6/R15 và checkpoint tổng còn lại.