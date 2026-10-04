### Phần 1: Phân tích nguyên nhân đứt gãy đường dẫn

1\. Sử dụng đường dẫn tuyệt đối (Absolute Path) phụ thuộc vào môi trường cố định Đường dẫn của Bình chỉ ra vị trí chính xác từ gốc ổ đĩa (`C:\`). Khi sang máy giáo viên, tên thư mục người dùng (`User Profile`) thay đổi (ví dụ: `C:\Users\ThayGiao\...`), hoặc máy không có ổ `C:\`, Python sẽ không thể tìm thấy file theo đúng cấu trúc cứng đó.

2\. Lỗi ký tự thoát (Escape Character) trong chuỗi Python trên Windows Trong chuỗi (string) Python, dấu gạch chéo ngược `\` được dùng làm ký tự thoát (escape sequence). Các cụm như `\U` trong `\Users` hoặc `\a` trong `\assets` sẽ bị Python giải mã thành ký tự đặc biệt (Unicode / Bell ascii), dẫn đến sai lệch chuỗi đường dẫn ban đầu.

### Phần 2: Giải pháp & Viết lại đường dẫn tương đối (Relative Path)

#### 1\. Viết lại đường dẫn tương đối

Giả sử file code (`main.py` hoặc `bai1.py`) nằm ngay trong thư mục `Session-02/`, cấu trúc thư mục dự án như sau:

Session-02/assets/logo.png   
Session-02/[main.py](http://main.py)

