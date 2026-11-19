# **XÂY DỰNG CHUỖI PROMPT VIẾT BÀI PR SẢN PHẨM CÔNG NGHỆ**

## **1. Prompt 1: Nghiên cứu khách hàng mục tiêu (Research)**

**Mục tiêu:** Xác định khách hàng mục tiêu và những vấn đề mà AI Chatbot có thể giải quyết.

```
Bạn là chuyên gia nghiên cứu thị trường.

Hãy nghiên cứu khách hàng mục tiêu cho sản phẩm AI Chatbot dành cho doanh nghiệp.

Thực hiện các nhiệm vụ:
1. Xác định nhóm khách hàng mục tiêu.
2. Phân tích nhu cầu của khách hàng.
3. Liệt kê ít nhất 5 nỗi đau (Pain Points).
4. Đề xuất cách AI Chatbot giải quyết từng vấn đề.
5. Xác định lợi ích nổi bật của sản phẩm.

Thông tin sản phẩm:
- Tên: AI Chatbot Business.
- Chức năng: Tự động trả lời khách hàng 24/7.
- Hỗ trợ tư vấn sản phẩm và chăm sóc khách hàng.
- Giúp doanh nghiệp tiết kiệm thời gian và chi phí.

Đầu ra theo cấu trúc:
CUSTOMER_PROFILE:
- Khách hàng mục tiêu:
- Nhu cầu:
- Pain Points:
- Giải pháp:
- Lợi ích sản phẩm:

Yêu cầu: Trình bày rõ ràng, thực tế, không tự tạo số liệu.
```

## **2. Prompt 2: Xây dựng dàn ý bài PR (Outline)**

**Mục tiêu:** Sử dụng kết quả Prompt 1 để xây dựng dàn ý bài viết chuẩn SEO.

```
Bạn là chuyên gia Content Marketing và SEO.

Dựa trên dữ liệu CUSTOMER_PROFILE từ Prompt 1, hãy xây dựng dàn ý chi tiết cho bài PR giới thiệu sản phẩm AI Chatbot Business.

Yêu cầu:
1. Tiêu đề thu hút khách hàng.
2. Đoạn mở đầu nêu vấn đề của khách hàng.
3. Giới thiệu sản phẩm và tính năng.
4. Phân tích cách sản phẩm giải quyết Pain Points.
5. Nêu lợi ích khi doanh nghiệp sử dụng.
6. Kết luận và lời kêu gọi hành động (CTA).

Cấu trúc đầu ra:
- Headline:
- Từ khóa SEO chính:
- Từ khóa SEO phụ:
- Lead:
- H2:
  + H3:
  + H3:
- CTA:

Yêu cầu:
- Dàn ý có trình tự logic.
- Nội dung hướng đến khách hàng doanh nghiệp.
- Giữ giọng văn chuyên nghiệp, đáng tin cậy.
- Độ dài bài viết dự kiến 1000–1500 từ.

Đầu vào bắt buộc: Kết quả CUSTOMER_PROFILE từ Prompt 1.
```

## **3. Prompt 3: Viết bài PR hoàn chỉnh (Content Generation)**

**Mục tiêu:** Phát triển dàn ý thành bài PR hoàn chỉnh, có tối ưu SEO.

```
Bạn là chuyên gia viết bài PR và SEO Marketing.

Dựa trên OUTLINE từ Prompt 2, hãy viết bài PR hoàn chỉnh giới thiệu AI Chatbot Business.

Yêu cầu:
1. Độ dài từ 1000–1500 từ.
2. Có tiêu đề Headline hấp dẫn.
3. Có đoạn mở đầu Lead thu hút.
4. Triển khai đầy đủ các tiêu đề H2 và H3.
5. Phân tích rõ lợi ích sản phẩm và cách giải quyết Pain Points.
6. Phân bổ từ khóa SEO tự nhiên.
7. Có CTA rõ ràng ở cuối bài.

Quy định:
- Giữ giọng văn chuyên nghiệp, tin cậy từ đầu đến cuối.
- Không lặp ý giữa các phần.
- Không tự tạo số liệu hoặc tính năng chưa được cung cấp.
- Bám sát dàn ý Prompt 2.
- Không bỏ sót nội dung quan trọng.

Nếu bài viết bị ngắt giữa chừng:
Hãy dừng tại điểm kết thúc hiện tại và ghi lại:
+ Phần đã hoàn thành.
+ Tiêu đề đang viết.
+ Câu cuối cùng đã viết.
+ Phần nội dung chưa hoàn thành.

Khi được yêu cầu tiếp tục, phải viết tiếp chính xác từ vị trí bị ngắt, không viết lại phần cũ và giữ nguyên giọng văn.
```

## **4. Cấu trúc truyền dữ liệu giữa 3 Prompt**

| Bước     | Đầu vào            | Xử lý                 | Đầu ra                |
| -------- | ------------------ | --------------------- | --------------------- |
| Prompt 1 | Thông tin sản phẩm | Nghiên cứu khách hàng | CUSTOMER_PROFILE      |
| Prompt 2 | CUSTOMER_PROFILE   | Xây dựng dàn ý SEO    | OUTLINE               |
| Prompt 3 | OUTLINE            | Viết bài PR           | Bài viết 1000–1500 từ |

## **5. Prompt xử lý khi AI bị ngắt giữa chừng (Continue Prompting)**

```
Hãy tiếp tục viết bài PR từ vị trí bị ngắt trước đó.

Yêu cầu:
1. Đọc lại nội dung đã hoàn thành.
2. Xác định chính xác câu cuối cùng.
3. Tiếp tục ngay sau câu cuối cùng đó.
4. Không lặp lại nội dung cũ.
5. Giữ nguyên dàn ý, từ khóa SEO và giọng văn chuyên nghiệp.
6. Hoàn thành các phần còn thiếu.
7. Đảm bảo CTA nằm ở cuối bài.

Nếu tiếp tục bị ngắt, hãy ghi lại trạng thái để có thể tiếp tục ở lần sau.
```
