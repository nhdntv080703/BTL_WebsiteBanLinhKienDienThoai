
# Giao diện người dùng
- **Hiển thị khi chưa đăng nhập**
    * Màn hình `TRANG CHỦ`: 
        * Thanh menu điều hướng [Trang chủ](http://localhost/HKT-shop/index.php), [Sản phẩm](http://localhost/HKT-shop/productList.php), [Đăng ký](http://localhost/HKT-shop/register.php), [Đăng nhập](http://localhost/HKT-shop/login.php), Đơn hàng, Giỏ hàng
        * Hiển thị slider tự động chuyển động các ảnh trong thư mục `./images/slider/`
        * Hiển thị tất cả sản phẩm theo thứ tự giảm của số lượng đã bán
        * Khi di chuyệt vào 1 sản phẩm, hình ảnh sẽ đc phòng to lên xíu, và để chuột trên 3 giây thì hiển thị tên đầy đủ của sản phẩm đó
        * Khi kích vào nút `THÊM VÀO GIỎ`, thì sản phẩm đó `không` được thêm vào giỏ hàng, và chuyển sang màn hình `ĐĂNG NHẬP`
        * Khi kích vào nút `XEM CHI TIÊT`, thì màn hình sẽ chuyển sang màn hình chi tiết sản phẩm đó và cũng có thể tiến hành thêm vào giỏ hàng

    * Màn hình `ĐĂNG KÝ` tài khoản:
        * `Thanh điều hướng và slider như trên`
        * Các ô nhậ dữ liệu không được để trống
        * Nhập email khớp với định dạng email
        * Nhập lại mật khẩu phải giống mật khẩu đã nhập
        * Nhập ngày sinh phải đúng với định dạng date
        * Ấn đăng ký(chỗ này của em vẫn còn bug, ấn load lại trang để truyển bước tiếp theo ạ)
        * Nhập mã xác mình( có thể lấy từ mã captcha từ (bẳng users)[http://localhost/phpmyadmin/index.php?route=/sql&db=hkt_shop&table=users])
        * Thông báo xác minh thành công

    * Màn hình `ĐĂNG NHẬP`:
        * `Thanh điều hướng và slider như trên`
        * Không được để trống
        * Nhập email khợp với định dạng email
        * Email hoặc password không đúng thì thông báo: `"Tên đăng nhập hoặc mật khẩu không đúng!"`
        * Nếu nhập đúng mà tải khoản chưa đước xác nhận hoặc tài khoản bị khóa thì thông báo: `"Tài khoản bạn đang bị khóa hoặc chưa được xác nhận. Vui lòng liên hệ với ADMIN để được xử lý!"`
        * Nếu nhập đúng và tk đc chấp nhận hoặc không bị khóa thì đăng nhập thành công. Màn hình chuyển sang giao diện sang `TRANG CHỦ` ở trạng thái đã đăng nhập

    * Màn hình `ĐƠN HÀNG` và giỏ hàng
        * Không hiển thị, vì chưa đăng nhập
        * Chuyển sang màn hình `ĐĂNG NHẬP`

- **Hiển thị khi đã đăng nhập**

    * Màn hình `TRANG CHỦ`: 
        * Thanh menu điều hướng [Trang chủ](http://localhost/HKT-shop/index.php), [Sản phẩm](http://localhost/HKT-shop/productList.php), Đăng xuất, [Đơn hàng](), [Giỏ hàng]()
        * Hiển thị slider tự động chuyển động các ảnh trong thư mục `./images/slider/`
        * Hiển thị tất cả sản phẩm theo thứ tự giảm của số lượng đã bán
        * Khi di chuyệt vào 1 sản phẩm, hình ảnh sẽ đc phòng to lên xíu, và để chuột trên 3 giây thì hiển thị tên đầy đủ của sản phẩm đó
        * Khi kích vào nút `THÊM VÀO GIỎ`, thì sản phẩm đó được thêm vào giỏ hàng, và giỏ hàng được tăng thêm 1
        * Khi kích vào nút `XEM CHI TIÊT`, thì màn hình sẽ chuyển sang màn hình chi tiết sản phẩm đó và cũng có thể tiến hành thêm vào giỏ hàng

    * Màn hình `ĐĂNG XUẤT` tài khoản:
        * Màn hình chuyển sang giao diện sang `ĐĂNG NHẬP` ở trạng thái chưa đăng nhập

### Giao diện Admin
    * Màn hinh [QUẢN LÝ SẢN PHẨM
        * Thanh menu điều hướng [Quản lý sản phẩm](http://localhost/HKT-shop/admin/productlist.php), [Quản lý danh mục](http://localhost/HKT-shop/admin/categoriesList.php),  [Quản lý đơn hàng](http://localhost/HKT-shop/admin/orderlist.php), [Quản lý người dùng](http://localhost/HKT-shop/admin/userlist.php)
        * Xử dụng phân trang để hiển thị(tối đa 8 sản phẩm trên 1 trang)
        * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Tên sản phẩm, hình ảnh, giá gốc, giá  khuyến mãi, tạo bởi, số lượng, trạng thái
        * Thao tác `Thêm mới`, màn hình chuyển sang giao diện thêm mới:
            * Gồm các trường: Tên sản phẩm, giá gốc, giá khuyễn mãi, hình ảnh(upload file), loại sản phẩm, số lượng, mô tả
            * Các trường nhập dữ liệu thì không được để trống
            * Trường giá và só lượng thì chỉ được nhập số
            * Hình ảnh, dùng upload file
            * Loại sản phẩm sẽ được lựa chọn theo option
            * Và nút `Lưu` để tạo mới sản phẩm
        * Thao tác `Sửa`, màn hình chuyển sang giao diện chỉnh sửa sản phẩm:
            * Gồm các trường: Tên sản phẩm, giá gốc, giá khuyến mãi, hình ảnh(upload file), loại sản phẩm, số lượng, mô tả với thông tin đã có lấy từ database
            * Các trường nhập dữ liệu thì không được để trống
            * Trường giá và só lượng thì chỉ được nhập số
            * Hình ảnh, dùng upload file và ghi đè lên file cũ
            * Loại sản phẩm sẽ được lựa chọn theo option
            * Và nút `Lưu` sửa sản phẩm
        * Thao tác `Xóa`: Khi kích nút `Xóa` thì màn hình sẽ hiển thị thông báo
            * Thông báo "Xóa thất bại"
            * Thông báo "Xóa thành công"
        * Thao tác `Khóa`: Khi kích nút `Khóa` thì màn hình sẽ hiển thị thông báo
            * Thông báo "Khóa sản phẩm thành công", Trạng thái chuyển sang dạng "Block"
            * Thông báo "Khóa sản phẩm thất bại"
        * Thao tác `Mở`: Khi kích nút `Mở` thì màn hình sẽ hiển thị thông báo
            * Thông báo "Kích hoạt sản phẩm thành công", Trạng thái chuyển sang dạng "Active"
            * Thông báo "Kích hoạt sản phẩm thất bại"
        * Thao tác `Tìm kiếm`
            * Nhập dữ liệu vào ô tìm kiếm
            * Màn hình sẽ hiển thị tất cả sản phẩm có tên sản phẩm thuộc từ khóa ( dử dụng LIKE '%search')
    
    * Màn hinh [QUẢN LÝ ĐƠN HÀNG](http://localhost/HKT-shop/admin/productlist.php)
        * Thanh menu điều hướng [Quản lý sản phẩm](http://localhost/HKT-shop/admin/productlist.php), [Quản lý danh mục](http://localhost/HKT-shop/admin/categoriesList.php),  [Quản lý đơn hàng](http://localhost/HKT-shop/admin/orderlist.php), [Quản lý người dùng](http://localhost/HKT-shop/admin/userlist.php)
        * Hiển thị các mục [Đang xử lý](), [Đã xử lý](), [Đang giao hàng](), [Đã hoàn thành]()
        * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Mã đơn hàng, ngày đặt, ngày nhận, tình trạng (được lấy từ csdl)
        * Khi kích vào nut [Đang xử lý](http://localhost/HKT-shop/admin/orderlist.php)
            * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Mã đơn hàng, ngày đặt, ngày giao, tình trạng (được lấy từ csdl)
            * Khi kích vào nút `Chi tiết`, màn hình sẽ chuyển sang thông tin chi tiết của đơn hàng đó
                * Khi ấn vào `Xác nhận`, đơn hàng sẽ được chuyển sang [Đã xử lý]()
        * Khi kích vào nut [Đã xử lý](http://localhost/HKT-shop/admin/orderlist.php)
            * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Mã đơn hàng, ngày đặt, ngày giao, tình trạng (được lấy từ csdl)
            * Khi kích vào nút `Giao hàng`, đơn hàng sẽ được chueyern sang [Đang giao hàng]()
        * Khi kích vào nut [Đang giao hàng](http://localhost/HKT-shop/admin/orderlist.php)
            * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Mã đơn hàng, ngày đặt, ngày giao, tình trạng (được lấy từ csdl)
            * Khi kích vào nút `Chi tiết`, màn hình sẽ chuyển sang thông tin chi tiết của đơn hàng đó
        * Khi kích vào nut [Đã hoàn thành](http://localhost/HKT-shop/admin/orderlist.php)
            * Hiển thị các sản phẩm theo dạng bảng gồm các thông tin về: Mã đơn hàng, ngày đặt, ngày giao, tình trạng (được lấy từ csdl)
            * Khi kích vào nút `Chi tiết`, màn hình sẽ chuyển sang thông tin chi tiết của đơn hàng đó
    
    * Màn hinh [QUẢN LÝ NGƯỜI DÙNG](http://localhost/HKT-shop/admin/categoriesList.php)
        * Thanh menu điều hướng [Quản lý sản phẩm](http://localhost/HKT-shop/admin/productlist.php), [Quản lý danh mục](http://localhost/HKT-shop/admin/categoriesList.php),  [Quản lý đơn hàng](http://localhost/HKT-shop/admin/orderlist.php), [Quản lý người dùng](http://localhost/HKT-shop/admin/userlist.php)
        * Xử dụng phân trang để hiển thị(tối đa 8 danh mục sản phẩm trên 1 trang)
        * Hiển các danh mục theo dạng bảng gồm các thông tin: Họ và tên, Ngày sinh, Quê quán, Email, Chức vụ, Trạng thái (từ csdl)
        * Thao tác `Khóa`: Khi kích nút `Khóa` thì màn hình sẽ hiển thị thông báo
            * Thông báo "Khóa người dùng thành công", Trạng thái chuyển sang dạng "Block"
            * Thông báo "Khóa người dùng thất bại"
        * Thao tác `Mở`: Khi kích nút `Mở` thì màn hình sẽ hiển thị thông báo
            * Thông báo "Kích hoạt người dùng thành công", Trạng thái chuyển sang dạng "Active"
            * Thông báo "Kích hoạt người dùng thất bại"
        * Thao tác `Tìm kiếm`
            * Nhập dữ liệu vào ô tìm kiếm
            * Màn hình sẽ hiển thị tất cả sản phẩm có tên sản phẩm thuộc từ khóa ( dử dụng LIKE '%search')

