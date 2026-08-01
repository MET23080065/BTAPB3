graph TD
    Start((Bắt đầu: 35 HS)) --> Prep[Nhập danh sách 35 HS vào Wheel of Names]
    Prep --> Config[Cấu hình sỉ số: 5 Nhóm x 6 HS + 1 Nhóm x 5 HS]
    Config --> SetGroup[Bắt đầu chia: Nhóm 1]

    SetGroup --> Spin[Bấm quay Vòng quay]
    Spin --> Pick[Vòng quay dừng: Chọn được 1 HS]
    Pick --> Assign[Điền tên HS vào Nhóm hiện tại]
    Assign --> Remove[Bấm 'Remove' để xóa HS khỏi Vòng quay]

    Remove --> CheckGroup{Nhóm hiện tại đã đủ sỉ số?}
    
    CheckGroup -- Chưa đủ --> CheckWheel
    CheckGroup -- Đã đủ --> NextGroup[Chuyển sang Nhóm tiếp theo]
    
    NextGroup --> CheckWheel{Vòng quay còn tên HS không?}
    CheckWheel -- Còn tên --> Spin
    CheckWheel -- Hết tên --> Export[Xuất Bảng Danh sách 6 Nhóm hoàn chỉnh]
    
    Export --> End((Hoàn tất))

    %% Định dạng màu sắc
    style Start fill:#f9f,stroke:#333,stroke-width:2px,color:#000
    style End fill:#9f9,stroke:#333,stroke-width:2px,color:#000
    style Spin fill:#ff9,stroke:#333,stroke-width:2px,color:#000
    style CheckGroup fill:#fca,stroke:#333,stroke-width:1px,color:#000
