# Credit_Card_Fraud_Detection_Comparing_models

## About Dataset

- Digital payments are evolving, but so are cyber criminals.

- According to the Data Breach Index, more than 5 million records are being stolen on a daily basis, a concerning statistic that shows - fraud is still very common both for Card-Present and Card-not Present type of payments.

- In today’s digital world where trillions of Card transaction happens per day, detection of fraud is challenging.

**This Dataset sourced by some unnamed institute.**

## Feature Explanation:

- distance_from_home - the distance from home where the transaction happened.

- distance_from_last_transaction - the distance from last transaction happened.

- ratio_to_median_purchase_price - Ratio of purchased price transaction to median purchase price.

- repeat_retailer - Is the transaction happened from same retailer.

- used_chip - Is the transaction through chip (credit card).

- used_pin_number - Is the transaction happened by using PIN number.

- online_order - Is the transaction an online order.

- fraud - Is the transaction fraudulent.

**Ref : https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud**

---

# Result

| 	| model |	resampling |	recall |	precision |	f1 |	accuracy |	auc |
|---|---|---|---|---|---|---|---|
| 0	| logistict Regression |	No |	0.554328 |	0.797191 |	0.653938 |	0.948569 |	0.941450 |
| 1	| logistict Regression |	Random oversampling |	0.886140 |	0.361035 |	0.513044 |	0.852537 |	0.943272 |
| 2	| logistict Regression |	Smote oversampling |	0.886283 |	0.360810 |	0.512841 |	0.852394 |	0.943270 |
| 3	| logistict Regression |	Borderline smote oversampling |	0.929488 |	0.298945 |	0.452391 |	0.802737 |	0.940498 |
| 4	| logistict Regression |	Adasyn oversampling |	0.927991 |	0.304368 |	0.458391 |	0.807763 |	0.941535 |
| 5	| logistict Regression |	Class weight |	0.886497 |	0.360793 |	0.512859 |	0.852369 |	0.943262 |
| 6	| Decision Tree Classifier |	No |	1.000000 |	0.999929 |	0.999964 |	0.999994 |	0.999997 |
| 7	| Decision Tree Classifier |	Random oversampling |	1.000000 |	0.999929 |	0.999964 |	0.999994 |	0.999997 |
| 8	| Decision Tree Classifier |	Smote oversampling |	1.000000 |	0.999786 |	0.999893 |	0.999981 |	0.999990 |
| 9	| Decision Tree Classifier |	Borderline smote oversampling |	1.000000 |	0.999288 |	0.999644 |	0.999938 |	0.999966 |
| 10	| Decision Tree Classifier |	Adasyn oversampling |	1.000000 |	0.999145 |	0.999572 | 	0.999925 |	0.999959 |
| 11	| Decision Tree Classifier |	Class weight |	1.000000 |	0.999929 |	0.999964 |	0.999994 |	0.999997 |
| 12	| K Neighbors Classifier |	No |	0.965920 |	0.979114 |	0.972472 |	0.995206 |	0.998918 |
| 13	| K Neighbors Classifier |	Random oversampling |	0.992870 |	0.929950 |	0.960381 |	0.992819 |	0.997750 |
| 14	| K Neighbors Classifier |	Smote oversampling |	0.993013 |	0.931078 |	0.961049 |	0.992944 |	0.998276 |
| 15	| K Neighbors Classifier |	Borderline smote oversampling |	0.990731 |	0.930868 |	0.959867 |	0.992738 |	0.998047 |
| 16	| K Neighbors Classifier |	Adasyn oversampling |	0.995152 |	0.920530 |	0.956388 |	0.992044 |	0.997930 |


- Decision Tree Classifier มีประสิทธิภาพดีที่สุดในการตรวจจับรายการ fraud
- class imbalanced ไม่มีผลต่อตัว model เพราะถึงจะไม่ทำ oversampling หรือใส่ weights ก็ได้ผลที่เหมือนกัน
