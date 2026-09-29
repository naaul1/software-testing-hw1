**Khoa Công nghệ Thông tin (FIT) – Trường Đại học Khoa học Tự nhiên (HCMUS)**

**CS423 / CSC13003 – Kiểm chứng Phần mềm (AI-augmented · 2026\)**

**CHÍNH SÁCH AI · BIỂU MẪU — 2026 v1.0**

# **AI Audit Report — Mẫu 5 mục cho mỗi Artifact**

*Phụ lục bắt buộc đính kèm cho mọi bài tập có dùng AI (HW\#01–HW\#06, Seminar).*

*Tài liệu được biên soạn lại từ Med Kharbach, PhD (2026) — Mẫu Chính sách Sử dụng AI cho Giáo dục Đại học. Giấy phép CC BY-NC-SA 4.0. Phiên bản này được FIT@HCMUS điều chỉnh cho môn CS423 / CSC15003 Kiểm chứng Phần mềm.*

## **1\. Thông tin Sinh viên**

| Mục | Giá trị |
| :---- | :---- |
| **Họ tên sinh viên (in hoa):** | TRẦN ĐÌNH LUÂN |
| **MSSV:** |  23120059 |
| **Lớp / Khoá:** | 23CTT1\_3 |
| **Mã bài tập (ví dụ HW\#00, HW\#02):** | HW01 |
| **Ngày làm bài:** | 29/09/2026 |
| **Công cụ AI đã dùng:** | Opencode (Model MuseSpark 1.3 free), Claude Web (Model Sonnet 5.5) |
| **Công cụ AI đã dùng:** | \[ \] Có  \[ \] Không |

## **2\. Hướng dẫn (đọc trước khi điền)**

* Thêm 1 hàng cho mỗi artifact AI sinh (test case, script, checklist, OpenAPI spec, JMeter plan…).  
* Dán nguyên văn prompt — KHÔNG paraphrase.  
* Dán nguyên văn output AI (hoặc kèm screenshot có chú thích trong báo cáo).  
* Gắn nhãn: VALID / INVALID / INCOMPLETE.  
* Lý do phải dẫn chiếu slide, mục ISTQB, hoặc RFC kỹ thuật.  
* Hiển thị bản sửa với phần thay đổi được tô sáng.  
* Hàng mẫu in nghiêng — thay trước khi nộp.

## **3\. Bảng Audit — 1 hàng / artifact**

| (1) Prompt \+ Công cụ | (2) Output AI | (3) Verdict | (4) Lý do (ISTQB) | (5) Bản SV sửa |
| :---- | :---- | :---- | :---- | :---- |
| **Artifact #1 - Phân tích AI impact 10 tin (Req 1)**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 02:40:26 22/09/2026 (+07)Prompt (Prompt-log #2, nguyên văn):"read @report.md . for each entry in requirement1 of the file, write a short (1-2 sentences) AI impact analysis." | 10 dòng phân tích AI impact + nhận định chung 6/10 tin yêu cầu AI. Full text xem Prompt-log #2 (Phụ lục A). | INCOMPLETE | 2 tin JT1/VIECOI quá 60 ngày nên phải thay. Ngày đăng dạng "X ngày trước" chỉ là tương đối. ISTQB FL mục 5.2 yêu cầu kiểm chứng nguồn và tiêu chí lựa chọn trước khi dùng. | Thay #1-#2 bằng Zeya Labs AI và Simpson Strong-Tie (Prompt-log #15); giữ 6/10 tin AI; sửa bullet lương theo tin mới. |
| **Artifact #2 - Danh sách 20 lỗi 2022-2026 (Req 2)**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 02:57:51 22/09/2026 (+07)Prompt (Prompt-log #3, nguyên văn):"find 20 software defects publicized between 2022-2026. then, find 5 or more defects related to AI/LLM (hallucination, prompt injection, bias, etc). for each defects, include source link, description, severity, consequences and solution. have the infos above be writen in @report.md , be sure to not touch any other section other than requirement2." | 20 mục lỗi kèm link, severity, hậu quả, giải pháp; 6 lỗi AI/LLM. Full text xem Prompt-log #3. | INCOMPLETE | Gắn nhãn sai lỗi #20 Gemini là "thiên kiến" trong khi bản chất là overcorrect cân bằng đa dạng dẫn đến sinh sai sự thật. ISTQB FL mục 2.3 về phân loại lỗi và mục 5.1 về review độc lập. | Giữ 20 mục; sửa mục 1.2 trong report.md: đổi nhãn "bias" thành "hallucination do overcorrect"; giữ nguyên link gốc. |
| **Artifact #3 - Khung 15 test case ấm đun (Req 3)**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 19:29:37 22/09/2026 (+07)Prompt (Prompt-log #7, nguyên văn):"design me 15 test cases and then put it in the file named req3.md (not created yet)" | Khung 15 TC ấm đun trong req3.md (lúc đầu Actual/Verdict để trống). Chi tiết xem req3.md + Prompt-log #7. | INCOMPLETE | Thiếu edge case vật lý (đun khi mở nắp, đun lại ngay, nhấc ấm giữa chừng). TC14 giả định nhiều vạch chia, TC15 giả định lưới lọc trong khi ấm chỉ có vạch MAX và không có lưới. ISTQB FL mục 4.2 và 4.3 yêu cầu BVA và edge case theo đặc điểm thiết bị thật. | Sửa TC14 thành kiểm dung tích 1,7 lít tại vạch MAX duy nhất; sửa TC15 thành độ bền khớp nắp + lòng ấm (Prompt-log #8-#9); chốt 3 edge AI sót: TC05, TC06, TC13. |
| **Artifact #4 - Sửa TC14/TC15 theo cấu tạo thật**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 17:33:00 và 17:37:32 27/09/2026 (+07)Prompt (Prompt-log #8 + #9, nguyên văn):"redesign test case number 14 and 15, as my kettle does not have any water level mark beside max, and does not have a filter net" + "lid seal test case somewhat overlap test case number 9" | TC14 kiểm dung tích tại MAX bằng cốc đong; TC15 chỉ làm cơ khí (đóng/mở 10 lần, bản lề, lòng ấm), bỏ check rót nước. Xem req3.md hiện tại. | VALID | Bản sửa khớp cấu tạo thật của ấm (chỉ 1 vạch MAX, không lưới lọc) và hết trùng lặp với TC09. ISTQB FL mục 5.3 về thiết kế test không trùng lặp và thực thi được. | Dùng nguyên, không sửa thêm. |
| **Artifact #5 - Thay 2 tin quá hạn (Req 1)**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 04:02:37 28/09/2026 (+07)Prompt (Prompt-log #15, nguyên văn):"the 2 first entries in requirement1 section as dated more than 60 days from today, so i need to replace them, as well as the description of them in 1.2 Phan tich tac dong AI theo tung tin. after that, draw a QA/QC role mindmap in markdown format, right at the end of requiremnt1 section" | #1 Zeya Labs AI, #2 Simpson Strong-Tie, cả 2 đã kiểm live và yêu cầu AI. Xem report.md 1.1-1.2. | VALID | 2 tin mới trong cửa sổ 60 ngày, link sống, giữ 6/10 tin AI theo rubric. ISTQB FL mục 5.2 về tiêu chí chấp nhận và truy xuất nguồn. | Dùng nguyên; sinh viên tự chụp Q1-01/Q1-02 khi đăng nhập. |
| **Artifact #6 - Mindmap QA/QC + ISTQB (G9.1)**Tool: Claude Web - Sonnet 5.5Thời gian: 23:42:02 28/09/2026 (+07)Prompt (Prompt-log #16, nguyên văn):"doc requirement1, o phan ve so do mindmap, hay xem xet noi dung va ve lai so do the hien QA/QC role mindmap va ISTQB process, uu tien theo dang markdown nhung neu khong the the hien duoc thi co the dung anh hay svg cung duoc." | File images/mindmap.svg + mã Mermaid 9 nhánh. Full text xem Prompt-log #16. | INCOMPLETE | Mất gốc nối Performance và Kỹ năng chung; quy trình ISTQB chỉ còn 6 bước, gộp implementation + execution thành "thực hiện", thiếu monitoring and control; node Kỹ năng chung lặp lại ISTQB. ISTQB FL mục 5.1 quy trình 7 bước. | Giữ hình AI vẽ; thêm report.md 1.3 liệt kê 3 lỗi trên. |
| **Artifact #7 - AI điền Actual/Verdict 15 TC (Req 3)**Tool: OpenCode - Muse Spark 1.3 FreeThời gian: 28/09/2026 (Prompt-log #12, Plan mode, không ghi giờ) và 03:52:48 28/09/2026 (+07) (Prompt-log #13)Prompt (Prompt-log #12 + #13, nguyên văn):"prepare to fill in requirement 3 of @report.md , using content from @req3.md . knowing the device used is happy cook 1.7 litre HEK-17WF, sold in 2020. every function working as expected except turn the kettle on without water as it is too dangerous." + "confirm, carry out" | AI điền Actual/Verdict 15 TC vào req3.md và report.md theo lời kể của sinh viên (14 Pass, TC03 Blocked). Sinh viên phải kiểm chứng bằng chạy thật + video. | INCOMPLETE | Actual/Verdict phải đến từ chạy thật trên thiết bị, AI không được bịa kết quả. ISTQB FL mục 5.3 về thực thi test và ghi nhận bằng chứng độc lập; requirements.md cấm bịa ảnh/video. | Giữ khung bảng; sinh viên tự chạy lại, tự quay 5 video có giọng thuyết minh, tự chịu trách nhiệm số liệu Actual. |

## **4\. Tổng kết Độ chính xác AI**

Tổng hợp verdict từ Mục 3 và điền vào bảng dưới.

| Chỉ số | Số lượng | Tỉ lệ |
| :---- | :---- | :---- |
| **Tổng artifact AI sinh đã audit** | 7 | 100% |
| **VALID (đúng, dùng nguyên)** | 2 | 29% |
| **INVALID (sai; loại bỏ)** | 0 | 0% |
| **INCOMPLETE (chấp nhận sau khi sửa)** | 5 | 71% |

## **5\. Kết luận — Khi nào nên / không nên dùng AI?**

Viết 80–150 chữ mô tả pattern quan sát được. AI mạnh ở đâu? AI sai ở đâu? Khuyến nghị của bạn cho việc dùng AI trong loại công việc này?

Qua audit, AI mạnh ở chỗ thu thập và tổng hợp thông tin nhanh, tra cứu thông tin được từ nhiều nguồn và làm đúng công việc nếu yêu cầu kỹ. AI yếu ở việc kiểm chứng thông tin thực tế (vd. gắn sai nhãn cho nguyên nhân lỗi phần mềm, bỏ sót edge case, vẽ mindmap thiếu liên kết, tìm hiểu sai 7 bước ISTQB). Khuyến nghị cho việc dụng Ai vào công việc này là chỉ nên dùng để tra cứu thông tin, để soạn thảo và gợi ý cấu trúc, không dùng làm bằng chứng. Mọi output của Ai đều phải đối chiếu lại thủ công.

## **6\. Mandatory Disclosure (dán nguyên văn)**

"Các test case, danh sách tin tuyển dụng, danh sách lỗi và mindmap trong HW01 này được sinh bản đầu bởi OpenCode (Muse Spark 1.3 Free) và Claude Web (Sonnet 5.5); tôi đã rà soát và chỉnh sửa mục 1.1-1.3 Yêu cầu 1 (thay 2 tin quá hạn, sửa phân tích AI impact), toàn bộ 20 mục Yêu cầu 2 (sửa nhãn lỗi #20 Gemini), khung 15 test case và mindmap ở Yêu cầu 1 + 3, bổ sung 3 edge case TC05, TC06, TC13; ảnh chụp tin có tên tài khoản, ảnh thiết bị kèm thẻ sinh viên, 5 video chạy test có giọng thuyết minh và xác nhận lương sau đăng nhập do tôi tự viết. AI Audit Report chi tiết đính kèm ở Phụ lục A. Tôi cam đoan không dùng AI để sinh bất kỳ artifact nào thuộc danh mục bị cấm.”

## **Chữ ký**

| Họ tên sinh viên (in hoa): | TRẦN ĐÌNH LUÂN |
| :---- | :---- |
| **MSSV:** | 23120059 |
| **Lớp / Khoá:** | 23CTT1\_3 |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Giảng viên:** | Lâm Quang Vũ |
| **Ngày:** | 29/09/2026 |
| **Chữ ký:** | Luân - Trần Đình Luân |

## **Tham khảo**

* Kharbach, M. (2026). AI Use Policy Templates for Higher Education. CC BY-NC-SA 4.0.  
* ISTQB Foundation Level Syllabus (latest version).  
* Hardman, P. (2025). A Post-AI Learning Taxonomy.  
* Fuster Rabella, M. (2025). OECD Education Working Paper No. 338\.  
* Perkins, M., Roe, J., & Furze, L. (2025). AI Assessment Scale.  
* Anthropic (2025). Building reliable AI test agents — engineering blog.  
* DeepEval & Promptfoo documentation — testing frameworks for LLM systems.
