# seq2seq_word
seq2seq字符級別

效果非常不好，應該是哪有出了問題。

V2和 mse版本為都是最新版兩個差別在於loss函數不同
此程式為character attention seq2seq架構 輸入A產生Q

使用方式：
seq = seq2seq2_word2vec_all('P2_small_BN.h5','QA.txt') #參數說明第一個參數為儲存權重黨名稱，第二個參數為輸入txt檔

seq.train() #訓練模型

    while True:
        test_text = [input('【input Answer】 \n' )] #輸入問句
        result = seq.run_model(test_text) #產生問句
        print('【output question】 \n', result) #列印問句
