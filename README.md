KNN-Remote-Recognition
=============================

專案開發時間
--------------

2017/11/24~2018/9/25

摘要
------

在KNN的文字辨識有參考到別人的Github的專案，藉此延伸到應用上。這專案透過GenData.py產生出所要文字數值儲存到flattened_images.txt，給定圖片後以TrainAndTest.py做KNN文字辨識訓練，得出圖片中的文字。

個人專案主要是為了遠端文字擷取用，首先在遠端有個能在一定時間內刷新文件資料程式，並且在每個頁面上頭尾加入標籤(page)以便於辨識頁面，接著Local端有個在遠端視窗外抓取的程式(catch_windows.py)，經過一段時間後抓完全部資料，並透過個人修改過的TrainAndTest.py，先將圖片各別做切割後會輸出到對應數字的資料夾內，對資料夾裡的圖分別做KNN辨識，先判斷圖片裡有標籤(page)並且index是前後對齊的，則輸出這串文字到data資料夾下，最後透過data_integration.py整合data資料夾所有文字資料。

Program summary
-----------------

* KNN核心技術參考 : https://github.com/MicrocontrollersAndMore/OpenCV_3_KNN_Character_Recognition_Python

