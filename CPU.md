# CPU (Central Processing Unit)
## I) CPU là gì 
> CPU (Central Processing Unit) là đơn vị xử lí trung tâm. CPU có thể được xem như não bộ, một trong những phần tử cốt lõi nhất của máy vi tính. CPU là một mạch xử lý dữ liệu theo chương trình được thiết lập trước.

Ví dụ chip intel core i9-9900K 3,60 GHz có 8 core(CPU) 16 thread(logic CPU)
![](https://www.extremetech.com/wp-content/uploads/2017/05/core-i9-640x353.jpg)

Nhiều nhân cho phép máy tính của bạn làm được nhiều việc, xử lý nhiều tác vụ cùng 1 lúc. Hiện nay nhiều ứng dụng khi được lập trình cũng được phát triển để tận dụng các CPU đa nhân. Ví dụ như trình duyệt Chrome của Google. 
Chrome render mỗi website với từng tiến trình (process) riêng biệt. Điều này cho phép trình duyệt sử dụng các CPU khác nhau cho các website khác nhau thay vì sử dụng 1 CPU cho tất cả các tác vụ liên quan đến duyệt web. 
 
Từng CPU đều có tốc độ xung nhịp (clock speed) đại diện cho tốc độ làm việc nhanh hay chậm của con chip xử lý đó. Ví dụ,trên có tốc độ xung nhịp là 3.6 GHz. Như vậy có nghĩa là từng nhân trong trong con chip này đều có tốc độ 3.6 GHz.
 
Hiện nay, nhiều chương trình máy tính là các chương trình đơn, tức là nó không tận dụng được các CPU đa nhân. Chúng phải chạy trên 1 nhân mà thôi. Bởi thế, một con chip có số nhân gấp đôi không đồng nghĩa với việc hiệu năng được tăng
lên 2 lần. Nếu bạn có 1 ứng dụng đơn luồng chạy trên hệ thống có CPU 4 nhân tốc độ 3.6 GHz, ứng dụng đó sẽ chạy ở tốc độ chỉ 3.6 GHz mà thôi. Ứng dụng sẽ chỉ dùng tới 1 nhân xử lý, còn các nhân còn lại sẽ nằm ở trạng thái idle (nghỉ).
Nếu có một tác vụ khác được yêu cầu, các nhân này mới đi vào hoạt động. 

Các CPU của Intel sử dụng 1 công nghệ có tên gọi là “siêu phân luồng”. Với công nghệ này, mỗi nhân vật lý tự nó báo với HĐH là 2 nhân logic.Công nghệ này nhìn chung sẽ giúp cải tiến hiệu năng của chip trong 1 vài trường hợp, nhưng 
không có chuyện chip 4 nhân với siêu phân luồng sẽ cho hiệu năng ngang hay gần bằng với chip 8 nhân thực.

## II) Cấu tạo của CPU
### 1) CU (Control Unit)
Bộ điều khiển ( Control Unit ) Là các vi xử lí có nhiệm vụ thông dịch các lệnh của chương trình và điều khiển hoạt động xử lí,được điều tiết chính xác bởi xung nhịp đồng hồ hệ thống. 
### 2) ALU (Ahrithmetic Logical Unit)
Bộ số học-logic (ALU-Arithmetic Logic Unit) Có chức năng thực hiện các lệnh của đơn vị điều khiển và xử lý tín hiệu. Theo tên gọi,đơn vị này dùng để thực hiện các phép tính số học( +,-,*,/ )hay các phép tính logic (so sánh lớn hơn,
nhỏ hơn...)
### 3) Register
Là các bộ nhớ có dung lượng nhỏ nhưng tốc độ truy cập rất cao, nằm ngay trong CPU, dùng để lưu trữ tạm thời các toán hạng, kết quả tính toán, địa chỉ các ô nhớ hoặc thông tin điều khiển. Mỗi thanh ghi có một chức năng cụ thể. 
Thanh ghi quan trọng nhất là bộ đếm chương trình (PC - Program Counter) chỉ đến lệnh sẽ thi hành tiếp theo.

## III) Hoạt động
![](//upload.wikimedia.org/wikipedia/commons/thumb/d/d8/ABasicComputer.gif/370px-ABasicComputer.gif)
Các hoạt động cơ bản của hầu hết các CPU là thực hiện một chuỗi các tập lệnh được lưu trữ, gọi là chương trình. Các mã lệnh chờ thực hiện này được lưu giữ trong một số loại bộ nhớ máy tính. Gần như tất cả các CPU có các bước: 
**lấy thông tin, giải mã và thực hiện lệnh khi hoạt động** và được gọi chung là chu kỳ lệnh.

Sau khi thực hiện một lệnh, toàn bộ quá trình lặp đi lặp lại, với sự chu kỳ lệnh tiếp theo thường lấy các lệnh tiếp theo trong chuỗi vì giá trị tăng lên trong thanh ghi con trỏ lệnh. Nếu một lệnh nhảy được thực hiện, con trỏ lệnh sẽ 
được sửa đổi để chứa địa chỉ của lệnh đã thay đổi và thực hiện chương trình tiếp tục như bình thường. Trong các CPU phức tạp hơn, nhiều lệnh có thể được tải xuống, giải mã, và thực hiện đồng thời.

## IV) Các thông số kỹ thuật của CPU
- Tốc độ của CPU: Tốc độ xử lý của máy tính phụ thuộc vào tốc độ của CPU, nhưng nó cũng phụ thuộc vào các phần khác (như bộ nhớ trong, RAM, hay bo mạch đồ họa).Tốc độ CPU có liên hệ với tần số đồng hồ làm việc của nó (tính bằng các 
đơn vị như MHz, GHz, ...). Đối với các CPU cùng loại tần số này càng cao thì tốc độ xử lý càng tăng. Đối với CPU khác loại, thì điều này chưa chắc đã đúng; ví dụ CPU Core 2 Duo có tần số 2,6GHz có thể xử lý dữ liệu nhanh hơn CPU 
3,4GHz một nhân. Tốc độ CPU còn phụ thuộc vào bộ nhớ đệm của nó (Bộ nhớ đệm dùng để lưu các lệnh hay dùng, giúp cho việc nhập dữ liệu xử lý nhanh hơn). 
- FSB (Front Side Bus)  Là tốc độ truyền tải dữ liệu ra vào CPU hay là tốc độ dữ liệu chạy qua chân của CPU.Trong một hệ thống thì tốc độ Bus của CPU phải bằng với tốc độ Bus của North Chipset, tuy nhiên tốc độ Bus của CPU là 
duy nhất nhưng North Chipset có thể hỗ trợ từ hai đến ba tốc độ FSB.
- Bộ nhớ Cache: Vùng nhớ mà CPU dùng để lưu các phần của chương trình, các tài liệu sắp được sử dụng. Khi cần, CPU sẽ tìm thông tin trên cache trước khi tìm trên bộ nhớ chính.
    - Cache L1: Integrated cache (cache tích hợp) - cache được hợp nhất ngay trên CPU. Cache tích hợp tăng tốc độ CPU do thông tin truyền đến và truyền đi từ cache nhanh hơn là phải chạy qua bus hệ thống. Các nhà chế tạo thường gọi 
	cache này là on-die cache. Cache L1 - cache chính của CPU. CPU trước hết tìm thông tin cần thiết ở cache này. 
    - Cache L2: Cache thứ cấp. Thông tin tiếp tục được tìm trên cache L2 nếu không tìm thấy trên cache L1. Cache L2 có tốc độ thấp hơn cache L1 và cao hơn tốc độ của các chip nhớ (memory chip). Trong một số trường hợp (như Pentium 
	Pro), cache L2 cũng là cache tích hợp
    - Cache L3: L3 cache là bộ nhớ cache đặc biệt được CPU sử dụng & được tích hợp trên mainboard. Nó làm việc cùng với bộ nhớ cache L1 & L2 để tăng hiệu năng bằng cách chống lại hiện tượng nút cổ chai xảy ra trong quá trình thực thi
	các câu lệnh & tải dữ liệu. L3 cache cung cấp thông tin cho L2 cache sau đó chuyển thông tin cho L1. Thông thường L3 cache có tốc độ truy xuất thấp hơn so với L2 cache & tất nhiên thấp hơn nhiều so với L1 nhưng nó vẫn nhanh hơn 
	tốc độ truy xuất vào RAM