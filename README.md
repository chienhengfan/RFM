這是用測試資料來做RFM的程式

目的:區分客戶的等級，可延伸到觀察區域銷售資料的比較

定義單位: 以個人維單位
原因: 因為此資料來源維電商銷售資料，故推測受到地緣因素的影響較小


程式可拆分為以下幾個part:

1.資料清理
  >>>根據不同資料來源，ETL的方式也不同

2.RFM建立
  >>>找出指定時間內的最近一次消費、總消費金額、期間內消費次數
  >>>以電商為例，3個月未消費可說是已經失去的客戶，因此時段抓3個月較佳
  >>>因資料來源時間長度不夠，故以月區分
 
3.資料呈現
  >>>目前是以2個區間的資料差異 來呈現
  >>>未來希望以更好的方式呈現，如圖表視覺化
  
遇到的困難:
  >>>RFM是一個很吃行業經驗的模型，因為在最後給定分數完全要依賴對該產業的了解程度，無法像SVM或是KNN用演算法得到明確的切割點
