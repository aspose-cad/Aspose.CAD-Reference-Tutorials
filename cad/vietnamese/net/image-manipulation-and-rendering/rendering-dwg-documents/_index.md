---
title: Hiển thị tài liệu DWG trong C# - Hướng dẫn Aspose.CAD
linktitle: Hiển thị tài liệu DWG trong C#
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách hiển thị tài liệu DWG trong C# bằng Aspose.CAD. Hướng dẫn từng bước này bao gồm việc nhập, định cấu hình và lưu bằng các ví dụ về mã.
weight: 17
url: /vi/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hiển thị tài liệu DWG trong C# - Hướng dẫn Aspose.CAD

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện về cách hiển thị tài liệu DWG trong C# bằng Aspose.CAD. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu với .NET, hướng dẫn này sẽ hướng dẫn bạn quy trình tận dụng Aspose.CAD để hiển thị các tệp DWG một cách hiệu quả. Aspose.CAD là một API mạnh mẽ cung cấp các chức năng mạnh mẽ để làm việc với các định dạng tệp CAD, khiến nó trở thành lựa chọn phù hợp cho các nhà phát triển xử lý tệp DWG.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo rằng bạn có các điều kiện tiên quyết sau:

- Kiến thức cơ bản về ngôn ngữ lập trình C#.
- Visual Studio được cài đặt trên máy của bạn.
-  Thư viện Aspose.CAD được tích hợp vào dự án của bạn. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/cad/net/).
- Tệp DWG mẫu, chẳng hạn như "Bottom_plate.dwg," để làm theo cùng với các ví dụ.

## Nhập không gian tên

Để bắt đầu, hãy đảm bảo nhập các vùng tên cần thiết ở đầu mã C# của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Bây giờ, hãy chia ví dụ được cung cấp thành nhiều bước:

## Bước 1: Tải tệp DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Mã của bạn để tải tệp DWG có ở đây.
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Các cấu hình rasterization bổ sung có thể được thêm vào đây.
```

## Bước 3: Xác định vùng để vẽ

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Bước 4: Tạo một khung nhìn mới

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Bước 5: Thay thế Chế độ xem đang kích hoạt

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Bước 6: Định cấu hình tùy chọn PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 7: Lưu DWG được hiển thị dưới dạng PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã kết xuất thành công tài liệu DWG sang PDF bằng Aspose.CAD trong C#. Vui lòng khám phá thêm các tính năng và tùy chỉnh mã dựa trên yêu cầu cụ thể của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD với các định dạng tệp CAD khác không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF, DWF, v.v.

### Câu hỏi 2: Aspose.CAD có tương thích với .NET Core không?

Câu trả lời 2: Có, Aspose.CAD tương thích với cả .NET Framework và .NET Core.

### Câu hỏi 3: Làm cách nào tôi có thể xử lý các bố cục khác nhau trong tệp DWG?

 A3: Bạn có thể chỉ định bố cục mong muốn trong`Layouts` tài sản của`CadRasterizationOptions`.

### Câu hỏi 4: Có bất kỳ cân nhắc cấp phép nào khi sử dụng Aspose.CAD không?

 A4: Để biết chi tiết cấp phép, hãy truy cập[đây](https://purchase.aspose.com/buy).

### Câu hỏi 5: Tôi có thể tìm thêm hỗ trợ ở đâu?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
