## MUSIC MOOD AI - GỢI Ý NHẠC THEO TÂM 
Hệ thống gợi ý chọn nhạc theo tâm trạng giúp người dùng tìm bài hát phù hợp với cảm xúc hiện tại như vui, buồn, căng thẳng hay thư giãn. Dựa trên dữ liệu bài hát và lịch sử nghe, hệ thống cá nhân hóa gợi ý nhằm cải thiện tâm trạng và trải nghiệm nghe nhạc.
KEY: AIzaSyC2lvCkyog_2jgCCfgtXNG5ixrsBjhjZXc

**1. Giới thiệu**

**Music Mood AI** là một hệ thống gợi ý âm nhạc thông minh dựa trên tâm trạng người dùng, sử dụng mô hình ngôn ngữ lớn của Google Gemini kết hợp với Vector Database (ChromaDB) và kỹ thuật Semantic Search.

Người dùng chỉ cần mô tả cảm xúc hoặc trạng thái hiện tại, hệ thống sẽ tự động:

- Hiểu ngữ nghĩa tâm trạng
- Truy xuất bài hát phù hợp nhất
- Phát nhạc trực tiếp từ YouTube
= Tránh lặp lại các bài đã nghe trong cùng phiên

**2. Mục tiêu của đề tài**

- Ứng dụng AI để hiểu và xử lý ngôn ngữ tự nhiên (Natural Language Processing)
- Xây dựng hệ thống gợi ý dựa trên ngữ nghĩa thay vì từ khóa
- Cá nhân hóa trải nghiệm nghe nhạc theo cảm xúc
- Minh họa mô hình AI thực tế có thể triển khai và mở rộng

**3. Tổng quan mô hình hệ thống**

Luồng xử lý chính

1. Người dùng nhập mô tả tâm trạng
2. AI tạo embedding cho văn bản đầu vào
3. Truy vấn vector similarity trong ChromaDB
4. Chọn bài hát phù hợp (ưu tiên bài chưa nghe)
5. AI tạo câu dẫn ngắn theo ngữ cảnh
6. Hiển thị và phát nhạc qua giao diện Gradio

**4. Kiến trúc AI & RAG**
**4.1. Embedding**

- Mỗi bài hát được biểu diễn dưới dạng embedding vector
- Nội dung embedding bao gồm:
  + Tên bài hát
  + Mô tả vibe / cảm xúc
- Embedding được tạo bằng mô hình text-embedding-004

**5.2. Vector Database (ChromaDB)**

- Lưu trữ embedding của playlist
- Thực hiện semantic search dựa trên cosine similarity
- Truy vấn tối đa 30 kết quả để tăng khả năng lựa chọn

**5.3. Generative AI**

Gemini được dùng để:

- Viết câu dẫn ngắn theo ngữ cảnh tâm trạng
- Tăng trải nghiệm cảm xúc cho người dùng
