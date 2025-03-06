---
title: Các phần tử DGN được hỗ trợ trong Aspose.CAD cho .NET
linktitle: Các phần tử DGN được hỗ trợ
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Khám phá Aspose.CAD để biết các tính năng mạnh mẽ của .NET để xử lý tệp DGN. Làm theo hướng dẫn từng bước của chúng tôi để làm việc liền mạch với các phần tử 2D và 3D.
weight: 18
url: /vi/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Các phần tử DGN được hỗ trợ trong Aspose.CAD cho .NET

## Giới thiệu

Bạn có phải là nhà phát triển .NET muốn làm việc liền mạch với các tệp DGN không? Aspose.CAD cho .NET cung cấp một giải pháp mạnh mẽ để xử lý các tệp DGN một cách hiệu quả. Trong hướng dẫn này, chúng tôi sẽ đi sâu vào các phần tử DGN được hỗ trợ, hướng dẫn bạn trong quá trình làm việc với Aspose.CAD cho .NET.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có những điều sau:

- Kiến thức cơ bản về lập trình .NET.
- Visual Studio được cài đặt trên máy của bạn.
-  Thư viện Aspose.CAD cho .NET mà bạn có thể tải xuống[đây](https://releases.aspose.com/cad/net/).

## Nhập không gian tên

Để khởi động dự án của bạn, hãy nhập các vùng tên cần thiết vào ứng dụng .NET của bạn. Bước này đảm bảo rằng bạn có quyền truy cập vào các chức năng do Aspose.CAD cung cấp cho .NET.

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

## Bước 1: Tải tệp DGN

Bắt đầu bằng cách tải tệp DGN hiện có dưới dạng CadImage trong ứng dụng .NET của bạn.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Mã của bạn ở đây
}
```

## Bước 2: Lặp lại các phần tử DGN

Lặp lại các phần tử DGN bằng vòng lặp foreach. Aspose.CAD cho .NET cung cấp nhiều loại phần tử DGN khác nhau mà bạn có thể làm việc cùng.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Mã của bạn ở đây
}
```

## Bước 3: Xử lý các thực thể được hỗ trợ trước đây

Xử lý các thực thể 2D được hỗ trợ trước đây, hiện cũng được hỗ trợ cho 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Các trường hợp bổ sung
        {
            // Mã của bạn ở đây
            break;
        }
}
```

## Bước 4: Xử lý các thực thể 3D được hỗ trợ

Xử lý các thực thể 3D được hỗ trợ do Aspose.CAD cung cấp cho .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Mã của bạn ở đây
            break;
        }
}
```

## Bước 5: Xuất và lưu

Cuối cùng, xuất tệp DGN đã sửa đổi sang hình ảnh raster và lưu nó vào thư mục đã chỉ định.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá các khả năng của Aspose.CAD dành cho .NET trong việc xử lý và thao tác các tệp DGN. Bằng cách làm theo hướng dẫn từng bước, bạn có thể làm việc hiệu quả với các phần tử DGN được hỗ trợ, cho dù chúng là thực thể 2D hay 3D. Aspose.CAD cho .NET cho phép bạn tích hợp liền mạch quá trình xử lý tệp DGN vào các ứng dụng .NET của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu về Aspose.CAD cho .NET ở đâu?

 A1: Bạn có thể tìm tài liệu[đây](https://reference.aspose.com/cad/net/).

### Câu hỏi 2: Làm cách nào để tải xuống Aspose.CAD cho .NET?

 A2: Bạn có thể tải xuống thư viện[đây](https://releases.aspose.com/cad/net/).

### Câu hỏi 3: Có bản dùng thử miễn phí Aspose.CAD cho .NET không?

 Câu trả lời 3: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD cho .NET ở đâu?

 A4: Giấy phép tạm thời có sẵn[đây](https://purchase.aspose.com/temporary-license/).

### Câu 5: Cần trợ giúp hoặc có thắc mắc?

 Câu trả lời 5: Truy cập cộng đồng Aspose.CAD cho .NET[diễn đàn hỗ trợ](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
