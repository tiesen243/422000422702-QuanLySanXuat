# Contributing Guide

Hãy làm theo các bước sau để đảm bảo mọi thay đổi được quản lý rõ ràng và dễ dàng review.

## Quy trình đóng góp

1. Tạo Issue

   - Trước khi bắt đầu code, hãy kiểm tra xem đã có issue mô tả công việc chưa.
   - Nếu chưa có, bạn cần tạo issue mới bằng template:
     - feature_request: khi thêm tính năng
     - bug_report: khi sửa lỗi
   - Issue sẽ được assign cho chính người tạo (hoặc người được chỉ định).

2. Fork Repo

   - Bấm nút `Fork` để tạo bản copy repo về GitHub cá nhân.

3. Clone Repo

   - Clone repo fork của bạn về máy:
     ```bash
     git clone https://github.com/<username>/422000422702-QuanLySanXuat.git
     cd 422000422702-QuanLySanXuat
     ```
   - Thêm remote gốc (upstream):
     ```bash
     git remote add upstream https://github.com/tiesen243/422000422702-QuanLySanXuat.git
     ```
   - Đồng bộ nhánh `dev` từ upstream:
     ```bash
     git fetch upstream
     git checkout dev
     git merge upstream/dev
     ```

4. Tạo Branch Mới

   - Quy ước: `feature/<ten-tinh-nang>` hoặc `bugfix/<ten-bug>`
   - Ví dụ:
     ```bash
     git checkout -b feature/auth-login
     ```

5. Code & Test

   - Thực hiện thay đổi theo nội dung issue.
   - Chạy test đảm bảo tính năng/bugfix hoạt động đúng.

6. Tạo Changeset

   - Sau khi hoàn thành thay đổi, chạy:
     ```bash
     npm run changeset
     ```
   - Hệ thống sẽ hỏi:
     - Loại thay đổi: `patch`, `minor`, `major`
     - Mô tả ngắn gọn về thay đổi
   - Điều này giúp tự động cập nhật version và changelog.
   - Chọn loại version bump:
     - `patch`: Sửa lỗi, thay đổi nhỏ không ảnh hưởng API
     - `minor`: Thêm tính năng mới, không phá vỡ tương thích
     - `major`: Thay đổi lớn, phá vỡ tương thích
   - Quy tắc đơn giản:
     - Sửa lỗi → patch
     - Tính năng mới → minor
     - Thay đổi lớn → major

7. Push Code Lên Fork

   - Push branch lên fork repo của bạn:
     ```bash
     git push origin feature/feature-name
     ```

8. Tạo Pull Request (PR)

   - Sau khi push, truy cập repo fork của bạn trên GitHub.
   - Chọn branch mới tạo.
   - Bạn sẽ thấy nút **Contribute** → **Open pull request**.
   - Nhấn nút này để mở PR vào branch chính của dự án gốc (**dev**).

   **Yêu cầu PR:**

   - Tiêu đề PR phải link với issue đã tạo ở bước 1 theo cú pháp: `<tiền tố>: <mô tả ngắn>`.

   - Các tiền tố thường dùng:

     - `feat`: Thêm mới tính năng
     - `fix`: Sửa lỗi
     - `chore`: Công việc phụ trợ, không ảnh hưởng đến mã nguồn chính
     - `refactor`: Cải tiến cấu trúc mã, không thay đổi chức năng
     - `docs`: Thay đổi tài liệu
     - `test`: Thêm hoặc sửa test

   - Ví dụ:

     - `feat: Thêm chức năng đăng nhập`
     - `fix: Sửa lỗi đăng xuất`

   - Mô tả chi tiết những gì đã thay đổi, lý do và cách kiểm tra.

   - Các từ khoá liên kết issue: (để tự động đóng issue khi PR được merge)

     - close
     - closes
     - closed
     - fix
     - fixes
     - fixed
     - resolve
     - resolves
     - resolved

9. Review & Merge

   - Khi bạn tạo Pull Request, bot tự động (coderabbitai) sẽ kiểm tra tối ưu mã nguồn và chính tả, đưa ra nhận xét tự động.
   - Sau đó, các thành viên khác trong dự án sẽ tiếp tục review thủ công, góp ý hoặc yêu cầu chỉnh sửa nếu cần.
   - Chỉ khi vượt qua cả hai bước review này, PR mới được xem xét để hợp nhất vào dự án chính.
