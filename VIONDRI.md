#  📦 VIONDRI – Cấu trúc Model, Views, Data và Components

Dựa trên MVP của app VIONDRI:

    1.    To-do List ✅
    2.    Timetable 📅
    3.    Note Board ✍️
    4.    TabBar UI 🧭
    5.    Kết nối nhạc 🎧

⸻

📁 Models

Task.swift

struct Task: Identifiable, Codable {
    var id = UUID()
    var title: String
    var isCompleted: Bool = false
    var dueDate: Date?
}

Note.swift

struct Note: Identifiable, Codable {
    var id = UUID()
    var content: String
    var createdAt: Date = Date()
}

ScheduleItem.swift

struct ScheduleItem: Identifiable, Codable {
    var id = UUID()
    var title: String
    var startTime: Date
    var endTime: Date
    var day: String // ví dụ: "Monday", "Tuesday"
}

MusicSetting.swift

struct MusicSetting: Codable {
    var isConnected: Bool
    var service: MusicService
}

enum MusicService: String, Codable, CaseIterable {
    case spotify, appleMusic
}


⸻

📁 Views

MainTabView.swift
    •    Tab bar gồm: To-Do, Timetable, Notes, Music, Settings

ToDoView.swift
    •    Hiển thị danh sách công việc
    •    Thêm, xoá, đánh dấu hoàn thành

TimetableView.swift
    •    Hiển thị thời khoá biểu theo ngày
    •    Lựa chọn ngày, xem các lớp học

NoteBoardView.swift
    •    Ghi chú nhanh
    •    Hiển thị danh sách ghi chú

FocusMusicView.swift
    •    Giao diện kết nối với Spotify/Apple Music
    •    Nút connect/disconnect

SettingsView.swift
    •    Thay đổi tên, theme, âm nhạc yêu thích…

⸻

📁 Data

SampleData.swift

let sampleTasks = [
    Task(title: "Ôn Toán chương 5"),
    Task(title: "Viết dàn ý Văn"),
    Task(title: "Tập gym 30 phút", isCompleted: true)
]

let sampleNotes = [
    Note(content: "Lập dàn ý bài luận tiếng Anh."),
    Note(content: "Ghi lại công thức đạo hàm bậc 2.")
]

let sampleSchedule = [
    ScheduleItem(title: "Tiết 1: Toán", startTime: Date(), endTime: Date().addingTimeInterval(3600), day: "Monday"),
    ScheduleItem(title: "Tiết 2: Lý", startTime: Date(), endTime: Date().addingTimeInterval(7200), day: "Monday")
]


⸻

📁 Components

TaskCardView.swift

struct TaskCardView: View {
    var task: Task
    var body: some View {
        HStack {
            Image(systemName: task.isCompleted ? "checkmark.circle.fill" : "circle")
                .foregroundColor(task.isCompleted ? .green : .gray)
            Text(task.title)
                .strikethrough(task.isCompleted)
            Spacer()
        }
        .padding()
        .background(Color(.systemBackground))
        .cornerRadius(12)
        .shadow(radius: 2)
    }
}

ScheduleCell.swift

struct ScheduleCell: View {
    var item: ScheduleItem
    var body: some View {
        VStack(alignment: .leading) {
            Text(item.title).font(.headline)
            Text("\(item.startTime.formatted()) - \(item.endTime.formatted())")
                .font(.subheadline)
                .foregroundColor(.gray)
        }
        .padding(8)
        .background(Color(.secondarySystemBackground))
        .cornerRadius(10)
    }
}

NoteCardView.swift

struct NoteCardView: View {
    var note: Note
    var body: some View {
        VStack(alignment: .leading, spacing: 8) {
            Text(note.content)
                .font(.body)
                .lineLimit(4)
            Text(note.createdAt.formatted(date: .abbreviated, time: .shortened))
                .font(.caption)
                .foregroundColor(.gray)
        }
        .padding()
        .background(.ultraThinMaterial)
        .cornerRadius(12)
    }
}


⸻

💡 Mọi component đều có thể mở rộng hỗ trợ @Binding / @ObservedObject khi đưa vào chức năng tương tác như sửa, xóa, cập nhật realtime.

⸻

File này sẽ là nền tảng để ông code chính thức từng phần trong app VIONDRI 🎯

