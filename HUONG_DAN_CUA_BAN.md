# HƯỚNG DẪN — TỪ FILE NÀY ĐẾN WEBSITE THẬT ONLINE

File này viết cho người **không rành công nghệ**. Cứ làm theo đúng thứ tự, đừng bỏ bước nào.

---

## BƯỚC 1 — Tạo tài khoản GitHub (5 phút)

1. Mở trình duyệt, vào: https://github.com/signup
2. Nhập email, đặt mật khẩu, đặt tên tài khoản (username) tuỳ ý, ví dụ `masterchinese`.
3. Xác nhận email theo hướng dẫn trên màn hình.
4. Xong bước này, bạn có 1 tài khoản GitHub — đây là "kho lưu trữ code" của website.

## BƯỚC 2 — Tạo một "repository" (nơi chứa code website)

1. Sau khi đăng nhập GitHub, bấm nút xanh lá **"New"** (hoặc dấu **+** ở góc trên bên phải → **New repository**).
2. Ở ô **Repository name**, gõ: `master-chinese-website`
3. Để chế độ **Public**.
4. **KHÔNG** tick vào ô "Add a README file".
5. Bấm **Create repository**.
6. Bạn sẽ thấy một trang trống với hướng dẫn — cứ để nguyên trang đó, chuyển sang bước 3.

## BƯỚC 3 — Upload code lên GitHub (không cần biết lệnh gì cả)

1. Trên trang repository vừa tạo, tìm dòng chữ **"uploading an existing file"** (là một đường link màu xanh) và bấm vào.
2. Bạn sẽ thấy 1 ô để kéo-thả file.
3. Mở thư mục `master-chinese` mà tôi gửi bạn (giải nén file zip ra trước), **chọn TẤT CẢ file và thư mục bên trong** (Ctrl+A trên Windows / Cmd+A trên Mac), rồi **kéo thả** vào ô upload của GitHub.
   - ⚠️ Kéo thả **nội dung bên trong** thư mục `master-chinese`, không kéo cả thư mục `master-chinese` vào.
4. Đợi upload xong (thanh tiến trình chạy hết), cuộn xuống dưới, bấm nút xanh **Commit changes**.
5. Xong — code của bạn giờ đã nằm trên GitHub.

## BƯỚC 4 — Tạo tài khoản Netlify và kết nối với GitHub (10 phút)

1. Vào: https://app.netlify.com/signup
2. Chọn **"Sign up with GitHub"** — bấm vào, cho phép Netlify truy cập GitHub của bạn (bấm Authorize).
3. Sau khi vào Netlify, bấm **"Add new site"** → **"Import an existing project"**.
4. Chọn **"Deploy with GitHub"**.
5. Trong danh sách repository hiện ra, chọn `master-chinese-website` (repo bạn tạo ở Bước 2).
6. Netlify sẽ tự nhận diện đây là project Astro và tự điền sẵn:
   - Build command: `npm run build`
   - Publish directory: `dist`
   Bạn không cần sửa gì, cứ để mặc định.
7. Bấm **"Deploy site"**.
8. Đợi khoảng 1–2 phút, Netlify sẽ hiện chữ **"Site is live"** kèm 1 đường link dạng `random-name-123.netlify.app` — đó chính là **website của bạn, đã online thật**.

## BƯỚC 5 — Kiểm tra website

Mở link Netlify vừa tạo, bạn sẽ thấy:
- Trang chủ với 2 episode mẫu (nội dung tiếng Trung giả, tôi tạo để demo).
- Bấm vào 1 episode để xem trang chi tiết: transcript, pinyin, dịch nghĩa, từ vựng.
- Ô tìm kiếm ở trang chủ hoạt động được luôn.

Nếu thấy đúng như vậy — website đã chạy thành công.

## BƯỚC 6 — Đổi tên website (tuỳ chọn)

Trong Netlify, vào **Site settings → Change site name**, đổi từ tên random sang tên bạn muốn, ví dụ `masterchinese` → link sẽ thành `masterchinese.netlify.app`. Miễn phí, không cần mua domain riêng.

## BƯỚC 7 — Thêm episode thật của bạn (làm mỗi khi có podcast mới)

1. Vào GitHub, mở repo `master-chinese-website` → vào thư mục `src/data/episodes/`.
2. Bấm vào file `002.json` để xem mẫu, bấm biểu tượng **cây bút (Edit)**.
3. Bấm **"..."** (góc trên bên phải khu vực code) → chọn cách khác: bấm nút **Add file → Create new file**.
4. Đặt tên file mới, ví dụ: `003.json`
5. Copy nguyên nội dung của `001.json`, dán vào, rồi sửa các phần:
   - `title`, `youtubeUrl`, `publishDate`
   - `transcript`, `pinyin`, `translation`, `vocabulary`, `basicExplanation` — thay bằng nội dung episode thật của bạn.
   - Giữ nguyên `"access": "FREE"` (chưa cần đổi cho tới khi làm Membership).
6. Cuộn xuống, bấm **Commit changes**.
7. Chờ khoảng 1 phút — Netlify tự phát hiện thay đổi và tự build lại website. Refresh trang, episode mới đã xuất hiện.

**Đây là toàn bộ quy trình bạn sẽ lặp lại mỗi lần ra podcast mới — không cần biết code, chỉ copy-sửa-dán.**

## BƯỚC 8 — Gắn Ko-fi và VietQR thật

1. Vào https://ko-fi.com → **Sign up** → tạo trang cá nhân, đặt tên kênh, upload ảnh đại diện.
2. Vào **Settings → Page**, tắt (uncheck) mục hiển thị số supporter.
3. Copy link trang Ko-fi của bạn (dạng `ko-fi.com/tenkenh`).
4. Chuẩn bị 1 ảnh mã VietQR ngân hàng của bạn (chụp từ app ngân hàng, mục "Nhận tiền" → tạo mã QR).
5. Gửi tôi 2 thứ: link Ko-fi + ảnh VietQR — tôi sẽ sửa file `src/components/SupportBlock.astro` (2 dòng `KOFI_URL` và `VIETQR_IMAGE`) và gửi lại bạn phần code đã cập nhật để upload đè lên GitHub y như Bước 3.

---

## Nếu bạn bị kẹt ở bất kỳ bước nào

Chụp màn hình gửi tôi, tôi sẽ chỉ chính xác cần bấm vào đâu tiếp theo.
