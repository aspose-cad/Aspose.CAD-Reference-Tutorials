---
title: Xuất DWG sang PDF hoặc hình ảnh Raster - Hướng dẫn Aspose.CAD
linktitle: Xuất DWG sang PDF hoặc hình ảnh Raster
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Khám phá hướng dẫn toàn diện về cách xuất DWG sang PDF hoặc hình ảnh raster bằng Aspose.CAD cho .NET. Tìm hiểu các bước, điều kiện tiên quyết và bắt tay thực hành với thư viện mạnh mẽ này.
type: docs
weight: 11
url: /vi/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Giới thiệu

Bạn đang tìm cách chuyển đổi liền mạch các tệp DWG thành PDF hoặc hình ảnh raster trong ứng dụng .NET của mình? Đừng tìm đâu xa! Hướng dẫn từng bước này sẽ hướng dẫn bạn qua quy trình sử dụng thư viện Aspose.CAD cho .NET mạnh mẽ. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn này sẽ đáp ứng mọi cấp độ kỹ năng.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

- Hiểu biết cơ bản về lập trình .NET.
-  Đã cài đặt thư viện Aspose.CAD cho .NET. Nếu không thì tải về[đây](https://releases.aspose.com/cad/net/).
- Môi trường phát triển tích hợp (IDE) yêu thích của bạn được thiết lập để phát triển .NET.

## Nhập không gian tên

Hãy bắt đầu mọi thứ bằng cách nhập các vùng tên cần thiết vào dự án .NET của bạn. Điều này đảm bảo rằng bạn có quyền truy cập vào chức năng Aspose.CAD trong mã của mình.

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

Bắt đầu bằng cách tải tệp DWG mà bạn muốn chuyển đổi. Thay thế "Thư mục tài liệu của bạn" bằng đường dẫn đến tệp DWG của bạn.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Mã của bạn để tải DWG ở đây
}
```

## Bước 2: Thiết lập Xuất PDF

Bây giờ, hãy định cấu hình cài đặt xuất PDF. Ví dụ này trình bày cách thiết lập bố cục và xử lý chuyển đổi đơn vị.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Kiểm tra và xác định hệ thống đơn vị
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Mã của bạn để thiết lập xuất PDF có ở đây
```

## Bước 3: Xuất sang PDF

Thực hiện xuất sang PDF bằng cách sử dụng cài đặt đã định cấu hình.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Bước 4: Xuất sang hình ảnh raster

Mở rộng chức năng xuất sang hình ảnh raster, chẳng hạn như PNG.

```csharp
// Khổ A4 ở 300 dpi - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách sử dụng Aspose.CAD cho .NET để xuất tệp DWG sang cả hình ảnh PDF và raster. Thư viện mạnh mẽ này hợp lý hóa quy trình, giúp quy trình trở nên hiệu quả và thân thiện với nhà phát triển.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET trong các dự án thương mại của mình không?

 A1: Có, bạn có thể. Thăm nom[mua.aspose.com/buy](https://purchase.aspose.com/buy) để biết chi tiết cấp phép.

### Q2: Có bản dùng thử miễn phí không?

 A2: Chắc chắn rồi! Lấy bản dùng thử miễn phí của bạn[đây](https://releases.aspose.com/).

### Câu 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho .NET?

 A3: Đi tới[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng.

### Câu hỏi 4: Tôi có thể xin giấy phép tạm thời cho mục đích thử nghiệm không?

 A4: Có, bạn có thể nhận được giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể tìm tài liệu chi tiết ở đâu?

 A5: Tài liệu có sẵn tại[Aspose.CAD](https://reference.aspose.com/cad/net/).