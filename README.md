# WebsiteBanHang - He Thong Quan Ly Ban LAPTOP

## Moi truong
- **Framework:** ASP.NET MVC 5 (.NET Framework 4.7.2)
- **Database:** SQL Server LocalDB (`.\SQLEXPRESS01`)
- **ORM:** Entity Framework 6.1.3
- **Authentication:** Forms Authentication + Session
- **Frontend:** Bootstrap 3, jQuery, FontAwesome
- **Admin Theme:** SB Admin 2

---

## Cau hinh & Cai dat

### 1. Yeu cau he thong
- Windows 10/11
- Visual Studio 2019 hoac 2022
- SQL Server (LocalDB) da duoc cai dat
- .NET Framework 4.7.2 SDK

### 2. Khoi tao Database
Database `QuanLyBanHang.mdf` nam tai `src/WebsiteBanHang/App_Data/`. Khi chay lan dau, Entity Framework se tu dong tao bang.

Neu gap loi ket noi, kiem tra `Web.config`:
```xml
<connectionStrings>
  <add name="QuanLyBanHangEntities"
       connectionString="... data source=.\SQLEXPRESS01; ..."
       providerName="System.Data.EntityClient" />
</connectionStrings>
```

### 3. Chay du an
1. Mo `src/WebsiteBanHang/WebsiteBanHang.csproj` bang Visual Studio
2. Set project `WebsiteBanHang` lam startup project
3. Nhan `Ctrl + F5` de chay (khong debug)

### 4. Cai dat IIS Express (neu can)
- Port mac dinh: `https://localhost:44356/`
- Su dung Visual Studio IIS Express de host

---

## Tai khoan mac dinh

### Tai khoan Admin (Quan Tri Vien)
| Thuoc tinh    | Gia tri            |
|---------------|---------------------|
| Tai khoan     | `admin`             |
| Mat khau      | `123456`            |
| MaLoaiTV      | `1` (QuanTriVien)   |
| Quyen         | Tat ca quyen        |

### Tai khoan Quan Ly (Co nhung quyen han che)
| Thuoc tinh    | Gia tri            |
|---------------|---------------------|
| Tai khoan     | Tu tao             |
| Mat khau      | Tu dat khi tao      |
| MaLoaiTV      | `2` (QuanLy)        |
| Quyen         | QuanLy, QuanTriWeb  |

### Tai khoan Khach Hang (Thanh vien)
| Thuoc tinh    | Gia tri            |
|---------------|---------------------|
| Tai khoan     | Tu tao qua trang DangKy |
| Mat khau      | Tu dat khi tao      |
| MaLoaiTV      | `3` (KhachHang)     |

> **Luu y:** Can tao tai khoan admin thu cong trong bang `ThanhVien` voi `MaLoaiTV = 1` hoac su dung trang `/ThongKe/DangkyAdmin` roi thay doi `MaLoaiTV` thanh `1` trong database.

---

## Cac chuc nang hien co

### Traang nguoi dung (Khach hang)
| Chuc nang | Mo ta |
|-----------|-------|
| Trang chu | Hien thi san pham moi, banner quang cao |
| Danh sach san pham | Loc theo loai, nha san xuat, phan trang |
| Chi tiet san pham | Hinh anh, mo ta, binh luan, dat hang |
| Gio hang | Them/sua/xoa san pham, tinh tong tien |
| Dat hang | Nhap thong tin giao hang, xac nhan don |
| Tim kiem | Tim san pham theo ten |
| Dang ky | Tao tai khoan thanh vien (co Captcha) |
| Dang nhap | Dang nhap tai khoan |

### Trang quan tri (Admin)
| Chuc nang | Mo ta |
|-----------|-------|
| Dashboard | Thong ke doanh thu, don hang, thanh vien |
| Quan ly san pham | Them, sua, xoa, upload hinh san pham |
| Quan ly loai san pham | Them, sua, xoa loai |
| Quan ly nha san xuat | Them, sua, xoa nha san xuat |
| Quan ly don hang | Duyet don, cap nhat trang thai giao hang |
| Quan ly thanh vien | Xem, sua, xoa tai khoan nguoi dung |
| Quan ly phieu nhap | Nhap hang, ds san pham sap het |
| Quan ly quyen | Them, sua, xoa quyen |
| Phan quyen | Gan quyen cho tung loai thanh vien |

---

## Lien ket quan trong

| Trang | URL |
|-------|-----|
| Trang chu | `/Home` hoac `/` |
| San pham | `/SanPham/SanPham` |
| Gio hang | `/GioHang/XemGioHang` |
| Dang ky | `/Home/DangKy` |
| Dang nhap (trang Admin) | `/ThongKe/DangkyAdmin` |
| Dashboard Admin | `/ThongKe/Index` |
| Quan ly san pham | `/QuanLySanPham/Index` |
| Quan ly don hang | `/QuanLyDonHang/ChuaThanhToan` |
| Quan ly thanh vien | `/QuanLyThanhVien/Index` |
| Quan ly loai | `/QuanLyLoai/Index` |
| Quan ly nha san xuat | `/QuanLyNhaSX/Index` |
| Nhap hang | `/QuanLyPhieuNhap/NhapHang` |
| Quan ly quyen | `/QuanLyQuyen/Index` |
| Phan quyen | `/PhanQuyen/Index` |
| Loi phan quyen | `/Home/LoiPhanquyen` |

---

## Cau truc thu muc

```
WebsiteBanHang/
├── App_Data/
│   └── QuanLyBanHang.mdf          # Database SQL Server LocalDB
├── App_Start/
│   ├── BundleConfig.cs            # Cau hinh bundle CSS/JS
│   ├── FilterConfig.cs            # Cau hinh filter
│   └── RouteConfig.cs             # Cau hinh route
├── Content/
│   ├── AdminLayout/               # Giao dien Admin (SB Admin 2)
│   ├── css/                       # CSS chung
│   ├── fontawesome/               # Font Awesome icons
│   └── js/                       # JavaScript files
├── Controllers/
│   ├── HomeController.cs         # Trang chu, dang nhap/dang ky
│   ├── SanPhamController.cs      # Trang san pham
│   ├── GioHangController.cs       # Gio hang
│   ├── TimKiemController.cs       # Tim kiem
│   ├── ThongKeController.cs       # Dashboard & thong ke
│   ├── QuanLySanPhamController.cs
│   ├── QuanLyDonHangController.cs
│   ├── QuanLyThanhVienController.cs
│   ├── QuanLyLoaiController.cs
│   ├── QuanLyNhaSXController.cs
│   ├── QuanLyPhieuNhapController.cs
│   ├── QuanLyQuyenController.cs
│   └── PhanQuyenController.cs
├── Models/
│   ├── QuanLyBanHangModel.Context.cs
│   ├── QuanLyBanHangModel.cs
│   ├── QuanLyBanHangModel.edmx    # Entity Framework model
│   ├── Metadata/                  # Metadata annotations
│   ├── ViewModel/                # View models
│   └── *.cs                      # Entity classes
├── Views/
│   ├── Home/
│   ├── SanPham/
│   ├── GioHang/
│   ├── TimKiem/
│   ├── ThongKe/
│   ├── QuanLySanPham/
│   ├── QuanLyDonHang/
│   ├── QuanLyThanhVien/
│   ├── QuanLyLoai/
│   ├── QuanLyNhaSX/
│   ├── QuanLyPhieuNhap/
│   ├── QuanLyQuyen/
│   ├── PhanQuyen/
│   ├── Layout/                   # Master layouts
│   └── Shared/
├── Global.asax.cs
└── Web.config
```

### Bang du lieu chinh

| Bang | Mo ta |
|------|-------|
| `ThanhVien` | Tai khoan nguoi dung |
| `LoaiThanhVien` | Loai tai khoan (Admin/QuanLy/Khach) |
| `Quyen` | Cac quyen he thong |
| `LoaiThanhVien_Quyen` | Bang trung gian phan quyen |
| `SanPham` | San pham |
| `LoaiSanPham` | Loai san pham |
| `NhaSanXuat` | Nha san xuat |
| `NhaCungCap` | Nha cung cap |
| `DonDatHang` | Don dat hang |
| `ChiTietDonDatHang` | Chi tiet don dat hang |
| `PhieuNhap` | Phieu nhap hang |
| `ChiTietPhieuNhap` | Chi tiet phieu nhap |
| `KhachHang` | Thong tin khach hang |
| `BinhLuan` | Binh luan san pham |

---

## Cac loi thuong gap va cach xu ly

### 1. Loi "Cannot attach the file ... as database 'QuanLyBanHang'"
**Nguyen nhan:** SQL Server LocalDB chua khoi tao hoac duong dan database sai.

**Cach fix:**
- Mo **SQL Server Management Studio (SSMS)**
- Ket noi: `.\SQLEXPRESS01`
- Kiem tra database `QuanLyBanHang` da ton tai chua
- Neu chua co, tao database moi voi ten `QuanLyBanHang`
- Hoac sua `Web.config` cho dung duong dan:
```xml
<add name="QuanLyBanHangEntities"
     connectionString="... attachdbfilename=|DataDirectory|\QuanLyBanHang.mdf; ..."
     providerName="System.Data.EntityClient" />
```

### 2. Loi "The operation cannot be completed because the DbContext has been disposed"
**Nguyen nhan:** Controller goi `Dispose()` 2 lan.

**Cach fix:** Chi giu mot loi goi trong `Dispose`:
```csharp
protected override void Dispose(bool disposing)
{
    if (disposing && db != null)
    {
        db.Dispose();
    }
    base.Dispose(disposing);
}
```

### 3. Loi "A network-related or instance-specific error occurred"
**Nguyen nhan:** SQL Server LocalDB chua duoc khoi dong hoac ten instance sai.

**Cach fix:**
- Mo **Command Prompt**:
```batch
sqllocaldb start .\SQLEXPRESS01
```
- Hoac mo Visual Studio Installer, cai them **SQL Server LocalDB**
- Kiem tra ten instance trong `Web.config` (`.\SQLEXPRESS01`)

### 4. Loi "Session timeout nhanh (1 phut)"
**Nguyen nhan:** `Web.config` cau hinh `sessionState timeout="1"` (1 phut).

**Cach fix:** Sua trong `Web.config`:
```xml
<sessionState timeout="60"></sessionState>
```

### 5. Loi "Login failed" khi chay tren IIS
**Nguyen nhan:** IIS su dung user khac de truy cap database.

**Cach fix:**
- Mo **SQL Server Configuration Manager**
- Dam bao SQL Server cho phep **Mixed Mode Authentication**
- Hoac sua connection string su dung SQL Authentication:
```xml
<add name="QuanLyBanHangEntities"
     connectionString="... user id=sa; password=yourpassword; ..."
     providerName="System.Data.EntityClient" />
```

### 6. Loi hinh anh san pham khong hien thi
**Nguyen nhan:** Thu muc `Content/images/` khong co hinh hoac duong dan sai.

**Cach fix:**
- Kiem tra thu muc `Content/images/` da co hinh san pham
- Kiem tra duong dan trong cot `HinhAnh` cua bang `SanPham`
- Vi du: `Content/images/tenhinh.jpg`

### 7. Loi "401 Unauthorized" khi truy cap trang Admin
**Nguyen nhan:** Chua dang nhap hoac tai khoan khong co quyen.

**Cach fix:**
- Dang nhap tai `/ThongKe/DangkyAdmin` voi tai khoan admin
- Dam bao tai khoan co `MaLoaiTV = 1` trong database

### 8. Loi Entity Framework "Unable to load the specified metadata resource"
**Nguyen nhan:** Duong dan metadata trong connection string sai.

**Cach fix:** Kiem tra connection string trong `Web.config`:
```xml
<add name="QuanLyBanHangEntities"
     connectionString="
       metadata=res://*/Models.QuanLyBanHangModel.csdl|
               res://*/Models.QuanLyBanHangModel.ssdl|
               res://*/Models.QuanLyBanHangModel.msl;
       provider=System.Data.SqlClient;
       provider connection string=&quot;data source=.\SQLEXPRESS01;...&quot;"
     providerName="System.Data.EntityClient" />
```
- Dam bao cac file `.csdl`, `.ssdl`, `.msl` ton tai trong `Models/`

### 9. Loi "Captcha not valid" khi dang ky
**Nguyen nhan:** Ma Captcha nhap sai.

**Cach fix:**
- Nhap dung chu cai hien thi trong hinh Captcha
- Neu loi lien tuc, kiem tra `CaptchaMvc` da duoc tham chieu dung chua

### 10. Loi build "Roslyn" tren mot so may
**Nguyen nhan:** Thieu Roslyn compiler package.

**Cach fix:**
```batch
cd src/WebsiteBanHang
nuget restore
```
Hoac trong Visual Studio: **Tools > NuGet Package Manager > Package Manager Console > Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -Reinstall**

---

## Phan quyen he thong

| MaQuyen | Ten quyen | Mo ta |
|---------|-----------|-------|
| `QuanLy` | QuanLy | Quan ly don hang |
| `QuanTriWeb` | QuanTriWeb | Quan tri toan bo |
| `Admin` | Admin | Quan tri he thong |
| `ThanhVien` | ThanhVien | Thanh vien |
| `KhachHang` | KhachHang | Khach hang |

MaLoaiTV = 1: QuanTriVien (tat ca quyen)
MaLoaiTV = 2: QuanLy (quyen han che)
MaLoaiTV = 3: KhachHang (thanh vien binh thuong)

---

## Ghi chu them
- Du an su dung **Forms Authentication** voi **cookie** luu quyen (het han sau 3 gio)
- Session timeout 1 phut (mac dinh), co the thay doi trong `Web.config`
- San pham bi danh dau `DaXoa = true` se khong hien thi ngoai trang nguoi dung
- Don dat hang can duyet trang thai `DaThanhToan` va `TinhTrangGiaoHang` trong trang Admin
