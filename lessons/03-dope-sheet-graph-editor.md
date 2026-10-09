# Lesson 03 — Dope Sheet & Graph Editor cơ bản

**Trạng thái:** DONE  
**Phần mềm:** Blender 5.2

## Mục tiêu

- Biết dùng Dope Sheet để chỉnh thời điểm và khoảng cách giữa các keyframe.
- Biết dùng Graph Editor để xem và chỉnh cách giá trị thay đổi giữa các keyframe.
- Hiểu ảnh hưởng của timing và interpolation đến tốc độ chuyển động.

## 1. Dope Sheet — chỉnh timing

Dope Sheet hiển thị keyframe theo trục thời gian. Dùng nó để chọn, di chuyển và thay đổi khoảng cách giữa các keyframe.

### Thực hành đã hoàn thành

1. Mở Dope Sheet và tìm các keyframe của object.
2. Chọn keyframe rồi nhấn `G` để di chuyển nó trên timeline.
3. Đưa keyframe cuối ra xa hơn để quan sát chuyển động kéo dài.
4. Nhấn `A` để chọn tất cả keyframe, sau đó nhấn `S` để scale khoảng cách thời gian:
   - Scale lớn hơn 1 (ví dụ `S`, nhập `2`) làm khoảng thời gian giữa các keyframe dài ra.
   - Scale nhỏ hơn 1 (ví dụ `S`, nhập `0.5`) làm khoảng thời gian ngắn lại.

**Kết luận:** Dope Sheet chủ yếu dùng để chỉnh *khi nào* keyframe xảy ra và timing của animation.

## 2. Graph Editor — chỉnh interpolation

Graph Editor biểu diễn sự thay đổi giá trị animation theo thời gian bằng các đường cong. Trục ngang là thời gian; trục dọc là giá trị của thuộc tính đang xem.

### Thực hành đã hoàn thành

1. Mở Graph Editor và quan sát các đường cong animation.
2. Chọn keyframe rồi nhấn `T` để mở menu interpolation.
3. So sánh:
   - **Linear:** giá trị thay đổi đều giữa hai keyframe; chuyển động có tốc độ tương đối ổn định.
   - **Bezier:** đường cong được làm mượt theo tay nắm/handles; tốc độ có thể tăng hoặc giảm giữa các keyframe.

**Kết luận:** Graph Editor dùng để chỉnh *giá trị thay đổi như thế nào* giữa các keyframe, qua đó ảnh hưởng đến tốc độ và cảm giác chuyển động.

## 3. Bài kiểm tra cuối — PASS

Thiết lập animation từ Frame 1 đến Frame 30, sau đó di chuyển keyframe cuối đến Frame 60 và đặt interpolation là Linear.

**Câu 1: Vì sao khi chuyển keyframe cuối từ Frame 30 sang Frame 60, khối lập phương chuyển động chậm hơn?**

Trả lời: Vì cùng một quãng đường được thực hiện trong thời gian dài hơn gấp đôi nên tốc độ trung bình giảm.

**Câu 2: Dope Sheet khác Graph Editor ở điểm nào?**

Trả lời: Dope Sheet dùng để chỉnh keyframe và timing; Graph Editor dùng để điều chỉnh cách các thuộc tính được nội suy giữa các keyframe.

Cả hai câu trả lời đều đúng.

## Hotkeys đã học

| Phím | Tác dụng |
|---|---|
| `A` | Chọn tất cả keyframe trong vùng đang hoạt động |
| `G` | Di chuyển keyframe đã chọn |
| `S` | Scale khoảng cách thời gian giữa các keyframe đã chọn |
| `T` | Mở menu interpolation cho keyframe đã chọn |

## Ghi nhớ nhanh

- **Dope Sheet = Timing:** keyframe xảy ra khi nào, cách nhau bao lâu.
- **Graph Editor = Value/Interpolation:** giá trị thay đổi ra sao theo thời gian.
- **Linear:** thay đổi đều.
- **Bezier:** thay đổi theo đường cong, có thể tạo easing.

## Tiến độ

Lesson 03 đã hoàn thành và được đánh dấu PASS sau khi thực hành các bước trong Blender 5.2 và trả lời đúng hai câu kiểm tra cuối.
