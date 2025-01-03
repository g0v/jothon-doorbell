# Jothon 門鈴

g0v.github.io/jothon-doorbell/

g0v 揪松團 NPOHub 的網頁版門鈴通知系統，監控 Slack 訊息並在有人按門鈴時提供即時通知。

## 功能

- 即時監控 g0v Slack 訊息
- 視覺閃爍提醒效果
- 馬力歐金幣音效通知
- 瀏覽器通知（需要授權）
- 顯示目前時間和最後一次門鈴時間
- 可透過 URL 參數自訂監控頻道

## 使用方式

1. 直接開啟 `index.html` 會監控預設的 #Jothon 頻道
2. 若要監控其他頻道，可加上 `?channel=頻道ID` 參數，例如：
   - `index.html?channel=C0385B90D`（Jothon 頻道）
   - `index.html?channel=其他頻道ID`
3. 點擊頁面任意處以允許播放音效和通知
4. 保持分頁開啟以接收門鈴通知

## 運作原理

系統每秒會查詢 ronnywang 的 slack archive API 來檢查是否有包含「開門」的新訊息。當偵測到這類訊息時，會觸發視覺閃爍效果、馬力歐金幣音效，並在瀏覽器發送通知。
