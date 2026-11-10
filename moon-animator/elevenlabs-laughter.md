# ElevenLabs — Tạo tiếng cười (Laughter)

Ghi chú dùng cho voice trong Roblox animation.

## 1. Chọn model

- Ưu tiên **Eleven v4** để thử audio tags.
- **Eleven v3** cũng hỗ trợ audio tags.
- Các model khác như Multilingual v2 / Flash không hỗ trợ cùng hệ audio-tag theo cách này; kết quả phụ thuộc ngữ cảnh, dấu câu và thiết lập voice.

## 2. Audio tags tiếng cười

Thử từng tag riêng để nghe sự khác biệt:

| Tag | Cách dùng / sắc thái mong muốn |
|---|---|
| `[laughs]` | Cười nói chung |
| `[starts laughing]` | Bắt đầu bật cười |
| `[laughs harder]` | Cười lớn / mạnh dần |
| `[wheezing]` | Cười đến hụt hơi |
| `[chuckles]` | Cười khúc khích nhẹ |
| `[mischievously]` | Sắc thái tinh quái; dùng kết hợp với tag tiếng cười |

## 3. Một số cách phối hợp để thử

Các chuỗi dưới đây là prompt thử nghiệm, không đảm bảo kết quả giống hệt ý định:

**Cười khúc khích**
```text
[chuckles]
```

**Bắt đầu cười rồi cười lớn dần**
```text
[starts laughing] [laughs harder]
```

**Cười tinh quái / kiểu phản diện**
```text
[mischievously] [laughs]
```

**Cười lớn đến hụt hơi**
```text
[laughs] [wheezing]
```

## 4. Quy trình thử

1. Chọn model Eleven v4 (hoặc Eleven v3).
2. Chọn voice muốn dùng cho nhân vật.
3. Nhập một tag hoặc một chuỗi phối hợp ngắn trong Text to Speech.
4. Generate và nghe thử; thay tag hoặc voice nếu sắc thái chưa đúng.
5. Nên tạo tiếng cười thành clip riêng để dễ căn thời điểm trong Moon Animator 2 / khi dựng video.

## 5. Lưu ý

- `[evil laughter]` không nằm trong các ví dụ audio tag tiếng cười chính thức được ElevenLabs nêu. Thay vào đó, thử `[mischievously] [laughs]`.
- Audio tags là chỉ dẫn cho model, không phải lệnh đảm bảo đầu ra chính xác. Kết quả còn tùy voice và cách model diễn giải.
- Nếu tag bị đọc thành lời hoặc không tạo ra tiếng cười như mong muốn, kiểm tra lại model đang chọn và thử tag `[laughs]` đơn lẻ trước.

## Tài liệu chính thức

- [How to make the voice laugh?](https://elevenlabs.io/docs/help-center/product/core-capabilities/text-to-speech/how-to-make-the-voice-laugh)
- [How do audio tags work with Eleven v3 and v4?](https://elevenlabs.io/docs/help-center/product/core-capabilities/text-to-speech/how-do-audio-tags-work-with-eleven-v3-and-v4)
- [Text to Speech — Best practices / Audio tags](https://elevenlabs.io/docs/overview/capabilities/text-to-speech/best-practices)
