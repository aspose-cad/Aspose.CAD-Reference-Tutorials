---
title: Làm việc với tệp DWG trong C# - Nhận kích thước bố cục DWF
linktitle: Làm việc với tệp DWG trong C# - Nhận kích thước bố cục DWF
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Khám phá sức mạnh của Aspose.CAD cho .NET trong việc xử lý các tệp DWG. Tìm hiểu cách trích xuất kích thước bố cục DWF một cách dễ dàng bằng C#.
type: docs
weight: 10
url: /vi/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Giới thiệu

Trong lĩnh vực thiết kế có sự hỗ trợ của máy tính (CAD) và phát triển .NET, Aspose.CAD là một công cụ mạnh mẽ để xử lý các tệp DWG. Hướng dẫn này sẽ hướng dẫn bạn trong quá trình làm việc với các tệp DWG trong C# và trích xuất kích thước của bố cục DWF. Trước khi đi sâu vào mã, hãy đảm bảo bạn đã thiết lập mọi thứ để bắt đầu hành trình này.

## Điều kiện tiên quyết

Để làm theo hướng dẫn này một cách liền mạch, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo rằng bạn đã cài đặt Aspose.CAD cho .NET. Bạn có thể tải nó xuống từ[Trang tải xuống Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).

Bây giờ bạn đã có các công cụ cần thiết, hãy chuyển sang lĩnh vực mã hóa.

## Nhập không gian tên

Trước khi bắt đầu làm việc với mã, hãy nhập các không gian tên được yêu cầu:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Các không gian tên này sẽ cung cấp các lớp và phương thức cần thiết để xử lý tệp CAD bằng Aspose.CAD trong ứng dụng C# của bạn.

## Bước 1: Thiết lập môi trường của bạn

Bắt đầu bằng cách đảm bảo bạn đã thiết lập đúng môi trường cho dự án của mình. Tham khảo thư viện Aspose.CAD trong dự án C# của bạn.

## Bước 2: Xác định đường dẫn tệp

Xác định đường dẫn cho tệp DWG của bạn và thư mục đầu ra cho tệp JPG được tạo:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Bước 3: Tải hình ảnh DWF

Tải hình ảnh DWF bằng Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Mã cho các bước tiếp theo sẽ có ở đây
}
```

## Bước 4: Lặp lại các trang

Lặp lại qua các trang của hình ảnh DWF:

```csharp
foreach (var page in image.Pages)
{
    // Mã cho các bước tiếp theo sẽ có ở đây
}
```

## Bước 5: Nhận thông tin bố cục

Nhận thông tin bố cục từ mỗi trang:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Bước 6: Thiết lập tùy chọn JPG

Thiết lập tùy chọn lưu bố cục dưới dạng tệp JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Mã cho các bước tiếp theo sẽ có ở đây
}
```

## Bước 7: Xác định kích thước trang

Xác định kích thước của bố cục DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Mã cho các bước tiếp theo sẽ có ở đây
```

## Bước 8: Thiết lập kích thước trang

Thiết lập kích thước trang dựa trên loại đơn vị:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Bước 9: Lưu tệp JPG

Lưu tệp JPG với các tùy chọn được chỉ định:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Bây giờ bạn đã trích xuất thành công kích thước của bố cục DWF từ tệp DWG bằng Aspose.CAD trong C#. Vui lòng khám phá thêm các tính năng và chức năng mà Aspose.CAD cung cấp để phát triển .NET.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu quy trình làm việc với các tệp DWG trong C# bằng Aspose.CAD. Bằng cách làm theo các bước này, bạn không chỉ có thể nhận được kích thước của bố cục DWF mà còn có thể tận dụng các khả năng của Aspose.CAD cho các tác vụ khác nhau liên quan đến CAD trong các dự án .NET của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với các định dạng tệp DWG mới nhất không?

 Trả lời 1: Aspose.CAD hỗ trợ nhiều định dạng tệp DWG khác nhau, bao gồm cả các phiên bản mới nhất. Tham khảo đến[tài liệu](https://reference.aspose.com/cad/net/) để biết chi tiết tương thích cụ thể.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.CAD cho cả dự án thương mại và cá nhân không?

 Câu trả lời 2: Có, Aspose.CAD cung cấp các tùy chọn cấp phép linh hoạt cho cả mục đích sử dụng thương mại và cá nhân. Tham quan[trang mua hàng](https://purchase.aspose.com/buy) để biết thêm chi tiết.

### Câu 3: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD?

 A3: Bạn có thể nhận được giấy phép tạm thời từ[đây](https://purchase.aspose.com/temporary-license/) cho mục đích đánh giá.

### Câu hỏi 4: Tôi có thể tìm hỗ trợ cho Aspose.CAD ở đâu?

A4: Nếu có bất kỳ thắc mắc hoặc trợ giúp nào, hãy truy cập[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Câu hỏi 5: Aspose.CAD có bản dùng thử miễn phí không?

 Câu trả lời 5: Có, bạn có thể truy cập phiên bản dùng thử miễn phí của Aspose.CAD[đây](https://releases.aspose.com/).