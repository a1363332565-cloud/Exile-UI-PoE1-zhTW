# Exile UI — PoE1 繁體中文開箱即用整合包（v1.66.0）

基於上游 [Lailloken/Exile-UI](https://github.com/Lailloken/Exile-UI)（MIT 授權）製作的 **Path of Exile 1 國際服 + PoeChinese3 官方繁中補丁（`language=fr`）** 整合版。

解壓後無需手動複製語言包或套用補丁，安裝好 AutoHotkey v1.1 即可直接運行。

---

## 安裝與啟動步驟

1. **安裝 AutoHotkey v1.1（64 位元）**
   - 下載並安裝 **AutoHotkey v1.1.36+（必須是 v1.1 系列，勿安裝 v2）**：[https://www.autohotkey.com/](https://www.autohotkey.com/)
2. **下載並解壓整合包**
   - 前往本倉庫右側 **Releases** 下載最新 `.zip` 壓縮包，解壓至無特殊權限限制的資料夾（例如 `D:\Tools\Exile-UI-PoE1-zhTW\`）。
3. **確認遊戲設定**
   - PoE 需設定為 **無邊框全螢幕（Windowed Fullscreen）** 或 **視窗化（Windowed）**。
   - 使用 PoeChinese3 繁中補丁（遊戲設定檔 `Documents\My Games\Path of Exile\production_Config.ini` 中為 `language=fr`）。
4. **啟動插件**
   - 先啟動遊戲或直接雙擊 `Exile UI.ahk`（建議以一般使用者權限執行即可；若遊戲以系統管理員權限啟動，Exile UI 也需以相同權限啟動）。
   - 整合包已預先將介面語言設為繁體中文（`ini\config.ini` 中 `language="fr"`），進入遊戲後依畫面提示完成首次螢幕校準即可使用。

---

## 本整合版已完成的繁中相容與修復

除了提供全套遊戲數據與介面繁中翻譯（`data\fr\`）外，還針對 PoE1 繁中用戶端修復了 16 個模組的硬編碼英文檢查：

- **全域中英反查資料庫**（`data\global\[poe1] zh_to_en.json`）：涵蓋 4,491 個物品基底、90 個物品類別、745 個核心天賦，供各模組網頁外鏈與過濾器匯出自動轉英。
- **物品詞綴分析（Item-Checker）**：支援通貨、花園種子、譫妄玉、殘片、祝福、邀請函等物品分析（不再誤報不支援），修復 `精良的` / `穢生` 前綴、星團珠寶基底、`{ 大師工藝` 標籤，以及全部詞綴圖示與基底屬性繁中解析。
- **塗油與附魔查詢（Anoints）**：內建 60 個常用繁中詞綴關鍵字與 20 個凋落戒指防禦塔關鍵字，支援輸入 1 個中文字即時搜尋。
- **軍團珠寶探索（Seed-Explorer）**：修復征服者名稱與種子編號繁中擷取，支援市集繁/英雙向查價與 vilsol 計算器英文天賦反查。
- **過濾器編輯（FilterSpoon）**：完整解析繁中剪貼簿物品資訊（稀有度、物品等級、插槽、品質、護甲/閃避/能量護盾、破裂/追憶/勢力等），匯出過濾器規則時自動轉為遊戲要求之英文 `Class` / `BaseType`。
- **萬能鍵與市集（Omni-Key / Exchange / Stash-Ninja）**：支援繁中技能寶石（自動剝離 `瓦爾．` / `改造`）、`poewiki.net` / `poedb.tw/tw` / `craftofexile` 反查跳轉、繁中稀有度 `魔法` 與標價前綴 `備註: ~b/o` 識別。
- **章節拓荒 / 地圖 / 刷圖紀錄 / 聖域 / 合成器 / 反叛密教 / 小工具**：修復繁中物品剪貼簿解析、PoB 寶石連法匹配、待穿裝備追蹤、優越寶石與譫妄地圖前綴剝離、聖域聖物基底剝離、精髓懸停預覽等問題。

---

## 注意事項與已知邊界

- **請勿使用插件內建的「線上更新」功能**：內建更新器會從上游 `Lailloken/Exile-UI` 下載官方原版並覆蓋本整合包的相容補丁與語言包。日後更新請直接到本倉庫 Releases 下載新版整合包。
- **詞綴精簡提示（TLDR）**：因上游設計依賴 Windows 英文 OCR 辨識詞綴單字，於非英文用戶端預設停用。
- **章節拓荒 PoB 匯入**：需貼入英文版 Path of Building 匯出代碼或 `pobb.in` 連結；匯入成功後，遊戲內的寶石連線懸浮窗、商店正則與待穿裝備提醒均可正常對應繁中客戶端。

---

## 授權與致謝

- 原作專案：[Lailloken/Exile-UI](https://github.com/Lailloken/Exile-UI)（MIT License，詳見 [LICENSE.md](LICENSE.md)）
- 繁中客戶端環境：PoeChinese3
- 繁中語言包與 PoE1 繁中相容補丁整理：B站 MQisme
