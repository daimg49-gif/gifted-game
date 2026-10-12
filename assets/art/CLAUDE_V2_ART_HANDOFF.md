# Claude v2 美術已交付

2026-10-12｜依 docs/ART_SPEC_for_ChatGPT.md 製作。18 張正式接入圖片直接位於 assets/art/，所有檔名與 v2 index.html 相符。美術使用內建 imagegen；最後尺寸、格式、圖集拆檔為素材輸出作業。

## 直接使用的圖片

| 檔名 | 尺寸 | 備註 |
| --- | --- | --- |
| island.webp | 1200×1600 | v2 五地標配置，深藍暗窗；碼頭已向下調至84%附近 |
| island-wide.webp | 1920×1080 | 中央保留安靜星空，地景在两側 |
| xiaoguang-idle.png | 512×512 | 靜態微笑，透明 |
| xiaoguang-guide.png | 512×512 | 指引，透明 |
| xiaoguang-think.png | 512×512 | 思考，透明 |
| xiaoguang-happy.png | 512×512 | 開心，透明 |
| scene-treehouse.webp | 1600×700 | 家長觀察樹屋 |
| scene-repair.webp | 1600×700 | 機關修理所 |
| scene-craft.webp | 1600×700 | 河邊石匠工坊與圓石 |
| scene-observatory.webp | 1600×700 | 望遠鏡與無字星圖 |
| scene-dock.webp | 1600×700 | 碼頭、小船、遠方陸地 |
| parent-card-1.webp ～ parent-card-6.webp | 800×600 | 六張家長情境卡 |
| fluffball.png | 256×256 | 背紅色行李、面向右的毛球，透明 |

總大小約4.0MB，每張低於300,000 bytes。v2-manifest.json 包含實際尺寸、檔案大小、格式透明資訊。所有圖片已實際解碼檢查，PNG 確認透明 alpha。小光四圖由同一張四姿勢角色圖集輸出，比例一致，腳底約在下緣上方5%。

## 素材與程式邊界

本次只新增／整理圖片與美術文件，不修改 Claude 的 index.html、遊戲規則、招生資料或測試文件。程式依既有圖片偵測機制讀取上述18檔。軌道、踏石圖形、星星記憶、資料及按鈕均由程式繪製。

主圖建築依美術規格位置排列。生成圖與窗光 overlay 是不同層，最終手機點擊熱區與窗光視覺仍由 Claude 進行頁面驗收；不因圖檔存在就宣稱遊戲功能已測試。

圖片是靜態插畫；需要的角色浮動、星光、窗戶點亮由 CSS／Canvas 製作。減少動態模式需靜止。背景中的外部燈籠可以發亮，但建築窗戶初始是暗藍。

## 原腳本美術備選

images/ 中另外保留19張／組原腳本美術備選，包含原先探索島、全景、工具、植物、過河提案、紀念卡。它們沒有接入 v2；不要把原腳本中的三遊戲規則覆蓋到現在的 v2。若未來採回原腳本，可參考 CLAUDE_ART_HANDOFF.md 與 docs/WEBSITE_DESIGN_SCRIPT.md。

圖像提示集合：V2_PROMPTS.json 為新版生成素材，PROMPTS.json 為原腳本備選。真實學校課程照片仍由學校授權提供，幻想圖片不作實況照片。
