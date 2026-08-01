

## I. Yêu cầu bài tập
* **Tổng số học sinh:** 35 học sinh.
* **Số lượng nhóm:** 6 nhóm.
* **Quy tắc phân bổ:** $35 \div 6 = 5$ dư 5 $\rightarrow$ **5 nhóm 6 học sinh** và **1 nhóm 5 học sinh**.

---

## II. Sơ đồ Workflow (Quy trình thực hiện)

```mermaid
graph TD
    Start((Bắt đầu: 35 HS)) --> Logic[Tính toán sỉ số: 35 / 6 = 5 dư 5]
    
    Logic --> Distribute[Phân bổ sỉ số nhóm]
    Distribute --> G1[5 Nhóm x 6 HS]
    Distribute --> G2[1 Nhóm x 5 HS]

    G1 --> Criteria{Chọn tiêu chí chia}
    G2 --> Criteria

    Criteria -- Bốc thăm ngẫu nhiên --> Process[Thực hiện phân nhóm]
    Criteria -- Chia theo điểm/Danh sách --> Process

    Process --> Review[Kiểm tra & Rà soát sỉ số]
    
    Review --> |Hợp lệ: Đủ 35 HS / 6 nhóm| End((Hoàn tất chia nhóm))
    Review --> |Không hợp lệ| Criteria
