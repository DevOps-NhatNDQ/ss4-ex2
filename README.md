"Nội dung được cập nhật trực tiếp trên nhánh main"
Nội dung được cập nhật từ nhánh feature-update

Báo cáo Bài 2: Quản lý nhánh và Giải quyết xung đột (Merge Conflict)

1. Nội dung file README.md (Sau khi đã giải quyết xung đột)
Nội dung đã được giải quyết xung đột: Kết hợp cập nhật từ main và feature-update.

2. Quy trình xử lý xung đột thủ công
- Bước 1: Tạo nhánh `feature-update`, cập nhật dòng 1 tệp `README.md` và commit.
- Bước 2: Quay lại nhánh `main`, cập nhật cùng dòng 1 tệp `README.md` nội dung khác và commit.
- Bước 3: Chạy `git merge feature-update` từ nhánh `main`, Git thông báo Merge Conflict ở `README.md`.
- Bước 4: Mở tệp `README.md`, tiến hành xóa thủ công các ký hiệu `<<<<<<< HEAD`, `=======`, `>>>>>>> feature-update` và chỉnh sửa lại nội dung hoàn chỉnh.
- Bước 5: Thực hiện `git add README.md` và `git commit -m "Merge branch 'feature-update' into main and resolve conflict"`.

3. Lịch sử đồ thị nhánh (git log --graph --oneline)
```
*   ea5d461 (HEAD -> master) Merge branch 'feature-update' into main and resolve conflict
|\
| * e8bdb3c (feature-update) Update README from feature-update branch
* | d0718e5 Update README from main branch
|/
* a9849f7 init project
```

