# 🎓 CMC Buddy — Academic & Admissions Advisor Skill for Antigravity

[![Antigravity Skill](https://img.shields.io/badge/Antigravity-Skill-blue.svg)](https://antigravity.google)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Institution: CMC University](https://img.shields.io/badge/Institution-CMC_University-red.svg)](https://cmcu.edu.vn)

**CMC Buddy** là bộ kỹ năng (Skill) thông minh dành cho trợ lý AI Antigravity, đóng vai trò là chuyên gia **Cố vấn Tuyển sinh & Quy chế Đào tạo** toàn diện của **Trường Đại học CMC (CMC University)**. 

Skill được thiết kế theo kiến trúc **RAG (Retrieval-Augmented Generation)** với kho tri thức dày đặc, đã được lọc sạch 100% tạp âm, quảng cáo và đường dẫn rác, giúp Agent trả lời nhanh chóng, chính xác tuyệt đối và trích dẫn chuẩn theo văn bản quy chế chính thức.

---

## 🌟 Tính Năng Nổi Bật

### 1. 🏛️ Tra cứu Cơ sở & Địa chỉ đào tạo
* Cung cấp địa chỉ chính xác của tất cả các cơ sở tại **Hà Nội** (Trụ sở Duy Tân Cầu Giấy, Cơ sở 1 & 2 Hà Đông, Cơ sở 3 Tây Mỗ) và **TP. Hồ Chí Minh** (Cơ sở Tân Thuận - CMC Creative Space Q7).

### 2. 📝 Tư vấn Tuyển sinh & Kỳ thi CMC-TEST
* Hướng dẫn chi tiết các phương thức xét tuyển: Điểm thi tốt nghiệp THPT, Học bạ THPT, Tuyển thẳng, Điểm thi ĐGNL (ĐHQGHN, ĐHQG-HCM) và kỳ thi đánh giá năng lực **CMC-TEST**.
* Điểm chuẩn trúng tuyển các ngành qua các năm.

### 3. 💰 Chính sách Học phí & Quỹ Học bổng
* Biểu phí chi tiết theo từng kỳ và từng năm học.
* Điều kiện cấp và **quy định duy trì học bổng** Quỹ *"CMC – Vì bạn xứng đáng"* (100%, 70%, 50% học phí):
  - Yêu cầu GPA tích lũy năm $\ge 3.0/4.0$.
  - Không nợ môn / không bị điểm F trong năm học xét duyệt.
* Tiêu chuẩn xét Học bổng Khuyến khích học tập (KKHT).

### 4. 📚 Cố vấn Các Ngành & Chương trình Đào tạo
* Thông tin chi tiết 5 Khoa đào tạo và hơn 15 chuyên ngành mũi nhọn:
  - **Khoa CNTT & TT (FICT):** Trí tuệ nhân tạo (AI), Khoa học máy tính, Kỹ thuật phần mềm, Công nghệ thông tin, An ninh mạng (Cyber Security).
  - **Khoa Kinh doanh & Quản lý (FBM):** Digital Marketing, Kinh doanh quốc tế, Logistics & Quản lý chuỗi cung ứng, Thương mại điện tử.
  - **Khoa Mỹ thuật & Thiết kế (FAD):** Thiết kế mỹ thuật số, Đồ họa Game.
  - **Khoa Truyền thông & Marketing (FIMC):** Quan hệ công chúng (PR), Truyền thông đa phương tiện.
  - **Khoa Ngôn ngữ & Văn hóa (FLC):** Ngôn ngữ Trung (Chương trình liên kết 2+2 với ĐH Sư phạm Thủ đô Bắc Kinh), Ngôn ngữ Hàn, Ngôn ngữ Nhật, Ngôn ngữ Anh.

### 5. ⚖️ Quy chế Học vụ & Điều kiện Tốt nghiệp
* Thời gian đào tạo & Khung tín chỉ: **Cử nhân** (9 học kỳ, 120-135 TC) vs **Kỹ sư** (11 học kỳ, 150-164 TC).
* Chuẩn đầu ra Ngoại ngữ: **Hệ Chuẩn (SM)** đạt Bậc 3/6 (B1 CEFR), **Hệ Song ngữ (GM)** đạt Bậc 4/6 (B2 CEFR).
* Quy định thi lại (điểm tối đa mức C), học lại (lấy điểm cao nhất), cảnh báo học tập và xét điều kiện tốt nghiệp.

### 6. 📰 Kho dữ liệu hơn 1.100 bài viết chính thức
* Tích hợp hơn 1.100 bài viết tin tức, hướng nghiệp, đời sống sinh viên, gương mặt thủ khoa, sự kiện hợp tác quốc tế (Tsinghua SIGS, Steinbeis Đức, Woori Bank...) kèm file chỉ mục `articles_index.json`.

---

## 📖 Nguồn Dữ Liệu (Data Sources)

Dữ liệu trong bộ Skill được thu thập và thẩm định từ các nguồn chính thống:
1. **Văn bản pháp lý nội bộ:** Quyết định số `22/2023/QĐ-ĐHCMC-HĐT` ngày 01/12/2023 của Chủ tịch Hội đồng Trường Đại học CMC về việc ban hành *Quy chế đào tạo trình độ đại học*.
2. **Cổng thông tin điện tử chính thức:** [https://cmcu.edu.vn/](https://cmcu.edu.vn/)
3. **Cổng tuyển sinh Đại học CMC:** [https://xettuyen.cmcu.edu.vn/](https://xettuyen.cmcu.edu.vn/)

---

## 📂 Cấu Trúc Thư Mục Skill

```text
.agents/skills/cmc-buddy/
├── README.md                          # Tài liệu giới thiệu & hướng dẫn cài đặt skill
├── SKILL.md                           # File cấu hình & chỉ dẫn hành vi chính cho Agent
└── references/                        # Kho tri thức tham chiếu RAG (đã lọc sạch tạp âm)
    ├── quy_che_dao_tao.md             # Toàn văn 27 Điều Quy chế đào tạo đại học ĐH CMC
    ├── dia_chi_co_so.md               # Địa chỉ trụ sở & các cơ sở đào tạo HN & TP.HCM
    ├── thong_tin_tuyen_sinh.md        # Đề án tuyển sinh, điểm chuẩn, kỳ thi CMC-TEST
    ├── chinh_sach_hoc_bong.md         # Quy định học phí, học bổng tuyển sinh & KKHT
    ├── cac_nganh_dao_tao.md           # Chi tiết các khoa và ngành đào tạo
    ├── campus_tieng_anh_giang_vien.md # Lộ trình tiếng Anh, Campus, giảng viên, Humans of CMCU
    └── articles/                      # Hơn 1.100 bài viết phân loại theo danh mục
        ├── articles_index.json        # Chỉ mục tìm kiếm nhanh (Title, Date, Category, Excerpt)
        ├── tuyen_sinh/                # Bài viết chuyên đề tuyển sinh & nhập học
        ├── hoc_bong/                  # Bài viết học bổng & gương mặt sinh viên xuất sắc
        ├── nganh_hoc_nghe_nghiep/     # Bài viết phân tích ngành nghề & thị trường việc làm
        ├── su_kien_hop_tac/           # Bài viết sự kiện, hợp tác quốc tế & doanh nghiệp
        └── tin_tuc_chung/             # Bài viết tin tức hoạt động chung
```

---

## 💻 Hướng Dẫn Cài Đặt & Sử Dụng

### Cách 1: Sử dụng trong Project Workspace (Khuyên dùng)
Đặt thư mục `cmc-buddy` vào thư mục `.agents/skills/` tại gốc workspace của bạn:
```bash
your-project/
└── .agents/
    └── skills/
        └── cmc-buddy/
```

### Cách 2: Cài đặt Toàn cục (Global Skill cho mọi Workspace)
Sao chép thư mục `cmc-buddy` vào thư mục cấu hình Antigravity của người dùng:
* **Windows:** `C:\Users\<Your-Username>\.gemini\antigravity\builtin\skills\cmc-buddy\`
* **macOS / Linux:** `~/.gemini/antigravity/builtin/skills/cmc-buddy/`

### 🚀 Cách kích hoạt Skill:
Agent Antigravity sẽ **tự động kích hoạt** kỹ năng này bất cứ khi nào bạn đặt câu hỏi liên quan đến Trường Đại học CMC, ví dụ:
* *"Trường Đại học CMC có những cơ sở nào?"*
* *"Kỳ thi CMC-TEST gồm những môn gì?"*
* *"Học bổng 100% của CMC cần duy trì điểm GPA bao nhiêu?"*
* *"Ngành Trí tuệ nhân tạo (AI) tại CMC học mấy năm và có chuẩn đầu ra tiếng Anh thế nào?"*

---

## 👤 Tác Giả & Bản Quyền

* **Tác giả:** konanguyen
* **Email:** [ng.hao2711@gmail.com](mailto:ng.hao2711@gmail.com)
* **Phiên bản:** 1.0.0 (Cập nhật tháng 08/2026)
* **Giấy phép:** MIT License
