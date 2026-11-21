---
name: vn-vat-tax-audit
description: >-
  Rà soát, phân loại thuế suất GTGT Việt Nam (8%, 10%, 5%, KCT, KKT) theo từng giai đoạn
  chính sách 2020-2026, đối chiếu đa luật chuyên ngành (Luật Thuế GTGT, Luật Viễn thông,
  Luật KDBĐS, Luật Thuế TTĐB, QĐ 43/2018) và công văn thuế, kèm quy trình xuất & kiểm tra
  file Excel bảng kê hóa đơn. Kích hoạt khi người dùng hỏi về thuế suất 8%/10%, kiểm tra
  hóa đơn đầu vào/đầu ra, hoặc cần căn cứ pháp lý thuế GTGT để làm việc với đối tác.
---

# Quy trình rà soát thuế suất GTGT (`vn-vat-tax-audit`)

Luôn thực hiện đầy đủ 4 bước sau khi rà soát thuế suất GTGT hoặc kiểm tra file hóa đơn:

## Bước 1: Xác định đúng mốc chính sách theo `Ngày HĐ`
Tra cứu chi tiết tại [vat-decrees-and-laws.md](./references/vat-decrees-and-laws.md):
1. **Trước `01/02/2022`** & **`01/01/2023 – 30/06/2023`**: Không áp dụng giảm 8% -> mức phổ thông là **10%** (chỉ tách riêng nhóm **5%**, **KCT**, **KKT**).
2. **`01/02/2022 – 31/12/2022`**: **NĐ 15/2022/NĐ-CP** (NQ 43/2022/QH15) — có Phụ lục I, II, III.
3. **`01/07/2023 – 31/12/2023`**: **NĐ 44/2023/NĐ-CP** (NQ 101/2023/QH15) — có Phụ lục I, II, III.
4. **`01/01/2024 – 30/06/2024`**: **NĐ 94/2023/NĐ-CP** (NQ 110/2023/QH15) — có Phụ lục I, II, III.
5. **`01/07/2024 – 31/12/2024`**: **NĐ 72/2024/NĐ-CP** (NQ 142/2024/QH15) — có Phụ lục I, II, III.
6. **`01/01/2025 – 30/06/2025`**: **NĐ 180/2024/NĐ-CP** (NQ 174/2024/QH15) — có Phụ lục I, II, III.
7. **`01/07/2025 – 31/12/2026`**: **NĐ 174/2025/NĐ-CP** (NQ 204/2025/QH15) — **bãi bỏ Phụ lục III (CNTT & điện tử)**, đưa xăng/dầu/khí đốt tinh chế/nhiều hóa chất ra khỏi Phụ lục I, **nhưng vẫn giữ Viễn thông, BĐS, Ngân hàng, Kim loại đúc sẵn, Khai khoáng (trừ than), Hàng/DV chịu TTĐB**.

## Bước 2: Phân loại theo thứ tự ưu tiên (tránh sai sót chéo ngành)
1. **Kiểm tra nhóm `5%`, `KCT`, `KKT` trước**: Không bao giờ xét giảm xuống 8% đối với hàng hóa/dịch vụ đang chịu **5%** (nước sạch, thuốc, thiết bị y tế), **KCT** (đào tạo theo Luật GD, tên miền `.vn` lệ phí NSNN, bảo hiểm nhân thọ/sức khỏe), hoặc **KKT** (nông sản chưa chế biến ở khâu TM giữa DN với DN).
2. **Kiểm tra Luật chuyên ngành & Phụ lục I, II, III**:
   - Không chỉ đọc Nghị định giảm thuế — phải đối chiếu **Luật Viễn thông 24/2023/QH15**, **Luật KDBĐS 29/2023/QH15**, **Luật Thuế TTĐB 27/2008/QH12**, **Luật Các TCTD 32/2024/QH15**, **Luật KDBH 08/2022/QH15**, **QĐ 43/2018/QĐ-TTg**.
   - Tra cứu các tình huống dễ nhầm lẫn tại [industry-rulings-and-edge-cases.md](./references/industry-rulings-and-edge-cases.md).
3. **Gắn cờ `Cần kiểm tra lại HĐ` với diễn giải mơ hồ**: Không đoán bừa đối với các dòng gộp (`Sao kê thẻ tín dụng`, `Tạm ứng`, `Giải chi`), `Tinh dầu` (mã HS hóa chất), `Spa` (làm đẹp 8% vs massage 10%), `Khóa học` (KCT vs 8%), `Khẩu trang + Gel rửa tay`, `Trái cây`, `Hoa tươi`.

## Bước 3: Quy chuẩn trích dẫn căn cứ pháp lý
Khi trả lời hoặc ghi cột căn cứ trong Excel, **luôn nêu đủ**:
- Số hiệu Nghị quyết/Nghị định + **Điều/Khoản/Phụ lục** tương ứng với ngày hóa đơn.
- Luật chuyên ngành / Thông tư / Quyết định / Công văn cơ quan thuế nếu là nhóm đặc thù (ví dụ: `Khoản 11 Điều 3 Luật Viễn thông 24/2023/QH15 & CV 67216/CTHN-TTHT` cho Cloud/O365 từ 01/07/2025).

## Bước 4: Kiểm tra chất lượng khi xuất Excel (`.xlsx`)
- Đảm bảo đủ cột: `Kỳ chính sách GTGT`, `Nhóm ngành hàng/Dịch vụ`, `Thuế suất đúng quy định`, `Kết quả đối chiếu`, `Chênh lệch tiền thuế`, `Căn cứ pháp lý chi tiết`.
- Sau khi tạo `.xlsx`, **bắt buộc chạy script kiểm tra toàn vẹn XML** (`xml.etree.ElementTree.fromstring`) trên mọi file `.xml` và `.rels` trong gói `.xlsx` trước khi trả link cho người dùng.
