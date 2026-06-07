# HDFS資料集(https://huggingface.co/datasets/logfit-project/HDFS_v1)
使用 HDFS 資料集，取其中 387 筆資料進行訓練，我們針對系統沒有識別出來但有異常的項目(Anomaly=True & Level=INFO)，以及系統覺得有異常實際沒有問題的項目(Anomaly=False & Level=WARN) (False Alarm)，也進行取樣，為了避免資料不平衡造成訓練時模型產生偏頗，因此在一開始資料選清理時，進行平均取樣，確保每個項目的訓練資料數沒有急遽的落差。

訓練資料: hdfs_matrix_train.json

測試資料: hdfs_matrix_test.json (取5筆訓練沒看過的資料)

# 訓練程式碼
hdfs_train.ipynb

