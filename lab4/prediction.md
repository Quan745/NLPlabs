Prediction 1 — TF-IDF + Logistic Regression
- Prediction: Mô hình có khả năng hoạt động tốt trong bài toán phân loại văn bản cơ bản.
- Reason: TF-IDF biểu diễn mức độ quan trọng của từ trong văn bản, còn Logistic Regression học mối quan hệ giữa các đặc trưng và nhãn. Phương pháp này phù hợp khi các từ hoặc cụm từ đặc trưng giúp phân biệt các lớp.
- Confidence: Khá cao đối với bài toán phân loại văn bản có tín hiệu từ vựng rõ ràng.

Prediction 2 — Average Word2Vec có chắc chắn tốt hơn TF-IDF không?
- Prediction: Không chắc chắn Average Word2Vec tốt hơn TF-IDF.
- Reason: Word2Vec biểu diễn từ bằng vector dense có thông tin ngữ nghĩa, nhưng việc lấy trung bình các vector có thể làm mất thứ tự từ và các thông tin quan trọng. TF-IDF có thể hiệu quả hơn khi những từ đặc trưng quyết định nhãn.
- Confidence: Cao đối với nhận định rằng không có phương pháp nào luôn tốt hơn trong mọi bài toán.

Prediction 3 — Tăng vocabulary size có chắc chắn làm Accuracy tăng không?
- Prediction: Không.
- Reason: Tăng vocabulary size có thể bổ sung những đặc trưng hữu ích, nhưng cũng có thể thêm từ ít xuất hiện hoặc đặc trưng nhiễu. Không phải đặc trưng mới nào cũng cải thiện khả năng tổng quát hóa của mô hình.
- Confidence: Cao.

Prediction 4 — Bỏ stopwords có chắc chắn cải thiện performance không?
- Prediction: Không.
- Reason: Một số stopwords ít đóng góp cho việc phân loại, nhưng một số từ như “not” có vai trò quan trọng đối với ngữ nghĩa và cảm xúc. Nếu loại bỏ từ phủ định, mô hình có thể mất thông tin phân biệt giữa “good” và “not good”.
- Confidence: Cao.

Prediction 5 — Accuracy và F1 có thể cho kết luận khác nhau không?
- Prediction: Có.
- Reason: Accuracy đo tỷ lệ dự đoán đúng trên toàn bộ mẫu, trong khi F1 kết hợp Precision và Recall. Khi dữ liệu mất cân bằng, Accuracy có thể cao dù mô hình nhận diện lớp thiểu số kém.
- Confidence: Cao.