---
date: 2026-03-16
description: Học cách chuyển đổi DWG sang PDF hoặc hình ảnh raster với Aspose.CAD
  cho .NET. Hướng dẫn từng bước chuyển đổi CAD sang PDF này bao gồm việc xuất DWG
  sang các định dạng hình ảnh như PNG và chỉ ra cách xuất DWG sang các tệp hình ảnh
  một cách hiệu quả.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách chuyển đổi DWG sang PDF và hình ảnh raster bằng Aspose.CAD cho .NET
url: /vi/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG sang PDF hoặc Hình ảnh Raster - Hướng dẫn Aspose.CAD

## Giới thiệu

Nếu bạn cần **chuyển đổi DWG sang PDF** (hoặc sang các định dạng raster như PNG) trực tiếp từ một ứng dụng .NET, bạn đang ở đúng nơi. Trong hướng dẫn này, chúng ta sẽ đi qua các bước chính xác để sử dụng Aspose.CAD cho .NET thực hiện việc chuyển đổi, giải thích vì sao thư viện này là lựa chọn vững chắc, và chỉ cho bạn cách xử lý cả đầu ra PDF và hình ảnh chỉ với vài dòng mã.

## Câu trả lời nhanh
- **Thư viện nào xử lý chuyển đổi DWG?** Aspose.CAD cho .NET  
- **Tôi có thể xuất DWG sang PNG cũng như PDF không?** Có – các tùy chọn rasterization hoạt động cho cả hai định dạng.  
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Những phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Việc chuyển đổi đơn vị có được tự động xử lý không?** Bạn có thể định nghĩa hệ thống đơn vị một cách thủ công (hệ mét hoặc hệ Anh) như trong mã mẫu.

## “chuyển DWG sang PDF” là gì?
Chuyển DWG sang PDF có nghĩa là lấy một bản vẽ CAD (DWG) và render nó thành một tài liệu di động, chỉ xem được (PDF). Điều này hữu ích để chia sẻ thiết kế với các bên liên quan không có phần mềm CAD, tạo tài liệu có thể in, hoặc lưu trữ bản vẽ ở định dạng có thể đọc được trên mọi nền tảng.

## Tại sao nên dùng Aspose.CAD cho việc chuyển đổi này?
- **Không phụ thuộc bên ngoài** – thư viện hoạt động hoàn toàn trong mã quản lý.  
- **Độ trung thực cao** – giữ lại các lớp, độ dày đường, và thông tin bố cục.  
- **Tùy chọn raster tích hợp** – cho phép xuất sang PNG, JPEG, BMP, v.v., chỉ với một đối tượng cấu hình.  
- **Đa nền tảng** – hoạt động trên Windows, Linux và macOS với .NET Core.

## Yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn rằng bạn đã chuẩn bị các yếu tố sau:

- Kiến thức cơ bản về lập trình .NET.  
- Thư viện Aspose.CAD cho .NET đã được cài đặt. Nếu chưa, tải về [tại đây](https://releases.aspose.com/cad/net/).  
- IDE yêu thích của bạn đã được cấu hình để phát triển .NET.

## Nhập không gian tên

Hãy bắt đầu bằng việc nhập các không gian tên cần thiết trong dự án .NET của bạn. Điều này đảm bảo bạn có quyền truy cập vào các chức năng của Aspose.CAD trong mã.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Bước 1: Tải tệp DWG

Bắt đầu bằng việc tải tệp DWG mà bạn muốn chuyển đổi. Thay `"Your Document Directory"` bằng đường dẫn tới tệp DWG của bạn.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Bước 2: Cấu hình xuất PDF (Cách xuất DWG sang PDF)

Bây giờ, hãy cấu hình các thiết lập xuất PDF. Ví dụ này minh họa cách đặt bố cục và xử lý chuyển đổi đơn vị.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Bước 3: Xuất sang PDF

Thực thi việc xuất sang PDF bằng các thiết lập đã cấu hình.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Bước 4: Xuất sang Hình ảnh Raster (xuất dwg sang hình ảnh)

Mở rộng chức năng để xuất sang hình ảnh raster, chẳng hạn như PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Trang trắng trong PDF** | Bố cục không được chỉ định đúng | Đảm bảo `rasterizationOptions.Layouts` bao gồm tên bố cục chính xác (ví dụ: `"Model"`). |
| **Kích thước không đúng** | DPI hoặc kích thước trang không khớp | Điều chỉnh giá trị `PageHeight`, `PageWidth` và DPI trong `CadRasterizationOptions`. |
| **Đơn vị hiển thị sai** | Chưa định nghĩa chuyển đổi đơn vị | Sử dụng `DefineUnitSystem` để đặt `currentUnitIsMetric` và `currentUnitCoefficient` dựa trên `cadImage.UnitType`. |
| **Lỗi giấy phép** | Giới hạn phiên bản dùng thử | Áp dụng giấy phép tạm thời hoặc vĩnh viễn trước khi gọi `Image.Load`. |

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD cho .NET trong các dự án thương mại không?
A1: Có, bạn có thể. Tham khảo chi tiết giấy phép tại [purchase.aspose.com/buy](https://purchase.aspose.com/buy).

### Q2: Có bản dùng thử miễn phí không?
A2: Chắc chắn! Tải bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q3: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho .NET?
A3: Hãy truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ.

### Q4: Tôi có thể lấy giấy phép tạm thời để thử nghiệm không?
A4: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q5: Tôi có thể tìm tài liệu chi tiết ở đâu?
A5: Tài liệu có sẵn tại [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Làm sao **lưu CAD dưới dạng PNG** với chất lượng cao?
A6: Đặt `PageHeight` và `PageWidth` thành kích thước pixel mong muốn và chọn DPI từ 300 trở lên trong `CadRasterizationOptions`.

### Q7: Cách tốt nhất để **chuyển đổi dwg** khi tệp nguồn chứa nhiều bố cục là gì?
A7: Điền `rasterizationOptions.Layouts` với tất cả các tên bố cục bạn muốn xuất, sau đó lặp qua mỗi bố cục và gọi `Save` cho từng định dạng đầu ra.

---

**Cập nhật lần cuối:** 2026-03-16  
**Đã kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}