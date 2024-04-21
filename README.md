EN: 
ABSTRACT:

According to the current world situation, people are facing dangers from complex diseases accompanied by high mortality rates and stroke is one of them. According to statistics, the number of young stroke patients is increasing. Currently, stroke patients under 40 years old account for 5% of stroke patients. According to the World Health Organization, each year about 6.5 million people die from stroke. This is also the second highest cause of death in the world, accounting for about 11% of all deaths. On average, there is 1 death from stroke every 6 seconds and 1 in 6 people has a stroke. Realizing the seriousness of this disease and the need to help prevent stroke, we decided to choose the topic "Analyzing the causes and prediction of stroke".

INTRODUCE:
To clearly understand the causes of stroke, and thereby provide comments and evaluations for this prediction, our team has posed the following research questions:

- Factors affecting the rate of stroke and their impact rate:

+ Explanatory variable (X): 11 variables in the data set (except id variable).

+ Result variable (Y): stroke.

+ Usage charts (expected): Mosaic plots, correlation heatmap, scatter plot.

+ Usage method: using visual charts, data collection, data processing, statistics.

+ Meaning: determine the relationship between variables X and Y and then draw conclusions.

- Statistics on the age at which strokes usually occur:

+ Explanatory variables (X): stroke, age.

+ Outcome variable (Y): a temporary variable storing the age with the highest risk of stroke.

+ Usage chart (estimated): Histogram, boxplot, correlation heatmap, scatter plot.

+ Method used: Inferential statistics - includes methods to estimate characteristics of the population, analyze relationships between research phenomena, predict or produce results.
Decide on the basis of collecting information from sample observation results.

+ Meaning: From this statistic we can determine that age has the greatest correlation with stroke.

- Develop a program to predict stroke risk:

+ Explanatory variable (X): 11 variables in the data set (except id variable).

+ Outcome variable (Y): 1 variable containing stroke rate.

+ Charts used: Histogram, boxplot, correlation heatmap, scatter plot, Line Graph.

+ Methods used: Logistic Regression, Random Forest, Decision Tree...

+ Meaning: after execution, the result will be a stroke rate based on the input data.

DATA: 

Data pulled on Kaggle has URL:
<https://www.kaggle.com/code/joshuaswords/predicting-a-stroke-shap-lime-explainer-eli5/data>.
The data has 5120 rows and 12 columns. The data is described as follows:
- id: unique identifier
- gender: "Male", "Female" or "Other"
- age: patient's age
- hypertension: 0 if the patient does not have hypertension, 1 if the patient has hypertension
- heart_disease: 0 if the patient does not have any heart disease, 1 if the patient has heart disease
- ever_married: ever married "No" or "Yes"
- work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-Employed"
- Residence_type: "Rural" or "Urban"
- avg_glucose_level: average blood sugar level
- BMI: body mass index
- smoking_status: "previously smoked", "never smoked", "smoked" or "Unknown"
("Unknown" in smoking_status means information is not available for this patient)



VIE: 

### 1. TÓM TẮT (ABSTRACT)

Theo tình hình thế giới hiện nay, con người đang phải đối diện với các nguy hiểm từ các căn bệnh phức tạp kèm theo đó là tỷ lệ tử vong cao và đột quỵ là một trong số chúng. Theo thống kê, số lượng bệnh nhân đột quỵ trẻ ngày càng gia tăng. Hiện nay bệnh nhân đột quỵ dưới 40 tuổi đã chiếm 5% trong số bệnh =nhân đột quỵ. Theo Tổ chức Y tế thế giới, mỗi năm có khoảng 6,5 triệu người tử vong do đột quỵ. Đây cũng là nguyên nhân gây tử vong cao thứ hai trên thế giới, chiếm khoảng 11% tổng số ca tử vong. Trung bình có 1 ca tử vong do đột quỵ sau mỗi 6 giây và cứ 6 người thì có 1 người bị đột quỵ. Nhận thấy tính nghiêm trọng của căn bệnh này với nhu cầu giúp ích trong việc phòng ngừa ngăn chặn bệnh đột quỵ, chúng em quyết định chọn đề tài "Phân tích nguyên nhân và dự đoán đột quỵ".

### 2. GIỚI THIỆU (INTRODUCE)

Để hiểu rõ được nguyên nhân dẫn đến đột quỵ, từ đó đưa ra những nhận xét và đánh giá cho dự đoán này, nhóm chúng em đã đặt ra những vấn đề nghiên cứu sau:

-   Các yếu tố ảnh hưởng đến tỷ lệ đột quỵ và tỷ lệ ảnh hưởng của chúng:

+   Biến giải thích (X): 11 biến trong bộ dữ liệu (trừ biến id).

+   Biến kết quả (Y): stroke.

+   Biểu đồ sử dụng (dự tính): Biểu đồ khảm (mosaic plots), bản đồ nhiệt tương quan (correlation heatmap), biểu đồ phân tán (scatter plot).

+   Phương pháp sử dụng: sử dụng biểu đồ trực quan, thu thập dữ liệu, xử lí dữ liệu, thống kê.

+   Ý nghĩa: xác định đượng mối quan hệ giữa các biến X và Y từ đó đưa ra kết luận.

-   Thống kê độ tuổi thường mắc đột quỵ:

+   Biến giải thích (X): stroke, age.

+   Biến kết quả (Y): một biến tạm lưu độ tuổi có nguy cơ đột quỵ cao nhất.

+   Biểu đồ sử dụng (dự tính): Biểu đồ tần suất (histogram), biểu đồ hộp (boxplot), bản đồ nhiệt tương quan (correlation heatmap), biểu đồ phân tán (scatter plot).

+   Phương pháp sử dụng: Thống kê suy luận (Inferential statistics) - là bao gồm các phương pháp ước lượng các đặc trưng của tổng thể, phân tích mối liên hệ giữa các hiện tượng nghiên cứu, dự đoán hoặc ra
quyết định trên cơ sở thu thập thông tin từ kết quả quan sát mẫu.

+   Ý nghĩa: Từ thống kê này ta có thể xác định độ tuổi có tương quan lớn nhẩt với đột quỵ.

-   Xây dựng chương trình dự đoán nguy cơ đột quỵ:

+   Biến giải thích (X): 11 biến trong bộ dữ liệu (trừ biến id).

+   Biến kết quả (Y): 1 biến chứa tỷ lệ đột quỵ.

+   Biểu đồ sử dụng: Biểu đồ tần suất(histogram), biểu đồ hộp(boxplot), bản đồ nhiệt tương quan(correlation heatmap), biểu đồ phân tán (scatter plot), Line Graph(biểu đồ đường).

+   Phương pháp sử dụng: Logistic Regression (hồi quy logistic), Random Forest, Decision Tree ...

+   Ý nghĩa: sau khi thực hiện sẽ xuất ra kết quả là 1 tỷ lệ đột quỵ dựa trên các dữ liệu đầu vào.

### 3. DỮ LIỆU (DATA)

Dữ liệu được lấy trên Kaggle có URL:
<https://www.kaggle.com/code/joshuaswords/predicting-a-stroke-shap-lime-explainer-eli5/data>.
Dữ liệu có 5120 dòng và 12 cột Dữ liệu được mô tả như sau : 
- id: định danh duy nhất
- gender: "Nam", "Nữ" hoặc "Khác" 
- age: tuổi của bệnh nhân 
- hypertension: 0 nếu bệnh nhân không bị tăng huyết áp, 1 nếu bệnh nhân bị tăng huyết áp 
- heart_disease: 0 nếu bệnh nhân không mắc bất kỳ bệnh tim nào, 1 nếu bệnh nhân có bệnh tim 
- ever_married : đã từng kết hôn "Không" hoặc "Có" 
- work_type: "children", "Govt_jov", "Never_worked", "Tư nhân" hoặc "Tự kinh doanh" 
- Residence_type: "Nông thôn" hoặc "Thành thị"
- avg_glucose_level: mức đường trung bình trong máu 
- BMI: chỉ số khối cơ thể 
- smoking_status: "trước đây đã hút thuốc", "chưa bao giờ hút thuốc", "hút thuốc"hoặc "Không xác định"
("Không xác định" trong smoking_status có nghĩa là thông tin không có sẵn cho bệnh nhân này) 
- stroke: 1 nếu bệnh nhân bị đột quỵ hoặc 0 nếu không
