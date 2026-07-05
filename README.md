# QH Plus BDD Copilot

Workspace AI Agent thường trực hỗ trợ **Giám đốc Phát triển Kinh doanh (BDD) của QH Plus Corporation** (kiêm Deputy Director General, HOMEMAS). Agent phục vụ 4 mảng — nghiên cứu thị trường, phân tích đối thủ, chiến lược kinh doanh, quản lý công việc & pipeline — đồng thời hỗ trợ tài liệu kỹ thuật (bản vẽ, BOQ, hồ sơ thầu) và kinh doanh (proposal, pitch deck, văn bản song ngữ Việt–Anh).

"Bộ não" của agent nằm ở `CLAUDE.md` (vai trò, nguyên tắc, bối cảnh QH Plus Group: 3 BU HMS–QHPS–QHPI, quy trình BDD 8 bước, định dạng đầu ra).

## Cấu trúc thư mục
- `knowledge/` — tài liệu tham chiếu công ty (infographic, catalog 3 BU, case study, profile). Agent đọc trước khi phân tích.
- `pipeline/` — theo dõi cơ hội (`pipeline.md`).
- `research/market/` · `research/competitors/` — kết quả nghiên cứu thị trường & đối thủ.
- `proposals/` — proposal & pitch deck đầu ra.
- `reports/` — báo cáo cho CEO/BOD.
- `templates/` — mẫu proposal, email, brief họp, cấu trúc BOQ.
- `.claude/commands/` — các lệnh tắt.

## Lệnh tắt (gõ `/tên-lệnh`)
| Lệnh | Chức năng |
|------|-----------|
| `/market` | Nghiên cứu thị trường: TAM/SAM/SOM, động lực cầu, phân khúc ưu tiên, rào cản → lưu `research/market/`. |
| `/competitor` | Hồ sơ & phân tích đối thủ theo từng BU: Porter, định vị, khác biệt hóa → lưu `research/competitors/`. |
| `/strategy` | Khung chiến lược: định vị, cross-sell, GTM, SWOT/TOWS, lộ trình 30/60/90 + KPI. |
| `/pipeline` | Rà soát pipeline: cơ hội đình trệ, SLA sắp trễ, 3 việc ưu tiên tuần này. |
| `/brief` | Brief 1 trang trước họp khách hàng: bối cảnh, mục tiêu, câu hỏi, phản biện, cross-sell. |
| `/report` | Báo cáo tiến độ cho CEO/BOD từ pipeline (song ngữ khi cần) → lưu `reports/`. |
| `/crosssell` | Kịch bản cross-sell HMS–QHPS–QHPI cho dự án/khách được nêu. |
| `/proposal` | Dàn ý/bản nháp proposal hoặc pitch deck → lưu `proposals/`. |
| `/tender` | Hỗ trợ kỹ thuật hồ sơ thầu: đọc bản vẽ/BOQ, tóm tắt phạm vi, rà soát khối lượng, nêu rủi ro. |
| `/bilingual` | Chuyển nội dung sang bản song ngữ Việt–Anh, thuật ngữ ngành chuẩn xác. |

## Bắt đầu
1. Thả tài liệu tham chiếu QH Plus vào `knowledge/` (2 infographic, catalog 3 BU, case study…).
2. Cập nhật cơ hội thực tế vào `pipeline/pipeline.md`.
3. Bật web search / MCP (gõ `/mcp`) để chạy nghiên cứu thị trường & đối thủ.
