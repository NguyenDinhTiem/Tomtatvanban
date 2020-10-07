# Tóm tắt văn bản
<p><b>Mô tả bài toán</b>:Khi đọc một bài báo, truyện ...... dài vươn thì mình rất nản, hoa cả mắt, nên mình muốn tạo ra một chương trình có thể tóm tắt những ý chính có thể có ích với mình, ngắn ngắn thôi :))</p>
<p><b>Ý tưởng</b>: Loại bỏ ngững câu tương tự để rút gọn văn bản
_Mục tiêu_: Mình sẽ xây dựng ứng dụng hoành tráng, khủng bố, bá đạo triệu đô :))) (đùa thôi). Mình sẽ dùng thuật toán phân cụm kmean, tiền xử lí văn bản, vecto hóa....</p>
<p><b>Cách xây dựng</b>:
<p>B1:Bạn cần nhập các văn bản cần rút gọn tại file data</p> 

```python
import pickle
```


```python
contents = {1:'Mây tương đối nặng. Nước trong các đám mây điển hình có thể có khối lượng hàng triệu tấn, mặc dù mỗi mét khối mây chứa chỉ khoảng 5 gam nước. Các giọt nước trong mây nặng hơn hơi nước khoảng 1.000 lần, vì thế chúng nặng hơn không khí. Lý do tại sao chúng không rơi, mà lại được giữ trong khí quyển là các giọt nước lỏng được bao quanh bởi không khí ấm. Không khí bị ấm lên do năng lượng nhiệt giải phóng khi nước ngưng tụ từ hơi nước. Do các giọt nước rất nhỏ, chúng "dính" với không khí ấm. Khi mây được tạo thành, không khí ấm mở rộng hơn là giảm thể tích sau khi hơi nước ngưng tụ, làm cho các đám mây bị đẩy lên cao, và sau đó mật độ riêng của mây giảm tới mức mật độ trung bình của không khí và mây trôi đi trong không khí.',
            2:'Vào ngày sinh nhật lần thứ 8 của em, bà ngoại có tặng em một chú mèo rất dễ thương và đáng yêu. Vừa nhìn thấy chú là em đã vui mừng và thích thú lắm. Em thường gọi chú với cái tên dễ thương là Mi.Meo, meo, meo, hôm nào cũng vậy, cứ khi em ngồi vào bàn học bài là chú Mi lại đến nằm dụi đầu vào chân em. Mi thân thiết và gắn bó với em từng ngày. Ngày bà ngoại cho, con mèo chỉ bằng chai nước khoáng nhỏ nhưng bây giờ thì nó đã to bằng cái chai Cô-ca đại bự. Toàn thân chú được bao phủ một màu vàng và điểm thêm vài vệt trắng làm cho chiếc áo của chú lại càng thêm đẹp.Cái đầu của chú to hơn quả bóng ten-nít một chút. Đôi mắt tròn như hai hòn bi ve và sáng như đèn pha. Cái mũi phơn phớt hồng, lúc nào cũng ươn ướt như người bị cúm sổ mũi vậy. Cái tai của chú mới thính làm sao! Chỉ một tiếng động nhỏ, chú đều phát hiện được đó là tiếng gì, có cần phải giải quyết hay không. Cái tai và cái mũi đó chính là cái ra-đa của chú để phát hiện những tên chuột láu lỉnh hay phá hoại, ăn trộm thóc gạo của người.',
            3:'Cổ Mi được quàng một chiếc khăn màu trắng đục. Bốn cái chân không cao lắm so với thân hình chú nhưng lại chạy rất nhanh. Dưới bàn chân là một lớp thịt dày, mịn, màu hồng nhạt. Bà em bảo những miếng thịt đó giúp Mi di chuyển nhẹ nhàng, không gây một tiếng động nhỏ, làm cho nhiều chú chuột không ngờ. Những chiếc vuốt của chú rất nhọn và sắc. Đã có lần, những chiếc vuốt đó đã để lại dấu vết trên tay em khi em đùa vui, nghịch ngợm với chú. Chính những chiếc vuốt đó là thứ vũ khí lợi hại của chú mà mỗi con chuột khi nhìn thấy phải kinh hoàng.Mỗi khi muốn chơi với em, chú lại dùng đầu dụi vào tay em rồi lấy những cái vuốt ấy cào cào nhẹ vào bàn tay em. Chao ôi! Cái đuôi của chú mới dẻo làm sao! Chiếc đuôi như một cái dấu ngã, chẳng giấu vào đâu được. Hôm nào cũng vậy, chú ta cứ ngủ khì. Thế nhưng lũ chuột cũng chẳng dám ra quấy phá vì chú rất tinh, cũng có thể lũ chuột cảnh giác, nghĩ là Mi đang rình chúng đấy.',
            4:'Ban đêm, Mi ta mới đi làm cho chủ. Chú ta biết hết đường đi lối lại của bọn chuột. Không con chuột nào chạy thoát nếu chú đã phát hiện được. Có lần, em được chứng kiến nó bắt chuột ban ngày. Có lẽ, con chuột đó đói quá phải đi ăn trộm ban ngày. Chú Mi ngụy trang rất khéo, chú nằm khuất sau cái chổi cạnh chân hòm cáng thóc. Một con chuột nhắt rất tinh ranh, mắt lấm lét, đi nhẹ nhàng đến định trèo lên hòm thóc để chui vào ăn thóc. Mi nằm yên như đang ngủ. Bỗng “chụp” một cái, chỉ nghe thấy tiếng “chít” tuyệt vọng, Mi ta đã vồ gọn con mồi trong móng vuốt của chú.Hả hê với chiến thắng của mình, Mi tha con chuột đó ra vườn. Chú nhả con chuột ra, lấy cái chân trước vờn đi vờn lại con chuột đó. Con chuột vội chạy đi nhưng chạy sao thoát. Em nghĩ con chuột đó chỉ sợ đã chết. Thế rồi, chú ta ung dung ngồi chén hết con chuột nhắt đó. Mỗi lần chú bắt được chuột, em đều vuốt ve động viên chú. Đến bữa, em lại thưởng cho chú những miếng ăn ngon nhất. Mi tỏ vẻ sung sướng lắm.Mi ăn rất ít, hàng ngày chú ta ăn không hết một bát cơm. Khi ăn, chú ta cứ nhỏ nhẻ từng tí một. Em thường nghe mọi người nói “ăn như mèo” quả không sai. Dù đói đến đâu thì Mi cũng ăn rất từ tốn. Khác với Vàng - chú cún tinh nghịch nhà em, cứ ăn hùng hục. Vàng và Mi rất thân với nhau. Ngày nào, chúng cũng chơi đùa với nhau mà không có xích mích gì cả.Buổi sáng, khi nắng vàng trải khắp sân, Mi nằm duỗi dài bốn chân, mắt lim dim, trông thật đáng yêu. Thỉnh thoảng, nó lại cho tay lên mặt cào cào, như là nó đang rửa mặt. Buổi tối, khi cả nhà ăn cơm xong, bao giờ Mi cũng tranh thủ ngồi vào lòng em nũng nịu.Em rất yêu quý Mi. Mi không chỉ là vật kỉ niệm của bà ngoại tặng cho em mà nó còn là “dũng sĩ diệt chuột” của nhà em. Mi giúp nhà em rất nhiều trong chiến dịch diệt chuột. Từ ngày có Mi, nhà em không còn lo lũ chuột quấy phá. Em sẽ chăm sóc Mi cho khỏe, chơi với Mi vui vẻ để làm theo đúng lời dặn của bà em khi bà tặng Mi cho em.',
           }
filename = "data.pkl"
file = open(filename, "wb")
pickle.dump(contents, file)
```




<p>B2: Tiền xử lí văn bản: Loại bỏ những khoảng trắng thừa, chuyển hết chữ hoa về chữa thường.........</p>

```python
contents_parsed = content.lower() #Biến đổi hết thành chữ thường
contents_parsed = contents_parsed.replace('\n', '. ') #Đổi các ký tự xuống dòng thành chấm câu
contents_parsed = contents_parsed.strip() #Loại bỏ đi các khoảng trắng thua
```
<p>B3: Tách câu trong văn bản: Ở bước này, chúng ta sẽ tách 1 đoạn văn bản cần tóm tắt đã qua xử lý thành 1 danh sách các câu trong nó</p>

```python
#Tách các câu trong đoạn văn
import nltk
#nltk.download('punkt')
```
```python
sentences = nltk.sent_tokenize(contents_parsed.lower().strip())
```
```python
print(sentences)
```

    ['ban đêm, mi ta mới đi làm cho chủ.', 'chú ta biết hết đường đi lối lại của bọn chuột.', 'không con chuột nào chạy thoát nếu chú đã phát hiện được.', 'có lần, em được chứng kiến nó bắt chuột ban ngày.', 'có lẽ, con chuột đó đói quá phải đi ăn trộm ban ngày.', 'chú mi ngụy trang rất khéo, chú nằm khuất sau cái chổi cạnh chân hòm cáng thóc.', 'một con chuột nhắt rất tinh ranh, mắt lấm lét, đi nhẹ nhàng đến định trèo lên hòm thóc để chui vào ăn thóc.', 'mi nằm yên như đang ngủ.', 'bỗng “chụp” một cái, chỉ nghe thấy tiếng “chít” tuyệt vọng, mi ta đã vồ gọn con mồi trong móng vuốt của chú.hả hê với chiến thắng của mình, mi tha con chuột đó ra vườn.', 'chú nhả con chuột ra, lấy cái chân trước vờn đi vờn lại con chuột đó.', 'con chuột vội chạy đi nhưng chạy sao thoát.', 'em nghĩ con chuột đó chỉ sợ đã chết.', 'thế rồi, chú ta ung dung ngồi chén hết con chuột nhắt đó.', 'mỗi lần chú bắt được chuột, em đều vuốt ve động viên chú.', 'đến bữa, em lại thưởng cho chú những miếng ăn ngon nhất.', 'mi tỏ vẻ sung sướng lắm.mi ăn rất ít, hàng ngày chú ta ăn không hết một bát cơm.', 'khi ăn, chú ta cứ nhỏ nhẻ từng tí một.', 'em thường nghe mọi người nói “ăn như mèo” quả không sai.', 'dù đói đến đâu thì mi cũng ăn rất từ tốn.', 'khác với vàng - chú cún tinh nghịch nhà em, cứ ăn hùng hục.', 'vàng và mi rất thân với nhau.', 'ngày nào, chúng cũng chơi đùa với nhau mà không có xích mích gì cả.buổi sáng, khi nắng vàng trải khắp sân, mi nằm duỗi dài bốn chân, mắt lim dim, trông thật đáng yêu.', 'thỉnh thoảng, nó lại cho tay lên mặt cào cào, như là nó đang rửa mặt.', 'buổi tối, khi cả nhà ăn cơm xong, bao giờ mi cũng tranh thủ ngồi vào lòng em nũng nịu.em rất yêu quý mi.', 'mi không chỉ là vật kỉ niệm của bà ngoại tặng cho em mà nó còn là “dũng sĩ diệt chuột” của nhà em.', 'mi giúp nhà em rất nhiều trong chiến dịch diệt chuột.', 'từ ngày có mi, nhà em không còn lo lũ chuột quấy phá.', 'em sẽ chăm sóc mi cho khỏe, chơi với mi vui vẻ để làm theo đúng lời dặn của bà em khi bà tặng mi cho em.']
    

<p> B4: Chuyển các câu sang dạng vector số thực: Để phục vụ cho phương pháp tóm tắt ở bước tiếp theo, chúng ta cần chuyển các câu văn (độ dài ngắn khác nhau) thành các vector số thực có độ dài cố định, sao cho vẫn phải đảm bảo được "độ khác nhau" về ý nghĩa giữa 2 câu cũng tương tự như độ sai khác giữa 2 vector tạo ra. Điều này mình sẽ giới thiệu một phương pháp mình cho là khá đơn giản cũng như giải thích kỹ hơn cho các bạn ở phần sau khi chúng ta đi vào code.</p>

```python
from gensim.models import KeyedVectors 
#Chuyển các câu thành vecto
w2v = KeyedVectors.load_word2vec_format("vi.vec")
```


```python
vocab = w2v.wv.vocab
```
<p>B5: Phân cụm: Với các bạn nghiên cứu về Machine Learning thì đây chắc hẳn là một thuật toán rất quen thuộc (K-Means Clustering). Thuật toán này sẽ giúp chúng ta phân ra những cụm câu có ý nghĩa giống nhau, để từ đó chọn lọc và loại bỏ bớt các câu có cùng ý nghĩa.
</p>

```python
# tách các từ trong câu và lấy tổng để được các vector cho từng câu trong danh sách mà chúng ta vừa có trên kia
X = []
for sentence in sentences:
    sentence = ViTokenizer.tokenize(sentence)
    words = sentence.split(" ")
    sentence_vec = np.zeros((100))
    for word in words:
        if word in vocab:
            sentence_vec+=w2v.wv[word]
    X.append(sentence_vec)

```
<p> B6: Xây dựng đoạn văn bản tóm tắt: Sau khi đã có các cụm, trong mỗi cụm (phân loại theo ý nghĩa), chúng ta sẽ chọn ra 1 câu duy nhất trong cụm đó để tạo nên văn bản được tóm tắt!
</p>

```python
from sklearn.metrics import pairwise_distances_argmin_min
#xây dựng văn bản tóm tắt
avg = []
for j in range(n_clusters):
    idx = np.where(kmeans.labels_ == j)[0]
    avg.append(np.mean(idx))
closest, _ = pairwise_distances_argmin_min(kmeans.cluster_centers_, X)
ordering = sorted(range(n_clusters), key=lambda k: avg[k])
summary = ' '.join([sentences[closest[idx]] for idx in ordering])
```


```python
summary
```
```
 'chú mi ngụy trang rất khéo, chú nằm khuất sau cái chổi cạnh chân hòm cáng thóc. bỗng “chụp” một cái, chỉ nghe thấy tiếng “chít” tuyệt vọng, mi ta đã vồ gọn con mồi trong móng vuốt của chú.hả hê với chiến thắng của mình, mi tha con chuột đó ra vườn. em nghĩ con chuột đó chỉ sợ đã chết. khi ăn, chú ta cứ nhỏ nhẻ từng tí một. mi tỏ vẻ sung sướng lắm.mi ăn rất ít, hàng ngày chú ta ăn không hết một bát cơm. ngày nào, chúng cũng chơi đùa với nhau mà không có xích mích gì cả.buổi sáng, khi nắng vàng trải khắp sân, mi nằm duỗi dài bốn chân, mắt lim dim, trông thật đáng yêu. mi không chỉ là vật kỉ niệm của bà ngoại tặng cho em mà nó còn là “dũng sĩ diệt chuột” của nhà em. em sẽ chăm sóc mi cho khỏe, chơi với mi vui vẻ để làm theo đúng lời dặn của bà em khi bà tặng mi cho em.'

```
