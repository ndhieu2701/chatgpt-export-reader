🗂️ ChatGPT Export Viewer

Một công cụ offline giúp bạn đọc lại toàn bộ lịch sử hội thoại đã Export từ ChatGPT, bao gồm tin nhắn, ảnh, video, âm thanh, markdown, code block, v.v. — hiển thị lại đúng kiểu giao diện ChatGPT.

✨ Tính năng chính

🧠 Đọc file export gốc từ ChatGPT (conversations.json)

🖼️ Hiển thị đầy đủ nội dung: tin nhắn, markdown, code block, ảnh, video, audio

⚡ Chạy hoàn toàn offline (không cần server hay upload)

🪶 Lazy load media — ảnh/video/audio chỉ tải khi cần, load cực nhanh

📜 Phân trang tin nhắn — hiển thị 100 tin nhắn mỗi lần để tránh lag

💾 Tương thích export gốc từ ChatGPT, bao gồm file đính kèm (file-service://...)

🔒 Không gửi dữ liệu ra ngoài, toàn bộ xử lý nội bộ trình duyệt

🧩 Cấu trúc thư mục export ChatGPT

Khi bạn “Export Data” từ ChatGPT (Settings → Data Controls → Export), bạn sẽ nhận được một file .zip.
Sau khi giải nén, bạn sẽ thấy thư mục chứa:

chatgpt-export/
│
├── conversations.json     ← 📄 file chứa toàn bộ lịch sử hội thoại
├── file_0000000xxxxx.png  ← 📸 ảnh đính kèm
├── file_0000000xxxxx.mp4  ← 🎥 video
├── file_0000000xxxxx.wav  ← 🎧 audio
└── ... các file khác ...

⚙️ Cách sử dụng
1️⃣ Tải file viewer

Tải file index.html từ repository này
→ hoặc copy nội dung trong file index.html
.

2️⃣ Đặt file index.html chung thư mục export

Ví dụ:

C:\ChatGPTExport\
   ├─ conversations.json
   ├─ file_1234abcd.png
   ├─ file_5678efgh.mp4
   ├─ index.html   ← 📄 đặt file này tại đây

3️⃣ Mở trình duyệt & load dữ liệu

Mở file index.html bằng trình duyệt bất kỳ (Chrome, Edge, Firefox).
→ Mở trực tiếp bằng file:/// (không cần server).

Chọn thư mục chứa file conversations.json.

Chọn hội thoại muốn xem từ sidebar bên trái.

4️⃣ Trình xem hội thoại

Giao diện hiển thị bao gồm:

Thành phần	Mô tả
📂 Sidebar	Danh sách tất cả hội thoại (theo title)
💬 Cửa sổ chính	Hiển thị tin nhắn user & ChatGPT theo đúng thứ tự
🖼️ Media	Ảnh, video, âm thanh, link được hiển thị tự động
🔽 Nút “Tải thêm”	Dùng khi hội thoại có nhiều hơn 100 tin nhắn
💡 Lưu ý kỹ thuật

File viewer chỉ hoạt động nếu index.html nằm cùng thư mục export (hoặc ở gốc cùng cấp).

Nếu bạn mở từ nơi khác, đường dẫn file:// có thể bị trình duyệt chặn vì lý do bảo mật.

Tất cả hình ảnh, video, audio được tải trực tiếp từ ổ đĩa, không có upload lên Internet.
