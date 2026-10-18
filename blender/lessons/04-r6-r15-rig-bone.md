# Lesson 04 — R6/R15, Rig & Bone

**Trạng thái:** DONE  
**Phần mềm:** Blender 5.2

## Mục tiêu
Hiểu cấu trúc character, rig, bone và các khái niệm cần thiết trước khi chuẩn bị character Roblox để animate.

## 1. Khái niệm cốt lõi

- **Mesh:** hình học nhìn thấy được của nhân vật.
- **Bone:** xương điều khiển chuyển động của một phần rig.
- **Armature:** object trong Blender chứa hệ thống bone.
- **Rig:** hệ thống điều khiển giúp animator tạo pose/chuyển động cho nhân vật.
- **Parent/Child:** quan hệ cha-con giữa các bone; bone con có thể đi theo chuyển động của bone cha.

## 2. Object Mode, Edit Mode và Pose Mode

- **Object Mode:** thao tác với toàn bộ object Armature.
- **Edit Mode:** chỉnh cấu trúc, vị trí và quan hệ của bone.
- **Pose Mode:** điều khiển bone để tạo tư thế và animation.

Animation thường được tạo bằng cách đặt keyframe cho pose trong Pose Mode, không phải bằng cách sửa cấu trúc bone trong Edit Mode.

## 3. Parent/Child hierarchy

Đã thực hành tạo/xem bone cha và bone con, rồi xoay bone cha trong Pose Mode để quan sát ảnh hưởng lên bone con.

## 4. Constraint và IK

Đã thực hành:
- Bone Constraint như Copy Rotation và phân biệt với Object Constraint.
- Thêm Inverse Kinematics (IK) constraint.
- Đặt Chain Length = 2 để IK điều khiển chuỗi bone của cánh tay.
- Dùng IK Target để điều khiển vị trí đầu chuỗi.
- Dùng Pole Target để thay đổi hướng gập khuỷu tay.
- Kiểm tra bằng cách di chuyển target/pole và bật/tắt constraint.

## 5. R6 và R15 trong Roblox

- **R6:** rig cổ điển với 6 bộ phận cơ thể chính; cấu trúc đơn giản hơn.
- **R15:** rig chia cơ thể thành nhiều bộ phận hơn, tạo nhiều khớp và khả năng chuyển động linh hoạt hơn.
- Cấu trúc rig quyết định các khớp nào có thể được animate và ảnh hưởng đến khả năng tương thích của animation.

## Ghi nhớ
- Edit Mode = sửa cấu trúc bone.
- Pose Mode = tạo pose/chuyển động.
- Dope Sheet chỉnh timing; Graph Editor chỉnh cách giá trị thay đổi.
- IK Target điều khiển vị trí đầu chuỗi IK; Pole Target giúp kiểm soát hướng gập.
- Cần xác định đúng loại rig Roblox trước khi chuẩn bị character và animate.

## Tiến độ
Lesson 04 được đánh dấu DONE theo xác nhận hoàn thành của người học.
