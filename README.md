# Nghiên cứu về đọc hiểu tự động cho thành ngữ tiếng Việt  
# Giới thiệu:  
  Xây dựng bộ ngữ liệu về thành ngữ, tục ngữ tiếng Việt và nghiên cứu bộ ngữ liệu đã tạo với các mô hình LLMs như BERT và các biến thể của chúng.  
# Bộ dữ liệu về thành ngữ và tục ngữ tiếng Việt (ViID):  
  Bộ ngữ liệu được xây dựng theo phương pháp Cloze-style Machine Reading Comprehension, trong đó các câu thành ngữ, tục ngữ đáp án được thay thế thành các ô **[BLANK]**, và có một danh sách đáp án sẽ được tạo ra với các đáp án ngẫu nhiên và đáp án đúng.
  Trong quá trình xây dưng, ViID có ba mức độ chính như sau:  
  - Mức 1: Điểm dữ liệu chỉ có một ô **[BLANK]**.  
  - Mức 2: Điểm dữ liệu có nhiều ô **[BLANK]** ứng với một thành ngữ, tục ngữ.
  - Mức 3: Điểm dữ liệu có nhiều ô **[BLANK]** ứng với nhiều thành ngữ, tục ngữ.

  Bộ dữ liệu gồm có 3 phiên bản:
  - Data_ver1: Bộ dữ liệu chỉ có dữ liệu ở mức 1.
  - Data_ver2: Bộ dữ liệu gồm dữ liệu ở mức 1 và 2.
  - Data_ver3: Bộ dữ liệu gồm dữ liệu ở mức 1 và 3.
# Thực nghiệm và kết quả:
  Kết quả:

|                           | Mẫu 1         | Mẫu 1           | Mẫu 2         | Mẫu 2           | Mẫu 3         | Mẫu 3           |
|---------------------------|---------------|-----------------|---------------|-----------------|---------------|-----------------|
|                           | Accuracy      | F1-score        | Accuracy      | F1-score        | Accuracy      | F1-Score        |
|                           | Dev | Test    | Dev | Test      | Dev | Test    | Dev | Test      | Dev | Test    | Dev | Test      |
| BERT-Multiligual-Cased    | 0.58 | 0.51   | 0.57 | 0.51     | 0.43 | 0.39   | 0.42 | 0.38     | 0.40 | 0.34   | 0.40 | 0.33     |
| DistilBERT-Base-VI-Cased  | 0.62 | 0.52   | 0.62 | 0.52     | 0.37 | 0.38   | 0.36 | 0.38     | 0.37 | 0.38   | 0.37 | 0.38     |
| PhoBERT                   | 0.58 | 0.54   | 0.58 | 0.54     | 0.43 | 0.38   | 0.43 | 0.38     | 0.38 | 0.36   | 0.38 | 0.36     |
| XLM-RoBERTa-base          | 0.61 | 0.52   | 0.61 | 0.51     | 0.41 | 0.41   | 0.41 | 0.40     | 0.39 | 0.36   | 0.39 | 0.36     |
| InfoXLM-Base              | 0.61 | 0.52   | 0.61 | 0.51     | 0.41 | 0.41   | 0.41 | 0.40     | 0.39 | 0.36   | 0.39 | 0.36     |

    
