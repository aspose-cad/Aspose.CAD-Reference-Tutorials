---
title: Chuyển đổi DWG sang PDF bằng tọa độ trong C# - Hướng dẫn Aspose.CAD
linktitle: Chuyển đổi DWG sang PDF bằng tọa độ trong C#
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách chuyển đổi DWG sang PDF với tọa độ cụ thể trong C# bằng Aspose.CAD. Hãy làm theo hướng dẫn từng bước của chúng tôi để chuyển đổi tệp CAD chính xác và hiệu quả.
weight: 11
url: /vi/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWG sang PDF bằng tọa độ trong C# - Hướng dẫn Aspose.CAD

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện này về cách chuyển đổi tệp DWG sang PDF với tọa độ được chỉ định bằng Aspose.CAD cho .NET. Aspose.CAD là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc liền mạch với các định dạng tệp CAD trong các ứng dụng .NET của họ. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình chuyển đổi tệp DWG sang PDF đồng thời cung cấp tọa độ cụ thể để nâng cao độ chính xác.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

- Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD cho .NET. Bạn có thể tìm thấy thư viện[đây](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Đảm bảo rằng bạn đã thiết lập môi trường phát triển tương thích, bao gồm Visual Studio hoặc bất kỳ IDE ưa thích nào khác.

- Tệp DWG: Chuẩn bị sẵn tệp DWG để chuyển đổi. Bạn có thể sử dụng tệp ví dụ được cung cấp hoặc tệp DWG tùy chỉnh của mình.

## Nhập không gian tên

Trong dự án C# của bạn, hãy nhập các không gian tên cần thiết:

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

Hãy chia nhỏ mã thành hướng dẫn từng bước để hiểu rõ hơn:

## Bước 1: Xác định thư mục tài liệu

```csharp
string MyDir = "Your Document Directory";
```

## Bước 2: Đặt đường dẫn tệp DWG nguồn

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Bước 3: Tải tệp DWG và định cấu hình các tùy chọn rasterization

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Bước 4: Xác định tọa độ và khung nhìn

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

## Bước 5: Áp dụng cài đặt khung nhìn

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

## Bước 6: Định cấu hình tùy chọn PDF và xuất

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Bước 7: Hiển thị thông báo thành công

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Phần kết luận

Chúc mừng! Bạn đã chuyển đổi thành công tệp DWG sang PDF với tọa độ được chỉ định bằng Aspose.CAD cho .NET. Hướng dẫn này bao gồm các bước thiết yếu và cung cấp hướng dẫn rõ ràng cho các nhà phát triển.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD với các định dạng tệp CAD khác không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF, DWF, v.v.

### Q2: Làm cách nào để xử lý lỗi trong quá trình chuyển đổi?

Câu trả lời 2: Triển khai cơ chế xử lý lỗi bằng cách sử dụng các khối thử bắt để nắm bắt và quản lý các ngoại lệ.

### Câu 3: Aspose.CAD có phù hợp với cả môi trường Windows và Linux không?

Câu trả lời 3: Có, Aspose.CAD tương thích với cả nền tảng Windows và Linux.

### Q4: Tôi có thể tùy chỉnh thêm đầu ra PDF không?

A4: Chắc chắn rồi! Khám phá các tùy chọn mở rộng do Aspose.CAD cung cấp để điều chỉnh đầu ra PDF theo yêu cầu cụ thể của bạn.

### Câu hỏi 5: Tôi có thể tìm thêm hỗ trợ hoặc thảo luận cộng đồng ở đâu?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
