# Team14-FE
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Liên kết Bootstrap từ CDN -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <title>Quản lý thông tin khách hàng </title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        table, th, td {
            border: 1px solid black;
            padding: 8px;
        }
        
        th {
            background-color: #dddddd;
        }
        
        .pagination {
            display: inline-block;
        }
        
        .pagination a {
            color: black;
            float: left;
            padding: 8px 16px;
            text-decoration: none;
            border: 1px solid #ddd;
        }
        
        .pagination a.active {
            background-color: #4CAF50;
            color: white;
            border: 1px solid #4CAF50;
        }
        
        .pagination a:hover:not(.active) {
            background-color: #ddd;
        }
        
        .title {
            text-align: center;
            margin-bottom: 20px;
        }
    </style>
</head>

<body>
    <div class="container">
        <!-- Tạo biểu mẫu ngang -->
        <form class="form-horizontal" action="/action_page.php">
            <!-- Tiêu đề biểu mẫu -->
            <h2 class="text-center">Quản Lý Thông Tin khách hàng</h2>
            <!-- Nhóm các trường nhập liệu và nhãn -->
            <div class="form-group row">
                <!-- Nhãn cho trường họ và tên -->
                <label for="name" class="col-sm-2 col-form-label">Họ và tên:</label>
                <!-- Trường nhập liệu cho họ và tên -->
                <div class="col-sm-10">
                    <input type="text" class="form-control" id="name" placeholder="Nhập họ và tên">
                </div>
            </div>
            <div class="form-group row">
                <!-- Nhãn cho trường email -->
                <label for="email" class="col-sm-2 col-form-label">Email:</label>
                <!-- Trường nhập liệu cho email -->
                <div class="col-sm-10">
                    <input type="email" class="form-control" id="email" placeholder="Nhập email">
                </div>
            </div>
            <div class="form-group row">
                <!-- Nhãn cho trường email -->
                <label for="email" class="col-sm-2 col-form-label">SDT:</label>
                <!-- Trường nhập liệu số điện thoại -->
                <div class="col-sm-10">
                    <input type="SDT" class="form-control" id="SDT" placeholder="Nhập SDT">
                </div>
            </div>
            <div class="form-group row">
                <!-- Nhãn cho trường giới tính -->
                <label for="gender" class="col-sm-2 col-form-label">Giới tính:</label>
                <!-- Trường nhập liệu cho giới tính -->
                <div class="col-sm-10">
                    <select class="form-control" id="gender">
                        <option>Nam</option>
                        <option>Nữ</option>
                        <option>Khác</option>
                    </select>
                </div>
            </div>
            <div class="form-group row">
                <!-- Nhãn cho trường email -->
                <label for="email" class="col-sm-2 col-form-label">Địa chỉ:</label>
                <!-- Trường nhập liệu cho email -->
                <div class="col-sm-10">
                    <input type="Địa chỉ" class="form-control" id="Địa chỉ" placeholder="Nhập địa chỉ">
                </div>
            </div>
            <div class="form-group row">
                <!-- Nhãn cho trường mật khẩu -->
                <label for="password" class="col-sm-2 col-form-label">Mật khẩu:</label>
                <!-- Trường nhập liệu cho mật khẩu -->
                <div class="col-sm-10">
                    <input type="password" class="form-control" id="password" placeholder="Nhập mật khẩu">
                </div>
            </div>
            <!-- Nhóm các nút chức năng -->
            <div class="form-group row">
                <!-- Nút thêm -->
                <div class="col-sm-3">
                    <button type="submit" class="btn btn-primary btn-block">Thêm</button>
                </div>
                <!-- Nút sửa -->
                <div class="col-sm-3">
                    <button type="submit" class="btn btn-success btn-block">Sửa</button>
                </div>
                <!-- Nút xóa -->
                <div class="col-sm-3">
                    <button type="submit" class="btn btn-danger btn-block">Xóa</button>
                </div>
                <!-- Nút thoát -->
                <div class="col-sm-3">
                    <button style="background-color:chartreuse;" type="submit" class="btn btn-danger btn-block">thoát</button>
                </div>
            </div>
            <table id="usersTable">
                <tr>
                    <th>Họ và tên</th>
                    <th>Email</th>
                    <th>Số điện thoại</th>
                    <th>Giới tính</th>
                    <th>Địa chỉ </th>
                    <th>Mật khẩu </th>
                    <th>xem chi tiết </th>
                </tr>
                <tr>
                    <td>Nguyễn Văn A</td>
                    <td>test1@example.com</td>
                    <td>0123456789</td>
                    <td>nam</td>
                    <td>đà nẵng</td>
                    <td>ngyenvana</td>
                    <td>xem chi tiết</td>
                </tr>
                <tr>
                    <td>Nguyễn Văn b</td>
                    <td>test12xample.com</td>
                    <td>0123456789</td>
                    <td>nam</td>
                    <td>đà nẵng</td>
                    <td>ngyenvanb</td>
                    <td>xem chi tiết </td>
                </tr>
                <tr>
                    <td>Nguyễn Văn A</td>
                    <td>test1@example.com</td>
                    <td>0123456789</td>
                    <td>nam</td>
                    <td>đà nẵng</td>
                    <td>ngyenvana</td>
                    <td>xem chi tiết </td>
                </tr>
                <!-- Các dòng dữ liệu khác -->
            </table>
            
            <div class="pagination">
                <a href="#">&laquo;</a>
                <a href="#" class="active">1</a>
                <a href="#">2</a>
                <a href="#">3</a>
                <a href="#">4</a>
                <a href="#">5</a>
                <a href="#">&raquo;</a>
            </div>
            
        </form>
    </div>

    <!-- Liên kết Bootstrap JS từ CDN -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>


