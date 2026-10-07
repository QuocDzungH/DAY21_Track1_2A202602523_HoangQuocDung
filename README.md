# Lab 21 — Phân tích rủi ro AI qua case study thực tế

- Họ và tên: Hoàng Quốc Dũng
- MSSV / mã học viên: 2A202602523
- Lớp: AI Thực Chiến — Khóa 4, Level 3, lớp 3B
- Ngành đã chọn: **Giáo dục / AI tutor**
- Phạm vi: AI trong giáo dục, gồm hỗ trợ học toán, hỗ trợ viết bài học thuật và kiểm tra liêm chính học thuật bằng công cụ phát hiện văn bản AI.



### 1. Industry Risk Snapshot

| Nội dung | Đánh giá của tôi và lý do |
| --- | --- |
| Những tác hại chính có thể xảy ra | Người học có thể tiếp nhận kiến thức sai, dùng nguồn không tồn tại hoặc phụ thuộc vào lời giải AI mà thiếu khả năng tự làm. Nếu dùng AI để đánh giá, học sinh còn có nguy cơ bị chấm sai và mất cơ hội. Giảng viên có thể mất thời gian sửa lỗi, kiểm tra nguồn và đánh giá lại năng lực. Đây là nhận định về ngành; ba case bên dưới cung cấp bằng chứng cho một phần các rủi ro này. |
| Mức độ high-stakes | **Trung bình** trong phạm vi hỗ trợ học và viết bài: lỗi có thể sửa trước khi nộp, nhưng có thể ảnh hưởng kiến thức và kết quả học tập. **Cao** nếu đầu ra được dùng trực tiếp cho thi cử, tốt nghiệp, tuyển sinh, quyết định học bổng hoặc xử lý kỷ luật học thuật. Không xem mọi tương tác với AI tutor là high-stakes. |
| Dữ liệu nhạy cảm có thể được sử dụng | Thông tin định danh, mã học sinh, điểm, lịch sử học tập, hội thoại, thông tin về hoàn cảnh gia đình hoặc nhu cầu hỗ trợ đặc biệt. Đây là các loại dữ liệu có thể xuất hiện khi triển khai, không phải khẳng định các nghiên cứu bên dưới đã sử dụng tất cả các loại này. |
| Nhu cầu human review | **Cao** với kiến thức nền tảng, nguồn học thuật và quyết định đánh giá. Giảng viên kiểm tra nội dung trước khi dùng; người học đối chiếu nguồn trước khi nộp bài; giáo viên kiểm tra khả năng tự giải sau khi học với AI. Có thể kiểm tra theo mẫu với bài luyện tập ít rủi ro, nhưng quyết định ảnh hưởng cơ hội học tập cần người có thẩm quyền xem xét. |

### 2. Case study 1 — GPT Base và sự phụ thuộc vào AI khi học toán

#### Brief Case

- **Tổ chức / sản phẩm AI:** Nhóm Hamsa Bastani và cộng sự; hai trợ lý dựa trên GPT-4: GPT Base và GPT Tutor.
- **Thời gian, địa điểm / bối cảnh:** Một trường trung học tại Thổ Nhĩ Kỳ, học kỳ mùa thu năm học 2023–2024; công bố ngày 25/06/2025.
- **AI được dùng để làm gì:** Hỗ trợ luyện toán. GPT Base mô phỏng giao diện ChatGPT thông thường; GPT Tutor dùng hướng dẫn bảo vệ việc học.
- **Vấn đề hoặc sự kiện đáng chú ý:** Nhóm GPT Base làm tốt hơn khi có AI nhưng đạt kết quả thấp hơn nhóm không được cấp AI khi thi không có công cụ. GPT Tutor giảm đáng kể tác động tiêu cực này.
- **Số liệu có nguồn:** Thí nghiệm với gần 1.000 học sinh. Khi có AI, kết quả nhóm GPT Base tăng **48%**, GPT Tutor tăng **127%**; khi bỏ AI, kết quả thi nhóm GPT Base thấp hơn nhóm đối chứng **17%**. Đây là thay đổi tương đối của kết quả, không phải điểm phần trăm hay tỷ lệ học sinh bị hại.
- **Nguồn:** Hamsa Bastani, Osbert Bastani, Alp Sungu, Haosen Ge, Özge Kabakcı và Rei Mariman — *Generative AI without guardrails can harm learning: Evidence from high school mathematics* — PNAS 122(26), e2422633122, 25/06/2025; mục Abstract, mô tả thí nghiệm và Fig. 1. [DOI](https://doi.org/10.1073/pnas.2422633122) · [Abstract và hình trên PubMed](https://pubmed.ncbi.nlm.nih.gov/40560616/) · [Toàn văn trên PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC12232635/).
- **Phân biệt bằng chứng và nhận định:** Nguồn xác nhận chênh lệch kết quả trong thí nghiệm. Tôi suy luận rằng giảm khả năng tự làm có thể ảnh hưởng cơ hội học tập; nguồn không chứng minh học sinh đã mất học bổng, trượt tốt nghiệp hoặc bị suy giảm năng lực lâu dài. Không khái quát kết quả sang mọi AI tutor.

#### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Trong lúc luyện toán, học sinh dùng lời giải AI để hoàn thành bài nhưng chưa tự thực hiện được các bước suy luận; sau đó phải thi không có AI. Điểm rủi ro là lời giải sẵn có thay thế hoạt động luyện kỹ năng. |
| Stakeholder bị ảnh hưởng | Học sinh là bên trực tiếp; giáo viên cần đánh giá đúng năng lực; nhà trường và phụ huynh có thể dựa vào kết quả luyện tập để nhận định tiến bộ. |
| Failure mode | **Over-reliance:** dựa vào công cụ để làm bài, nhưng khả năng tự làm không theo kịp kết quả khi có hỗ trợ. Không cần AI trả lời sai thì tình huống này mới gây hại. |
| Layer bắt đầu lỗi | **Grounding — hướng dẫn hệ thống**, là lớp tôi chọn phân tích: hướng dẫn cần ưu tiên gợi mở và yêu cầu học sinh suy luận. Nghiên cứu công bố sự khác biệt về prompts giữa hai trợ lý. Đây là điểm can thiệp được nguồn mô tả, không chứng minh prompt là nguyên nhân duy nhất; các khác biệt trong thiết kế có thể cùng tác động. |
| Harm xảy ra là gì? | **Đã ghi nhận:** học sinh trong nhóm GPT Base có kết quả thi tự làm thấp hơn nhóm đối chứng. **Nguy cơ:** người học mất cơ hội đạt kết quả tốt khi tiếp tục dùng AI thay cho luyện tập; giáo viên đánh giá quá cao năng lực nếu chỉ nhìn bài có AI hỗ trợ. |
| Harm lens | **Opportunity loss:** suy giảm kết quả tự làm có thể gây bất lợi trong học tập. Nghiên cứu chưa xác nhận việc mất cơ hội cụ thể như học bổng hoặc tuyển sinh. |
| Severity | **Medium — nhận định của tôi.** Kết quả học tập bị ảnh hưởng, nhưng nguồn chưa xác nhận hậu quả không thể khắc phục hoặc kéo dài. Không đủ căn cứ chọn Critical. |
| Scale | Phạm vi bằng chứng là một trường và mẫu thí nghiệm gần 1.000 học sinh. Đây là quy mô nghiên cứu, **không phải số học sinh được xác nhận bị hại**; chưa đủ dữ liệu về quy mô tác động ngoài mẫu. |
| Probability | **Chưa đủ dữ liệu để đánh giá xác suất một học sinh bị hại.** Mức giảm kết quả của nhóm không cung cấp tỷ lệ cá nhân gặp hậu quả. Tôi không chuyển mức giảm 17% thành xác suất. |
| Frequency | **Chưa đủ dữ liệu về tần suất tác hại ngoài thí nghiệm.** Không thể từ chênh lệch kết quả kết luận hậu quả xảy ra mỗi lần dùng AI hoặc mỗi tuần. |
| Vì sao? | Tôi chọn Over-reliance vì vấn đề nằm ở khoảng cách giữa hoàn thành bài có hỗ trợ và tự làm. Severity dựa trên hậu quả học tập đo được; Scale giới hạn theo mẫu. Probability và Frequency để chưa đủ dữ liệu vì nguồn không cung cấp tỷ lệ cá nhân hay số lần tác hại theo thời gian. Kết quả của GPT Tutor cũng cho thấy cần xem xét thiết kế hỗ trợ học, thay vì kết luận AI luôn làm giảm việc học. |

### 3. Case study 2 — ChatGPT tạo tài liệu tham khảo không tồn tại trong bài học thuật

#### Brief Case

- **Tổ chức / sản phẩm AI:** William H. Walters và Esther Isabelle Wilder; đánh giá ChatGPT GPT-3.5/GPT-4 của OpenAI.
- **Thời gian, địa điểm / bối cảnh:** Sinh văn bản trong tuần đầu tháng 04/2023; công bố ngày 07/09/2023. Bài mô phỏng dạng tổng quan tài liệu thường giao cho sinh viên năm nhất tại Mỹ; không phải sự cố trong một lớp cụ thể.
- **AI được dùng để làm gì:** Viết bài học thuật kèm thư mục tài liệu tham khảo.
- **Vấn đề hoặc sự kiện đáng chú ý:** ChatGPT tạo nguồn không tồn tại và thông tin thư mục sai; nguồn có hình thức học thuật chưa chắc là nguồn thật.
- **Số liệu có nguồn:** **84 bài / 42 chủ đề / 636 tài liệu tham khảo**. Trong **222** mục của GPT-3.5, **55%** là nguồn giả; trong **414** mục của GPT-4, **18%** là nguồn giả. Trong phần nguồn thật, tỷ lệ có lỗi thư mục đáng kể lần lượt là **43% và 24%**. Hai loại tỷ lệ có mẫu số khác nhau, không cộng trực tiếp.
- **Nguồn:** William H. Walters và Esther Isabelle Wilder — *Fabrication and errors in the bibliographic citations generated by ChatGPT* — Scientific Reports 13, 14045, 07/09/2023; Methods, trang 2–3; Tables 3–4, trang 4. [Bài gốc](https://www.nature.com/articles/s41598-023-41032-5) · [PDF](https://www.nature.com/articles/s41598-023-41032-5.pdf) · [PubMed](https://pubmed.ncbi.nlm.nih.gov/37679503/).
- **Phân biệt bằng chứng và nhận định:** Nguồn xác nhận lỗi đầu ra trong thử nghiệm năm 2023. Thiệt hại về điểm, danh dự hoặc thời gian của sinh viên là nguy cơ tôi phân tích, chưa được nghiên cứu đo; các tỷ lệ không đại diện ChatGPT hiện nay.

#### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Người học đưa tài liệu tham khảo do ChatGPT sinh vào bài nộp và dùng tài liệu đó làm bằng chứng, trước khi kiểm tra sự tồn tại và nội dung nguồn. |
| Stakeholder bị ảnh hưởng | Sinh viên viết bài; giảng viên chấm bài; người đọc tiếp nhận kết luận; thủ thư hoặc người hỗ trợ tìm tài liệu. Các bên ngoài nhóm nghiên cứu là stakeholder của tình huống tôi phân tích, không phải người đã được xác nhận chịu thiệt hại. |
| Failure mode | **Hallucination** là lỗi chính: sinh tài liệu không tồn tại. **Over-reliance** là nguy cơ bổ sung nếu người học tin và sử dụng thư mục mà không đối chiếu. Lỗi đầu ra đã được kiểm chứng; sự phụ thuộc của sinh viên chưa được đo trong nghiên cứu này. |
| Layer bắt đầu lỗi | **Chưa đủ bằng chứng để xác định lớp khởi phát.** Nghiên cứu đo đầu ra, không đủ để quy lỗi riêng cho UX, Grounding, Safety hay Model. Giả thuyết của tôi: cần kiểm tra lớp Grounding xem thông tin thư mục có được đối chiếu với nguồn xác thực không; không khẳng định hệ thống thử nghiệm có hoặc thiếu RAG. |
| Harm xảy ra là gì? | **Đã ghi nhận:** các bài thử nghiệm chứa nguồn giả và lỗi thư mục. **Nguy cơ:** sinh viên dùng bằng chứng không có thật, mất thời gian tìm nguồn và bị đánh giá bất lợi khi nộp bài; giảng viên và người đọc bị dẫn tới kết luận thiếu căn cứ. Nguồn không xác nhận sinh viên cụ thể bị kỷ luật. |
| Harm lens | **Misinformation** là lens chính. **Opportunity loss** là nguy cơ thứ cấp nếu bài nộp chứa nguồn giả bị đánh giá thấp; chưa có số liệu đo hậu quả này. |
| Severity | **Medium — nhận định của tôi** trong tình huống bài học thuật thông thường. Nguồn giả làm giảm giá trị bằng chứng và có thể ảnh hưởng kết quả học tập, nhưng có thể phát hiện, thay thế trước khi nộp. |
| Scale | Quy mô kiểm chứng là tập bài và thư mục thử nghiệm đã nêu ở Brief Case, không phải số sinh viên bị hại. **Chưa đủ dữ liệu** về số bài nộp thực tế hoặc số người bị ảnh hưởng. |
| Probability | Tỷ lệ nguồn giả đã nêu là **tỷ lệ lỗi quan sát trên mục thư mục trong mẫu**. Đó không phải xác suất một sinh viên bị hại hoặc xác suất một bài có nguồn giả. Chưa đủ dữ liệu về xác suất hậu quả sau khi sử dụng và kiểm tra nguồn. |
| Frequency | Lỗi xuất hiện lặp lại trong tập đầu ra thử nghiệm; không phải chỉ một mục sai đơn lẻ. **Chưa đủ dữ liệu về tần suất theo ngày/tháng** hoặc khi sử dụng trong lớp học thực tế. |
| Vì sao? | Hallucination phù hợp vì lỗi là sự tồn tại của tài liệu, không chỉ định dạng trích dẫn. Tôi chọn Medium theo hậu quả của tình huống học tập giả định và khả năng sửa trước khi nộp. Không suy từ tỷ lệ nguồn giả sang tỷ lệ người chịu thiệt hại. Không xác định layer khi chưa có bằng chứng kiến trúc; không dùng kết quả các phiên bản cũ để đánh giá phiên bản hiện tại. |


### 4. Case study 3 — AI detector gắn nhãn sai bài viết của người không dùng tiếng Anh như tiếng mẹ đẻ

#### Brief Case

- **Tổ chức / sản phẩm AI:** Nhóm nghiên cứu Stanford gồm Weixin Liang, Mert Yuksekgonul, Yining Mao, Eric Wu và James Zou; đánh giá 7 công cụ phát hiện văn bản AI, trong đó có GPTZero, ZeroGPT và Originality.AI.
- **Thời gian, địa điểm / bối cảnh:** Nghiên cứu năm 2023; bài chính thức công bố trực tuyến ngày 10/07/2023 trên Patterns. Đánh giá bài viết tiếng Anh từ các bộ dữ liệu, không phải theo dõi việc xử lý gian lận tại một trường cụ thể.
- **AI được dùng để làm gì:** Phân loại văn bản do con người viết hoặc do AI tạo, có thể hỗ trợ kiểm tra liêm chính học thuật.
- **Vấn đề hoặc sự kiện đáng chú ý:** Các công cụ thường gắn nhãn sai bài viết của người không dùng tiếng Anh như tiếng mẹ đẻ thành văn bản do AI tạo.
- **Số liệu có nguồn:** Thử nghiệm 7 detector trên **91 bài TOEFL do người viết** và **88 bài của học sinh lớp 8 tại Mỹ**. Tỷ lệ dương tính giả trung bình trên tập TOEFL là **61,3%** theo bài Patterns. Đây là tỷ lệ bài người viết bị nhận nhầm thành AI trong mẫu thử nghiệm, không phải tỷ lệ sinh viên bị phạt oan.
- **Nguồn:** Weixin Liang và cộng sự — *GPT detectors are biased against non-native English writers* — Patterns, 4(7), 100779, công bố trực tuyến 10/07/2023; mục “GPT detectors exhibit bias against non-native English authors” và Figure 1. [DOI](https://doi.org/10.1016/j.patter.2023.100779) · [Toàn văn mở](https://pmc.ncbi.nlm.nih.gov/articles/PMC10382961/) · [Bản nghiên cứu có phương pháp và danh sách detector](https://arxiv.org/html/2304.02819v3).
- **Phân biệt bằng chứng và nhận định:** Nguồn xác nhận lỗi phân loại trong thử nghiệm. Tôi suy luận rằng sử dụng nhãn này để kết luận gian lận có thể gây bất lợi cho người học. Nghiên cứu không xác nhận số sinh viên thực tế bị trừ điểm, đình chỉ hoặc mất học bổng; kết quả năm 2023 không đại diện cho mọi detector hiện nay.

#### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Giảng viên nhận kết quả “AI-generated” và dùng kết quả đó để kết luận sinh viên gian lận hoặc áp dụng hình phạt, trước khi kiểm tra quá trình làm bài và cho sinh viên giải trình. Đây là tình huống rủi ro tôi lựa chọn phân tích. |
| Stakeholder bị ảnh hưởng | Người học không dùng tiếng Anh như tiếng mẹ đẻ; giảng viên đánh giá bài; bộ phận xử lý liêm chính học thuật; nhà trường chịu trách nhiệm bảo đảm đánh giá công bằng. |
| Failure mode | **Bias / fairness:** công cụ có mức nhận nhầm cao đối với nhóm bài TOEFL trong mẫu. **Over-reliance** là nguy cơ bổ sung nếu người đánh giá coi kết quả detector là bằng chứng quyết định, không kiểm tra thêm. |
| Layer bắt đầu lỗi | **Chưa đủ bằng chứng để xác định lớp khởi phát của từng sản phẩm.** Tôi đặt giả thuyết ở **Model**, vì cần kiểm tra khả năng phân loại giữa các nhóm văn bản. Không khẳng định dữ liệu huấn luyện hay kiến trúc cụ thể khi chưa được công bố. Nếu nhà trường tự động xử phạt theo nhãn, quy trình human review cũng là điểm cần kiểm tra; nghiên cứu không xác nhận quy trình đó đã xảy ra. |
| Harm xảy ra là gì? | **Đã ghi nhận:** bài viết do người tạo bị gắn nhãn sai là AI. **Nguy cơ:** người học bị nghi ngờ gian lận, phải mất thời gian chứng minh quá trình làm bài, bị trừ điểm hoặc chịu xử lý bất lợi nếu kết quả detector được dùng thiếu kiểm chứng. Chưa có số liệu xác nhận các hậu quả này trong nghiên cứu. |
| Harm lens | **Dignity loss:** nguy cơ tổn hại danh dự khi bị quy kết thiếu trung thực. **Opportunity loss:** nguy cơ mất điểm hoặc cơ hội học tập nếu bị xử lý oan. Hai hậu quả này là phân tích của tôi, không phải kết quả đã được đo. |
| Severity | **High — đánh giá của tôi trong tình huống dùng detector để quyết định xử phạt.** Hậu quả có thể ảnh hưởng điểm, hồ sơ và danh dự. Nếu nhãn chỉ dùng để yêu cầu kiểm tra thêm, mức nghiêm trọng sẽ thấp hơn. |
| Scale | Bằng chứng giới hạn trong các tập bài và 7 công cụ được thử nghiệm. **Chưa đủ dữ liệu về số người thực tế bị hại.** Không coi số bài trong mẫu là số sinh viên đã bị xử phạt. |
| Probability | Tỷ lệ dương tính giả ở Brief Case cho thấy lỗi phân loại đáng kể trong mẫu. **Chưa đủ dữ liệu về xác suất bị phạt oan**, vì hậu quả còn phụ thuộc chính sách, human review và khả năng giải trình. Không sử dụng tỷ lệ lỗi này như xác suất áp dụng cho mọi sinh viên. |
| Frequency | Lỗi lặp lại trên tập bài thử nghiệm, không chỉ là một đầu ra sai đơn lẻ. **Chưa đủ dữ liệu về tần suất theo ngày, tháng hoặc học kỳ** khi triển khai tại trường. |
| Vì sao? | Tôi chọn Bias / fairness vì kết quả cho thấy chênh lệch đáng lo ngại giữa các nhóm văn bản. Tuy nhiên, các tập bài còn khác nhau về bối cảnh và dạng bài, nên không quy mọi chênh lệch duy nhất cho tiếng mẹ đẻ. Severity đánh giá hậu quả của tình huống xử phạt giả định; Scale, Probability và Frequency giữ đúng giới hạn bằng chứng. Biện pháp tôi đề xuất là dùng detector như tín hiệu để kiểm tra thêm, kết hợp bản nháp, lịch sử chỉnh sửa và giải trình; quyết định xử lý cần người có thẩm quyền xem xét. |
