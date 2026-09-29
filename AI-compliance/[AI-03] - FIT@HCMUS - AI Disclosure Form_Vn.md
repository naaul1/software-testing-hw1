**Khoa Công nghệ Thông tin (FIT) – Trường Đại học Khoa học Tự nhiên (HCMUS)**

**CS423 / CSC15003 – Kiểm chứng Phần mềm (AI-augmented · 2026\)**

**CHÍNH SÁCH AI · BIỂU MẪU — 2026 v1.0**

# **Biểu mẫu Khai báo Sử dụng AI**

*Đính kèm cho mọi bài tập có dùng AI ở bất kỳ mức nào.*

*Tài liệu được biên soạn lại từ Med Kharbach, PhD (2026) — Mẫu Chính sách Sử dụng AI cho Giáo dục Đại học. Giấy phép CC BY-NC-SA 4.0. Phiên bản này được FIT@HCMUS điều chỉnh cho môn CS423 / CSC15003 Kiểm chứng Phần mềm.*

## **1\. Thông tin Môn học & Sinh viên**

| Mục | Giá trị |
| :---- | :---- |
| **Môn học:** | CS423 / CSC13003 – Kiểm chứng Phần mềm |
| **Mã bài tập:** | HW01 |
| **Tên bài tập:** | HW01 - QA/QC Jobs, 20 Defects, Test a Physical Product |
| **Cấp độ AI (1-5):** | Cấp 3 (AI hỗ trợ soạn bản đầu, sinh viên kiểm chứng và quyết định toàn bộ; Bloom-AI G9.1 + G9.3) |
| **Ngày:** | 29/09/2026 |
| **Họ tên sinh viên:** | Trần Đình Luân |
| **MSSV:** | 23120059 |

## **2\. Câu hỏi Khai báo**

### **1\. Công cụ AI đã dùng:**

*Liệt kê mọi công cụ AI dùng cho bài tập này (ví dụ AI Tool (e.g., ChatGPT, Claude, Gemini), ChatGPT, GitHub Copilot, Cursor, Gemini).*

- OpenCode (AI coding agent; model Muse Spark 1.3 Free): nghiên cứu tin tuyển dụng, soạn phân tích AI impact, tìm 20 lỗi, sinh khung 15 test case, thay 2 tin quá hạn.
- Claude Web (model Sonnet 5.5): vẽ mindmap QA/QC + ISTQB (file images/mindmap.svg + mã Mermaid).


### **2\. Giai đoạn nào của bài tập có dùng AI:**

*Tick tất cả: \[ \] brainstorm  \[ \] outline  \[ \] viết nháp  \[ \] phản hồi  \[ \] sửa chữa  \[ \] code  \[ \] phân tích dữ liệu  \[ \] thiết kế đồ hoạ  \[ \] khác (ghi rõ).*

[x] brainstorm [x] outline [x] viết nháp [ ] phản hồi [x] sửa chữa [ ] code [x] phân tích dữ liệu [x] thiết kế đồ hoạ [ ] khác.



### **3\. Prompt / nhiệm vụ chính cho AI:**

*Dán nguyên văn 2–3 prompt quan trọng nhất. Để xem đầy đủ, đính kèm Phụ lục A (prompt\_log.md).*

Prompt 1 (Prompt-log #3, Req 2 - tìm 20 lỗi):
```
find 20 software defects publicized between 2022-2026. then, find 5 or more defects related to AI/LLM (hallucination, prompt injection, bias, etc). for each defects, include source link, description, severity, consequences and solution. have the infos above be writen in @report.md , be sure to not touch any other section other than requirement2.
```
Prompt 2 (Prompt-log #7, Req 3 - sinh 15 test case):
```
design me 15 test cases and then put it in the file named req3.md (not created yet)
```
Prompt 3 (Prompt-log #16, Req 1 - vẽ mindmap):
```
đọc requirement1, ở phần vẽ sơ đồ mindmap, hãy xem xét nội dung và vẽ lại sơ đồ thể hiện QA/QC role mindmap và ISTQB process, ưu tiên theo dạng markdown nhưng nếu không thể thể hiện được thì có thể dùng ảnh hay svg cũng được.
```
Đầy đủ xem Phụ lục A (prompt-log.md).


### **4\. Phần cụ thể AI đóng góp:**

*Càng cụ thể càng tốt. Ví dụ: 'AI sinh TC01–TC15 ở Mục 3.2; tôi viết lại TC04 và TC11; AI KHÔNG đóng góp vào Mục 1, 2, 4, hoặc AI Critique.'*

AI sinh bản đầu: 10 dòng phân tích AI impact (Req 1); danh sách 20 lỗi kèm link/severity/hậu quả/giải pháp (Req 2); khung 15 test case ấm đun (Req 3); mindmap QA/QC + ISTQB (images/mindmap.svg).
Tôi sửa: thay 2 tin JT1/VIECOI quá 60 ngày bằng Zeya Labs AI và Simpson Strong-Tie; sửa nhãn lỗi #20 Gemini từ bias thành hallucination do overcorrect; sửa TC14/TC15 theo cấu tạo thật của ấm; liệt kê 3 lỗi mindmap ở report.md 1.3; bổ sung 3 edge case AI sót là TC05, TC06, TC13.
AI KHÔNG đóng góp: ảnh chụp 10 tin có tên tài khoản, ảnh ấm + thẻ sinh viên, 5 video chạy test có giọng thuyết minh, xác nhận lương sau đăng nhập.


### **5\. Cách tôi rà soát / chỉnh sửa / xác minh đầu ra AI:**

*Mô tả phương pháp xác minh (chạy test, kiểm tra spec, hỏi TA, tra RFC, đối chiếu ISTQB syllabus, v.v.).*

Mở lại từng link tin tuyển dụng và link nguồn lỗi để kiểm còn sống; đối chiếu ngày đăng với cửa sổ 60 ngày và giai đoạn 2022-2026.
Đối chiếu output AI với ISTQB FL syllabus (mục 2.3, 4.2, 4.3, 5.1-5.3): bắt lỗi gắn nhãn sai, thiếu edge case, mindmap sai 7 bước quy trình.
Kiểm cấu tạo thật của ấm (chỉ 1 vạch MAX, không lưới lọc) rồi sửa TC14/TC15; chạy lại các TC trên thiết bị thật và quay video thuyết minh để xác minh cột Actual.


### **6\. Trích dẫn (nếu môn yêu cầu):**

*Môn Kiểm chứng Phần mềm dùng phong cách IEEE. Ví dụ: Anthropic. (2026). AI Tool (e.g., ChatGPT, Claude, Gemini) \[Large language model\]. https://claude.ai*

Anthropic. (2025). Claude Sonnet 5.5 [Large language model]. https://claude.ai
SST. (2026). OpenCode [AI coding agent; model Muse Spark 1.3 Free]. https://opencode.ai
Cert Sensei (2026).The ISTQB Fundamental Test Process Explained. https://certsensei.io/blog/istqb-ctfl/istqb-ctfl-v4-test-process


## **3\. Cam đoan Trung thực**

*Bằng việc ký tên dưới đây, tôi cam đoan thông tin khai báo ở trên là chính xác và đầy đủ. Tôi hiểu rằng việc không khai báo hoặc khai báo sai lệch về việc dùng AI sẽ bị coi là vi phạm liêm chính học thuật và có thể dẫn đến điểm 0 cho bài tập cùng việc bị chuyển lên hội đồng kỷ luật.*

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
