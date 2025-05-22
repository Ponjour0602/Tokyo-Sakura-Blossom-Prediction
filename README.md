# Tokyo-Sakura-Blossom-Prediction
Predicting Cherry Blossom Bloom in Tokyo Using Traditional Statistical Methods and Machine Learning

此專案在預測日本東京櫻花的開花日期，基於 TasnimAhmedEee 的原始專案，進行一些修改、微調，使用傳統統計、迴歸、機器學習模型進行開花日預測。

# 簡介
以東京地區過去的氣溫資料為基礎，來預測東京的開花日，使用了三種方法來預測。  

資料集來源：日本氣象廳（日本東京歷年氣象數據、開花日紀錄）

 # 模型說明
	•	600度法則：從2月1日起，累積每日的「最高氣溫」總和達到 600 度的那一天即開花日
	•	迴歸模型： 使用阿瑞尼斯方程式來應用迴歸模型計算「冬眠結束日」到「開花日」所需日數
	•	MLP模型： 利用 PyTorch 建立深度神經網路，輸入每年前 120 天的氣象特徵，預測開花所需天數  

# 評估指標
	•	平均平方誤差（MSE）
	•	平均平方根誤差（RMSE）
	•	決定係數（R² Score）

 # 檔案說明
	•	Data Crawler for Blossom Date.ipynb：獲取東京的開花日歷史紀錄
	•	Data Crawler for Tokyo Weather.ipynb：獲取東京的過去每日氣象記錄
	•	Data Preprocessing.ipynb：將所有資料做前處理
	•	weather_dataset.csv：前處理後的資料集
 	•	train.csv：訓練集
	•	test.csv：測試集
	•	600 Degree Rule.ipynb：600度法則預測
 	•	Linear Regression（DTS Formula）.ipynb：迴歸模型預測
 	•	MLP（Feature=5） .ipynb：多層感知機預測（選定特徵5項）
 	•	MLP（Feature=6） .ipynb：多層感知機預測（選定特徵6項）
 	•	MLP（Feature=11） .ipynb：多層感知機預測（選定特徵11項）

  # 參考資料來源： https://github.com/TasnimAhmedEee/Cherry-Blossom-Date-Prediction
