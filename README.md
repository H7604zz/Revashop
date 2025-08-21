# RevaShop - E-commerce Platform

## 🚀 Giới thiệu

RevaShop là một nền tảng thương mại điện tử toàn diện được phát triển bằng ASP.NET Core 8.0, cho phép người dùng tạo và quản lý cửa hàng trực tuyến với hệ thống gói dịch vụ subscription linh hoạt.

## ✨ Tính năng chính

### 🛍️ Dành cho khách hàng
- **Mua sắm trực tuyến**: Duyệt và mua sản phẩm từ nhiều cửa hàng
- **Quản lý đơn hàng**: Theo dõi trạng thái đơn hàng realtime
- **Hệ thống voucher**: Áp dụng mã giảm giá cho đơn hàng
- **Tài khoản cá nhân**: Quản lý thông tin và lịch sử mua hàng

### 🏪 Dành cho người bán
- **Quản lý cửa hàng**: Tạo và tùy chỉnh cửa hàng online
- **Quản lý sản phẩm**: Thêm, sửa, xóa sản phẩm với hình ảnh
- **Quản lý đơn hàng**: Xử lý đơn hàng từ khách hàng
- **Thống kê bán hàng**: Báo cáo doanh thu và hiệu suất
- **Gói dịch vụ**: Đăng ký gói premium để mở rộng tính năng

### 👨‍💼 Dành cho Admin
- **Dashboard tổng quan**: Thống kê toàn hệ thống
- **Quản lý người dùng**: Quản lý tài khoản và phân quyền
- **Quản lý gói dịch vụ**: Tạo và chỉnh sửa các gói subscription
- **Quản lý danh mục**: Tổ chức danh mục sản phẩm
- **Báo cáo doanh thu**: Theo dõi doanh thu theo tháng và gói dịch vụ

## 🛠️ Công nghệ sử dụng

### Backend
- **Framework**: ASP.NET Core 8.0 MVC
- **Database**: SQL Server với Entity Framework Core
- **Authentication**: Cookie-based Authentication
- **Real-time**: SignalR cho cập nhật trạng thái thanh toán
- **File Upload**: Cloudinary integration
- **Payment**: PayOS integration

### Frontend
- **UI Framework**: Bootstrap 5
- **JavaScript**: Vanilla JS với AJAX
- **Styling**: Custom CSS với responsive design

### Packages chính
```xml
<PackageReference Include="Microsoft.EntityFrameworkCore" Version="8.0.13" />
<PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="8.0.13" />
<PackageReference Include="Microsoft.AspNetCore.Identity.EntityFrameworkCore" Version="8.0.13" />
<PackageReference Include="CloudinaryDotNet" Version="1.27.4" />
<PackageReference Include="Microsoft.AspNetCore.SignalR" Version="1.2.0" />
<PackageReference Include="payOS" Version="1.0.9" />
<PackageReference Include="BCrypt.Net-Next" Version="4.0.3" />
```

## 📦 Cài đặt và chạy dự án

### Yêu cầu hệ thống
- .NET 8.0 SDK
- SQL Server
- Visual Studio 2022 hoặc VS Code

### Các bước cài đặt

1. **Clone dự án**
```bash
git clone https://github.com/H7604zz/Revashop.git
cd ProjectEXE
```

2. **Cấu hình Database**
- Mở `appsettings.json` và cập nhật connection string:
```json
{
  "ConnectionStrings": {
    "MyCnn": "Server=YOUR_SERVER;Database=RevaShop;Trusted_Connection=true;TrustServerCertificate=true;"
  }
}
```

3. **Migration Database**
```bash
dotnet ef database update
```

4. **Cấu hình Services**
Cập nhật `appsettings.json` với các thông tin:
```json
{
  "AdminPayment": {
    "BankAccount": "YOUR_BANK_ACCOUNT",
    "BankName": "YOUR_BANK_NAME",
    "QRCodeUrl": "YOUR_QR_CODE_URL"
  },
  "Cloudinary": {
    "CloudName": "YOUR_CLOUD_NAME",
    "ApiKey": "YOUR_API_KEY",
    "ApiSecret": "YOUR_API_SECRET"
  }
}
```

5. **Chạy ứng dụng**
```bash
dotnet run
```

Ứng dụng sẽ chạy tại: `https://localhost:5001`

## 🏗️ Cấu trúc dự án

```
ProjectEXE/
├── Controllers/          # MVC Controllers
├── Models/              # Entity Models
├── Services/            # Business Logic
│   ├── Interfaces/      # Service Interfaces
│   └── Implementations/ # Service Implementations
├── ViewModels/          # View Models
├── Views/               # Razor Views
├── wwwroot/             # Static files
├── DTO/                 # Data Transfer Objects
├── Helpers/             # Helper classes
└── Hubs/                # SignalR Hubs
```

## 🗃️ Database Schema

### Bảng chính
- **Users**: Thông tin người dùng
- **Shops**: Thông tin cửa hàng
- **Products**: Sản phẩm
- **Orders**: Đơn hàng
- **ServicePackages**: Gói dịch vụ
- **PackageSubscriptions**: Đăng ký gói dịch vụ
- **PackagePayments**: Thanh toán gói dịch vụ
- **Vouchers**: Mã giảm giá

## 🔐 Phân quyền

- **Admin**: Quản lý toàn hệ thống
- **Seller**: Quản lý cửa hàng và sản phẩm
- **Customer**: Mua sắm và quản lý đơn hàng

## 💳 Hệ thống thanh toán

- **PayOS Integration**: Thanh toán online cho đơn hàng
- **Bank Transfer**: Thanh toán gói dịch vụ qua chuyển khoản
- **Real-time Updates**: Cập nhật trạng thái thanh toán qua SignalR

## 📱 Responsive Design

Website được thiết kế responsive, tương thích với:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (< 768px)

## 🤝 Đóng góp

1. Fork dự án
2. Tạo feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Tạo Pull Request

## 📄 License

Dự án này được phát triển cho mục đích học tập tại FPT University.

## 👥 Team Development

- **Repository**: [Revashop](https://github.com/H7604zz/Revashop)
- **Branch**: main
- **Course**: EXE201 - FPT University

## 📞 Liên hệ

Nếu có thắc mắc hoặc cần hỗ trợ, vui lòng tạo issue trên GitHub repository.

---

**© 2025 RevaShop - E-commerce Platform**
