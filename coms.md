#  🧩 Components – TaskCard, NoteCard, ScheduleCell

✅ TaskCardView.swift

import SwiftUI

struct TaskCardView: View {
    var task: Task

    var body: some View {
        HStack {
            Image(systemName: task.isCompleted ? "checkmark.circle.fill" : "circle")
                .foregroundColor(task.isCompleted ? .green : .gray)
            Text(task.title)
                .strikethrough(task.isCompleted, color: .gray)
            Spacer()
            if let due = task.dueDate {
                Text(due, style: .date)
                    .font(.caption)
                    .foregroundColor(.secondary)
            }
        }
        .padding(.vertical, 8)
    }
}


⸻

📝 NoteCardView.swift

import SwiftUI

struct NoteCardView: View {
    var note: Note

    var body: some View {
        VStack(alignment: .leading, spacing: 6) {
            Text(note.content)
                .font(.body)
            Text(note.createdAt, style: .time)
                .font(.caption2)
                .foregroundColor(.gray)
        }
        .padding(8)
    }
}


⸻

📅 ScheduleCell.swift

import SwiftUI

struct ScheduleCell: View {
    var item: ScheduleItem

    var body: some View {
        VStack(alignment: .leading, spacing: 4) {
            Text(item.title)
                .font(.headline)
            Text("\(item.startTime.formatted(date: .omitted, time: .shortened)) - \(item.endTime.formatted(date: .omitted, time: .shortened))")
                .font(.caption)
                .foregroundColor(.secondary)
        }
        .padding(.vertical, 6)
    }
}


⸻

💡 Gợi ý UI: Dùng .background, .cornerRadius, .shadow để polish UI sau MVP.

