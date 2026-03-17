# 🌈 Game tô màu cho bé các động vật hoang dã 

**Game giáo dục cho trẻ 3-4 tuổi, giúp rèn kỹ năng nhận diện các động vật thông qua các màn chơi tương tác, trực quan bằng Phaser 3 + TypeScript.**

---

## 🧩 Tech Stack

- **Phaser 3** – game engine canvas chính để dựng Scene, tween và âm thanh.  
- **TypeScript** – đảm bảo định kiểu trong toàn bộ scene, helper và audio manager.  
- **Vite** – bundler nhanh, hỗ trợ `assetsInclude` cho `png/jpg/mp3/json`, reload tức thì.  
- **Asset pipeline** – `public/assets/{images,audio,data}` đi kèm `TextureKeys`, `AudioKeys`, `DataKeys` để preload tập trung trong `PreloadScene`.  
- **Các helper riêng**: `PaintManager`, `IdleManager`, `GameUtils`, `AudioManager`, `BackgroundManager`, `rotateOrientation`.

---

## 📷 Ảnh demo
---

## 🛠️ Cài đặt

1. Clone repository:
   ```bash
   git clone <repo-url>
   cd listen-color-14-game
   ```
2. Cài phụ thuộc:
   ```bash
   npm install
   ```
3. Kiểm tra thư mục asset:
   - `public/assets/images/`: chứa UI, Scene1, Scene2, bg.  
   - `public/assets/audio/`: các SFX/voice.  
   - `public/assets/data/level_s2_config.json`: config phần tô màu.

---

## ▶️ Chạy game

- **Dev**: `npm run dev` → mở `http://localhost:5173`.  
- **Build production**: `npm run build`.  
- **Preview sau build**: `npm run preview`.  
- **Tương tác UI**:
  - `btn-reset`: dừng âm thanh, reset music + restart `Scene1`.  
  - `btn-exit`: khi chạy trong host (Iruka), gọi `host.complete()` kèm trạng thái.  
- **Flow**: Preload → Scene1 (tô màu con hà mã) → Scene2 (tô màu tô màu con cá sấu) → EndGame.

---

## 📚 Tài liệu tham khảo
- [Algorithms & Problem Solving](docs/ALGORITHMS.md) – logic cấp cao, tween, hint, idle.  
- [Gameplay Mechanics](docs/GAME_MECHANICS.md) – luật chơi, điểm, win/lose, spawn.  
- [Development Guide](docs/DEVELOPMENT.md) – cấu trúc thư mục, quy trình đóng góp, build/deploy.  
- README này là entry point; mở rộng trong `/docs` khi cần deep dive.

---