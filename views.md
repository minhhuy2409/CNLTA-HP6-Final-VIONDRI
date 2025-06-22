#  📄 Views – ToDo, Timetable, Notes, Music, Settings

✅ ToDoView.swift

import SwiftUI

struct ToDoView: View {
    @State private var tasks: [Task] = sampleTasks

    var body: some View {
        NavigationView {
            List {
                ForEach(tasks) { task in
                    TaskCardView(task: task)
                }
            }
            .navigationTitle("To-Do List")
        }
    }
}


⸻

📅 TimetableView.swift

import SwiftUI

struct TimetableView: View {
    @State private var selectedDay: String = "Monday"
    let days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]

    var body: some View {
        VStack {
            Picker("Select Day", selection: $selectedDay) {
                ForEach(days, id: \ .self) { day in
                    Text(day)
                }
            }
            .pickerStyle(SegmentedPickerStyle())
            .padding()

            List(sampleSchedule.filter { $0.day == selectedDay }) { item in
                ScheduleCell(item: item)
            }
        }
        .navigationTitle("Timetable")
    }
}


⸻

📝 NoteBoardView.swift

import SwiftUI

struct NoteBoardView: View {
    @State private var notes: [Note] = sampleNotes

    var body: some View {
        NavigationView {
            List {
                ForEach(notes) { note in
                    NoteCardView(note: note)
                }
            }
            .navigationTitle("Note Board")
        }
    }


⸻

🎧 FocusMusicView.swift

import SwiftUI

struct FocusMusicView: View {
    @State private var musicSetting = MusicSetting(isConnected: false, service: .spotify)

    var body: some View {
        VStack(spacing: 20) {
            Text("Focus Music")
                .font(.title)

            Toggle("Kết nối với \(musicSetting.service.rawValue.capitalized)", isOn: $musicSetting.isConnected)
                .padding()

            Picker("Chọn dịch vụ", selection: $musicSetting.service) {
                ForEach(MusicService.allCases, id: \ .self) { service in
                    Text(service.rawValue.capitalized)
                }
            }
            .pickerStyle(.segmented)
            .padding()
        }
        .navigationTitle("Music")
    }
}


⸻

⚙️ SettingsView.swift

import SwiftUI

struct SettingsView: View {
    @AppStorage("username") var username = ""

    var body: some View {
        Form {
            Section(header: Text("User Info")) {
                TextField("Enter your name", text: $username)
            }
        }
        .navigationTitle("Settings")
    }
}

💡 Gợi ý: mỗi View sau này có thể tách ViewModel nếu cần chia nhỏ logic.

