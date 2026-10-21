LAB 05 — DỰ ĐOÁN TRƯỚC KHI THỰC NGHIỆM

1. So sánh TF-IDF + Logistic Regression và RNN

- Prediction: mô hình RNN có khả năng xử lý thứ tự từ trong câu tốt hơn TF-IDF kết hợp Logistic Regression. Tuy nhiên, TF-IDF kết hợp Logistic Regression vẫn có thể đạt kết quả phân loại cạnh tranh.

- Reason: TF-IDF biểu diễn mức độ quan trọng của các từ nhưng không trực tiếp giữ lại thứ tự xuất hiện của chúng. Trong khi đó, RNN xử lý các từ theo trình tự và cập nhật trạng thái ẩn qua từng bước, nhờ vậy có thể học được một phần thông tin ngữ cảnh.

- Confidence: 80%.

2. So sánh RNN và LSTM khi xử lý phụ thuộc dài hạn

- Prediction: LSTM có khả năng xử lý các mối phụ thuộc dài hạn tốt hơn RNN thông thường.

- Reason: RNN thông thường có thể gặp khó khăn khi học các mối quan hệ giữa những từ cách xa nhau do vấn đề tiêu biến gradient. LSTM sử dụng trạng thái ô nhớ và các cổng để kiểm soát thông tin được giữ lại, cập nhật hoặc loại bỏ.

- Confidence: 80%

3. Ảnh hưởng của độ dài chuỗi: 50, 100 và 200 từ

- Prediction: mô hình sử dụng độ dài chuỗi 100 hoặc 200 từ có thể đạt kết quả tốt hơn độ dài 50 từ vì giữ lại được nhiều thông tin hơn trong bài đánh giá. Tuy nhiên, tăng độ dài từ 100 lên 200 từ chưa chắc cải thiện kết quả.

- Reason: Chuỗi dài hơn có thể giữ lại những thông tin quan trọng về cảm xúc, nhưng cũng làm tăng thời gian tính toán và có thể chứa nhiều thông tin ít liên quan. Hiệu quả thực tế phụ thuộc vào dữ liệu và cách huấn luyện mô hình.

- Confidence: 60%

4. Ảnh hưởng của việc chỉ giữ lại 30 từ đầu tiên

- Prediction: việc cắt mỗi bài đánh giá xuống còn 30 từ đầu tiên có thể làm giảm độ chính xác phân loại so với việc sử dụng chuỗi dài hơn.

- Reason: 30 từ đầu tiên có thể chưa đủ để xác định cảm xúc tổng thể của bài đánh giá. Những ý kiến quan trọng, từ phủ định hoặc kết luận thể hiện cảm xúc có thể xuất hiện ở phần sau của văn bản.

- Confidence: 80%

Trạng thái kiểm chứng: Cần thực hiện thí nghiệm riêng với độ dài chuỗi tối đa là 30 từ để xác nhận dự đoán này.

5. LSTM có luôn tốt hơn RNN không?

- Prediction: LSTM không phải lúc nào cũng đạt kết quả tốt hơn RNN thông thường trong mọi thí nghiệm.

- Reason: Mặc dù LSTM được thiết kế để học các mối phụ thuộc dài hạn hiệu quả hơn, kiến trúc này phức tạp hơn và có thể cần nhiều thời gian tính toán, huấn luyện hơn. Kết quả còn phụ thuộc vào kích thước dữ liệu, siêu tham số và quá trình khởi tạo mô hình.

- Confidence: 80%

6. So sánh GRU và LSTM

- Prediction: GRU và LSTM có thể đạt kết quả phân loại tương đương nhau, trong khi GRU có khả năng huấn luyện nhanh hơn nhờ kiến trúc đơn giản hơn.

- Reason: GRU sử dụng cổng cập nhật và cổng đặt lại, không có trạng thái ô nhớ riêng biệt như LSTM. LSTM sử dụng trạng thái ô nhớ cùng ba cổng chính. Cấu trúc đơn giản hơn của GRU có thể giúp giảm chi phí tính toán, nhưng không đảm bảo mô hình luôn đạt độ chính xác cao hơn.

- Confidence: 60%