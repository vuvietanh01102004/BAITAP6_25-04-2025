# Bài tập 6: Hệ quản trị CSDL
## Chủ đề: Câu lệnh Select
## Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

# DEADLINE: 23H59:59 NGÀY 25/4/2025

## Ghi chú: Giải thích tại sao lại có SQL như vậy
## Bài làm
1. Nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server
- Tạo Database mới:
![image](https://github.com/user-attachments/assets/6877c666-dc77-4963-ad76-3447b416856b)
![image](https://github.com/user-attachments/assets/d2f24585-899e-4c32-853c-b4c3b4a6d693)
- Tiến hành kiểm tra dữ liệu trong bảng:
![image](https://github.com/user-attachments/assets/2ba55dac-6e29-4f5a-a415-5768bff77267)
2. Dữ liệu của bản thân sinh viên
```
SELECT *
FROM [SV]
WHERE ten = N'Anh'
AND ns = N'2004-10-01'
AND sdt = N'339561298';
```
![image](https://github.com/user-attachments/assets/c5a771e2-e3cc-4ec6-9230-c2ded2ad6751)
3. Nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm
```
SELECT * FROM SV
WHERE ns = '2004-10-01';
```
![image](https://github.com/user-attachments/assets/bd719e6f-33e4-4d4d-ab3b-1d9851c59223)
4. Nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh
```
SELECT * FROM SV
WHERE DAY(ns) = 01 AND MONTH(ns) = 10;
```
![image](https://github.com/user-attachments/assets/9d5aab58-d0e3-424f-9100-d695dd846086)
5. Nhập sql để tìm xem có những sv nào trùng tháng và năm sinh
![Uploading image.png…]()



