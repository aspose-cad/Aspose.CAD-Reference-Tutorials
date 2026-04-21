---
date: 2026-03-13
description: Tìm hiểu cách thiết lập các tùy chọn raster hóa CAD và xuất các bố cục
  DWG cụ thể sang PDF bằng Aspose.CAD cho .NET – hướng dẫn toàn diện để tạo PDF từ
  tệp CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Đặt tùy chọn raster hóa CAD – Xuất bố cục cụ thể sang PDF - Hướng dẫn Aspose.CAD
url: /vi/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất các bố cục cụ thể ra PDF - Hướng dẫn Aspose.CAD

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách thiết lập tùy chọn raster hóa CAD** để có thể xuất một bố cục — hoặc nhiều bố cục — từ tệp DWG trực tiếp sang PDF. Aspose.CAD cho .NET làm cho quá trình *dwg to pdf conversion c#* trở nên đơn giản, cho phép bạn kiểm soát toàn bộ kích thước trang, độ phân giải và lựa chọn bố cục. Khi kết thúc hướng dẫn, bạn sẽ có thể **tạo PDF từ tệp CAD** chỉ với vài dòng mã.

## Trả lời nhanh
- **“set cad rasterization options” làm gì?**  
  Nó cho Aspose.CAD biết cách render dữ liệu vector (bố cục, lớp, độ dày đường) thành các trang PDF đã raster hóa.  
- **Phương thức nào xuất bố cục DWG ra PDF?**  
  Sử dụng `Image.Save` cùng với một `PdfOptions` đã được cấu hình, trong đó chứa `CadRasterizationOptions` của bạn.  
- **Có thể xuất nhiều hơn một bố cục cùng lúc không?**  
  Có – cung cấp một mảng tên bố cục trong thuộc tính `Layouts`.  
- **Có cần giấy phép cho việc sử dụng trong môi trường production không?**  
  Cần giấy phép thương mại; bản dùng thử miễn phí có sẵn để đánh giá.  
- **Các phiên bản .NET nào được hỗ trợ?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 và các phiên bản sau.

## “set cad rasterization options” là gì?
`CadRasterizationOptions` là lớp điều khiển cách các thực thể CAD được raster hóa khi chuyển đổi sang các định dạng dựa trên raster như PDF. Bằng cách cấu hình các thuộc tính của nó — kích thước trang, lựa chọn bố cục, màu nền, v.v. — bạn quyết định kết quả hình ảnh của thao tác **export dwg layout to pdf**.

## Tại sao cần thiết lập tùy chọn raster hóa CAD?
- **Độ chính xác** – Giữ nguyên độ dày và tỷ lệ đường nét chính xác như trong bản vẽ CAD gốc.  
- **Hiệu suất** – Chỉ render những bố cục bạn cần, giảm kích thước tệp và thời gian xử lý.  
- **Linh hoạt** – Điều chỉnh chiều rộng/chiều cao trang, DPI và nền để phù hợp với tiêu chuẩn báo cáo của bạn.  

## Yêu cầu trước

Trước khi bắt đầu viết mã, hãy chắc chắn rằng bạn đã:

- **Cài đặt Aspose.CAD cho .NET**. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/cad/net/).  
- Một môi trường phát triển .NET (Visual Studio, VS Code, hoặc bất kỳ IDE nào bạn thích).  
- Một tệp DWG chứa ít nhất một bố cục (tệp mẫu được dùng ở đây là `visualization_-_conference_room.dwg`).

## Nhập không gian tên

Trong dự án .NET của bạn, nhập các không gian tên cần thiết cho Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hướng dẫn từng bước

### Bước 1: Tải tệp DWG

Đầu tiên, chỉ định cho Aspose.CAD vị trí tệp DWG nguồn mà bạn muốn chuyển đổi.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Bước 2: Thiết lập **CadRasterizationOptions**

Ở đây chúng ta cấu hình các thiết lập raster hóa quyết định kích thước và độ phân giải của trang PDF.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Mẹo chuyên nghiệp:** Điều chỉnh `PageWidth` và `PageHeight` sao cho phù hợp với kích thước bố cục PDF mục tiêu của bạn. Giá trị lớn hơn sẽ tăng chi tiết nhưng đồng thời làm tăng kích thước tệp.

### Bước 3: Chỉ định tên bố cục

Cho Aspose.CAD biết bố cục nào (các) cần render. Thay `"Layout1"` bằng tên chính xác của bố cục trong tệp DWG của bạn.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Tại sao lại quan trọng:** Bằng cách giới hạn mảng `Layouts` bạn tránh việc xuất các sheet không mong muốn, giúp thao tác **dwg to pdf conversion c#** nhanh hơn và PDF tạo ra sạch sẽ hơn.

### Bước 4: Tạo `PdfOptions`

Liên kết các thiết lập raster hóa với tùy chọn xuất PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Bước 5: Xuất ra PDF

Cuối cùng, lưu bố cục đã render dưới dạng tệp PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Bước 6: Hiển thị thông báo thành công

Một dòng console nhanh sẽ xác nhận thao tác đã thành công.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **Không tạo được PDF** | Mảng `Layouts` không khớp với bất kỳ tên bố cục nào trong DWG. | Kiểm tra lại tên bố cục bằng một trình xem CAD và cập nhật thuộc tính `Layouts`. |
| **Trang trắng** | `PageWidth`/`PageHeight` được đặt thành 0 hoặc giá trị quá nhỏ. | Sử dụng kích thước thực tế (ví dụ: 1600 × 1600) hoặc để Aspose tự tính toán bằng cách bỏ qua các thuộc tính này. |
| **Tỷ lệ không đúng** | DPI chưa được đặt khi cần đầu ra độ phân giải cao. | Đặt `rasterizationOptions.Resolution = 300;` (hoặc DPI mong muốn) trước khi xuất. |

## Câu hỏi thường gặp

**H: Tôi có thể xuất nhiều bố cục cùng lúc không?**  
Đ: Có, chỉ cần sửa mảng `Layouts` ở Bước 3 để bao gồm tất cả các tên bố cục mong muốn, ví dụ `new string[] { "Layout1", "Layout2" }`.

**H: Aspose.CAD có tương thích với các định dạng CAD khác không?**  
Đ: Chắc chắn. Nó hỗ trợ DWG, DXF, DWF, DGN và nhiều định dạng khác nữa.

**H: Làm sao tôi có thể điều chỉnh các thiết lập xuất PDF ngoài kích thước trang?**  
Đ: Khám phá các thuộc tính bổ sung của `CadRasterizationOptions` như `Resolution`, `BackgroundColor` và `DrawType` để tinh chỉnh kết quả.

**H: Tôi có thể tìm tài liệu Aspose.CAD bổ sung ở đâu?**  
Đ: Truy cập [tài liệu](https://reference.aspose.com/cad/net/) để xem các tham chiếu API chi tiết và ví dụ.

**H: Có bản dùng thử miễn phí không?**  
Đ: Có, bạn có thể truy cập bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

## Kết luận

Bạn đã học cách **thiết lập tùy chọn raster hóa CAD** và sử dụng chúng để **xuất các bố cục DWG cụ thể ra PDF** với Aspose.CAD cho .NET. Cách tiếp cận này cho phép bạn kiểm soát chính xác quá trình chuyển đổi, giúp tích hợp chức năng CAD‑to‑PDF vào bất kỳ ứng dụng C# nào một cách nhanh chóng và đáng tin cậy.

---

**Cập nhật lần cuối:** 2026-03-13  
**Kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}