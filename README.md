# `vn-vat-tax-audit` — Bộ kiến thức & Skill rà soát thuế suất GTGT Việt Nam (2020–2026)

Kho lưu trữ chuẩn hóa kiến thức kiểm tra thuế suất GTGT (`8%`, `10%`, `5%`, `KCT`, `KKT`), đối chiếu đa luật chuyên ngành và công văn hướng dẫn của cơ quan thuế, đóng gói theo chuẩn **Antigravity Skill**.

## Cấu trúc thư mục

```text
.
├── README.md
└── skills/
    └── vn-vat-tax-audit/
        ├── SKILL.md
        └── references/
            ├── vat-decrees-and-laws.md
            └── industry-rulings-and-edge-cases.md
```

## Nội dung cốt lõi
1. **8 mốc thời gian chính sách giảm thuế GTGT (2020–2026)**:
   - `Trước 01/02/2022` & `01/01–30/06/2023`: Không giảm (10%).
   - `NĐ 15/2022/NĐ-CP`, `NĐ 44/2023/NĐ-CP`, `NĐ 94/2023/NĐ-CP`, `NĐ 72/2024/NĐ-CP`, `NĐ 180/2024/NĐ-CP`.
   - `NĐ 174/2025/NĐ-CP` (hiệu lực `01/07/2025 – 31/12/2026`): Bãi bỏ Phụ lục III (CNTT & điện tử), mở rộng giảm 8% cho xăng/dầu/khí đốt/than/nhiều hóa chất; giữ nguyên loại trừ 10% với Viễn thông, BĐS, Tài chính ngân hàng, Kim loại đúc sẵn, Khai khoáng (trừ than), Hàng/DV chịu TTĐB.
2. **Đối chiếu đa luật chuyên ngành & Công văn thuế**:
   - **Luật Thuế GTGT 48/2024/QH15** & **Thông tư 219/2013/TT-BTC** (nhóm 5%, KCT, KKT).
   - **Luật Viễn thông 24/2023/QH15** (Khoản 11 Điều 3) & **Công văn 67216/CTHN-TTHT**: Cloud, VPS, Data Center, Office365 thuê bao vẫn là dịch vụ viễn thông (Phụ lục I -> **10%**) từ `01/07/2025`.
   - **Luật KDBĐS 29/2023/QH15**, **Luật Thuế TTĐB 27/2008/QH12**, **Luật Các TCTD 32/2024/QH15**, **Luật KDBH 08/2022/QH15**, **QĐ 43/2018/QĐ-TTg**.
3. **Bảng xử lý các tình huống dễ nhầm lẫn (Edge Cases)**:
   - Phần cứng CNTT (`10%` trước `07/2025` -> `8%` từ `07/2025`) vs Dịch vụ sửa chữa máy tính/máy in (`8%`).
   - Nước sạch, Thuốc, Kít xét nghiệm y tế (`5%`, không giảm xuống 8%).
   - Gas LPG (`10%` trước `07/2025` -> `8%` từ `07/2025`), Kim loại đúc sẵn (`10%`), Rượu/Bia/Golf (`10%`), Gửi xe gắn BĐS vs trông giữ xe (`10%` vs `8%`).
   - Tự động gắn cờ `Cần kiểm tra lại HĐ` đối với diễn giải mơ hồ (`Sao kê`, `Tạm ứng`, `Tinh dầu`, `Spa/Massage`, `Khóa học`).

## Cách cài đặt vào Antigravity (Global Skill)
Sao chép thư mục `skills/vn-vat-tax-audit` vào:
- Windows: `%USERPROFILE%\.gemini\config\skills\vn-vat-tax-audit\`
- macOS / Linux: `~/.gemini/config/skills/vn-vat-tax-audit/`
