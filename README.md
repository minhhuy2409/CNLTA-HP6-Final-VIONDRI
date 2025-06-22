#  VIONDRI – Focused Productivity & Creative Workspace

VIONDRI là một ứng dụng được phát triển bằng SwiftUI, được thiết kế để giúp người dùng duy trì sự tập trung, lên kế hoạch, ghi chú và làm việc sáng tạo trong một không gian cá nhân hoá. Ứng dụng lấy cảm hứng từ Notion, kết hợp với khả năng trang trí kéo-thả, tích hợp âm nhạc và bảng nháp để làm việc hiệu quả.

⸻

🎯 Mục Tiêu Học Tập (Learning Objectives – SwiftUI Học phần 5)

I. Thành phần giao diện cơ bản và nâng cao (Components)
    •    Image: hiển thị và tuỳ chỉnh hình ảnh.
    •    TextField: tạo ô nhập liệu và liên kết dữ liệu bằng @State.
    •    Slider, Toggle, Picker, ProgressView, Spacer.

II. Tùy biến giao diện với Modifiers
    •    Sử dụng .padding, .frame, .font, .foregroundColor, .background, .cornerRadius, .shadow…
    •    Hiểu vai trò và thứ tự áp dụng modifiers.

III. Xây dựng Custom Components (Custom Views)
    •    Tạo View con như: PrimaryButton, TitleLabel…
    •    Tái sử dụng logic và style giao diện.

IV. Quản lý dữ liệu reactive với Property Wrappers
    •    Sử dụng @State, @Binding, @ObservedObject, @Published, @EnvironmentObject.
    •    Hiểu Source of Truth và cách giữ trạng thái khi View tái tạo.

V. Kỹ thuật Reverse Engineering
    •    Phân tích UI/UX của app mẫu, xác định model, view, logic.
    •    Dựng lại cấu trúc bằng SwiftUI từ một app thực tế.

VI. Làm việc với ForEach và List
    •    Lặp dữ liệu xác định (Identifiable), tạo view con, hỗ trợ xóa/thêm mục.

VII. Tổ chức ứng dụng với TabView
    •    Sử dụng .tabItem, enum tag, quản lý tabs bằng selection.

VIII. Thực hành tổng hợp
    •    Thiết kế models, UI nhiều màn hình (To-do, Timetable, Note, Settings…)
    •    Hiển thị có điều kiện, tương tác, định dạng dữ liệu.

⸻

🧱 Kiến Trúc & Thành phần chính của VIONDRI

📁 Models
    •    Task: Quản lý mục tiêu/to-do cá nhân.
    •    Note: Ghi chú tự do trong lúc làm việc.
    •    ScheduleItem: Thời khoá biểu theo ngày/tuần.
    •    MusicSetting: Tùy chọn kết nối Spotify/Apple Music.

📁 Views
    •    MainTabView: Giao diện chính với TabView.
    •    ToDoView, TimetableView, NoteBoardView, FocusMusicView, SettingsView

📁 Components
    •    TaskCardView, AddNoteView, TimetableCell, PrimaryButton, MusicConnectBox

📁 ViewModels
    •    TaskManager, NoteManager, ScheduleManager: Quản lý trạng thái tập trung thông qua ObservableObject.

⸻

✅ MVP – Minimum Viable Product
    1.    Tạo/lưu To-do và đánh dấu hoàn thành.
    2.    Hiển thị thời khoá biểu theo ngày.
    3.    Ghi chú nhanh (bảng nháp khi học).
    4.    Giao diện tabbar với icon và điều hướng.
    5.    Kết nối với Spotify hoặc Apple Music (mock ban đầu).

⸻

🧠 Kiến Thức Đã Áp Dụng
    •    State Management nâng cao: @State, @Binding, @ObservedObject.
    •    Modular UI với View con tái sử dụng.
    •    Kết hợp layout linh hoạt bằng VStack, HStack, ZStack, Spacer.
    •    Dữ liệu động với ForEach + Identifiable.
    •    UI/UX tối giản, dễ thao tác và mượt mà trên iOS.

⸻

📚 Tài Nguyên & Gợi Ý
    •    Figma/Sketch: Thiết kế wireframe.
    •    Git: Theo dõi tiến độ phát triển app.
    •    Swift Playgrounds / Xcode Preview: Test UI component.

⸻

💬 Gợi Ý Slogan

“VIONDRI – Create. Plan. Focus. Flow.”

“Your private space for powerful productivity.”

⸻

🧩 Phiên bản tương lai (V2.0 trở đi)
    •    Drag & drop trang trí cho bảng nháp.
    •    Nhắc lịch học/làm việc theo thói quen.
    •    Hệ thống thống kê thời gian làm việc.
    •    Cloud Sync & Đăng nhập tài khoản.

⸻

✨ Made with SwiftUI – by [Tăng Hoàng Minh Huy]

App được xây dựng từ nền móng vững chắc, với từng bước học tập – thiết kế – phát triển rõ ràng, hướng đến trải nghiệm người dùng và chất lượng code cao nhất.

