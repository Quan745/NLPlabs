
# LAB 05 — Sequence Models: RNN, LSTM and GRU

## 1. Mục tiêu

- Khảo sát dữ liệu IMDb Movie Reviews.
- Xây dựng baseline TF-IDF + Logistic Regression.
- Tự cài đặt một Simple RNN cell.
- Xây dựng và so sánh RNN, LSTM và GRU.
- Thực nghiệm với các giá trị max_length = 50, 100, 200.
- Đánh giá bằng Accuracy, Precision, Recall, F1 và Confusion Matrix.
- Theo dõi training loss, validation loss và training time.
- Phân tích các ví dụ dự đoán đúng và sai.

## 2. Cấu trúc dự án

```text
lab05/
├── README.md
├── calculations.md
├── prediction.md
├── rnn_cell.py
├── sequence_classification.ipynb
├── results.csv
├── learning_curves.png
├── confusion_matrix.png
├── error_analysis.md
└── reflection.md
```

## 3. Dataset

Dataset: IMDb Movie Reviews.

Các cột dự kiến:
- review: nội dung đánh giá phim.
- sentiment: nhãn positive hoặc negative.

Cần kiểm tra tên cột thực tế trước khi xử lý.

## 4. Môi trường

Python 3.10+
Jupyter Notebook hoặc Google Colab

Các thư viện:
- pandas
- numpy
- matplotlib
- scikit-learn
- torch

## 5. Pipeline

Raw reviews
→ Dataset inspection
→ Train/validation/test split
→ Tokenization
→ Vocabulary
→ Padding/truncation
→ Embedding
→ RNN/LSTM/GRU
→ Classification
→ Evaluation
→ Error analysis

## 6. Cách chạy

1. Đặt `IMDB Dataset.csv` trong thư mục dự án.
2. Cài đặt các thư viện cần thiết.
3. Chạy các cell trong `sequence_classification.ipynb` theo thứ tự.
4. Kiểm tra các bảng kết quả và biểu đồ được sinh ra.
5. Hoàn thiện các file báo cáo từ kết quả thực tế.

## 7. Nguyên tắc thực nghiệm

- Tách dữ liệu trước khi fit preprocessing.
- Giữ train/validation/test split nhất quán giữa các model.
- Dùng validation set để lựa chọn mô hình.
- Chỉ dùng test set cho đánh giá cuối cùng.
- Không so sánh model chỉ dựa trên Accuracy.
- Ghi lại seed, hyperparameters, thời gian và số tham số.

## 8. Reproducibility

Random seed: 42.

Các kết quả có thể thay đổi theo phần cứng, phiên bản thư viện,
số epoch và cấu hình thực nghiệm.
