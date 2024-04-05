---
title: Thêm văn bản vào tệp DWG trong C# - Hướng dẫn Aspose.CAD
linktitle: Thêm văn bản vào tệp DWG trong C#
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách thêm văn bản vào tệp DWG bằng C# và Aspose.CAD. Hãy làm theo hướng dẫn từng bước này để tích hợp liền mạch. Khám phá tài liệu Aspose.CAD để được hướng dẫn toàn diện.
type: docs
weight: 14
url: /vi/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Giới thiệu

Trong lĩnh vực năng động của thiết kế có sự hỗ trợ của máy tính (CAD) và phát triển .NET, Aspose.CAD nổi bật như một công cụ mạnh mẽ để thao tác các tệp DWG. Thêm văn bản vào tệp DWG là một yêu cầu phổ biến và trong hướng dẫn này, chúng ta sẽ khám phá cách đạt được điều này bằng cách sử dụng C# và Aspose.CAD.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

-  Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD từ[Liên kết tải xuống](https://releases.aspose.com/cad/net/).

-  Thư mục Tài liệu: Thiết lập một thư mục cho tài liệu của bạn và ghi lại đường dẫn của nó như`MyDir`.

Bây giờ, hãy chia quy trình thành các bước có thể quản lý được.

## Nhập không gian tên

Trong mã C# của bạn, hãy bao gồm các vùng tên cần thiết để truy cập các chức năng của Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Bước 1: Tải tệp DWG

 Tải tệp DWG vào một`Image` đối tượng sử dụng thư viện Aspose.CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Mã của bạn cho các bước tiếp theo sẽ ở đây
}
```

## Bước 2: Tạo đối tượng CadText

 Khởi tạo một`CadText` đối tượng đại diện cho văn bản bạn muốn thêm vào tệp DWG.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Bước 3: Thêm văn bản vào DWG

 Thêm cái đã tạo`CadText` phản đối tệp DWG bằng Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Bước 4: Định cấu hình tùy chọn PDF

Định cấu hình các tùy chọn PDF để lưu tệp DWG đã sửa đổi dưới dạng PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Bước 5: Lưu dưới dạng PDF

Lưu tệp DWG đã sửa đổi dưới dạng PDF có văn bản được thêm vào.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Bây giờ, bạn đã thêm thành công văn bản vào tệp DWG bằng C# và Aspose.CAD. Vui lòng khám phá thêm các tính năng và chức năng của Aspose.CAD cho nhu cầu thao tác CAD của bạn.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã trình bày các bước cần thiết để thêm văn bản vào tệp DWG bằng C# và Aspose.CAD. Sự kết hợp mạnh mẽ này mở ra khả năng tạo tài liệu CAD động và tùy chỉnh.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các phiên bản của tệp DWG không?

Trả lời 1: Aspose.CAD hỗ trợ nhiều phiên bản tệp DWG, đảm bảo khả năng tương thích với nhiều phần mềm CAD khác nhau.

### Câu hỏi 2: Tôi có thể thêm nhiều thực thể văn bản vào một tệp DWG bằng Aspose.CAD không?

Câu trả lời 2: Có, bạn có thể thêm nhiều thực thể văn bản vào tệp DWG bằng cách lặp lại quy trình được nêu trong hướng dẫn.

### Câu 3: Làm cách nào để thay đổi phông chữ và kiểu văn bản trong Aspose.CAD?

 A3: Để sửa đổi phông chữ và kiểu văn bản, hãy điều chỉnh các thuộc tính của`CadText` đối tượng trước khi thêm nó vào tệp DWG.

### Câu hỏi 4: Có bất kỳ cân nhắc cấp phép nào khi sử dụng Aspose.CAD trong một dự án thương mại không?

 Câu trả lời 4: Có, đảm bảo tuân thủ các điều khoản cấp phép của Aspose.CAD. tham khảo[Mua Aspose.CAD](https://purchase.aspose.com/buy) để biết chi tiết.

### Câu hỏi 5: Tôi có thể tìm trợ giúp hoặc thảo luận các truy vấn liên quan đến Aspose.CAD ở đâu?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19)để kết nối với cộng đồng và nhận được sự hỗ trợ.