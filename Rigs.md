# Roblox Rigs for Blender

Danh sách rig/template và tài nguyên liên quan để làm animation nhân vật Roblox trong Blender. Ưu tiên rig có IK/FK và control để tái sử dụng cho nhiều short.

## Rig bên thứ ba

### 1. R15 Roblox Starter Rigs — Paribes
- Tải: https://paribes.gumroad.com/l/r15robloxrigs?layout=profile
- Ghi chú: Bộ rig nhân vật R15 dựng sẵn, được giới thiệu có IK/FK switching. Kiểm tra file tải về và khả năng tương thích với Blender 5.2 trước khi đưa vào pipeline.
- Lưu ý: Chưa xác minh có thể tự động thay toàn bộ mesh của avatar tùy chỉnh hay không.

### 2. R15 Rig FK/IK — MrXeno
- Tải: https://mrxen0.gumroad.com/l/xrdqsb
- Thảo luận/hướng dẫn: https://devforum.roblox.com/t/r15-rig-for-blender-40-fk-ik-switching/3606878
- Ghi chú: Rig R15 cho Blender 4.0+, có điều khiển IK/FK và RigUI theo thông tin của tác giả. Đây là rig người học hiện đang dùng.
- Lưu ý: Khi mở file .blend có thể hiện cảnh báo script. Chỉ bật script nếu tin cậy nguồn và đã kiểm tra nội dung/tài liệu đi kèm.

### 3. Fluid Rig — ComixProductions
- Tải: https://comixproductions.gumroad.com/l/FluidRig
- Ghi chú: Rig phục vụ animation Roblox, được giới thiệu có các control IK và thư viện pose.
- Lưu ý: Xác nhận hỗ trợ phiên bản Blender đang dùng và đọc điều khoản sử dụng trước khi dùng cho dự án thương mại.

### 4. R6 IK/FK Blender Rig
- Thảo luận/tải: https://devforum.roblox.com/t/r6-ik-fk-blender-rig-v222/3586405
- Ghi chú: Lựa chọn dành cho nhân vật R6 cổ điển; không phải rig R15.

### 5. Roblox Rigs Suite — BlendAtlas
- Trang sản phẩm: https://blendatlas.com/products/roblox-rigs-suite
- Ghi chú: Bộ rig/addon được giới thiệu hỗ trợ nhiều loại nhân vật R6/R15. Kiểm tra giá, phiên bản Blender và điều khoản cấp phép trên trang chính thức trước khi tải.

## Tài liệu rig chính thức của Roblox

### Roblox Creator Hub — Rig a humanoid model
- Tài liệu: https://create.roblox.com/docs/art/modeling/rig-a-humanoid-model
- Ghi chú: Tham khảo cấu trúc rig và cách rig nhân vật humanoid theo quy ước Roblox.

### Roblox Creator Docs — Character body templates
- Thư mục tài liệu/mẫu: https://github.com/Roblox/creator-docs/tree/main/content/en-us/avatar/character-bodies
- Ghi chú: Tài nguyên tham khảo chính thức về character bodies; không mặc định rằng mọi file ở đây là rig Blender có control IK/FK.

## Công cụ liên quan đến import/animation

### Blender-Animations-Plugin
- GitHub: https://github.com/Cautioned/Blender-Animations-Plugin
- Releases: https://github.com/Cautioned/Blender-Animations-Plugin/releases
- Ghi chú: Addon liên quan đến import/export model và animation Roblox. Không nhầm addon này với rig điều khiển IK/FK chuyên dụng.

### Rokoko Studio Live for Blender
- GitHub: https://github.com/Rokoko/rokoko-studio-live-blender
- Ghi chú: Công cụ có tính năng retarget animation; cần kiểm tra khả năng tương thích phiên bản Blender hiện tại và cấu trúc rig đích trước khi dùng với rig Roblox.

## Pipeline đang hướng tới

1. Chọn một rig R15 có control tốt.
2. Kiểm tra rig chạy được trong Blender 5.2 và đọc kỹ cảnh báo script.
3. Thử gắn một avatar Roblox mẫu lên rig; phân biệt mesh liền cần skinning với các bộ phận khối cứng có thể parent vào bone.
4. Kiểm tra phụ kiện, tỉ lệ, pose và chuyển động.
5. Lưu thành template tái sử dụng sau khi test đạt yêu cầu.

## Checklist trước khi dùng

- [ ] File mở được trong phiên bản Blender đang cài.
- [ ] Đã kiểm tra nguồn tải và script trước khi cho phép chạy.
- [ ] IK/FK, RigUI và keyframe hoạt động đúng.
- [ ] Đã thử thay mesh/avatar và kiểm tra phụ kiện.
- [ ] Đã đọc license/điều khoản sử dụng, đặc biệt nếu video được kiếm tiền.
