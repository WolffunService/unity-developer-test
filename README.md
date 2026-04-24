# Recruitment Test — Unity Developer

| | |
|---|---|
| **Company** | Wolffun |
| **Position** | Unity Developer |
| **Duration** | 5 days from the date of receipt |
| **Unity Version** | 2022.3 LTS or Unity 6.3 LTS (any patch) |

---

## 1. Overview

Build a **prototype** for a casual **puzzle rescue** game — the player uses color-matching cannons to shoot down the dragon and rescue the girl.

**Gameplay reference:**
https://play.google.com/store/apps/details?id=com.save.princess.girl.dragon.out.and

> Candidates should install and play the reference game before starting the test.

---

## 2. Required Features

### 2.1. Core Gameplay

> The prototype should capture the feel of the reference game. You do **not** need to clone it 1:1 — focus on the main loop below.

**Main loop:**
- [ ] Each level places a **girl** that needs rescuing and **one dragon** as the threat
- [ ] The level contains multiple **colored cannons** at fixed positions
- [ ] The player **taps a cannon** to fire a projectile matching the cannon's color
- [ ] Projectiles only damage dragon parts of the **same color**
- [ ] The level is **won** when the dragon is fully destroyed and the girl is rescued
- [ ] The level is **lost** when the dragon reaches the girl

**Cannon:**
- [ ] Each cannon has a fixed **color** and limited **ammo** (configurable per level)
- [ ] Visual + audio feedback on fire, reload, and empty states

**Dragon:**
- [ ] The dragon is composed of **multiple colored parts/segments**
- [ ] Parts take damage only from the matching color
- [ ] The dragon **moves/advances** toward the girl over time
- [ ] Destroying parts gives **visual feedback** (particles, shake, etc.)

**Boosters:**
- [ ] The game must include **3 boosters** the player can use during a level, following the reference game
- [ ] Booster parameters are **configurable by GD**
- [ ] Booster activation has clear **visual + audio feedback**

**UI:**
- [ ] **Level progress** indicator (dragon HP or parts remaining)
- [ ] **Current level** number and simple in-level HUD (ammo remaining, booster buttons)
- [ ] **Win / Lose** screens with retry and next-level buttons

### 2.2. Level

- [ ] Minimum **5 levels** with increasing difficulty (more parts, more colors, tighter timing, new obstacle types, etc.)
- [ ] After each level, **reset per-run state** (ammo, etc.) back to the level's defaults
- [ ] Each level defines its own **dragon layout**, **cannon placement + colors**, and **win/lose conditions**
- [ ] Includes a **level transition system** (level selection or auto-advance)

### 2.3. Level Editor Tool (Editor Window / Custom Inspector)

Deliverables — the tool must support the following workflow end-to-end:

- [ ] Open the tool from a menu path (e.g., `Tools/Level Editor`)
- [ ] Create / select a `LevelConfig` asset (**ScriptableObject** recommended)
- [ ] Configure per-element properties (color, HP, ammo, etc.) via inspector or custom UI
- [ ] Save level data as an asset file — **no hard-coding in scenes**
- [ ] Runtime loads from the same asset — round-trip must reproduce the identical layout

> **Purpose:** Evaluate the ability to build tools that support team workflow, not just gameplay coding.

### 2.4. Technical Requirements

- **Core gameplay logic** (color-matching damage, dragon progression, win/lose resolution) must be self-implemented. You may use a plugin, but you must understand its internals and be able to modify or extend it on request during the interview.
- **Performance:** stable frame rate on a mid-range mobile device, no memory leaks during extended play.

---

## 3. Evaluation Criteria

| Criteria | Weight | Description |
|----------|--------|-------------|
| **Code Quality** | 35% | Clean code, clear naming, proper separation of concerns, no hard-coding |
| **Gameplay Feel** | 25% | Responsive input, readable feedback, satisfying hit/destroy reactions |
| **Level Editor Tool** | 20% | Easy to use, GD-friendly, save/load works correctly |
| **Project Structure** | 15% | Clean folder structure, proper use of prefabs, easy to extend |
| **Level Design** | 5% | 5 levels with variety and reasonable progression |

### Bonus (Optional)

- Additional cannon / projectile types
- Sound effects & juice (screen shake, slow-motion on kill, combo text, etc.)
- Object pooling for projectiles and particles
- Responsive UI for multiple screen ratios
- **Addressable Asset System** for asset management and loading
- **Performance optimization** (profiling, reduced GC allocation, draw call batching, etc.)

---

## 4. Submission

### Required:

1. **Source code** — push to a **GitHub** repository and share the link
2. **APK build** — a working APK for Android (or Windows build if no Android device is available). Must build without errors and play smoothly from Menu → Level 1 → Level 5 without crashes
3. **Video demo** — a short video demonstrating the game (screen recording of gameplay, upload to YouTube/Google Drive and include the link)
4. **README.md** in the repo including:
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

| | |
|---|---|
| **Công ty** | Wolffun |
| **Vị trí** | Unity Developer |
| **Thời hạn** | 5 ngày kể từ ngày nhận đề |
| **Unity Version** | 2022.3 LTS hoặc Unity 6.3 LTS (bất kỳ patch nào) |

---

## 1. Tổng Quan

Xây dựng **prototype** cho một game casual dạng **puzzle giải cứu** — người chơi dùng các khẩu đại bác theo màu để bắn hạ rồng và cứu cô gái.

**Tham khảo gameplay:**
https://play.google.com/store/apps/details?id=com.save.princess.girl.dragon.out.and

> Ứng viên nên cài và chơi thử game tham khảo trước khi bắt đầu làm bài.

---

## 2. Yêu Cầu Bắt Buộc

### 2.1. Core Gameplay

> Prototype cần đúng cảm giác của game tham khảo. Không cần clone 1:1 — tập trung vào main loop bên dưới.

**Main loop:**
- [ ] Mỗi level có **cô gái** cần giải cứu và **một con rồng** là mối đe dọa
- [ ] Level có nhiều **đại bác theo màu** đặt ở vị trí cố định
- [ ] Người chơi **tap vào đại bác** để bắn viên đạn có màu tương ứng
- [ ] Đạn chỉ gây sát thương lên phần rồng có **cùng màu**
- [ ] **Thắng** khi rồng bị phá hủy hoàn toàn và cô gái được cứu
- [ ] **Thua** khi rồng chạm tới cô gái

**Đại bác (Cannon):**
- [ ] Mỗi đại bác có **màu cố định** và **số đạn giới hạn** (config theo level)
- [ ] Có visual + audio feedback khi bắn, nạp đạn, và hết đạn

**Rồng (Dragon):**
- [ ] Rồng gồm **nhiều phần/đoạn có màu**
- [ ] Mỗi phần chỉ nhận sát thương từ đạn đúng màu
- [ ] Rồng **di chuyển / tiến dần** về phía cô gái theo thời gian
- [ ] Phá phần rồng phải có **visual feedback** (particle, shake, v.v.)

**Booster:**
- [ ] Game phải có **3 booster** người chơi có thể dùng trong level, bám theo game gốc
- [ ] Tham số booster **do GD config**
- [ ] Khi kích hoạt booster phải có **visual + audio feedback** rõ ràng

**UI:**
- [ ] **Tiến trình level** (HP rồng hoặc số phần còn lại)
- [ ] **Số level hiện tại** và HUD đơn giản (số đạn còn lại, nút booster)
- [ ] Màn hình **Win / Lose** với nút retry và next-level

### 2.2. Level

- [ ] Tối thiểu **5 levels** với độ khó tăng dần (nhiều phần hơn, nhiều màu hơn, timing chặt hơn, có thêm loại obstacle mới, v.v.)
- [ ] Sau mỗi level, **reset state mỗi run** (số đạn, v.v.) về default của level
- [ ] Mỗi level định nghĩa riêng **layout rồng**, **vị trí + màu đại bác**, và **điều kiện thắng/thua**
- [ ] Có hệ thống **chuyển level** (level selection hoặc auto-advance)

### 2.3. Level Editor Tool (Editor Window / Custom Inspector)

Deliverable — tool phải hỗ trợ workflow end-to-end như sau:

- [ ] Mở tool qua menu path (ví dụ `Tools/Level Editor`)
- [ ] Tạo / chọn asset `LevelConfig` (khuyến khích **ScriptableObject**)
- [ ] Cấu hình thuộc tính từng element (màu, HP, số đạn, v.v.) qua inspector hoặc custom UI
- [ ] Lưu level data dưới dạng asset file — **không hard-code trong scene**
- [ ] Runtime load từ cùng asset — round-trip phải tái tạo đúng layout ban đầu

> **Mục đích:** Đánh giá khả năng tạo tool phục vụ workflow của team, không chỉ code gameplay.

### 2.4. Yêu Cầu Kỹ Thuật

- **Core gameplay logic** (color-matching damage, rồng di chuyển, xử lý win/lose) phải tự implement. Có thể dùng plugin, nhưng bắt buộc phải hiểu rõ internals và có thể chỉnh sửa/mở rộng theo yêu cầu trong buổi phỏng vấn.
- **Performance:** frame rate ổn định trên thiết bị mobile tầm trung, không memory leak khi chơi liên tục.

---

## 3. Tiêu Chí Đánh Giá

| Tiêu chí | Trọng số | Mô tả |
|-----------|----------|-------|
| **Code Quality** | 35% | Clean code, đặt tên rõ ràng, tách biệt logic hợp lý, không hard-code |
| **Gameplay Feel** | 25% | Input nhạy, feedback rõ ràng, cảm giác bắn / phá đã tay |
| **Level Editor Tool** | 20% | Tool dễ sử dụng, GD-friendly, save/load hoạt động đúng |
| **Project Structure** | 15% | Folder structure gọn gàng, prefab hợp lý, dễ mở rộng |
| **Level Design** | 5% | 5 levels có sự đa dạng và progression hợp lý |

### Điểm Cộng (Bonus — Không Bắt Buộc)

- Thêm loại đại bác / đạn khác
- Sound effects & juice (screen shake, slow-motion khi hạ, combo text, v.v.)
- Object pooling cho đạn và particle
- Responsive UI cho nhiều tỉ lệ màn hình
- Sử dụng **Addressable Asset System** để quản lý và load asset
- Tối ưu **performance** (profiling, giảm GC allocation, batching draw calls, v.v.)

---

## 4. Yêu Cầu Nộp Bài

### Bắt buộc:

1. **Source code** — push lên **GitHub** repository và gửi link
2. **Build APK** — 1 file APK chạy được trên Android (hoặc Windows build nếu không có thiết bị Android). Build không lỗi và chơi mượt từ Menu → Level 1 → Level 5 không crash
3. **Video demo** — quay video ngắn demo gameplay (screen recording, upload lên YouTube/Google Drive và gửi kèm link)
4. **README.md** trong repo bao gồm:
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
