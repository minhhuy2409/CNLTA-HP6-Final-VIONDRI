#  # 📄 Data – Sample Data for MVP

> Dữ liệu giả định để preview UI và phát triển tính năng MVP: Task, Note, Schedule.

---

## ✅ SampleTasks

```swift
let sampleTasks: [Task] = [
    Task(title: "Ôn tập Toán chương 5"),
    Task(title: "Soạn Văn nghị luận"),
    Task(title: "Tập gym 30 phút", isCompleted: true)
]
```

---

## 📝 SampleNotes

```swift
let sampleNotes: [Note] = [
    Note(content: "Lập dàn ý bài luận tiếng Anh về công nghệ."),
    Note(content: "Công thức đạo hàm bậc 2: f''(x) = ..."),
    Note(content: "Ý tưởng app: VIONDRI = Workspace x Music x Mood")
]
```

---

## 📅 SampleSchedule

```swift
let sampleSchedule: [ScheduleItem] = [
    ScheduleItem(
        title: "Tiết 1: Toán",
        startTime: Date(),
        endTime: Date().addingTimeInterval(3600),
        day: "Monday"
    ),
    ScheduleItem(
        title: "Tiết 2: Lý",
        startTime: Date().addingTimeInterval(3600),
        endTime: Date().addingTimeInterval(7200),
        day: "Monday"
    ),
    ScheduleItem(
        title: "Tiết 3: Văn",
        startTime: Date().addingTimeInterval(7200),
        endTime: Date().addingTimeInterval(10800),
        day: "Tuesday"
    )
]
```

---

> 💡 Gợi ý mở rộng:

* Thêm thuộc tính như màu, nhãn dán, độ ưu tiên (priority).
* Lưu trữ và cập nhật bằng `@AppStorage`, `UserDefaults`, hoặc `CoreData` sau MVP.


