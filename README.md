# JS-Mapty
The given code is a workout tracking application that allows users 
to add and view their workouts on a map. 
It uses Leaflet.js library for map functionality. 
The application supports two types of workouts: running and cycling. 
The user can input the details of their workout, such as distance, duration, cadence, 
and elevation gain. The application then displays the workout on the map as a marker 
and also lists it in the workout list. The workouts are stored in local storage, 
allowing the user to retrieve their previous workouts even after refreshing the page.

這段程式碼是用於追蹤運動的應用程式的前端部分，它主要做以下幾件事：

1. 匯入必要的 HTML 元素和 Leaflet 庫，用於在地圖上顯示位置資訊。
2. 定義了三個類別：`Workout`、`Running` 和 `Cycling`。 `Workout` 類別是父類，`Running` 和 `Cycling` 類別繼承自 `Workout` 類，用於表示不同類型的運動。
3. 創建了幾個範例對象，包括 `run1` 和 `cycling1`，這些對象代表了不同類型的運動，包括跑步和騎自行車。
4. 定義了一個名為 `App` 的主應用程式類，該類別包含了整個應用程式的主要邏輯。
5. 在 `App` 類別的建構子中，執行了以下操作：
    - 取得使用者的地理位置資訊。
    - 從本地儲存中取得先前儲存的運動資料。
    - 新增事件監聽器，以便在表單提交時建立新的運動記錄。
    - 新增事件監聽器，以便在選擇不同的運動類型時切換表單欄位的可見性。
    - 新增事件監聽器，以便在點擊運動記錄清單中的項目時將地圖視圖移至對應的位置。
6. `_getPosition` 方法用於獲取使用者的地理位置信息，如果瀏覽器支援地理位置資訊獲取的話。
7. `_loadMap` 方法用來載入 Leaflet 地圖，並在地圖上顯示使用者的位置。
8. `_showForm` 方法用來顯示運動記錄輸入表單。
9. `_hideForm` 方法用於隱藏運動記錄輸入表單，並清空輸入欄位。
10. `_toggleElevationField` 方法用於切換高程和步頻欄位的可見性。
11. `_newWorkout` 方法用於建立新的運動記錄對象，根據使用者的輸入資料以及選擇的運動類型。
12. `_renderWorkoutMarker` 方法用於在地圖上顯示運動記錄的標記。
13. `_renderWorkout` 方法用於在運動記錄清單中渲染運動記錄的詳細資訊。
14. `_moveToPopup` 方法用於點擊運動記錄清單中的項目時將地圖視圖移至對應的位置。
15. `_setLocalStorage` 和 `_getLocalStorage` 方法分別用於將運動資料儲存到本地儲存和從本地儲存中取得資料。
16. 最後，創建了一個 `App` 類別的實例，啟動了整個應用程式。

這個應用程式的主要功能是允許使用者記錄不同類型的運動，並在地圖上顯示這些運動的位置和詳細資訊。 同時，它還支援將運動資料保存在本地儲存中，以便在頁面重新載入時保留資料。
