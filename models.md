#  📄 Models – Task, Note, ScheduleItem, MusicSetting

✅ Task.swift

import Foundation

struct Task: Identifiable, Codable {
    var id = UUID()
    var title: String
    var isCompleted: Bool = false
    var dueDate: Date?
}


⸻

📝 Note.swift

import Foundation

struct Note: Identifiable, Codable {
    var id = UUID()
    var content: String
    var createdAt: Date = Date()
}


⸻

📅 ScheduleItem.swift

import Foundation

struct ScheduleItem: Identifiable, Codable {
    var id = UUID()
    var title: String
    var startTime: Date
    var endTime: Date
    var day: String // ví dụ: "Monday", "Tuesday"
}


⸻

🎵 MusicSetting.swift

import Foundation

enum MusicService: String, Codable, CaseIterable {
    case spotify
    case appleMusic
}

struct MusicSetting: Codable {
    var isConnected: Bool
    var service: MusicService
}

💡 Gợi ý mở rộng: thêm @Published nếu chuyển qua dạng class để dùng cùng ObservableObject trong ViewModel.

