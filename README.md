# Tomtatvanban
 Mô tả bài toán: Khi đọc một bài báo, truyện ...... dài vươn thì mình rất nản, hoa cả mắt, nên mình muốn tạo ra một chương trình có thể tóm tắt những ý chính có thể có ích với mình, ngắn ngắn thôi :))
 Ý tưởng: Loại bỏ ngững câu tương tự để rút gọn văn bản
 Mục tiêu: Mình sẽ xây dựng ứng dụng hoành tráng, khủng bố, bá đạo triệu đô :))) (đùa thôi). Mình sẽ dùng thuật toán phân cụm kmean, tiền xử lí văn bản, vecto hóa....
 Cách xây dựng:
 B1: Bạn cần nhập các văn bản cần rút gọn tại file data
 B2: Tiền xử lí văn bản: Loại bỏ những khoảng trắng thừa, chuyển hết chữ hoa về chữa thường.........
 B3: Tách câu trong văn bản: Ở bước này, chúng ta sẽ tách 1 đoạn văn bản cần tóm tắt đã qua xử lý thành 1 danh sách các câu trong nó
 B4: Chuyển các câu sang dạng vector số thực: Để phục vụ cho phương pháp tóm tắt ở bước tiếp theo, chúng ta cần chuyển các câu văn (độ dài ngắn khác nhau) thành các vector số thực có độ dài cố định, sao cho vẫn phải đảm bảo được "độ khác nhau" về ý nghĩa giữa 2 câu cũng tương tự như độ sai khác giữa 2 vector tạo ra. Điều này mình sẽ giới thiệu một phương pháp mình cho là khá đơn giản cũng như giải thích kỹ hơn cho các bạn ở phần sau khi chúng ta đi vào code.
 B5: Phân cụm: Với các bạn nghiên cứu về Machine Learning thì đây chắc hẳn là một thuật toán rất quen thuộc (K-Means Clustering). Thuật toán này sẽ giúp chúng ta phân ra những cụm câu có ý nghĩa giống nhau, để từ đó chọn lọc và loại bỏ bớt các câu có cùng ý nghĩa.
 B6: Xây dựng đoạn văn bản tóm tắt: Sau khi đã có các cụm, trong mỗi cụm (phân loại theo ý nghĩa), chúng ta sẽ chọn ra 1 câu duy nhất trong cụm đó để tạo nên văn bản được tóm tắt!
 
 
