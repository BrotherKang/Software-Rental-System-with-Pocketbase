這是一個簡易的單一軟體租借小系統
使用的架構是用HTML/JS搭配PocketBase來建立
因為主要是自己在用，所以很多功能還不是很完善，很歡迎大家回饋

1.首先要請下載 PocketBase
```
# 到 https://pocketbase.io/docs/ 下載對應您作業系統的版本
# 或使用以下命令（Linux/Mac）
wget https://github.com/pocketbase/pocketbase/releases/download/v0.19.0/pocketbase_0.19.0_linux_amd64.zip
unzip pocketbase_0.19.0_linux_amd64.zip
```
2.啟動 PocketBase
`./pocketbase serve`

3.在PocketBase管理介面中建立以下 Collection：
Collection: `reservations`

|  欄位名稱  | 類型  | 必填  | 說明  |
| :--: | :-----------: | :---: | :-----: |
|  unit_name  | Text  | 是  | 單位名稱  |
|  project_name  | Text  | 是  | 專案名稱  |
|  contact_name  | Text  | 是  | 聯絡人姓名  |
|   contact_phone  | Text  | 是  | 聯絡電話  |
|  quantity	Number | 是 | 預約數量  |
|  start_date	Date | 是 | 預約開始日期  |
|  end_date	Date | 是 | 預計結束日期  |
|  actual_end_date | Date | 否 | 實際結束日期  |
|  status | Select | 是 | 狀態 (active, completed, cancelled)  |

4.記得把HTML裡面的IP修改成自己的就可以了
