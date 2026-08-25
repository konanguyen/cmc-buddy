# 💻 CẨM NANG & QUY TẮC TỰ ĐỘNG TẠO LINK TƯ VẤN LAPTOP THEO YÊU CẦU SINH VIÊN

Tài liệu hướng dẫn AI Agent phân tích nhu cầu thực tế của từng sinh viên (ngành học, ngân sách, hãng yêu thích, cấu hình cần thiết) để **tự động sinh link bộ lọc CellphoneS tương ứng theo thời gian thực**.

---

## 🎁 1. Chính Sách Ưu Đãi Thiết Bị Của ĐH CMC (Luôn Nhắc Khi Tư Vấn)

* **Tặng iPad / Máy tính bảng:** Tân sinh viên xét tuyển sớm và đặt nguyện vọng 1, 2, 3 được tặng **01 iPad / Tablet** phục vụ E-Learning.
* **Phòng Lab máy trạm tại trường:** Miễn phí sử dụng Lab GPU AI (huấn luyện Deep Learning) và Studio bảng vẽ Wacom (cho sinh viên Thiết kế Đồ họa / Game Art) ngay tại Campus.

---

## 🧠 2. Quy Trình 4 Bước Khi Tư Vấn Laptop Cho Sinh Viên

Khi sinh viên hỏi mua laptop, Agent thực hiện theo quy trình sau:
1. **Xác định ngành học & yêu cầu phần cứng bắt buộc:**
   - **TKMTS / Game Art (FAD):** Bắt buộc có GPU rời NVIDIA RTX Series, CPU i7/Ryzen 7, RAM tối thiểu 16GB.
   - **CNTT / AI / KHMT (FICT):** Cần CPU đa nhân mạnh, RAM 16GB - 32GB (chạy Docker/máy ảo). Nếu học sâu AI/Vision cần GPU NVIDIA (nhân CUDA).
   - **Kinh doanh / Marketing / Logistics (FBM & FIMC):** Ưu tiên mỏng nhẹ, pin trâu 8-12h, RAM 16GB mở nhiều tab/dữ liệu.
   - **Ngôn ngữ (FLC):** Mỏng nhẹ, bàn phím tốt, pin bền, giá tiết kiệm.
2. **Xác định ngân sách sinh viên đưa ra** (Ví dụ: dưới 15 triệu, 18-22 triệu, trên 25 triệu...).
3. **Xác định hãng yêu thích** (nếu sinh viên có yêu cầu cụ thể như Asus, Dell, Lenovo, Apple...).
4. **Tự động ghép link CellphoneS chuẩn xác** và giải thích lý do lựa chọn cấu hình.

---

## 🛠️ 3. Bộ Quy Tắc Ghép Tham Số URL CellphoneS Động

**Cấu trúc URL gốc:** `https://cellphones.com.vn/laptop.html?{danh_sách_tham_số}&dir=asc&order=filter_price`

*(Nếu sinh viên chỉ tìm MacBook của Apple: Dùng URL gốc `https://cellphones.com.vn/laptop/mac.html?{tham_số}`)*

### Bảng Từ Điển Tham Số Ghép Link:

| Yếu tố sinh viên yêu cầu | Tên tham số URL | Cách ghép giá trị | Ví dụ cụ thể |
| :--- | :--- | :--- | :--- |
| **Ngân sách (Khoảng giá)** | `price` | `{min}-{max}` (đơn vị: VNĐ) | Dưới 15tr: `price=0-15000000`<br>15 - 20tr: `price=15000000-20000000`<br>20 - 30tr: `price=20000000-30000000`<br>Trên 25tr: `price=25000000-999999999` |
| **Hãng sản xuất** | `manufacturer` | Tên hãng viết thường, phân tách bằng dấu phẩy | Asus, Lenovo: `manufacturer=asus,lenovo`<br>Dell, HP: `manufacturer=dell,hp`<br>Apple: `manufacturer=apple`<br>MSI, Acer: `manufacturer=msi,acer` |
| **Nhu cầu sử dụng** | `nhu_cau_su_dung` | Phân tách bằng dấu phẩy theo ngành | Đồ họa/Game: `nhu_cau_su_dung=do-hoa-ky-thuat,gaming,laptop-sang-tao-noi-dung`<br>Văn phòng/Kinh tế: `nhu_cau_su_dung=hoc-tap-van-phong`<br>Cao cấp mỏng nhẹ: `nhu_cau_su_dung=hoc-tap-van-phong,cao-cap-sang-trong` |
| **Card đồ họa (VGA)** | `laptop_vga_filter` | Chọn loại card theo ngành | Đồ họa/AI (NVIDIA): `laptop_vga_filter=nvidia-geforce-series`<br>Văn phòng: `laptop_vga_filter=card-onboard`<br>AMD: `laptop_vga_filter=amd-radeon-series` |
| **Sắp xếp giá** | `order` & `dir` | Luôn thêm vào cuối link | `dir=asc&order=filter_price` (sắp xếp giá từ rẻ nhất tăng dần) |

---

## 🎯 4. Các Tình Huống Ghép Link Thực Tế Thường Gặp

* **Tình huống 1:** *"Em học Thiết kế Mỹ thuật số (TKMTS), tài chính 18 - 25 triệu, thích Asus hoặc Lenovo có card rời NVIDIA"*
  👉 `https://cellphones.com.vn/laptop.html?price=18000000-25000000&manufacturer=asus,lenovo&nhu_cau_su_dung=do-hoa-ky-thuat,laptop-sang-tao-noi-dung&laptop_vga_filter=nvidia-geforce-series&dir=asc&order=filter_price`

* **Tình huống 2:** *"Em học Trí tuệ Nhân tạo (AI), cần máy chạy mô hình Deep Learning có GPU Nvidia, ngân sách khoảng 20 - 30 triệu của Dell, Acer hoặc MSI"*
  👉 `https://cellphones.com.vn/laptop.html?price=20000000-30000000&manufacturer=dell,acer,msi&nhu_cau_su_dung=do-hoa-ky-thuat,gaming&laptop_vga_filter=nvidia-geforce-series&dir=asc&order=filter_price`

* **Tình huống 3:** *"Em là tân sinh viên Digital Marketing, cần mua máy mỏng nhẹ dưới 15 triệu"*
  👉 `https://cellphones.com.vn/laptop.html?price=0-15000000&nhu_cau_su_dung=hoc-tap-van-phong&dir=asc&order=filter_price`

* **Tình huống 4:** *"Em học Ngôn ngữ Hàn, muốn mua máy Dell hoặc HP mỏng nhẹ pin trâu từ 12 đến 18 triệu"*
  👉 `https://cellphones.com.vn/laptop.html?price=12000000-18000000&manufacturer=dell,hp&nhu_cau_su_dung=hoc-tap-van-phong&dir=asc&order=filter_price`

* **Tình huống 5:** *"Em học Quản trị Kinh doanh, muốn tìm MacBook Air M2/M3 giá tốt nhất"*
  👉 `https://cellphones.com.vn/laptop/mac/macbook-air.html?dir=asc&order=filter_price`
