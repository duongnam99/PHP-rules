# Clean Code PHP 
- Biến: 
    - Sử dụng tên biến dễ hiểu
    - Các số quan trọng nên được lưu vào biến với tên thể hiện ý nghĩa của nó, đặt tên sao cho dễ tìm kiếm 
    - Sử dụng cùng từ vựng cho cùng một loại biến 
    - Tránh lồng quá nhiều, nên return sớm 
    - Không nên thêm những thứ không cần thiết (nếu tên của class/object đẫ rõ ràng thì không nên viết lại trong biến)
    - Sử dụng đối số mặc định thay vì phải kiểm tra bằng biểu thức điều kiện
    - Sửu dụng identical comparison (khi cần so sánh cả kiểu của biến)
- Hàm: 
    - Đối số của hàm nên ít hơn hoặc bằng 2 
    - Hàm chỉ nên thực hiện một chức năng
    - Tên hàm nên thể hiển chức năng của hàm
    - Không sử dụng cờ như là một đối số của hàm
    - Tránh dùng điều kiện phủ định, đóng gói điều kiện
    - Không viết hàm global
    - Tránh kiểm tra dữ liệu 
    - Xóa code thừa
- Đối tượng và kiến trúc dữ liệu 
    - Sử dụng đối tượng đóng gói 
    - Tạo đối tượng chứa thuộc tính hoặc phương thức protected/private
- Lớp 
    - Ưu tiên kiểu thành phần hơn là kế thừa

# SOLID : 5 nguyên tắc cơ bản của lập trình hướng đối tượng 
- S: nguyên lí trách nhiệm duy nhất (SRP): không nên có nhiều hơn 1 lí do để thay đổi một class
- O: nguyên lí đóng mở (OCP): nguyên lý này đơn giản là nên cho phép người dùng thêm mới mà không được thay đổi code hiện tại
- L: nguyên lí thay thế (LSP): 
- I: nguyên lí phân tách (ISP): Không nên ép người dùng phải phụ thuộc vào interface mà họ không sử dụng
- D: nguyên lí đảo ngược dependencies (DIP): 
    - Module cấp cao không nên phụ thuộc vào module cấp thấp. Cả hai nên phụ thuộc vào abstract
    - Abstract không nên phụ thuộc vào chi tiết, mà phải ngược lại
- D: nguyên lí đừng lặp lại chính mình (DRY): Tốt nhất nên chống lặp code ngay khi có thể. Nếu có thể tạo một abstract tốt, hãy tạo nó! Đừng lặp lại code, nếu không bạn sẽ phải rất cực khổ mỗi khi muốn sửa đổi gì đó.
# Các chuẩn PSR trong PHP: 17 tiêu chuẩn (08/2018)
- PSR-1: tiêu chuẩn code cơ bản:
    - các file CẦN chỉ sử dụng thẻ mở <?php hoặc <?=.
    - các file CẦN chỉ mã hóa UTF-8 cho code PHP.
    - các file NÊN chỉ nên làm hoặc là khai báo class, function, constant ... hoặc chứa các cài đặt thay đổi câu hình .ini tuy nhiên không nên viết trong cùng một nơi.
    - namespace và class CẦN theo một chuẩn "autoload" PSR (PSR-0, PSR-4).
    - tên các Class CẦN được khai báo theo kiểu StudlyCaps.
    - các constant của Class CẦN được khai báo với tất cả bằng chữ hoa và phân tách giữa các từ bằng dấu gạch chân (vd: HTTP_STATUS).
    - phương thức CẦN được khai báo theo kiểu camelCase.

- PSR-2: phong cách code: 
    - code phải tuân theo tiêu chuẩn 1
    - dùng 4 đấu cách thay vì dùng tab
    - phải có một dòng trống sau namespace và use
    - một dòng nên có ít hơn 80 kí tự
    - abstract và final phải khai báo trước, static khai báo sau   
- PSR-4: tiêu chuẩn viết autoload
    - \<NamespaceName>(\<SubNamespaceNames>)*\<ClassName>
    - tên xác định đầy đủ phải có 1 namespace gốc
    - có thể có 1 hoặc nhiều namespace con 
    - phải có 1 tên lớp kết thúc
- PSR-7: chuẩn giao diện thông điệp:

# PHP design pattern 
Có 23 mẫu được chia làm 3 loại :

- Creational Patterns (Mẫu tạo lập) : Được sử dụng để tạo các đối tượng sao cho chúng có thể tách khỏi hệ thống triển khai  của chúng
- Structural Patterns (Mẫu cấu trúc) : Để tạo cấu trúc các đối tượng lớn giữa nhiều đối tượng khác nhau
- Behavioral Patterns (Mẫu hành vi) : Được sử dụng để quản lý các thuật toán, mối liên kết và ràng buộc giữa các đối tượng