---
title: Nhập hình ảnh vào tệp DWG bằng C# - Hướng dẫn Aspose.CAD
linktitle: Nhập hình ảnh vào tệp DWG bằng C#
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách nhập hình ảnh vào tệp DWG bằng C# với Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để tích hợp liền mạch.
type: docs
weight: 11
url: /vi/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## Giới thiệu

Trong lĩnh vực thiết kế có sự hỗ trợ của máy tính (CAD), việc kết hợp hình ảnh vào tệp DWG là một nhiệm vụ phổ biến và quan trọng. Aspose.CAD cho .NET cung cấp một bộ công cụ mạnh mẽ để hợp lý hóa quy trình này, giúp các nhà phát triển C# có thể truy cập được. Trong hướng dẫn này, chúng ta sẽ khám phá cách nhập hình ảnh vào tệp DWG theo từng bước.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

- Kiến thức cơ bản về lập trình C#.
-  Aspose.CAD cho .NET được cài đặt. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).
- Một môi trường phát triển được thiết lập.

## Nhập không gian tên

Đảm bảo bao gồm các không gian tên cần thiết trong dự án C# của bạn:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Bước 1: Thiết lập thư mục tài liệu của bạn

```csharp
string MyDir = "Your Document Directory";
```

## Bước 2: Tải tệp DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Bước 3: Xác định thuộc tính hình ảnh

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Bước 4: Đặt điểm chèn và vectơ

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Bước 5: Tạo và định cấu hình hình ảnh raster

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Bước 6: Thêm hình ảnh vào tệp DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Bước 7: Lưu dưới dạng PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Phần kết luận

Việc tích hợp hình ảnh vào tệp DWG bằng C# và Aspose.CAD cho .NET là một quy trình liền mạch, giúp các nhà phát triển có thể nâng cao các dự án CAD của họ bằng các yếu tố trực quan một cách dễ dàng.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET với các ngôn ngữ lập trình khác không?

Câu trả lời 1: Aspose.CAD được thiết kế chủ yếu cho .NET, nhưng Aspose cung cấp thư viện cho nhiều ngôn ngữ lập trình khác nhau.

### Câu hỏi 2: Aspose.CAD có bản dùng thử miễn phí cho .NET không?

 Câu trả lời 2: Có, bạn có thể khám phá bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Tôi có thể tìm tài liệu chi tiết về Aspose.CAD ở đâu?

 A3: Tài liệu có sẵn[đây](https://reference.aspose.com/cad/net/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD cho .NET?

 A4: Thăm quan[liên kết này](https://purchase.aspose.com/temporary-license/) để có được giấy phép tạm thời.

### Câu hỏi 5: Có diễn đàn cộng đồng nào hỗ trợ Aspose.CAD không?

 Câu trả lời 5: Có, bạn có thể tìm kiếm sự hỗ trợ và tương tác với cộng đồng[đây](https://forum.aspose.com/c/cad/19).