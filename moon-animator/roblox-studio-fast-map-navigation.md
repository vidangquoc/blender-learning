# Di chuyển nhanh trong Roblox Studio để tìm địa điểm

Tài liệu này tổng hợp các cách di chuyển camera nhanh khi khảo sát map và tìm vị trí đẹp để dựng cảnh (ví dụ: bãi câu).

## 1. Bay quanh map bằng camera controls

Trong cửa sổ 3D (Viewport):

- Giữ **chuột phải** và rê chuột để xoay góc nhìn.
- Khi vẫn giữ chuột phải, dùng **W / A / S / D** để tiến, lùi và di chuyển ngang.
- Dùng **E** để bay lên và **Q** để bay xuống.
- Giữ **Shift** trong lúc di chuyển để tăng tốc camera.
- Dùng **con lăn chuột** để zoom gần/xa.

> Trên Mac, thao tác bàn phím vẫn dùng các phím W/A/S/D, Q/E và Shift; nút chuột phải có thể thực hiện bằng secondary click hoặc chuột có nút phải.

## 2. Tăng Camera Speed

Nếu camera vẫn quá chậm:

1. Tìm điều khiển **Camera Speed** trong giao diện Roblox Studio (thường nằm trên thanh điều khiển camera của Viewport).
2. Tăng mức tốc độ.
3. Thử bay bằng chuột phải + W/A/S/D + Shift.
4. Giảm lại khi cần căn chỉnh vị trí chính xác.

Tên/vị trí điều khiển có thể thay đổi theo phiên bản Studio.

## 3. Nhảy thẳng đến một vật thể bằng phím F

Khi đã thấy một khu vực hoặc vật thể đáng chú ý:

1. Chọn Part hoặc Model đó trong Viewport hoặc Explorer.
2. Nhấn **F** để đưa camera focus vào đối tượng đang chọn.
3. Tiếp tục bay quanh khu vực để khảo sát góc máy và địa hình.

Đây là cách nhanh để quay lại một điểm đã tìm thấy, thay vì bay từ xa đến đó.

## 4. Dùng Command Bar để đưa camera đến tọa độ

Nếu đã biết tọa độ cần đến:

1. Mở **View > Command Bar**.
2. Thay X, Y, Z trong đoạn lệnh dưới đây bằng tọa độ mong muốn.
3. Chạy lệnh để đưa camera đến vị trí đó.

```lua
local target = Vector3.new(0, 20, 0) -- thay bằng tọa độ cần đến
workspace.CurrentCamera.CFrame = CFrame.lookAt(
    target + Vector3.new(0, 30, 50),
    target
)
```

Đoạn lệnh đặt camera cách điểm đích một khoảng để nhìn xuống khu vực. Có thể thay offset `Vector3.new(0, 30, 50)` để đổi hướng và khoảng cách.

## 5. Quy trình tìm địa điểm làm bãi câu

1. Dùng camera speed cao và Shift để bay nhanh qua map.
2. Khi thấy khu vực có tiềm năng, chọn một Part/Model gần đó và nhấn F để focus.
3. Giảm Camera Speed để khảo sát kỹ bờ nước, mặt bằng, hậu cảnh và góc camera.
4. Ghi lại tọa độ hoặc tạo một Part marker đặt tên, ví dụ `FishingSpot_01`.
5. Khi đã chọn được địa điểm, lưu lại tọa độ/marker để dễ quay lại khi dựng cảnh.

## Mẹo

- Dùng tốc độ cao để tìm khu vực tổng quát; giảm tốc độ khi kiểm tra bố cục.
- Không cần di chuyển nhân vật trong lúc khảo sát. Chỉ cần di chuyển camera.
- Nếu camera bị lạc, chọn một Part/Model gần nơi muốn đến rồi nhấn F.
- Trước khi dùng Command Bar, kiểm tra đúng tọa độ và lưu place nếu đang chỉnh sửa map.

---
*Ghi chú: Tên menu và vị trí Camera Speed có thể khác đôi chút giữa các phiên bản Roblox Studio.*
