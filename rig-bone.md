# Rig & Bone — Blender 5.2

## Mục tiêu

Hiểu bản chất của Rig, Armature và Bone, sau đó tự tạo một skeleton đơn giản và dùng nó để tạo chuyển động.

> Mục tiêu cuối: hiểu cách một bộ xương điều khiển character để chuẩn bị cho animation Roblox.

## Bài 1 — Rig là gì?

### 1.1. Rig

Rig là toàn bộ hệ thống điều khiển giúp ta pose và animate một character.

Một rig thường gồm:
- Armature
- Bone
- Quan hệ parent/child giữa các bone
- Các control hoặc constraint (ở rig nâng cao)
- Cách mesh character được gắn vào skeleton

Có thể hiểu đơn giản:

Mesh = cơ thể
Skeleton/Bone = bộ xương
Rig = hệ thống điều khiển bộ xương

## Bài 2 — Armature là gì?

Trong Blender, Armature là object chứa các bone.

Tạo một Armature:
1. Đưa chuột vào 3D Viewport.
2. Nhấn Shift + A.
3. Chọn Armature → Single Bone.
4. Blender tạo một Armature chứa một bone.

Single Bone chỉ là điểm bắt đầu để học. Một Armature có thể chứa rất nhiều bone.

## Bài 3 — Bone là gì?

Một Bone có hai đầu chính:
- Head — đầu bone
- Tail — đuôi bone

Bone biểu diễn một phần của skeleton.

```
Head
 ●
 │
 │  Bone
 │
 ●
Tail
```

Bone có thể được:
- di chuyển
- xoay
- scale
- nối với bone khác
- làm parent hoặc child của bone khác

## Bài 4 — Edit Mode và Pose Mode

### Edit Mode

Dùng để xây dựng skeleton.

Trong Edit Mode, ta có thể:
- di chuyển Head/Tail
- extrude bone mới
- nối các bone
- tạo hierarchy

### Pose Mode

Dùng để điều khiển skeleton khi animate.

Trong Pose Mode:
- R → xoay bone
- G → di chuyển bone
- I → tạo keyframe

> Quy tắc quan trọng: Edit Mode = xây bộ xương; Pose Mode = tạo tư thế/chuyển động.

## Bài 5 — Tạo bone thứ hai

1. Chọn Armature.
2. Nhấn Tab để vào Edit Mode.
3. Chọn một bone.
4. Chọn Tail của bone.
5. Nhấn E.
6. Kéo chuột để tạo bone mới.
7. Click để xác nhận.

Bone mới được tạo từ Tail của bone trước. Đây gọi là Extrude bone.

## Bài 6 — Hiểu Parent và Child

Khi bone B được tạo từ bone A bằng cách extrude từ Tail của A, Blender tạo quan hệ:

```
Bone A
   │
   └── Bone B
```

A = Parent
B = Child

Nếu Parent thay đổi vị trí hoặc xoay, Child có thể bị ảnh hưởng theo hierarchy.

Đây là nền tảng để tạo chuyển động cho character.

## Bài 7 — Tạo skeleton đơn giản

Từ một bone ban đầu, tạo skeleton:

```
          Head
           │
         Spine
           │
         Pelvis
        /      \
      Leg      Leg
       │        │
      Foot     Foot
```

Thực hành:
1. Vào Edit Mode.
2. Đặt bone trung tâm theo chiều dọc.
3. E để extrude các bone của cột sống.
4. Từ vùng pelvis, tạo nhánh sang trái/phải.
5. Từ mỗi nhánh tạo leg.
6. Từ leg tạo foot.

Chưa cần tạo skeleton đẹp. Mục tiêu là hiểu bone hierarchy.

## Bài 8 — Đối xứng

Khi tạo character, ta thường cần bên trái và bên phải giống nhau.

Có thể dùng công cụ đối xứng của Armature để tránh tạo thủ công từng bone.

Quy tắc đặt tên rất quan trọng:

```
arm.L
arm.R
leg.L
leg.R
```

.L = Left; .R = Right.

Tên đúng giúp Blender nhận biết các cặp bone trái/phải trong nhiều workflow rigging.

## Bài 9 — Pose Mode

Sau khi skeleton đã được tạo:
1. Chọn Armature.
2. Chuyển sang Pose Mode.
3. Chọn một bone.
4. Nhấn R.
5. Xoay bone.
6. Quan sát ảnh hưởng lên các bone con.

Thử:
- xoay Spine
- xoay Leg
- xoay Foot

Mục tiêu là cảm nhận hierarchy thay vì chỉ nhìn skeleton như các đường xương.

## Bài 10 — Bone và Animation

Tại frame 1:
1. Chọn một bone trong Pose Mode.
2. Đặt rotation ban đầu.
3. Nhấn I để tạo keyframe.

Tại frame 20:
1. Di chuyển sang frame 20.
2. Xoay bone sang tư thế mới.
3. Nhấn I lần nữa.

Blender sẽ nội suy chuyển động giữa hai keyframe.

## Bài 11 — Bone không phải Mesh

Mesh là hình học nhìn thấy được của character.

Bone là cấu trúc điều khiển.

Bone không phải là phần cơ thể. Bone dùng để xác định cách các phần của mesh biến dạng/chuyển động.

## Bài 12 — Armature + Mesh

Khi gắn mesh vào armature, bone thay đổi tư thế → mesh có thể biến dạng theo.

Cơ chế thường dùng để gắn character mesh với armature là Armature Deform / skinning.

Chi tiết về weight và automatic weights sẽ học sau.

## Bài 13 — Phân biệt 4 khái niệm

### Bone
Một xương riêng lẻ.

### Armature
Object chứa một hệ thống bone.

### Skeleton
Cấu trúc các bone tạo thành bộ xương.

### Rig
Hệ thống hoàn chỉnh dùng để điều khiển character.

Có thể nhớ:

Bone → Armature/Skeleton → Rig → Character Animation

## Checkpoint

Chỉ coi là hoàn thành phần Rig & Bone khi có thể tự trả lời:
- Rig là gì?
- Armature là gì?
- Bone là gì?
- Head và Tail là gì?
- Edit Mode dùng để làm gì?
- Pose Mode dùng để làm gì?
- Parent và Child là gì?
- Extrude bone bằng cách nào?
- Vì sao skeleton cần hierarchy?
- Bone khác Mesh như thế nào?
- Armature khác Rig như thế nào?

### Bài thực hành
Tạo một skeleton đơn giản có:
- 1 Head
- 2–3 Spine bones
- 1 Pelvis
- 2 Legs
- 2 Feet

Sau đó vào Pose Mode và thử xoay từng vùng.

Cuối cùng tạo một animation đơn giản: nhân vật nghiêng người hoặc nhấc một chân từ frame 1 đến frame 20.

## Chuẩn bị cho Roblox

Sau khi hiểu phần này, ta sẽ chuyển sang:

R6/R15 Roblox Character → cấu trúc skeleton thật → import/chuẩn bị trong Blender → animation Roblox.

Không cần học rig nâng cao ngay. Trước tiên phải hiểu chắc Bone → Hierarchy → Pose → Keyframe.
## Bài 14 — Constraint

Constraint là quy tắc bổ sung để điều khiển một bone hoặc object. Ví dụ Copy Rotation có thể làm một bone nhận hướng xoay từ một bone/object khác.

Phân biệt:
- Parent/Child là quan hệ phân cấp trong skeleton; Parent ảnh hưởng đến Child theo hierarchy.
- Constraint là một quy tắc điều khiển riêng, có thể liên kết chuyển động hoặc thuộc tính giữa các đối tượng/bone.

Để thêm Bone Constraint, cần chọn Armature chính, vào Pose Mode và chọn bone cần áp dụng. Dùng Bone Constraints Properties, không phải Object Constraints nếu muốn constraint tác động lên bone.

## Bài 15 — Inverse Kinematics (IK)

IK cho phép đặt một target ở vị trí mong muốn để Blender tự tính góc xoay của chuỗi bone nhằm đưa phần cuối chuỗi về phía target.

Thực hành đã hoàn thành:
1. Tạo một Armature riêng làm IK target.
2. Chọn bone cẳng tay trong Armature chính ở Pose Mode.
3. Thêm Inverse Kinematics constraint vào bone.
4. Chọn object IK target trong ô Target; nếu target là Armature, chọn bone target phù hợp trong ô Bone.
5. Đặt Chain Length = 2 để tính chuỗi cánh tay gồm cẳng tay và cánh tay trên.
6. Vào Pose Mode của IK target và di chuyển bone target bằng G.
7. Xác nhận chuỗi cánh tay tự xoay để theo target.

Lưu ý: IK constraint phải nằm trên bone của Armature chính. Trong Pose Mode, chỉ điều khiển bone thuộc Armature đang hoạt động; chọn target trong ô Target của constraint, không cần chọn hai Armature cùng lúc trong Viewport.

## Bài 16 — Pole Target (đang học)

Pole Target dùng để kiểm soát hướng gập của chuỗi IK, ví dụ hướng khuỷu tay hoặc đầu gối. Sau khi thêm Pole Target, cần đặt target lệch về phía hướng mà khuỷu tay nên gập và điều chỉnh Pole Angle nếu chuỗi xoay sai hướng.

Checkpoint thực hành:
- Di chuyển IK target và quan sát cánh tay theo target.
- Thêm Pole Target và thử di chuyển nó để điều khiển hướng gập khuỷu tay.

## Checkpoint bổ sung — Rig nâng cao

- Constraint khác Parent/Child ở điểm nào?
- Bone Constraint Properties khác Object Constraints như thế nào?
- IK làm gì và Chain Length có ý nghĩa gì?
- Vì sao IK target được chọn trong ô Target thay vì phải chọn cùng lúc trong Viewport?
- Pole Target giải quyết vấn đề gì?

Chưa đánh dấu Lesson 04 hoàn thành cho đến khi thực hành Pole Target và hoàn tất checkpoint tổng.
## Kết quả thực hành — IK và Pole Target

Đã xác nhận hoạt động trong Blender 5.2:
- Di chuyển IK target làm chuỗi cánh tay tự xoay để theo target.
- Di chuyển Pole.L làm thay đổi hướng gập khuỷu tay.
- Thử xoay UpperArm.L và bật/tắt IK Constraint để quan sát ảnh hưởng lên chuỗi.

Phần thực hành IK/Pole Target đã hoàn thành. Lesson 04 vẫn chưa đóng vì còn học cấu trúc Roblox R6/R15 và làm checkpoint tổng.