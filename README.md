# 2022AICUP-NLP-competition-

## 任務敘述
本競賽的每一筆輸入資料為一個三元組(q, r, s)，q是一則英文論述，r是一則對q進行回應的英文短文，s則是r對q的議論關係，可能是同意（agree）或不同意（disagree）。
輸出資料則是一個雙元組(q',r')，q'與r'分別是q與r的子序列（subsequence），且q'與r'提供了關鍵性的資訊，足以判斷q與r呈現s的關係。

## 評分方式
![image](https://user-images.githubusercontent.com/62208230/228327184-f8b4aa6d-34d8-44c7-b772-1457206d11af.png)

## 想法
透過QA模型來提取q',r'，所以先找出q_start,q_end,r_start,r_end作為訓練label
![image](https://user-images.githubusercontent.com/62208230/228325925-d446e4af-50fc-426a-8c9e-12e045cdc4c6.png)

## 模型測試
在huggingface上許多NLP相關模型，在嘗試Bert,Distilt-Bert, Multilingual-Bert, RoBERTa等模型後，發現以RoBERTa作為預訓練模型進行fine-tune得到的效果最好

## 結果
private score得到0.86
![image](https://user-images.githubusercontent.com/62208230/228327015-c8669ff6-7b21-441c-8a33-08d41439d894.png)
