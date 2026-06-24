---
date: 2026-04-03
description: Học cách thiết lập viewport và chuyển đổi DWG sang PDF trong C# bằng
  Aspose.CAD. Hướng dẫn dwg sang pdf này cho thấy việc xuất chính xác với tọa độ.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Chuyển đổi DWG sang PDF với tọa độ trong C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách Đặt Viewport Khi Chuyển Đổi DWG Sang PDF Với Tọa Độ trong C# - Hướng Dẫn
  Aspose.CAD
url: /vi/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển Đổi DWG sang PDF với Tọa Độ trong C# - Hướng Dẫn Aspose.CAD

## Giới Thiệu

Chào mừng bạn đến với hướng dẫn toàn diện về **cách đặt viewport** khi chuyển đổi tệp DWG sang PDF với các tọa độ được chỉ định bằng Aspose.CAD cho .NET. Bằng cách kiểm soát viewport, bạn sẽ có các tệp PDF pixel‑perfect khớp chính xác với khu vực bạn cần—hoàn hảo cho bản vẽ xây dựng, bản xem trước sơ đồ mặt bằng, hoặc bất kỳ quy trình BIM nào.

## Câu Trả Lời Nhanh
- **Câu hỏi “set viewport” có nghĩa là gì?** Nó xác định vùng hiển thị và tỷ lệ của bản vẽ CAD trong quá trình raster hóa.  
- **Thư viện nào thực hiện việc chuyển đổi?** Aspose.CAD cho .NET.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các nền tảng được hỗ trợ?** Windows, Linux và macOS với .NET 5/6/7 hoặc .NET Framework 4.6+.  
- **Thời gian thực hiện điển hình?** Khoảng 10‑15 phút cho một chuyển đổi cơ bản.

## Yêu Cầu Trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có các yêu cầu sau:

- **Thư viện Aspose.CAD** – Tải xuống và cài đặt thư viện Aspose.CAD cho .NET. Bạn có thể tìm thư viện [tại đây](https://releases.aspose.com/cad/net/).
- **Môi trường phát triển** – Visual Studio, Rider, hoặc bất kỳ IDE nào hỗ trợ phát triển .NET.
- **Tệp DWG** – Chuẩn bị một tệp DWG sẵn sàng để chuyển đổi. Bạn có thể sử dụng tệp mẫu được cung cấp hoặc tệp DWG tùy chỉnh của mình.

## Cách Đặt Viewport Để Xuất PDF Chính Xác

Đặt viewport là bước cốt lõi cho phép bạn xác định khu vực chính xác của bản vẽ mà bạn muốn render. Trong đoạn mã dưới đây, chúng ta tạo một `CadVportTableObject` mới, đặt vị trí bằng tọa độ góc trên‑trái, và tính toán chiều rộng, chiều cao, và tỷ lệ khung hình. Đây là cách **cài đặt viewport** điều khiển phần còn lại của quá trình chuyển đổi.

## Nhập Không Gian Tên

Trong dự án C# của bạn, nhập các không gian tên cần thiết:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Hãy phân tích đoạn mã thành hướng dẫn từng bước để hiểu rõ hơn:

## Bước 1: Xác Định Thư Mục Tài Liệu

```csharp
string MyDir = "Your Document Directory";
```

## Bước 2: Đặt Đường Dẫn Tệp DWG Nguồn

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Bước 3: Tải Tệp DWG và Cấu Hình Tùy Chọn Rasterization

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Bước 4: Xác Định Tọa Độ và Viewport  

Ở đây chúng ta thực sự **đặt viewport** (cách đặt viewport) bằng cách chỉ định góc trên‑trái, chiều rộng và chiều cao của khu vực bạn muốn xuất.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Bước 5: Áp Dụng Cài Đặt Viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Bước 6: Cấu Hình Tùy Chọn PDF và Xuất  

Bây giờ chúng ta kết hợp mọi thứ lại và **chuyển DWG sang PDF** bằng cách sử dụng các tùy chọn rasterization mà chúng ta vừa chuẩn bị.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Bước 7: Hiển Thị Thông Báo Thành Công

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Các Trường Hợp Sử Dụng Thông Thường

- **Tài liệu xây dựng** – Tạo PDF có thể in được cho các phần cụ thể của sơ đồ mặt bằng.  
- **Phối hợp BIM** – Xuất chỉ khu vực quan tâm để phát hiện xung đột.  
- **Trình bày với khách hàng** – Cung cấp PDF sạch sẽ của một phòng hoặc mặt đứng đã chọn mà không lộ toàn bộ bản vẽ.

## Kết Luận

Chúc mừng! Bạn đã thành công **chuyển DWG sang PDF** với các tọa độ chính xác và học được **cách đặt viewport** bằng Aspose.CAD cho .NET. **Hướng dẫn dwg sang pdf** này trình bày cách **tạo pdf từ dwg** và **xuất dwg dưới dạng pdf c#** đồng thời giữ toàn quyền kiểm soát khu vực đầu ra.

## Câu Hỏi Thường Gặp

### Q1: Tôi có thể sử dụng Aspose.CAD với các định dạng tệp CAD khác không?

A1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DWF và các định dạng khác.

### Q2: Làm thế nào tôi có thể xử lý lỗi trong quá trình chuyển đổi?

A2: Triển khai cơ chế xử lý lỗi bằng các khối try‑catch để bắt và quản lý ngoại lệ.

### Q3: Aspose.CAD có phù hợp cho cả môi trường Windows và Linux không?

A3: Có, Aspose.CAD tương thích với cả hai nền tảng Windows và Linux.

### Q4: Tôi có thể tùy chỉnh đầu ra PDF thêm không?

A4: Chắc chắn! Khám phá các tùy chọn phong phú do Aspose.CAD cung cấp để điều chỉnh đầu ra PDF theo yêu cầu cụ thể của bạn.

### Q5: Tôi có thể tìm hỗ trợ bổ sung hoặc thảo luận cộng đồng ở đâu?

A5: Truy cập [Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

## Câu Hỏi Thêm Thường Gặp

**Q: Phương pháp này có hoạt động với các tệp DWG lớn (hàng trăm MB) không?**  
A: Có. Quá trình rasterization được thực hiện từng trang, và bạn có thể điều chỉnh `rasterizationOptions` (ví dụ, `Resolution`) để cân bằng chất lượng và sử dụng bộ nhớ.

**Q: Tôi có thể xuất nhiều viewport thành các trang PDF riêng biệt không?**  
A: Bạn có thể lặp qua `cadImage.ViewPorts`, đặt mỗi viewport thành hoạt động, và gọi `Save` cho mỗi trang, sau đó hợp nhất các PDF bằng Aspose.PDF.

**Q: Có thể thêm watermark vào PDF đã tạo không?**  
A: Sau khi lưu PDF, bạn có thể mở lại bằng Aspose.PDF và áp dụng watermark dạng văn bản hoặc hình ảnh trước khi cung cấp cho người dùng.

---

**Cập Nhật Lần Cuối:** 2026-04-03  
**Đã Kiểm Tra Với:** Aspose.CAD 24.11 cho .NET  
**Tác Giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}