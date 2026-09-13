Bảng đối chiếu hoàn chỉnh
Tiêu chí	Tình huống A: ChuyenXe và LoTrinh	Tình huống B: DonHang và CachThucThanhToan
Mô tả nghiệp vụ	Một ChuyenXe có nhiều LoTrinh. Nếu Chuyến xe bị hủy, toàn bộ Lộ trình cũng bị hủy theo, không tồn tại độc lập.	DonHang có phương thức thanhToan(), nhận CachThucThanhToan chỉ để xử lý một lần, không lưu thành thuộc tính của DonHang.
Vòng đời dữ liệu	Phụ thuộc hoàn toàn, "cùng sinh cùng tử"	Tạm thời, không gắn vòng đời
Tên quan hệ	Composition	Dependency
Ký hiệu trên sơ đồ	Hình thoi đặc đặt ở phía lớp ChuyenXe	Đường nét đứt có mũi tên trỏ từ DonHang sang CachThucThanhToan
Bước 1: Kết luận phân biệt

Composition thể hiện quan hệ sở hữu chặt chẽ, trong đó đối tượng thành phần phụ thuộc vào vòng đời của đối tượng chứa; đối tượng chứa bị hủy thì thành phần cũng bị hủy.
Dependency chỉ thể hiện sự phụ thuộc tạm thời khi một lớp sử dụng lớp khác, nhưng không sở hữu và không quản lý vòng đời của đối tượng đó.

Ghi nhớ nhanh
Quan hệ	Đặc điểm	Ký hiệu
Composition	Cùng sinh, cùng tử	◆──
Dependency	Chỉ sử dụng tạm thời	- - ->
Bước 2: Class Diagram

<img width="1249" height="487" alt="mermaid-diagram (2)" src="https://github.com/user-attachments/assets/abbbb151-32b0-4b85-b381-98ef0a1b4a3f" />


Ý nghĩa sơ đồ
ChuyenXe *-- "1..*" LoTrinh
*-- = Composition
◆ nằm ở phía ChuyenXe
Một ChuyenXe có 1 đến nhiều LoTrinh.
Xóa ChuyenXe → các LoTrinh tương ứng cũng bị xóa.
DonHang ..> CachThucThanhToan
..> = Dependency
DonHang chỉ sử dụng tạm thời CachThucThanhToan.
CachThucThanhToan không thuộc vòng đời của DonHang.

Đáp án các dấu ...:

Tình huống B – Vòng đời: tạm thời, không gắn vòng đời
Tình huống A – Tên quan hệ: Composition
Tình huống B – Tên quan hệ: Dependency
Hình thoi đặc
Hình thoi đặt ở phía lớp ChuyenXe
Mũi tên nét đứt từ DonHang sang CachThucThanhToan.
