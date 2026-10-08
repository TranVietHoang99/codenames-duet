# 🕵️ Mật Danh Duet

Bản tiếng Việt của **Codenames Duet** (Vlaada Chvátil, Scot Eaton, CGE) cho 2 người, chơi ngay trên trình duyệt.
Trò chơi **hợp tác**: hai điệp viên cùng thắng hoặc cùng thua.

Chơi online: https://tranviethoang99.github.io/codenames-duet/

## Cách chơi online
- Bấm *Tạo phòng*, chọn số lượt (9 = chuẩn) và số lần nhầm tối đa, rồi gửi mã hoặc link cho đồng đội.
- Đồng đội nhập mã và bấm *Vào phòng*.
- Người tạo phòng phải **giữ tab mở**, vì máy chủ phòng giữ trạng thái ván chơi (và giữ kín khoá của từng người).

## Luật tóm tắt
- Bàn 25 từ. Mỗi người nhìn một mặt thẻ khoá: 9 điệp viên, 3 sát thủ, 13 người qua đường. Tổng cộng có 15 điệp viên khác nhau.
- Người ra gợi ý nói **một từ + một số**, gợi tới các ô xanh trên khoá của mình. Người kia đoán, kết quả tính theo khoá của người ra gợi ý:
  - điệp viên: lật ra, được đoán tiếp (phải đoán ít nhất 1 từ rồi mới được dừng);
  - người qua đường: hết lượt;
  - sát thủ: thua ngay.
- Mỗi lượt dùng 1 đồng hồ, hai người đổi vai. Ai đã được tìm hết 9 điệp viên thì chỉ còn làm người đoán.
- Hết đồng hồ thì vào **đột tử**: không còn gợi ý, mỗi người tự chạm từ mình nghĩ là điệp viên của đồng đội, sai một lần là thua.
- Thắng khi tìm đủ 15 điệp viên.

## Cách bấm
- Chạm một từ để chọn (đồng đội thấy viền cam), chạm lần nữa để chốt.
- 🚶 dưới ô: bạn đã chạm nhầm (người qua đường theo khoá đồng đội); 🚶 trên ô: đồng đội chạm nhầm theo khoá của bạn.
- Bỏ chọn *Tô màu khoá của tôi lên bàn* nếu muốn nhìn bàn trơn.

## Kỹ thuật
Một file `index.html` duy nhất, kết nối P2P bằng [PeerJS](https://peerjs.com/), cùng khung với Quoridor, Azul và Jaipur.
Bộ từ có hơn 500 danh từ tiếng Việt, nhiều từ hai nghĩa (Đường, Tên, Cờ, Bóng, Sao, Đá, Cầu…).
Không có chế độ chơi với máy vì máy cần hiểu nghĩa từ tiếng Việt để ra và đoán gợi ý.
Chạy thử: `npx http-server codenames-duet -p 5190`.
