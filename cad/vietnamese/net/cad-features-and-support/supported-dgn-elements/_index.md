---
date: 2026-03-29
description: Tìm hiểu cách chuyển đổi DGN sang PNG bằng Aspose.CAD cho .NET. Hướng
  dẫn này cũng đề cập đến hỗ trợ định dạng tệp CAD và toàn bộ các phần tử DGN được
  hỗ trợ.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Chuyển đổi DGN sang PNG với Aspose.CAD cho .NET
url: /vi/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DGN sang PNG với Aspose.CAD cho .NET

## Giới thiệu

Bạn là một nhà phát triển .NET đang tìm cách **convert DGN to PNG** một cách liền mạch? Aspose.CAD cho .NET cung cấp giải pháp mạnh mẽ để xử lý các tệp DGN một cách hiệu quả. Trong hướng dẫn này, chúng tôi sẽ khám phá các phần tử DGN được hỗ trợ, hướng dẫn bạn quy trình làm việc với Aspose.CAD cho .NET đồng thời chỉ cho bạn cách xuất các phần tử đó ra hình ảnh PNG.

## Câu trả lời nhanh
- **What does Aspose.CAD do?** Nó đọc, sửa đổi và chuyển đổi các tệp CAD/BIM (bao gồm DGN) sang các định dạng raster như PNG.  
- **Can I convert 2D and 3D DGN elements?** Có – cả thực thể 2‑D và 3‑D đều được hỗ trợ.  
- **Which .NET versions are required?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Do I need a license for testing?** Một bản dùng thử miễn phí có sẵn; giấy phép cần thiết cho môi trường sản xuất.  
- **Where do I get the library?** Tải xuống từ trang chính thức của Aspose (liên kết bên dưới).

## “convert DGN to PNG” là gì?
Chuyển đổi DGN sang PNG có nghĩa là render bản vẽ DGN dựa trên vector (2‑D hoặc 3‑D) thành định dạng ảnh raster (PNG). Điều này hữu ích khi bạn cần hiển thị bản vẽ CAD trên web, nhúng chúng vào báo cáo, hoặc tạo ảnh thu nhỏ mà không cần một trình xem CAD.

## Tại sao nên sử dụng Aspose.CAD cho .NET để hỗ trợ định dạng tệp CAD?
- **Full CAD file format support** – DGN, DWG, DXF, DWF, và hơn nữa.  
- **No external dependencies** – thư viện .NET thuần, không cần cài đặt CAD gốc.  
- **High‑fidelity rendering** – giữ nguyên độ dày đường, màu sắc và hình học 3‑D.  
- **Batch processing** – dễ dàng lặp qua nhiều tệp trong ứng dụng phía máy chủ.

## Yêu cầu trước

- Kiến thức cơ bản về lập trình .NET.  
- Visual Studio đã được cài đặt trên máy của bạn.  
- Thư viện Aspose.CAD cho .NET, bạn có thể tải xuống [here](https://releases.aspose.com/cad/net/).

## Nhập không gian tên

Để khởi động dự án của bạn, nhập các không gian tên cần thiết vào ứng dụng .NET của bạn. Bước này đảm bảo bạn có quyền truy cập vào các chức năng do Aspose.CAD cho .NET cung cấp.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Cách chuyển đổi DGN sang PNG

Dưới đây là hướng dẫn từng bước giúp bạn tải tệp DGN, duyệt các phần tử của nó, xử lý cả thực thể 2‑D và 3‑D, và cuối cùng xuất kết quả ra ảnh raster PNG.

### Bước 1: Tải tệp DGN

Bắt đầu bằng cách tải một tệp DGN hiện có dưới dạng `DgnImage` trong ứng dụng .NET của bạn.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Bước 2: Duyệt qua các phần tử DGN

Duyệt qua các phần tử DGN bằng vòng lặp `foreach`. Aspose.CAD cho .NET cung cấp nhiều loại phần tử DGN mà bạn có thể làm việc.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Bước 3: Xử lý các thực thể 2‑D đã được hỗ trợ trước đây

Các thực thể này hiện cũng được hỗ trợ cho việc render 3‑D. Câu lệnh switch cho phép bạn phân nhánh logic dựa trên loại phần tử.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Bước 4: Xử lý các thực thể 3‑D được hỗ trợ

Aspose.CAD bổ sung hỗ trợ đầy đủ cho một số phần tử DGN 3‑D. Mở rộng câu lệnh switch để xử lý chúng khi cần.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Bước 5: Xuất và lưu dưới dạng PNG

Sau bất kỳ thao tác nào cần thiết, xuất bản vẽ DGN ra ảnh raster PNG và lưu vào thư mục đã chỉ định.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** Sử dụng `Image.Save` với `new PngOptions()` để kiểm soát độ phân giải, màu nền và các cài đặt đặc thù của PNG.

## Tổng quan hỗ trợ định dạng tệp CAD

Aspose.CAD cho .NET không chỉ giới hạn ở DGN. Nó còn hỗ trợ DWG, DXF, DWF và nhiều định dạng CAD khác, cung cấp cho bạn một API duy nhất để xử lý một loạt rộng các bản vẽ kỹ thuật. Điều này làm cho nó trở nên lý tưởng cho các dự án cần **CAD file format support** trên nhiều tiêu chuẩn.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Lý do | Giải pháp |
|-------|--------|-----|
| **Hình ảnh xuất hiện trống** | Xuất với DPI bằng 0 | Chỉ định `ResolutionX` và `ResolutionY` trong `PngOptions`. |
| **Thiếu hình học 3‑D** | Loại phần tử không được xử lý trong switch | Thêm trường hợp `DgnElementType` còn thiếu và render tương ứng. |
| **Hết bộ nhớ khi xử lý tệp lớn** | Tải toàn bộ tệp một lần | Xử lý các phần tử theo lô hoặc sử dụng streaming khi có thể. |

## Câu hỏi thường gặp

### Q1: Tôi có thể tìm tài liệu cho Aspose.CAD cho .NET ở đâu?
A1: Bạn có thể tìm tài liệu [here](https://reference.aspose.com/cad/net/).

### Q2: Làm sao để tải Aspose.CAD cho .NET?
A2: Bạn có thể tải thư viện [here](https://releases.aspose.com/cad/net/).

### Q3: Có bản dùng thử miễn phí cho Aspose.CAD cho .NET không?
A3: Có, bạn có thể truy cập bản dùng thử miễn phí [here](https://releases.aspose.com/).

### Q4: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD cho .NET ở đâu?
A4: Giấy phép tạm thời có sẵn [here](https://purchase.aspose.com/temporary-license/).

### Q5: Cần trợ giúp hoặc có câu hỏi?
A5: Tham khảo cộng đồng Aspose.CAD cho .NET tại [support forum](https://forum.aspose.com/c/cad/19).

---

**Cập nhật lần cuối:** 2026-03-29  
**Được kiểm tra với:** Aspose.CAD for .NET 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}