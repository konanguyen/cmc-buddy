# Seminar Biểu diễn ảnh bằng các vector đặc trưng chiều cao, tối ưu đồ thị EMR và tính toán xếp hạng ảnh trong CBIR

* **Nguồn:** [https://cmcu.edu.vn/seminar-bieu-dien-anh-bang-cac-vector-dac-trung-chieu-cao-toi-uu-do-thi-emr-va-tinh-toan-xep-hang-anh-trong-cbir/](https://cmcu.edu.vn/seminar-bieu-dien-anh-bang-cac-vector-dac-trung-chieu-cao-toi-uu-do-thi-emr-va-tinh-toan-xep-hang-anh-trong-cbir/)
* **Ngày đăng:** 2023-01-07T01:16:53+00:00
* **Danh mục:** su_kien_hop_tac

---

## Seminar Biểu diễn ảnh bằng các vector đặc trưng chiều cao, tối ưu đồ thị EMR và tính toán xếp hạng ảnh trong CBIR

Ngày 05/01 vừa qua, Khoa Công nghệ Thông tin & Truyền thông tổ chức seminar Biểu diễn ảnh bằng các vector đặc trưng chiều cao, tối ưu đồ thị EMR (Xếp hạng đa tạp hiệu quả) và tính toán xếp hạng ảnh trong CBIR (Truy vấn ảnh theo nội dung) với sự tham gia của các thầy cô hội đồng chuyên môn khoa CNTT&TT và các nhà khoa học quan tâm đến chủ đề báo cáo.

Tham dự sự kiện có sự có mặt của TS Nguyễn Ngọc Bình – Hiệu trưởng Trường Đại học CMC, TS. Nguyễn Kim Cương – Trưởng ban Đại học Số, PGS.TS Bùi Thu Lâm – Chủ tịch Hội đồng Chuyên môn Khoa; PGS.TS Đỗ Văn Thành – Giám đốc Chương trình Đào tạo Công nghệ Thông tin, Phó Chủ tịch Hội đồng Chuyên môn Khoa với sự trình bày của TS Ngô Hoàng Huy – Trường Đại học CMC và ThSHoàng Văn Quý – Trường Đại học Hồng Đức.

Nội dung seminar trình bày 2 kết quả nghiên cứu mới về CBIR dựa trên thuật toán EMR:

Vấn đề 1, xác định các anchor points của EMR dựa trên thuật toán phân cụm mới kiểu C-means với điều kiện dữ liệu lớn (số vector, số cụm và số chiều của các vector đều rất lớn). Thuật toán (tạm gọi là LDM-FCM) được xây dựng với tính toán song song trên GPU, sử dụng kỹ thuật tìm kiếm vector ANN (approximate nearest neighbor) để tối ưu xử lý phân cụm C-means trên tập dữ liệu vector đặc trưng kiểu local data manifold (các vector được kết hợp từ các đặc trưng mức thấp và các đặc trưng trích xuất từ các mạng học sâu đã huấn luyện  và có kết hợp kỹ thuật fine-turning).

Vấn đề 2, tối ưu quá trình xây dựng đồ thị EMR và tính toán xếp hạng dataset ảnh theo ảnh truy vấn khi ảnh được biểu diễn bằng các vector chiều cao và số anchor points rất lớn. Thuật toán (tạm gọi là HD-EMR) đã sử dụng LDM-FCM để xác định anchor points của EMR,đồng thời sử dụng  kỹ thuật tìm kiếm vector ANN để tính các ma trận biểu diễn đồ thị quan hệ giữa các vector ảnh của EMR.

Cuối cùng một thủ tục lặp tính toán trên các ma trận thưa, không sử dụng các ma trận nghịch đảo cỡ lớn, tối ưu về tài nguyên (bộ nhớ và thời gian) được thiết lập để xếp hạng dataset ảnh theo ảnh truy vấn.

Hiện nay ngoài các bộ mô tả ảnh theo low-level feature (đặc trưng mức thấp, LF) truyền thống, các bộ mô tả ảnh bằng các Deep feature embedding (DFE) đã được ứng dụng rộng rãi và có hiệu suất rất cao trong truy vấn ảnh theo nội dung (CBIR).

Một dataset, qua các bộ mô tả ảnh DFE sẽ được xem như là một local data manifold với vector biểu diễn là chiều rất cao, và do đặc tính đa tạp các độ đo khoảng cách global kiểu Euclidean, cosin sẽ được thay thế bằng các độ đo local để đo độ tương tự ảnh.

EMR (xếp hạng đa tạp hiệu quả)là một thuật toán xếp hạng theo tiếp cận data manifold được ứng dụng rộng rãi trong CBIR, bằng cách biểu diễn quan hệ tương tự giữa các vectors thông qua một anchor point chung trong lân cận, tính “cong” của manifold đã được biểu diễn tốt với EMR.

Tuy vậy EMR được ứng dụng chủ yếu cho ảnh với các biểu diễn LF, và giả định rằng số anchor vectors không quá lớn. Do đó để có thể ứng dụng được EMR cho xếp hạng các local data manifold biểu diễn dataset ảnh nhúng trong không gian Euclidean chiều rất cao,  đồ thị EMR và xếp hạng hiệu quả cần được cải tiến bước về trích chọn anchor points, tối ưu bộ nhớ và thời gian tính toán.
