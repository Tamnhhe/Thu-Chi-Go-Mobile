# Thu Chi Go — Mobile Releases

Repo phát hành bản build **APK (Android)** và **IPA (iOS)** của app [Thu Chi Go](https://github.com/Tamnhhe/ThuChiGO).

Binary được đính vào **GitHub Release** (không commit vào git tree) nên repo này không phình dung lượng theo thời gian. Repo chính nhúng repo này làm git submodule tại `release/`.

## Link tải cố định

Các URL dưới đây **luôn trỏ tới bản mới nhất** (không đổi qua các lần cập nhật, vì mỗi release luôn đặt tên asset giống nhau):

- **Android:** https://github.com/Tamnhhe/Thu-Chi-Go-Mobile/releases/latest/download/ThuChiGO.apk
- **iOS:** https://github.com/Tamnhhe/Thu-Chi-Go-Mobile/releases/latest/download/ThuChiGO.ipa
- **Manifest (version + sha256):** https://github.com/Tamnhhe/Thu-Chi-Go-Mobile/releases/latest/download/manifest.json

Trang tải trên web: `https://thuchigo.com/download`.

## Cài đặt

### Android (APK)
1. Tải `ThuChiGO.apk` từ link trên.
2. Mở file trên điện thoại, cho phép **cài từ nguồn không xác định** nếu được hỏi.
3. Cài đặt và mở app.

### iOS (IPA — sideload qua AltStore)
Vì không có tài khoản Apple Developer trả phí, IPA **chưa ký**; dùng AltStore ký bằng Apple ID free (chứng chỉ hết hạn sau 7 ngày, tự refresh khi cùng Wi‑Fi với AltServer).

1. Cài **AltServer** trên máy Mac/Windows, cài **AltStore** lên iPhone qua AltServer.
2. Trên iPhone: **AltStore → My Apps → `+`** rồi chọn `ThuChiGO.ipa` (AirDrop/Files sang máy trước).
   - Hoặc trên Mac: **AltServer → Install .ipa** → chọn thiết bị → chọn `ThuChiGO.ipa`.
3. AltStore ký app bằng Apple ID free của bạn. Giữ AltServer chạy + cùng Wi‑Fi để tự refresh; nếu hết hạn thì mở AltStore bấm **Refresh All**.

> Giới hạn Apple ID free: tối đa 3 app sideload cùng lúc, refresh mỗi 7 ngày. Đây là giới hạn của Apple.

## Phát hành bản mới

Từ repo chính, sau khi build APK/IPA theo `mobile/BUILD_APP.md`:

```bash
./scripts/publish-mobile-release.sh <version> mobile/thuchigo.apk mobile/ios/build/thuchigo.ipa
```

Xem lịch sử phiên bản tại [`CHANGELOG.md`](./CHANGELOG.md).
