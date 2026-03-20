# Recruitment Test — Unity Developer

**Company:** Wolffun
**Position:** Unity Developer
**Duration:** 5 days from the date of receipt
**Unity Version:** 2022.3 LTS (any patch)

---

## 1. Overview

Build a **prototype** for a casual **Pixel Destruction** game — players use tools (weapons) to cut and destroy objects as required by each level.

**Gameplay reference:**
https://play.google.com/store/apps/details?id=com.dalakgames.pixeldestruction

> Candidates should install and play the reference game before starting the test.

---

## 2. Required Features

### 2.1. Core Gameplay

- [ ] Players can **drag/swipe** to control the weapon to cut objects
- [ ] Cut objects must have realistic physics responses (fall, split apart, etc.)
- [ ] Clear **win/lose** conditions for each level
- [ ] **Basic UI**: gameplay screen, win/lose screen, replay button

### 2.2. Weapon — Saw

- [ ] Implement at least **1 weapon: circular saw**
- [ ] The saw must have a spinning animation while active
- [ ] Cutting must provide visual feedback (particles, trails, or similar)
- [ ] The saw must interact correctly with objects — only cuts on contact, no clipping through

### 2.3. Levels

- [ ] Minimum **5 levels** with progressive difficulty
- [ ] Each level has a different object layout
- [ ] A **level transition** system (level selection or auto-advance)

### 2.4. Level Editor Tool (Editor Window / Custom Inspector)

- [ ] Create a **Unity Editor Tool** (using `EditorWindow`, `CustomEditor`, or `ScriptableObject` workflow) to support Game Designers:
  - **Create and arrange objects** in a level through a visual interface (no coding required for GD)
  - **Configure object properties** (material, size, destructible or not, etc.)
  - **Save/Load level data** — level config should be stored as data, **ScriptableObject** is recommended. No hard-coding in scenes

> **Purpose:** Evaluate the ability to build tools that support team workflow, not just gameplay coding.

---

## 3. Evaluation Criteria

| Criteria | Weight | Description |
|----------|--------|-------------|
| **Code Quality** | 35% | Clean code, clear naming, proper separation of concerns, no hard-coding |
| **Gameplay Feel** | 25% | Smooth cutting feel, reasonable physics, good visual feedback |
| **Level Editor Tool** | 20% | Easy to use, GD-friendly, save/load works correctly |
| **Project Structure** | 15% | Clean folder structure, proper use of prefabs, easy to extend |
| **Level Design** | 5% | 5 levels with variety and reasonable progression |

### Bonus (Optional)

- Additional weapon (hammer, laser, etc.)
- Sound effects & juice (screen shake, slow-motion on cut, etc.)
- Object pooling for debris
- Scoring system (stars, points)
- Responsive UI for multiple screen ratios
- **Addressable Asset System** for asset management and loading
- **Performance optimization** (profiling, reduced GC allocation, draw call batching, etc.)

---

## 4. Submission

### Required:

1. **Source code** — push to a **GitHub** repository and share the link
2. **APK build** — a working APK for Android (or Windows build if no Android device is available)
3. **README.md** in the repo including:
   - How to open and run the project
   - Brief explanation of the code architecture (main systems)
   - How to use the Level Editor Tool (with screenshots if possible)
   - What you would improve given more time

### Notes:

- **DO NOT** copy code from tutorials without understanding it — there will be a technical interview about your code
- Commit frequently with clear messages — we will review git history
- Prioritize **completing all required features** before working on bonuses

---

## 5. After Submission

1. **Code Review** — the team will review source code and git history
2. **Technical Interview (30–45 min)** — explain design decisions, walk through code, answer implementation questions
3. **Result** — feedback within 3 business days after the interview

---

**Good luck! If you have any questions about the test, please contact us via the recruitment email.**

---
---

# Bài Test Tuyển Dụng — Unity Developer

**Công ty:** Wolffun
**Vị trí:** Unity Developer
**Thời hạn:** 5 ngày kể từ ngày nhận đề
**Unity Version:** 2022.3 LTS (bất kỳ patch nào)

---

## 1. Tổng Quan

Xây dựng **prototype** cho một game casual dạng **Pixel Destruction** — người chơi sử dụng các công cụ (weapon) để cắt, phá hủy các vật thể theo yêu cầu của từng level.

**Tham khảo gameplay:**
https://play.google.com/store/apps/details?id=com.dalakgames.pixeldestruction

> Ứng viên nên cài và chơi thử game tham khảo trước khi bắt đầu làm bài.

---

## 2. Yêu Cầu Bắt Buộc

### 2.1. Core Gameplay

- [ ] Người chơi có thể **kéo/swipe** để điều khiển weapon cắt vào vật thể
- [ ] Vật thể bị cắt phải có phản hồi vật lý hợp lý (rơi, tách ra, v.v.)
- [ ] Có điều kiện **win/lose** rõ ràng cho mỗi level
- [ ] Có **UI cơ bản**: màn hình chơi, màn hình win/lose, nút replay

### 2.2. Weapon — Cái Cưa (Saw)

- [ ] Implement ít nhất **1 weapon: cái cưa (circular saw)**
- [ ] Cưa phải có animation quay khi hoạt động
- [ ] Hiệu ứng cắt phải có visual feedback (particle, trail, hoặc tương tự)
- [ ] Cưa phải tương tác đúng với vật thể — chỉ cắt khi chạm, không cắt xuyên qua

### 2.3. Level

- [ ] Tối thiểu **5 levels** với độ khó tăng dần
- [ ] Mỗi level có layout vật thể khác nhau
- [ ] Có hệ thống **chuyển level** (level selection hoặc auto-advance)

### 2.4. Level Editor Tool (Editor Window / Custom Inspector)

- [ ] Tạo **Unity Editor Tool** (dùng `EditorWindow`, `CustomEditor`, hoặc `ScriptableObject` workflow) để hỗ trợ Game Designer:
  - **Tạo và sắp xếp vật thể** trong level bằng giao diện trực quan (không cần GD phải code)
  - **Cấu hình thuộc tính** của vật thể (material, kích thước, có phá được hay không, v.v.)
  - **Save/Load level data** — level config được lưu dưới dạng data, khuyến khích dùng **ScriptableObject**. Không hard-code trong scene

> **Mục đích:** Đánh giá khả năng tạo tool phục vụ workflow của team, không chỉ code gameplay.

---

## 3. Tiêu Chí Đánh Giá

| Tiêu chí | Trọng số | Mô tả |
|-----------|----------|-------|
| **Code Quality** | 35% | Clean code, đặt tên rõ ràng, tách biệt logic hợp lý, không hard-code |
| **Gameplay Feel** | 25% | Cảm giác cắt mượt, physics hợp lý, visual feedback tốt |
| **Level Editor Tool** | 20% | Tool dễ sử dụng, GD-friendly, save/load hoạt động đúng |
| **Project Structure** | 15% | Folder structure gọn gàng, prefab hợp lý, dễ mở rộng |
| **Level Design** | 5% | 5 levels có sự đa dạng và progression hợp lý |

### Điểm Cộng (Bonus — Không Bắt Buộc)

- Thêm weapon thứ 2 (búa, laser, v.v.)
- Sound effects & juice (screen shake, slow-motion khi cắt, v.v.)
- Object pooling cho các mảnh vỡ
- Hệ thống scoring (sao, điểm)
- Responsive UI cho nhiều tỉ lệ màn hình
- Sử dụng **Addressable Asset System** để quản lý và load asset
- Tối ưu **performance** (profiling, giảm GC allocation, batching draw calls, v.v.)

---

## 4. Yêu Cầu Nộp Bài

### Bắt buộc:

1. **Source code** — push lên **GitHub** repository và gửi link
2. **Build APK** — 1 file APK chạy được trên Android (hoặc Windows build nếu không có thiết bị Android)
3. **README.md** trong repo bao gồm:
   - Hướng dẫn mở project và chạy
   - Giải thích ngắn về kiến trúc code (các system chính)
   - Hướng dẫn sử dụng Level Editor Tool (kèm screenshot nếu có)
   - Những điều bạn sẽ cải thiện nếu có thêm thời gian

### Lưu ý:

- **KHÔNG** copy code từ tutorial mà không hiểu — sẽ có phỏng vấn hỏi về code
- Commit thường xuyên với message rõ ràng — chúng tôi sẽ xem git history
- Ưu tiên **hoàn thành đủ yêu cầu bắt buộc** trước khi làm bonus

---

## 5. Quy Trình Sau Khi Nộp

1. **Code Review** — Team sẽ review source code và git history
2. **Phỏng vấn kỹ thuật (30–45 phút)** — Giải thích các quyết định thiết kế, walk through code, trả lời câu hỏi về implementation
3. **Kết quả** — Phản hồi trong vòng 3 ngày làm việc sau phỏng vấn

---

**Chúc bạn làm bài tốt! Nếu có thắc mắc về đề bài, hãy liên hệ qua email tuyển dụng.**
