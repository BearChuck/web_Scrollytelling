# EVENT OPTICS // 活動攝影焦段實戰時間軸 (Scrollytelling Demo)

一個單一檔案（Single-File HTML）的 **Scrollytelling 滾動向量時間軸互動展示網頁**，從**「活動攝影（論壇、記者會、晚宴、展場）」**的實戰視角，解析 `16mm` 到 `200mm` 鏡頭焦段的站位距離、視角 (FOV) 與舞台背板壓縮效果。

🔗 **線上體驗 Live Demo**：[https://bearchuck.github.io/web_Scrollytelling/](https://bearchuck.github.io/web_Scrollytelling/)

---

## ✨ 技術架構與動效特色

- **純原生輕量架構**：Single-File HTML5 + Vanilla JavaScript，零建置依賴，開箱即用。
- **深色科技視覺**：採用 Tailwind CSS (`Slate-950` 深色基底) 搭配 SVG `<filter id="neon-glow">` 螢光漸層發光濾鏡。
- **GSAP 3 + ScrollTrigger + ScrollToPlugin**：
  - 使用 `path.getTotalLength()` 與 `strokeDashoffset` 隨滾輪即時繪製中央平滑三次貝茲 SVG 曲線導軌。
  - 核心展示舞台採 `pin: true` 釘選與 `scrub: 1.0` 物理阻尼平滑跟隨。
  - **節點雙向聯動**：支援點擊 SVG 節點、階段說明卡片或底部 HUD 快捷導覽列，平滑捲動定位至對應焦段階段。
  - **舞台觀景窗模擬 (Stage Viewfinder)**：隨捲動進度線性插值計算當前焦距、對角線視角 (FOV)、舞台主視覺 LED 背板放大比例與聚光燈散景模糊度。

## 📸 活動攝影四大焦段階段

| 階段 | 焦段 | 對角線視角 (FOV) | 活動實戰站位與公關必拍畫面 |
| :--- | :--- | :--- | :--- |
| **Phase 01** | `16mm` 超廣角 | `107°` | **壓軸大合照與爆滿氣勢**：退無可退的前排大合照、千人展廳全場空景、走道低角度仰拍強化人潮張力 |
| **Phase 02** | `35mm` 人文廣角 | `63°` | **茶敘敬酒與展攤互動跟拍**：1.2m 社交距離抓拍貴賓交換名片與舉杯，同時帶入背後贊助商 Logo 與展攤環境 |
| **Phase 03** | `85mm` 人像中焦 | `28.5°` | **講者眼神特寫與雜物剝離**：站位 2.5m–4m，過濾桌上礦泉水瓶、麥克風線與工作人員，鎖定講者手勢與 VIP 專注神情 |
| **Phase 04** | `200mm` 望遠長焦 | `12°` | **遠距零干擾狙擊與滿版背板壓縮**：退至 8m–20m 音控台旁不擋視線，將舞台 LED 主視覺拉近貼滿講者背後，抓拍頒獎擁抱瞬間 |

## 🚀 本地端執行方式

直接於瀏覽器開啟 `index.html`，或使用任意靜態伺服器啟動：

```bash
npx serve .
```
