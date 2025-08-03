🧠 1. Ý tưởng & Tầm nhìn

🎯 Mục tiêu:
	•	Tạo một không gian làm việc sáng tạo, tập trung, đẹp mắt, thay thế Notion/GG Keep cho học sinh, sinh viên, người làm việc độc lập.
	•	Có timeline, to-do, draftboard, kết hợp âm nhạc giúp “vào flow”.

🔥 Khác biệt so với Notion:
	•	Tối ưu thao tác chạm/kéo-thả cho iOS/iPadOS
	•	Giao diện tối giản + cảm xúc (màu, nhạc, sticker, theme)
	•	Có “draftboard” như bảng nháp tự do
	•	Kết nối Apple Music/Spotify dễ dàng
	•	Gợi ý phương pháp học/làm việc theo chiến lược (Strategy)

⸻

🏗️ 2. Kiến trúc tổng thể

📁 Models/
    ├─ Task.swift
    ├─ DraftElement.swift
    ├─ Strategy.swift
    ├─ User.swift
    ├─ Song.swift, Playlist.swift
    ├─ Theme.swift
    └─ AppState.swift

📁 Views/
    ├─ MainTabView.swift
    ├─ PlannerView.swift
    ├─ DraftboardView.swift
    ├─ MusicView.swift
    ├─ ProfileView.swift
    └─ Subfolders/: Planner/, Draftboard/, Music/, Profile/

📁 Components/
    ├─ TaskCard.swift
    ├─ StrategyCard.swift
    ├─ ThemePreviewTile.swift
    ├─ VinylDiscView.swift
    ├─ ProfileCard.swift
    ├─ EmojiSticker.swift
    └─ ToolbarButton.swift

📁 Data/
    ├─ TaskData.swift
    ├─ StrategyData.swift
    ├─ StickerLibrary.swift
    ├─ MusicSampleData.swift
    └─ FriendListData.swift

🛠️ 3. Các tính năng MVP (Minimum Viable Product)

📅 PLANNER VIEW
	•	Hiển thị to-do theo ngày, có thể kéo-thả thay đổi thứ tự
	•	Thêm/sửa/xoá Task
	•	Deadline highlight + nhắc nhở
	•	Gắn màu/nhãn/emoji cho task
	•	Bộ lọc theo priority, category

🎨 DRAFTBOARD VIEW
	•	Kéo-thả sticker, note, hình ảnh
	•	Ghi chú text tự do (drag/resize)
	•	Giao diện như bảng trắng (zoom/pan nhẹ)
	•	Gợi ý theo chiến lược học tập (liên kết với Strategy)

🎧 MUSIC VIEW
	•	Hiển thị bài hát, playlist mẫu
	•	Giao diện vinyl/CD quay
	•	Kết nối Spotify / Apple Music API
	•	Điều khiển nhạc + lưu playlist cá nhân

🧠 STRATEGY SYSTEM
	•	Hiển thị các chiến lược học/làm việc hiệu quả
	•	Chọn chiến lược áp dụng cho tuần/tháng
	•	Tích hợp nhắc nhở/gợi ý vào planner/draftboard
	•	Gợi ý task layout theo từng strategy (eg. Pomodoro, Deep Work)

👤 PROFILE VIEW
	•	Thông tin cá nhân (avatar, tên, email…)
	•	Chọn theme, sticker yêu thích
	•	Giao diện “Profile Card” đẹp mắt chia sẻ được
	•	Giao diện setting cho chiến lược ưa thích

⸻

🧩 4. Tính năng bổ sung sau MVP
	•	iCloud sync hoặc local persistence (CoreData/UserDefaults)
	•	Widget nhỏ hiển thị task/draft
	•	Chế độ Focus: Tạm ẩn distractor, mở nhạc
	•	Tính năng bạn bè: Thêm bạn, xem chiến lược của nhau
	•	Chế độ học nhóm (beta)

⸻

✨ 5. Thiết kế giao diện (UI/UX)
	•	Style: Minimalist + Creative
	•	Màu: tông pastel, gradient nhẹ
	•	Font: Rounded, dễ đọc (San Francisco Rounded, Avenir)
	•	Component có: Shadow, bo góc 2xl, animation mượt (Framer Motion hoặc SwiftUI .transition)
	•	Kéo-thả trực quan, hỗ trợ cảm ứng
