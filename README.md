# Research Publication Trend Analyzer 📊🔬

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![OpenAlex API](https://img.shields.io/badge/API-OpenAlex-E65100?style=for-the-badge)
![Charts](https://img.shields.io/badge/Charts-fl__chart-4CAF50?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**Ứng dụng di động phân tích xu hướng công bố nghiên cứu khoa học toàn cầu sử dụng OpenAlex API**

</div>

---

## 🌟 1. Giới thiệu Dự án (Project Overview)

**Research Publication Trend Analyzer** là ứng dụng di động trên nền tảng **Flutter** kết nối trực tiếp với cơ sở dữ liệu mở **OpenAlex API** (hơn 250 triệu tài liệu học thuật toàn cầu). Ứng dụng cung cấp các biểu đồ trực quan hóa dữ liệu theo thời gian thực, cho phép các nhà nghiên cứu, giảng viên và sinh viên nhanh chóng nắm bắt tốc độ phát triển của các chủ đề khoa học, phân bố ấn phẩm qua các năm, các tác giả hàng đầu và nguồn tài liệu trích dẫn uy tín.

---

## 🚀 2. Các Tính năng Chính (Key Features)

### 📈 1. Phân tích Xu hướng Nghiên cứu (Trend Analysis Screen)
- **Biểu đồ động trực quan (`fl_chart`):** Hiển thị số lượng công bố khoa học và số lượt trích dẫn theo từng mốc thời gian (Line Chart & Bar Chart).
- **Bộ lọc thông minh:** Lọc xu hướng theo lĩnh vực (Computer Science, Medicine, AI, Engineering...), khoảng năm xuất bản và tổ chức nghiên cứu.

### 🔍 2. Tra cứu & Tìm kiếm Nâng cao (Search Screen)
- Tìm kiếm theo từ khóa bài báo, tên tác giả, DOI hoặc tạp chí khoa học (Journal/Conference).
- Hiển thị danh sách kết quả trực quan kèm hiệu ứng chờ `shimmer` và ảnh minh họa tối ưu với `cached_network_image`.

### 📋 3. Chi tiết Bài báo Khoa học (Publication Detail Screen)
- Hiển thị đầy đủ thông tin: Tiêu đề bài báo, danh sách tác giả, tóm tắt nội dung (Abstract), chỉ số trích dẫn (Citations count).
- Mở liên kết trực tiếp tới trang xuất bản gốc thông qua `url_launcher`.

### 📊 4. Dashboard Tổng quan (Dashboard Screen)
- Thống kê các chủ đề nghiên cứu nổi bật đang là "hot trend" trong cộng đồng khoa học quốc tế.
- Lưu trữ lịch sử tìm kiếm và đánh dấu bài báo yêu thích.

---

## 🛠 3. Kiến trúc & Công nghệ (Tech Stack)

| Lĩnh vực | Thư viện / Công nghệ | Vai trò trong hệ thống |
| :--- | :--- | :--- |
| **Mobile Core** | **Flutter SDK (>=3.0.0 <4.0.0)** | Bộ công cụ phát triển giao diện đa nền tảng |
| **Ngôn ngữ** | **Dart** | Ngôn ngữ phát triển chính |
| **Dữ liệu Khoa học**| **OpenAlex REST API** | Nguồn dữ liệu bài báo và trích dẫn mở toàn cầu |
| **Trực quan hóa** | **fl_chart (^0.66.2)** | Vẽ biểu đồ đường, biểu đồ cột tương tác mượt mà |
| **State Management**| **Provider (^6.1.1)** | Quản lý trạng thái và luồng dữ liệu bất đồng bộ |
| **Network & HTTP** | **http (^1.1.0)** | Gửi yêu cầu RESTful đến OpenAlex API |
| **UI Polish** | **shimmer, google_fonts** | Hiệu ứng tải dữ liệu mượt mà và font chữ Google Fonts |
| **Utilities** | **intl, url_launcher** | Định dạng ngày tháng, số lượng và điều hướng liên kết ngoài |

---

## 📂 4. Cấu trúc Thư mục Mã nguồn (Source Code Tree)

```
research-publication-trend-analyzer/
├── lib/
│   ├── main.dart                          # Điểm khởi chạy ứng dụng & Provider setup
│   ├── screens/
│   │   ├── dashboard_screen.dart          # Màn hình Dashboard tổng quan xu hướng
│   │   ├── trend_analysis_screen.dart     # Màn hình biểu đồ phân tích xu hướng chuyên sâu
│   │   ├── search_screen.dart             # Màn hình tìm kiếm ấn phẩm khoa học
│   │   └── publication_detail_screen.dart # Màn hình chi tiết bài báo & trích dẫn
│   ├── widgets/
│   │   └── common_widgets.dart            # Các thành phần UI dùng chung (Cards, Shimmers, Charts)
│   └── models/                            # DTOs & Data Models ánh xạ từ OpenAlex API
├── pubspec.yaml                           # Khai báo dependencies
└── test/                                  # Kiểm thử ứng dụng
```

---

## 💻 5. Hướng dẫn Cài đặt & Chạy ứng dụng (Getting Started)

### Điều kiện tiên quyết:
- Đã cài đặt [Flutter SDK](https://docs.flutter.dev/get-started/install) phiên bản từ `3.0.0` trở lên.
- Đã cấu hình biến môi trường Android SDK hoặc Xcode (cho macOS).

### Các bước thực hiện:

1. **Clone repository về máy (nếu chưa có):**
   ```bash
   git clone https://github.com/tkiennt/research-publication-trend-analyzer.git
   cd research-publication-trend-analyzer
   ```

2. **Cài đặt các thư viện phụ thuộc:**
   ```bash
   flutter pub get
   ```

3. **Chạy ứng dụng trên thiết bị / Giả lập:**
   ```bash
   flutter run
   ```

---

## 👥 6. Đóng góp & Tác giả (Credits)

- **Dự án:** Ứng dụng phân tích dữ liệu chuyên ngành Lập trình Di động (PRM393).
- **Thành viên đóng góp:** Trung Kiên ([@tkiennt](https://github.com/tkiennt)).
- **Nguồn dữ liệu:** Được hỗ trợ bởi nền tảng dữ liệu mở khoa học [OpenAlex](https://openalex.org/).
