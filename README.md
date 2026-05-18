📱 Smartphone Price Prediction using Machine Learning

📌 Project Overview

Dự án này tập trung vào việc xây dựng mô hình học máy (Machine Learning) để dự đoán giá bán thực tế của điện thoại thông minh dựa trên các thông số kỹ thuật. Mục tiêu là giúp các nhà bán lẻ tự động hóa chiến lược định giá và cung cấp thông tin chi tiết về các yếu tố ảnh hưởng mạnh nhất đến giá trị sản phẩm.

📊 Dataset

Nguồn: MobilePhone Dataset (Kaggle).

Quy mô: 1,715 bản ghi với 31 biến đặc trưng.

Các đặc trưng chính: RAM, Bộ nhớ trong (Storage), Chipset, Dung lượng pin, Trọng lượng, Kích thước màn hình, Thương hiệu, v.v.

🛠 Methodology (Quy trình thực hiện)

Data Preprocessing:

Xử lý giá trị thiếu (Missing values) bằng phương pháp Brand-based Imputation (điền khuyết dựa trên giá trị trung bình/yếu vị của từng hãng).

Xử lý Data Leakage bằng cách loại bỏ các biến dẫn xuất từ giá mục tiêu.
Feature Engineering:

Tạo biến 'Performance' dựa trên sự kết hợp giữa RAM và Storage để phản ánh hiệu năng thực tế.

Mã hóa biến định danh (Encoding) và chuẩn hóa dữ liệu.

Exploratory Data Analysis (EDA):

Sử dụng Histogram, Boxplot và Scatter plot để tìm mối tương quan.

Phân tích phân khúc thương hiệu (Premium vs. Budget).

Modeling:

Huấn luyện các mô hình: Linear Regression, Decision Tree, Random Forest.

Tối ưu hóa mô hình XGBoost Regressor làm mô hình cuối cùng.

📈 Results & Performance

Mô hình XGBoost đạt được kết quả ấn tượng:

R-squared (R²): 84.4%

Mean Absolute Error (MAE): 74.29 (đơn vị tiền tệ)

💡 Key Insights

Dung lượng lưu trữ (Storage) là yếu tố quan trọng nhất ảnh hưởng đến việc tăng/giảm giá.

Trọng lượng máy (Weight) đóng vai trò là một "biến đại diện" (proxy) cho chất lượng vật liệu (nhôm/thép vs. nhựa), phản ánh phân khúc cao cấp của sản phẩm.

Dung lượng Pin có ảnh hưởng rất ít đến giá bán ở phân khúc Flagship.

💻 Tech Stack

Language: Python

Libraries: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn.

Tools: Jupyter Notebook / Google Colab.
