# Recruitment Test — Unity Developer

| | |
|---|---|
| **Company** | Wolffun |
| **Position** | Unity Developer |
| **Duration** | 5 days from the date of receipt |
| **Unity Version** | 2022.3 LTS or Unity 6.3 LTS (any patch) |

---

## 1. Overview

Build a **prototype** for a casual **Pixel Destruction** game — players use tools (weapons) to cut and destroy objects as required by each level.

**Gameplay reference:**
https://play.google.com/store/apps/details?id=com.dalakgames.pixeldestruction

> Candidates should install and play the reference game before starting the test.

---

## 2. Required Features

### 2.1. Core Gameplay

> The prototype should be as close to the reference game as possible.

**Overview:**
- [ ] Each level has a **list of objects** that need to be cut. The game **spawns objects gradually** from above
- [ ] The map contains **obstacles** that block **falling objects**
- [ ] The player needs to **tap** or **place saws** to destroy the **objects**

**Win Condition:**
- [ ] The game is **won** when all objects are destroyed and successfully reach the bottom

**Object:**
- [ ] Objects are made up of **pixels** (small square units forming a shape)
- [ ] Objects **fall downward** due to gravity
- [ ] When an object is **cut**, it splits into **smaller independent objects** (each piece behaves like its own physics body, similar to the reference game)
- [ ] Small enough pieces can pass through gaps between obstacles and continue falling
- [ ] When objects **reach the bottom**, they are converted into **experience points (XP)**. The conversion rate is configurable by GD (e.g., 1 pixel = 1 XP)

**Weapon — Circular Saw:**
- [ ] The level contains **fixed positions** where weapons (saws) can be placed
- [ ] The saw has a **rotating animation** when active
- [ ] When an object touches the saw, it is **cut through**, splitting into smaller pieces
- [ ] Cutting effects must have **visual feedback** (particles, trails, or similar)

**Obstacle:**
- [ ] The level contains **obstacles** that prevent large objects from passing through
- [ ] Obstacles force players to use weapons to cut objects small enough to fit through gaps
- [ ] Saw placement positions also act as **obstacles**

**Tap to Destroy:**
- [ ] The player can **tap on an object** to deal damage to a pixel area
- [ ] Damage is **highest at the center** (max damage) and **decreases with distance** (min damage at the edge of the radius)
- [ ] GD can configure: **damage radius**, **max damage**, **min damage**

**Upgrades Saw:**
- [ ] Collect enough XP to **receive an upgrade**
- [ ] XP required for each upgrade is configurable: **starting XP** and **increment per upgrade** (e.g., start = 100, increment = 50 → Upgrade 1 needs 100, Upgrade 2 needs 150, Upgrade 3 needs 200...)
- [ ] Each time an upgrade is received, the player chooses **1 of 2 random upgrades**. Upgrade options include:
  - **Larger saw**
  - **Faster rotation speed**
  - **Higher damage**
  - Add **one new saw** (placed in an available slot chosen by the player)

**UI:**
- [ ] **XP progress bar** for upgrades
- [ ] Current **level progress and information** (level number)

### 2.2. Level

- [ ] Minimum **5 levels** with increasing difficulty (more objects, larger objects, narrower obstacle gaps, etc.)
- [ ] After each level, reset the **number of saws** (back to 0) and **all upgrades** (reset to default stats)
- [ ] Each level defines its own **object list**, **obstacle layout**, and **weapon placement positions**
- [ ] Includes a **level transition system** (level selection or auto-advance)

### 2.3. Level Editor Tool (Editor Window / Custom Inspector)

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

- Additional weapon types (hammer, laser, etc.)
- Sound effects & juice (screen shake, slow-motion on cut, etc.)
- Object pooling for split pieces and particles
- Responsive UI for multiple screen ratios
- **Addressable Asset System** for asset management and loading
- **Performance optimization** (profiling, reduced GC allocation, draw call batching, etc.)

---

## 4. Submission

### Required:

1. **Source code** — push to a **GitHub** repository and share the link
2. **APK build** — a working APK for Android (or Windows build if no Android device is available)
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

Xây dựng **prototype** cho một game casual dạng **Pixel Destruction** — người chơi sử dụng các công cụ (weapon) để cắt, phá hủy các vật thể theo yêu cầu của từng level.

**Tham khảo gameplay:**
https://play.google.com/store/apps/details?id=com.dalakgames.pixeldestruction

> Ứng viên nên cài và chơi thử game tham khảo trước khi bắt đầu làm bài.

---

## 2. Yêu Cầu Bắt Buộc

### 2.1. Core Gameplay

> Prototype càng giống game gốc càng tốt.

**Overview:**
- [ ] Mỗi level có **danh sách các object** cần được cắt. Game **thả từ từ** các object từ trên xuống
- [ ] Trong map sẽ có **obstacle** chặn **object** rơi xuống
- [ ] Người chơi cần **tap** hoặc **đặt cưa** để phá hủy các **object**

**Win Condition:**
- [ ] Game **chiến thắng** khi tất cả object đã được phá và chạm đáy thành công

**Object (Vật thể):**
- [ ] Vật thể được cấu thành từ **các pixel** (các ô vuông nhỏ tạo thành hình dạng)
- [ ] Vật thể **rơi từ trên xuống** theo trọng lực
- [ ] Khi vật thể bị **cắt**, nó tách thành **các object nhỏ hơn độc lập** (mỗi mảnh hoạt động như một physics body riêng, như trong game tham khảo)
- [ ] Vật thể đủ nhỏ sẽ lọt qua khe giữa các obstacle và tiếp tục rơi xuống
- [ ] Vật thể **chạm đáy** sẽ được quy đổi thành **kinh nghiệm (XP)**. Mức quy đổi do GD config (ví dụ: 1 pixel = 1 XP)

**Weapon — Cái Cưa (Circular Saw):**
- [ ] Trong màn chơi có các **vị trí cố định** để đặt weapon (cưa)
- [ ] Cưa có **animation quay** khi hoạt động
- [ ] Khi vật thể chạm vào cưa, cưa **cắt xuyên qua vật thể**, tách thành các mảnh nhỏ hơn
- [ ] Hiệu ứng cắt phải có **visual feedback** (particle, trail, hoặc tương tự)

**Obstacle (Vật cản):**
- [ ] Trong màn chơi có các **obstacle** ngăn cản vật thể quá to lọt qua
- [ ] Obstacle buộc người chơi phải dùng weapon để cắt vật thể đủ nhỏ mới lọt qua khe
- [ ] Vị trí đặt cưa cũng là **obstacle**

**Tap to Destroy (Chạm để phá hủy):**
- [ ] Người chơi có thể **Object** để gây sát thương lên một vùng pixel.
- [ ] Sát thương **cao nhất ở tâm** (max damage) và **giảm dần theo khoảng cách** (min damage ở rìa bán kính)
- [ ] GD có thể config: **bán kính gây sát thương**, **sát thương max**, **sát thương min**

**Upgrades Saw:**
- [ ] Thu thập đủ XP sẽ **nhận được Upgrade**
- [ ] Mức XP yêu cầu sau mỗi lần Upgarde có thể config: **XP khởi đầu** và **mức tăng thêm** mỗi lần Upgrade (ví dụ: khởi đầu=100, tăng=50 → Lần Upgrade 1 cần 100, Lần Upgrade 2 cần 150, Lần Upgrade 3 cần 200...)
- [ ] Mỗi lần nhận được Upgrade, người chơi được chọn **1 trong 2 nâng cấp random**. Danh sách nâng cấp:
  - Cái cưa **to hơn**
  - Cái cưa **xoay nhanh hơn**
  - Cái cưa **gây sát thương nhiều hơn**
  - Thêm **1 cưa mới** (đặt vào vị trí còn trống do người chơi chọn)

**UI:**
- [ ] Tiến trình **Thanh XP để nhận Upgrade** 
- [ ] Tiến trình và thông tin (level bao nhiêu) **level hiện tại**

### 2.2. Level

- [ ] Tối thiểu **5 levels** với độ khó tăng dần (nhiều object hơn, object lớn hơn, khe obstacle hẹp hơn, v.v.)
- [ ] Sau mỗi Level thì reset **số lượng cưa** (reset về 0) và **các nâng cấp** (reset về chỉ số Default) 
- [ ] Mỗi level định nghĩa riêng **danh sách object**, **layout obstacle**, và **vị trí đặt weapon**
- [ ] Có hệ thống **chuyển level** (level selection hoặc auto-advance)

### 2.3. Level Editor Tool (Editor Window / Custom Inspector)

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

- Thêm loại weapon khác (búa, laser, v.v.)
- Sound effects & juice (screen shake, slow-motion khi cắt, v.v.)
- Object pooling cho các mảnh tách và particle
- Responsive UI cho nhiều tỉ lệ màn hình
- Sử dụng **Addressable Asset System** để quản lý và load asset
- Tối ưu **performance** (profiling, giảm GC allocation, batching draw calls, v.v.)

---

## 4. Yêu Cầu Nộp Bài

### Bắt buộc:

1. **Source code** — push lên **GitHub** repository và gửi link
2. **Build APK** — 1 file APK chạy được trên Android (hoặc Windows build nếu không có thiết bị Android)
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
