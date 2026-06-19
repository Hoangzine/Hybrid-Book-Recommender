# Hệ thống gợi ý sách lai (Hybrid Book Recommender System)

## 📌 Tổng quan dự án
Xây dựng hệ thống gợi ý sách cá nhân hóa, giải quyết triệt để bài toán "Cold-Start" (khởi động lạnh) cho 3 nhóm đối tượng: người dùng lõi, người dùng ít tương tác và người dùng mới.

## 🛠 Tech Stack
* **Ngôn ngữ:** Python
* **Thư viện:** Pandas, Scikit-learn, Implicit, Ipywidgets, Seaborn
* **Thuật toán:** Alternating Least Squares (ALS), TF-IDF, Cosine Similarity

## 🚀 Quy trình thực hiện
1. **Khai phá dữ liệu:** Tiền xử lý bộ dữ liệu Book-Crossing quy mô lớn với hơn 271.000 cuốn sách và 1.1 triệu lượt đánh giá. Xử lý bài toán dữ liệu thưa (độ thưa 99.99%) và phân phối đuôi dài (long-tail).
2. **Xây dựng mô hình (Hybrid Approach):** * *Lọc cộng tác ALS:* Khai thác Latent Factors cho nhóm người dùng lõi.
   * *Content-Based:* Ứng dụng TF-IDF và Cosine Similarity theo tác giả/NXB cho nhóm ít tương tác.
   * *Popularity-Based:* Dành cho nhóm người dùng mới.
3. **Đánh giá hiệu năng:** Đo lường mô hình qua các chỉ số khắt khe: Precision@K, Recall@K, MAP@10, AUC.
4. **Tối ưu hóa:** Tích hợp ipywidgets để trích xuất gợi ý nhanh chóng (on-the-fly), tối ưu dung lượng bộ nhớ.
