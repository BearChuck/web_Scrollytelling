# OPTICAL TIMELINE // 鏡頭焦段光學時間軸 (Scrollytelling Demo)

一個單一檔案（Single-File HTML）的 **Scrollytelling 滾動向量時間軸互動展示網頁**，以「不同相機焦段（`16mm` — `200mm`）的物理距離與空間壓縮效果」為主題。

🔗 **線上體驗 Live Demo**：[https://bearchuck.github.io/web_Scrollytelling/](https://bearchuck.github.io/web_Scrollytelling/)

---

## ✨ 技術架構與動效特色

- **純原生輕量架構**：Single-File HTML5 + Vanilla JavaScript，零建置依賴，開箱即用。
- **深色科技視覺**：採用 Tailwind CSS (`Slate-950` 深色基底) 搭配 SVG `<filter id="neon-glow">` 螢光漸層發光濾鏡。
- **GSAP 3 + ScrollTrigger + ScrollToPlugin**：
  - 使用 `path.getTotalLength()` 與 `strokeDashoffset` 隨滾輪即時繪製中央平滑三次貝茲 SVG 曲線導軌。
  - 核心展示舞台採 `pin: true` 釘選與 `scrub: 1.0` 物理阻尼平滑跟隨。
  - **節點雙向聯動**：支援點擊 SVG 節點、階段說明卡片或底部 HUD 快捷導覽列，平滑捲動定位至對應焦段階段。
  - **即時光學觀景窗模擬 (Live Viewfinder)**：隨捲動進度線性插值計算當前焦距、對角線視角 (FOV)、背景建築放大比例與散景模糊度。

## 📸 四大光學焦段階段

| 階段 | 焦段 | 對角線視角 (FOV) | 核心視覺效果 |
| :--- | :--- | :--- | :--- |
| **Phase 01** | `16mm` 超廣角 | `107°` | 誇張透視與邊緣拉伸、強烈臨場張力 |
| **Phase 02** | `35mm` 人文廣角 | `63°` | 貼近雙眼自然視野、人物與環境敘事平衡 |
| **Phase 03** | `85mm` 人像中焦 | `28.5°` | 五官立體零變形、大光圈奶油散景剝離 |
| **Phase 04** | `200mm` 望遠長焦 | `12°` | 劇烈空間壓縮、遠景拉近與色塊平面化 |

## 🚀 本地端執行方式

直接於瀏覽器開啟 `index.html`，或使用任意靜態伺服器啟動：

```bash
npx serve .
```
