# POLYP SEGMENTATION
##Mục tiêu dự án 
Tiến hành tìm hiểu và phát triển các phương pháp phân đoạn hình ảnh dựa trên mô hình học sâu, cụ thể phương pháp này là TransNetR và TGANet.
##Giới hạn dự án
- Không so sánh thời gian thực thi của các phương pháp đã được đề xuất.
- Tập trung vào cải thiện độ chính xác và hiệu suất của các mô hình phân đoạn ảnh.
- Nghiên cứu sẽ khảo sát trên tập dữ liệu Kvasir-SEG và CVC-ClinicDB.
- Hiện thực hai mô hình TransNetR và TGANet.
- Đánh giá độ chính của các mô hình thông qua các chỉ số là: Jaccard-score, mIoU, mDSC, recall, precision và F2-score.
##Mô hình đề xuất
###TransNetR
<img width="313" height="511" alt="Screenshot 2025-07-16 122840" src="https://github.com/user-attachments/assets/22a8b308-da0c-4861-a70e-8fef50e60dc0" />
<img width="223" height="500" alt="Screenshot 2025-07-16 122847" src="https://github.com/user-attachments/assets/431540fa-bd59-495e-85c4-3711a4c81fec" />
###TGA-Net
<img width="630" height="498" alt="Screenshot 2025-07-16 123348" src="https://github.com/user-attachments/assets/217bf8bb-97e5-426d-b41e-ed488fb87787" />
##Tập dữ liệu
###Kvasir-SEG
Kích thước 46.2MB, 1000 ảnh polyp, 1000 ground truth, đuôi ảnh JPEG, độ phân giải ảnh thay đổi từ 332x487 đến 1920x1072.
<img width="491" height="167" alt="Screenshot 2025-07-16 125629" src="https://github.com/user-attachments/assets/64a05aea-0d7e-40b8-b2e8-defb1aee2a76" />
###CVC-ClinicDB
Kích thước 81MB, chứa 612 hình ảnh polyp và có 612 ground truth, đuôi ảnh JPEG, TIF, đô phân giải ảnh 384x288.
<img width="487" height="153" alt="Screenshot 2025-07-16 125645" src="https://github.com/user-attachments/assets/cc71d8ca-b7bc-45fa-a47c-7123d92f8867" />
##Kết quả thực hiện mô hình đối với từng tập dữ liệu 
###TransNetR  
<img width="692" height="179" alt="Screenshot 2025-07-16 130256" src="https://github.com/user-attachments/assets/9fa662c4-90a8-4a34-96e8-9289bbb2efc9" />
Kết quả của mô hình khi sử dụng tập dữ liệu Kvasir-SEG
<img width="700" height="169" alt="Screenshot 2025-07-16 130307" src="https://github.com/user-attachments/assets/aa2b8914-97f0-4162-bf7c-d065eeaa4bad" />
Kết quả của mô hình khi sử dụng tập dữ liệu CVC-ClinicDB
###TGA-Net
<img width="672" height="189" alt="Screenshot 2025-07-16 130534" src="https://github.com/user-attachments/assets/9d938fb5-01d8-497e-a83b-fbd3dd3f6209" />
Kết quả của mô hình khi sử dụng tập dữ liệu Kvasir-SEG
<img width="672" height="192" alt="Screenshot 2025-07-16 130543" src="https://github.com/user-attachments/assets/ca92b91e-de8b-4be5-b0fe-437de8141514" />
Kết quả của mô hình khi sử dụng tập dữ liệu CVC-ClinicDB
##Kết quả của hai mô hình thông qua các chỉ số
<img width="716" height="202" alt="Screenshot 2025-07-16 130720" src="https://github.com/user-attachments/assets/4e5f1689-ae50-4841-835f-3f106ac71dcc" />
