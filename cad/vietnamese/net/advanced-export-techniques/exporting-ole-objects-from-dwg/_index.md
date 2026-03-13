---
description: Tìm hiểu cách chuyển đổi DWG sang PNG và trích xuất các đối tượng OLE
  từ tệp DWG bằng Aspose.CAD cho .NET – một hướng dẫn nhanh, tập trung vào mã.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Chuyển đổi DWG sang PNG & Xuất đối tượng OLE - Hướng dẫn Aspose.CAD
url: /vi/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất các đối tượng OLE từ tệp DWG - Hướng dẫn Aspose.CAD

## Giới thiệu

Nếu bạn cần **convert DWG to PNG** đồng thời trích xuất các đối tượng OLE được nhúng, bạn đã đến đúng nơi. Aspose.CAD cho .NET làm cho quy trình hai bước này trở nên đơn giản, cho phép bạn tự động hoá việc trích xuất và raster hoá chỉ trong vài dòng C#. Trong vài phút tới, chúng ta sẽ đi qua toàn bộ quy trình, từ thiết lập môi trường đến lưu mỗi DWG dưới dạng PNG chứa dữ liệu OLE đã trích xuất.

## Câu trả lời nhanh
- **Hướng dẫn này đề cập đến gì?** Chuyển đổi DWG sang PNG và trích xuất các đối tượng OLE bằng Aspose.CAD cho .NET.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Có thể xử lý nhiều tệp DWG cùng lúc không?** Có – mẫu code lặp qua một mảng tên tệp.  
- **Tôi có thể tìm thêm ví dụ ở đâu?** Xem tài liệu chính thức của Aspose.CAD và các liên kết diễn đàn dưới đây.

## **convert DWG to PNG** là gì?
Chuyển đổi một DWG (bản vẽ AutoCAD) sang ảnh PNG sẽ raster hoá dữ liệu vector, giúp dễ dàng xem hoặc nhúng vào trang web, báo cáo, hoặc các ứng dụng khác không hỗ trợ DWG gốc. Khi có các đối tượng OLE, chúng có thể được trích xuất và lưu dưới dạng tài nguyên riêng trong quá trình chuyển đổi.

## Tại sao cần trích xuất các đối tượng OLE từ tệp CAD?
Nhiều bản vẽ DWG nhúng bảng tính, biểu đồ hoặc các tài liệu Office khác dưới dạng OLE. Việc trích xuất chúng cho phép bạn tái sử dụng dữ liệu gốc, tự động hoá báo cáo, hoặc chuyển nội dung sang định dạng mới mà không mất thông tin nhúng.

## Yêu cầu trước

- Thư viện Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt thư viện. Bạn có thể tải về từ [trang tải Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).
- Thư mục tài liệu: Tạo một thư mục chứa các tệp DWG của bạn. Thay thế `"Your Document Directory"` trong đoạn mã mẫu bằng đường dẫn thực tế.

## Nhập không gian tên

Trong dự án .NET của bạn, nhập các không gian tên cần thiết:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Hướng dẫn từng bước

### Bước 1: Đặt thư mục tài liệu

```csharp
string MyDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn nơi lưu các tệp DWG của bạn.

### Bước 2: Liệt kê các tệp DWG cần xử lý

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Bước 3: Cấu hình tùy chọn xuất cho việc chuyển đổi PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Bạn có thể điều chỉnh `CadRasterizationOptions` (ví dụ: `PageWidth`, `PageHeight`, `BackgroundColor`) để phù hợp với độ phân giải mong muốn.

### Bước 4: Duyệt qua từng DWG và thực hiện chuyển đổi

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Trong vòng lặp này, thư viện tự động **extract OLE objects** được nhúng trong mỗi bản vẽ và đưa chúng vào PNG được tạo. Nếu bạn cần luồng OLE thô, có thể truy cập bộ sưu tập `cadImage.OleObjects` – một cách tiện lợi để **how to extract ole** dữ liệu một cách lập trình.

## Các vấn đề thường gặp & Khắc phục

- **Missing layout name** – Đảm bảo layout bạn chỉ định (`"Layout1"` trong ví dụ) tồn tại trong DWG nguồn; nếu không rasterizer sẽ quay lại không gian mô hình mặc định.
- **Large files cause memory pressure** – Xử lý từng tệp một (như trong ví dụ) và giải phóng đối tượng `CadImage` kịp thời bằng `using`.
- **Unexpected colors** – Đặt `rasterizationOptions.BackgroundColor` phù hợp với nền bản vẽ nếu cần độ trong suốt.

## Câu hỏi thường gặp

### Q1: Aspose.CAD cho .NET có phù hợp với cả tệp CAD cấp junior và senior không?
A1: Có, Aspose.CAD cho .NET đa năng và có thể xử lý nhiều loại tệp CAD, bao gồm cả các biến thể junior và senior.

### Q2: Tôi có thể tùy chỉnh tùy chọn xuất cho các layout khác nhau không?
A2: Chắc chắn! Như đã minh họa trong hướng dẫn, bạn có thể điều chỉnh các tùy chọn xuất, bao gồm layout, để đáp ứng nhu cầu cụ thể.

### Q3: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho .NET ở đâu?
A3: Khám phá [tài liệu Aspose.CAD cho .NET](https://reference.aspose.com/cad/net/) để có thông tin sâu rộng và các ví dụ.

### Q4: Có bản dùng thử miễn phí không?
A4: Có, bạn có thể trải nghiệm khả năng của Aspose.CAD cho .NET với bản dùng thử miễn phí. Truy cập [liên kết này](https://releases.aspose.com/) để bắt đầu.

### Q5: Làm sao để nhận hỗ trợ hoặc kết nối với cộng đồng?
A5: Đối với **support** và giao lưu cộng đồng, hãy truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q6: Làm thế nào để **extract OLE from CAD** mà không chuyển đổi sang PNG?
A6: Sử dụng bộ sưu tập `CadImage.OleObjects` sau khi tải DWG; bạn có thể duyệt từng `OleObject` và lưu dữ liệu thô của nó vào tệp.

## Kết luận

Bạn đã thấy cách **convert DWG to PNG** đồng thời **extracting OLE objects** một cách liền mạch bằng Aspose.CAD cho .NET. Cách tiếp cận này tiết kiệm thời gian, loại bỏ các bước sao chép‑dán thủ công, và tích hợp mượt mà vào các pipeline tự động. Hãy thử nghiệm với các định dạng raster khác (JPEG, BMP) hoặc khám phá bộ tính năng phong phú của Aspose trong việc xử lý CAD.

---

**Cập nhật lần cuối:** 2026-03-13  
**Được kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}