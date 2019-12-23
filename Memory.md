# Memory
## ROM
### I) ROM là gì
> ROM(Read Only Memory):là loại bộ nhớ chỉ đọc trong đó dữ liệu đã được ghi vào từ trước và chứa các chương trình giúp máy tính "khởi động". Khác với RAM sẽ xóa sạch mọi dữ liệu lưu trữ tạm thời, ROM giữ lại nội dung ngay cả sau khi máy đã tắt; 

ROM, theo đúng nghĩa cũng như đối với các chip ROM thế hệ đầu, cho phép chỉ đọc dữ liệu từ chúng, và chỉ cho phép ghi dữ liệu một lần, gọi là nạp ROM.Do công nghệ phát triển và nhu cầu thực tế, các thế hệ ROM sau được chế tạo với khả năng xoá được và nạp nhiều lần, mà việc thực hiện nạp ROM phải tuân theo quy trình đặc biệt đặc trưng. Nó cho ra khả năng mềm dẻo trong việc sửa đổi tính năng vận hành của hệ thống điều khiển.

### II) Các loại ROM
- PROM (Programmable Read-Only Memory) hay Mask ROM: Được chế tạo bằng các mối nối (cầu chì - có thể làm đứt bằng mạch điện). Nó thuộc dạng WORM (Write-Once-Read-Many). Chương trình nằm trong PROM có thể lập trình được bằng những thiết bị đặc biệt. Loại ROM này chỉ có thể lập trình được một lần, và là rẻ nhất.
- EPROM được chế tạo bằng nguyên tắc phân cực tĩnh điện. Cửa sổ nhỏ dùng để xóa bằng tia cực tím.
EPROM (Erasable Programmable Read-Only Memory): Được chế tạo bằng nguyên tắc phân cực tĩnh điện. Loại ROM này có thể bị xóa bằng tia cực tím và ghi lại thông qua thiết bị ghi EPROM.
- EAROM (Electrically Alterable Read-Only Memory): Loại ROM này có thể thay đổi từng bit một lần. Tuy nhiên quá trình viết khá chậm và sử dụng điện thế không chuẩn. Việc viết lại EAROM không được thực hiện thường xuyên.
- EEPROM (Electrically Erasable Programmable Read-Only Memory): Được tạo bằng công nghệ bán dẫn. Nội dung của ROM này có thể viết vào và xóa (bằng điện).

### III) BIOS
> BIOS là viết tắt của từ Basic Input/Output System hay còn gọi là hệ thống đầu vào/ra cơ bản. BIOS là một nhóm lệnh được lưu trữ trên ROM. 

Nhiệm vụ của BIOS là kiểm soát các tính năng cơ bản của máy vi tính mà chúng ta ít khi để ý tới ví dụ như:
- Kết nối và chạy trình điều khiển (driver) cho các thiết bị ngoại vi  như chuột, bàn phím, usb…
- Đọc thứ tự ổ cứng để khởi động các hệ điều hành, hiển thị tín hiệu lên màn hình…
- Sử dụng BIOS bạn có thể thực hiện được các việc như: thay đổi thứ tự ổ đĩa khi khởi động, theo dõi nhiệt độ, tốc độ quạt, ép xung, khóa máy…

Khi máy tính khởi động, nhiệm vụ của BIOS là đánh thức các bộ phận khác trên hệ thống và bảo đảm các bộ phận đó thực hiện đúng chức năng, sau đó chuyển các chức năng này vào hệ điều hành hoặc Boot Loader.

### IV) UEFI
> UEFI(Unified Extensible Firmware Interface) là một hệ điều hành tối giản "nằm trên" phần cứng (hardware) và firmware của máy tính. 
Thay vì được lưu trong firmware giống như BIOS, chương trình UEFI được lưu trữ ở thư mục /EFI/ trong bộ nhớ non-volatile (là bộ nhớ đảm bảo cho dữ liệu không bị hỏng mỗi khi mất điện).Vì vậy, UEFI có thể chứa trong bộ nhớ flash NAND trên bo mạch chính (mainboard) hoặc cũng có thể để trên một ổ đĩa cứng, hay thậm chí là ngay cả trên một vùng tài nguyên mạng được chia sẻ. UEFI sẽ giúp quá trình khởi động an toàn hơn nhờ tính năng Secure Boot.

UEFI được phát triển bởi Intel để giải quyết những yếu điểm của BIOS cũng như sẽ thay thế dần chuẩn BIOS cũ kỹ, già cỗi.

| BIOS | UEFI |
|------|------|
|Ra đời từ 1975|Mới ra đời từ 2005|
|Tốc độ khởi động chậm|Tốc độ khởi động nhanh|
|Hỗ trợ ổ cứng chuẩn MBR|Hỗ trợ cả hai loại ổ cứng MBR và GPT|
|Chỉ hạn chế xử lí ở mức 16-bit và địa chỉ hóa bộ nhớ là 1MB|Có chức năng xử lý 32bit và 64bit, cho phép người dùng sử dụng nhiều RAM hơn để địa chỉ hóa xử lý nhiều việc phức tạp hơn. Hơn nữa UEFI được thiết kế với cấu trúc riêng biệt và dùng cấp driver cho các bộ phân một cách độc lập.|
|MBR giới hạn 4 phân vùng chính cho mỗi ổ đĩa và kích thước đĩa có thể khởi động chỉ đạt ở mức 2.2TB|UEFI dùng bảng phân vùng GUID và sử dụng Globally Unique ID để địa chỉ những phân vùng và cho phép khởi động ổ cứng lên tới 9.4 Zb|