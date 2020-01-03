# fast_bert繁體中文文本分類

# 環境  
python 3.6 用colab做訓練  
nvcc和torch.version.cuda版本要一樣才可以跑  
fast_bert算是新套件，會頻繁更新  
我程式碼在以後的版本不一定以後能用  
套件有多新參數請多Google爬文或是發問  

不是在我這邊發問 沒有用  
要去fast_bert作者Kaushal Trivedi的github那邊  
https://github.com/kaushaltrivedi/fast-bert


# 分類  

分類洋蔥理論的語句

    label 1 個人淺層資訊、愛好、興趣
    label 2 個人態度、處事觀點
    label 3 隱私、秘密、不被人接受的想法

輸入為一句話，輸出為一個dictionary  
輸出範例為['label1','0.3522','label2','0.245621','label3','0.12345']  
由大到小排序，輸出為機率

心理學家認為  
只要對話從最外層label 1慢慢往內層前進，就代表那個人跟自己的羈絆越深  
再用其他程式碼輔助兩人對話。

# 資料來源  

來自Dcard心情版和關係版  
如果要爬蟲的話在這邊  
https://github.com/ttpss930141011/Dcard_comment-Crawler  
這個爬蟲也可以爬其他版的ㄛ

# 模型正確性  
此模型的lable 3很不準，因為資料量少  
我只有一個人搞這個，資料自己標記到2000多筆就不錯了拉  
我的訓練資料有缺點，我強制把資料轉為互斥型態  
是label1就不會是label2、label3  
但正常的對話有可能是一句話包含label1、label2、label3的  
模型的訓練集也可以這樣輸入，進而訓練出更貼近人的模型  
相對的訓練數據也需要更多
阿幹我就是一個人阿 所以就這樣吧


# 模型訓練後的prediction  
模型訓練完後要進行文本預測的程式碼我會放在這邊  
https://github.com/ttpss930141011/fast_bert-Model-Prediction

# 致謝  
感謝wshuyi大大開啟我的fast_bert深度學習之路  
想入門的話可以看此為大大的詳細教學文  
了解一下各參數所代表的意義  
https://zhuanlan.zhihu.com/p/66440354  
與Github  
https://github.com/wshuyi


