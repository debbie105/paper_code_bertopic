\### CSV檔案說明：



* wos\_patent.csv	原始資料集
* wos\_patent1519.csv 	2015至2019的拆分資料集
* wos\_patent2024.csv	2020至2024的拆分資料集

--------------------------------------------------------------------------------------------


\### python檔案說明



0\_data\_preprocessing



step 1.該檔案內含有資料集整合 即為整理並析出資料集WOS\_patent之keyword欄位，並進行存檔，檔案名為processed\_keywordsnew.csv，後再以此建立辭典

*pre_data\keyword_new.csv、pre_data\keywordlistnew.csv兩個檔案無差別，結果皆類似，因此選用後者進行下一步驟
*split_keywords.csv有問題不要跑
*pre_data\\keywords_with_length.csv為計算詞彙長度
*STOP.txt為停用詞檔案


step.2 進行資料預處理，除去Abstract欄位中的空值與重複值，再利用spacy與N-gram建立corpus和dictonary

*data_words_gram為Ngram生成


step 3. 建立PMI與TF-IDF，以及PMI+TF-IDF三種加權方法

*corpus\lemmatized_abstract.pickle為詞性還原後的摘要
*corpus\id2word.npy = dictionary
*corpus\word_count_corpus.npy = Term Document Frequency, word count of corpus
*corpus\word_count.npy = word count
*corpus\data_lemmatized.npy = text
*corpus\word_count_corpus_pmi.npy 
*corpus\word_count_corpus_tfidf.npy
*corpus\word_count_corpus_pmi_tfidf.npy

--------------------------------------------------------------------------------------------



2\_bertopic\_both



使用兩種加權方法的檔案



* 檔案名含roberta的檔案是使用嵌入模型：all-roberta-large-v1 
* 檔案名含all的檔案是使用嵌入模型：all-MiniLM 
* 檔案名含有dot的檔案是使用嵌入模型：msmarco-bert-base-dot-v5

檔案缺失：


--------------------------------------------------------------------------------------------



2\_bertopic\_orignal



* 檔案名含roberta的檔案是使用嵌入模型：all-roberta-large-v1 
* 檔案名含all的檔案是使用嵌入模型：all-MiniLM 
* 檔案名含有dot的檔案是使用嵌入模型：msmarco-bert-base-dot-v5


--------------------------------------------------------------------------------------------



2\_bertopic\_tfidf



* 檔案名含roberta的檔案是使用嵌入模型：all-roberta-large-v1 
* 檔案名含all的檔案是使用嵌入模型：all-MiniLM 
* 檔案名含有dot的檔案是使用嵌入模型：msmarco-bert-base-dot-v5



--------------------------------------------------------------------------------------------



2\_bertopic\_pmi



* 檔案名含roberta的檔案是使用嵌入模型：all-roberta-large-v1 
* 檔案名含all的檔案是使用嵌入模型：all-MiniLM 
* 檔案名含有dot的檔案是使用嵌入模型：msmarco-bert-base-dot-v5



--------------------------------------------------------------------------------------------


\### xlsx檔與ppt檔說明：



* 論文表格收錄.xlsx	該檔案收錄論文中所有表格內數據
* 論文圖表收錄ppt	該檔案收錄論文中所有圖片與表格(轉成圖片)


--------------------------------------------------------------------------------------------

\### 3_wordcloud_embeding_test.ipynb

* 該檔案內部包含VOS json檔的文字雲與STS資料集的測試
* 原本計算嵌入模型之嵌入字數(論文用的)程式碼遺失


--------------------------------------------------------------------------------------------

\### json檔

202505021~202505024是整體VOSviewer檔案
保護0409跟law0409是專利保護與專利法的VOSviewer檔案



