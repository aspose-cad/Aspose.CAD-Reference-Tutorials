---
date: 2026-03-21
description: Tìm hiểu cách tạo PDF từ DWG và xuất DGN như một phần của DWG bằng Aspose.CAD
  cho .NET. Hướng dẫn này cũng chỉ cách chuyển đổi DWG sang PDF và thiết lập các tùy
  chọn PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Tạo PDF từ DWG và Xuất DGN như một phần của DWG – Aspose.CAD cho .NET
url: /vi/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ DWG và Xuất DGN như một phần của DWG – Aspose.CAD cho .NET

## Giới thiệu

Nếu bạn cần **tạo PDF từ DWG** đồng thời nhúng một thiết kế DGN như một phần của DWG, Aspose.CAD cho .NET giúp thực hiện một cách đơn giản. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình: tải DWG, tìm DGN underlay được nhúng, cấu hình các tùy chọn rasterization, và cuối cùng xuất kết quả ra tài liệu PDF. Dù bạn đang xây dựng công cụ chuyển đổi hàng loạt, một engine báo cáo, hay dịch vụ tích hợp CAD‑BIM, các bước dưới đây sẽ cung cấp nền tảng vững chắc, sẵn sàng cho môi trường sản xuất.

## Trả lời nhanh
- **Thư viện nào xử lý chuyển đổi DWG → PDF?** Aspose.CAD cho .NET  
- **Tôi có thể xuất DGN underlay khi tạo PDF không?** Có – underlay được truy cập qua `CadDgnUnderlay`.  
- **Phương thức nào thiết lập các tùy chọn PDF?** `PdfOptions` kết hợp với `CadRasterizationOptions`.  
- **Có cần giấy phép cho việc sử dụng thương mại không?** Có, cần một giấy phép Aspose.CAD hợp lệ.  
- **Các phiên bản .NET được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “tạo PDF từ DWG” là gì?

Tạo PDF từ một tệp DWG có nghĩa là render bản vẽ vector thành tài liệu PDF dạng raster hoặc vector. Quy trình này hữu ích để chia sẻ bản vẽ với những người không có phần mềm CAD, lưu trữ, hoặc tạo các báo cáo có thể in. Aspose.CAD đơn giản hoá công việc bằng cách xử lý việc phân tích các thực thể DWG và cung cấp kiểm soát chi tiết đối với đầu ra thông qua `PdfOptions`.

## Tại sao phải xuất DGN như một phần của DWG?

Một DGN underlay thường đại diện cho hình học tham chiếu từ các dự án MicroStation. Khi xuất DGN cùng với DWG, bạn giữ nguyên ngữ cảnh thiết kế gốc, đảm bảo người dùng cuối nhìn thấy bộ bản vẽ đầy đủ. Điều này đặc biệt có giá trị trong các dự án đa ngành nơi cả tệp DWG và DGN cùng tồn tại.

## Yêu cầu trước

- **Aspose.CAD cho .NET** – tải về [tại đây](https://releases.aspose.com/cad/net/).  
- **Môi trường phát triển** – Visual Studio (bất kỳ phiên bản mới nào) hoặc IDE .NET ưa thích của bạn.  
- **Kiến thức cơ bản về C#** – bạn nên quen thuộc với cú pháp C# và cấu trúc dự án .NET.

## Nhập không gian tên

Thêm các chỉ thị `using` cần thiết ở đầu tệp nguồn C# của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hướng dẫn từng bước

### Bước 1: Xác định đường dẫn tệp

Đặt tệp DWG đầu vào và tên tệp PDF đầu ra.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Bước 2: Tạo đối tượng `PdfOptions` (đặt tùy chọn pdf)

`PdfOptions` cho phép bạn kiểm soát cách PDF được tạo, chẳng hạn như kích thước trang, nén và siêu dữ liệu.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Bước 3: Tải tệp DWG

Tải DWG dưới dạng `CadImage` để bạn có thể kiểm tra các thực thể của nó.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Bước 4: Duyệt qua các thực thể

Duyệt qua mọi thực thể trong bản vẽ để tìm DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Bước 5: Kiểm tra loại thực thể (cách xuất dgn)

Xác định liệu thực thể hiện tại có phải là DGN underlay hay không.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Bước 6: Lấy đường dẫn Underlay

Lấy đường dẫn tham chiếu bên ngoài của tệp DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Bước 7: Định nghĩa tùy chọn Rasterization (chuyển dwg sang pdf)

Cấu hình cách DWG được raster hóa trước khi được chèn vào PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Bước 8: Xuất DWG ra PDF

Cuối cùng, lưu hình ảnh đã render thành tệp PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **`Image.Load` báo “File not found”** | Đường dẫn không đúng hoặc tệp bị thiếu. | Sử dụng đường dẫn tuyệt đối hoặc đảm bảo DWG được sao chép vào thư mục output. |
| **Đường dẫn Underlay rỗng** | DGN underlay không được nhúng hoặc tham chiếu bị hỏng. | Kiểm tra DWG thực sự chứa DGN underlay và tệp DGN bên ngoài có thể truy cập được. |
| **Kết quả PDF trống** | Các tùy chọn rasterization được đặt kích thước bằng 0. | Điều chỉnh `PageWidth`/`PageHeight` hoặc đặt `NoScaling = false`. |
| **Lỗi giấy phép** | Chạy mà không có giấy phép Aspose.CAD hợp lệ. | Áp dụng giấy phép trước khi tải hình ảnh: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD cho .NET trong các dự án thương mại không?
A1: Có, bạn có thể. Ghé thăm [tại đây](https://purchase.aspose.com/buy) để khám phá các tùy chọn mua giấy phép.

### Q2: Có giới hạn nào về kích thước tệp DWG tôi có thể xử lý không?
A2: Aspose.CAD hỗ trợ xử lý các tệp DWG lớn, nhưng có thể bị giới hạn bởi phần cứng.

### Q3: Có phiên bản dùng thử không?
A3: Có, bạn có thể tải bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q4: Làm sao để lấy giấy phép tạm thời?
A4: Giấy phép tạm thời có thể được nhận [tại đây](https://purchase.aspose.com/temporary-license/).

### Q5: Tôi có thể tìm trợ giúp ở đâu nếu gặp vấn đề?
A5: Bạn có thể truy cập diễn đàn Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19) để được hỗ trợ.

**Hỏi: Làm sao để đặt siêu dữ liệu PDF bổ sung (tác giả, tiêu đề, v.v.)?**  
Đáp: Sử dụng các thuộc tính `exportOptions.Metadata` trước khi gọi `Save`.

**Hỏi: Tôi có thể xuất nhiều layout thành các trang PDF riêng biệt không?**  
Đáp: Có – đặt `Layouts = new string[] { "Layout1", "Layout2" }` trong `CadRasterizationOptions`.

**Hỏi: Aspose.CAD có hỗ trợ chuyển DWG sang các định dạng ảnh khác không?**  
Đáp: Chắc chắn. Bạn có thể xuất ra PNG, JPEG, SVG và nhiều định dạng khác bằng cách sử dụng các overload tương ứng của `Image.Save`.

---

**Cập nhật lần cuối:** 2026-03-21  
**Kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}