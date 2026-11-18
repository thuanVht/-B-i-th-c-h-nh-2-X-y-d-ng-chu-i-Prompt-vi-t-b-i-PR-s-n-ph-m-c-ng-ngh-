

**Biến đầu vào**
```
SẢN_PHẨM: ChatAssist AI | NGÀNH: Bán lẻ
TÍNH_NĂNG: trả lời 24/7, tích hợp CRM, chuyển tiếp cho nhân viên
TỪ_KHÓA_CHÍNH: AI chatbot doanh nghiệp | TỪ_KHÓA_PHỤ: chăm sóc khách hàng tự động, chatbot bán lẻ
TONE: chuyên nghiệp, tin cậy
```

**Prompt 1: Nghiên cứu pain points**
```
Bạn là chuyên gia nghiên cứu thị trường B2B.
Sản phẩm: {SẢN_PHẨM}; tính năng: {TÍNH_NĂNG}; ngành: {NGÀNH}.
Nhiệm vụ: xác định 2 persona, mỗi persona 3 pain points, ghép với 1 tính năng, xếp hạng mức cấp thiết.
Ràng buộc: không bịa số liệu.
Chỉ trả về JSON: {"personas":[{"id":"P1","title":"","pain_points":[{"id":"P1-PP1","problem":"","matched_feature":"","priority":1}]}],"top_3":["P1-PP1"]}
```

**Prompt 2: Dàn ý (đầu vào bắt buộc là Output 1)**
```
Bạn là Content Strategist SEO.
<OUTPUT_1>{dán JSON Prompt 1}</OUTPUT_1>
Từ khóa chính: {TỪ_KHÓA_CHÍNH}; phụ: {TỪ_KHÓA_PHỤ}; độ dài 1000-1500 từ; tone: {TONE}.
Lập dàn ý: Headline, Lead, các H2/H3 (mỗi mục gắn pain point ID), CTA, kèm số từ từng mục.
Ràng buộc: phải có đủ top_3 pain points, không thêm tính năng ngoài đầu vào.
Chỉ trả về JSON: {"headline":"","lead":{"pp":[],"words":0},"sections":[{"h2":"","h3":[""],"pp":[],"words":0}],"cta":{"action":"","words":0}}
```

**Prompt 3: Viết bài (đầu vào bắt buộc là Output 1 và 2)**
```
Bạn là Copywriter PR kiêm chuyên gia SEO.
<OUTPUT_1>{JSON 1}</OUTPUT_1> <OUTPUT_2>{JSON 2}</OUTPUT_2>
Viết bài bám sát dàn ý theo thứ tự: Headline (H1) → Lead → H2/H3 → CTA.
Quy tắc: giữ tone {TONE} xuyên suốt; từ khóa chính ở Headline, Lead, 1 H2 và CTA; không bịa số liệu (ghi [CẦN BỔ SUNG NGUỒN]); mỗi đoạn tối đa 4 câu.
Sau mỗi H2 thêm <!--CHECKPOINT: H2-n done-->. Cuối bài ghi META (title ≤60, description ≤155 ký tự) và dòng <<<END_OF_ARTICLE>>>.
```

**Prompt tiếp tục (khi bị đứt do max token)**
```
a
```

Cách chạy: Prompt 1 → dán kết quả vào Prompt 2 → dán cả hai kết quả vào Prompt 3. Nếu bài thiếu dòng `<<<END_OF_ARTICLE>>>` thì dùng prompt tiếp tục.