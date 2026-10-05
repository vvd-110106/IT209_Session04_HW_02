# Báo cáo Bài 2: Quản lý nhánh và Giải quyết xung đột (Merge Conflict)

## 1. Mô tả quy trình thực hiện & Tạo xung đột

1. **Khởi tạo nội dung ban đầu:**
   Tạo file `README.md` trên nhánh `main` với nội dung ban đầu và thực hiện commit.

2. **Tạo nhánh tính năng:**
   Tạo và chuyển sang nhánh `feature-update`:
   `git checkout -b feature-update`

3. **Chỉnh sửa trên nhánh `feature-update`:**
   Sửa dòng 1 thành `Noi dung cap nhat tu nhanh feature-update`, sau đó commit.

4. **Chỉnh sửa trên nhánh `main`:**
   Chuyển về `main` (`git checkout main`), sửa cùng dòng 1 thành `Noi dung cap nhat tu nhanh main`, sau đó commit.

5. **Kích hoạt Merge Conflict:**
   Chạy lệnh gộp nhánh:
   `git merge feature-update`
   Git thông báo xung đột tại file `README.md` do cả 2 nhánh cùng sửa đổi ở cùng vị trí dòng code.

---

## 2. Các bước giải quyết xung đột thủ công

1. Mở tệp `README.md` để kiểm tra các thẻ đánh dấu xung đột từ Git:
   ```text
   <<<<<<< HEAD
   Noi dung cap nhat tu nhanh main
   =======
   Noi dung cap nhat tu nhanh feature-update
   >>>>>>> feature-update