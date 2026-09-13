Kiến trúc công nghệ (Technology Architecture)

• Mạng: Polygon

 • Tiêu chuẩn: ERC-20

 • Smart contract: công khai và được kiểm toán

 • Không có quyền nâng cấp (Immutable)

 • Không sử dụng oracle

Nguyên tắc thiết kế (Design Principles) Kiến trúc công nghệ được thiết kế dựa trên ba nguyên tắc cốt lõi sau.

1. Không can thiệp (Non-Intervention) • Tổ chức phát hành không thể can thiệp vào giá • Không có chức năng điều chỉnh mint hoặc burn bắt buộc
2. Đơn giản (Simple & Transparent) • Loại bỏ logic phức tạp • Cấu trúc dễ hiểu đối với sàn giao dịch, kiểm toán và cơ quan quản lý
3. Bất biến (Immutable) • Không thể thay đổi chức năng sau khi triển khai smart contract • Loại bỏ quyền nâng cấp và quyền quản trị

Lựa chọn mạng blockchain (Blockchain Network Selection)

 Các mạng hỗ trợ

 • Ethereum Mainnet

 • Polygon (Ethereum Layer 2)

 Việc lựa chọn mạng có thể thay đổi tùy theo điều kiện như niêm yết sàn, phí gas và môi

 trường thanh khoản, và không ảnh hưởng đến tính pháp lý hoặc kinh tế của token.

 Tiêu chí lựa chọn

 • Tính tiêu chuẩn toàn cầu

 • Khả năng tương thích với sàn giao dịch

 • Mức độ phát triển của hạ tầng kiểm toán smart contract

 • Mức độ phổ biến và sử dụng

Tiêu chuẩn Token (Token Standard)

 • Tuân thủ tiêu chuẩn ERC-20

 • Pure ERC-20 (không có khả năng mở rộng)

 • Loại bỏ các chức năng tài chính bổ sung:

 ✕ Kết nối Oracle

 ✕ Rebasing

 ✕ Logic duy trì peg

 ✕ Phân phối lợi nhuận

 ✕ Liên kết tài sản thế chấp

 Điều này ngăn chặn hoàn toàn về mặt kỹ thuật khả năng trở thành token chứng khoán hoặc

 token phái sinh.

Cấu trúc Smart Contract (Smart Contract Structure)

Thành phần hợp đồng cốt lõi

 Thành phần Mô tả

 Token Contract Hợp đồng token ERC-20 cơ bản

 Supply Logic Nguồn cung cố định (Fixed Supply)

 Transfer Logic Chức năng chuyển token tiêu chuẩn

 Approval Logic Chức năng phê duyệt tiêu chuẩn

 Áp dụng kiến trúc hợp đồng đơn (Single Contract Architecture) để loại bỏ sự phức tạp

 không cần thiết.

Chính sách phát hành (Minting Policy)

 • Phát hành một lần ban đầu (Genesis Mint)

 • Không thể phát hành thêm sau đó

 • Hàm mint() bị loại bỏ hoặc vô hiệu hóa

 Kết quả:

 • Ngay cả tổ chức phát hành cũng không thể điều chỉnh nguồn cung

 • Không có rủi ro lạm phát

 • Không thể kiểm soát giá

Chính sách đốt token (Burning Policy)

 • Về cơ bản không có chức năng burn

 • Nếu có burn theo sự kiện đặc biệt:

 o Đồng thuận cộng đồng

 o Giao dịch công khai

 o Thực hiện dựa trên địa chỉ minh bạch

 ※ Không sử dụng burn tự động hoặc burn gắn với giá (để tránh hiểu nhầm là cơ chế điều

 chỉnh giá).

Quyền quản trị và quản trị hệ thống

(Administrative Privileges and Governance)

Quyền quản trị

 • Quyền Owner được giảm thiểu hoặc loại bỏ

 • Không có các chức năng sau:

 o Đóng băng tài khoản

 o Thu hồi cưỡng chế

 o Thiết lập tham số liên quan đến giá

 o Giới hạn giao dịch

 Điều này loại bỏ hoàn toàn khả năng can thiệp thị trường bởi quản trị trung tâm.

Cấu trúc governance

 • Không có governance on-chain

 • Không có bỏ phiếu DAO

 • Không thể thay đổi tham số

 Nhờ đó:

 • Loại bỏ yếu tố “kỳ vọng tăng giá dựa trên nỗ lực của đội ngũ vận hành”

 • Loại bỏ một trong các yếu tố cốt lõi của Howey Test

Kiến trúc bảo mật (Security Architecture)

Kiểm toán smart contract

 • Kiểm toán bởi bên thứ ba

 • Công khai kết quả kiểm toán

 • Triển khai sau khi sửa các lỗ hổng

Phòng chống các vector tấn công

 • Reentrancy: không có logic vay hoặc liên quan

 • Oracle Manipulation: không sử dụng oracle

 • Price Manipulation: smart contract không thể can thiệp giá

 • Admin Abuse: tối thiểu hóa quyền quản trị

Chính sách nâng cấp và fork (Upgrade and Fork Policy)

 • Không thể nâng cấp contract

 • Không sử dụng proxy pattern

 • Khi xảy ra fork chain:

 o Chuỗi chính được lựa chọn dựa trên đồng thuận cộng đồng

Tóm tắt kiến trúc kỹ thuật (Technical Summary)

 Kiến trúc kỹ thuật đảm bảo:

 • Không thể phát hành thêm token

 • Không phụ thuộc oracle

 • Cấu trúc đơn giản và minh bạch
