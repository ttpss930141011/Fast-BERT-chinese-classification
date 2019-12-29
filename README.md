# fast_bert繁體中文文本分類

分類洋蔥理論的語句
label 1 個人淺層資訊、愛好、興趣
label 2 個人態度、處事觀點
label 3 隱私、秘密、不被人接受的想法

只要對話從最外層label 1慢慢往內層前進，就代表那個人跟自己的羈絆越深
再用其他程式碼輔助兩人對話。
資料來源是dcard心情版和關係版

此模型的lable 3很不準，因為資料量少，我只有一個人搞這個，資料自己標記到2000多筆就不錯了拉

python 3.6 用colab做訓練
nvcc和torch.version.cuda版本要一樣才可以跑
fast_bert算是新套件，會頻繁更新
我程式碼在以後的版本不一定以後能用

感謝wshuyi大大開啟我的fast_bert深度學習之路
想入門的話可以看此為大大的詳細教學文
https://zhuanlan.zhihu.com/p/66440354

只是他的程式碼已經因為fast_bert更新而不能用了
pytorch_transformers這個套件也會一直更新
所以要看改了哪裡，去調適程式碼
有甚麼更新的話請在fast_bert作者Kaushal Trivedi的github查詢或提問

