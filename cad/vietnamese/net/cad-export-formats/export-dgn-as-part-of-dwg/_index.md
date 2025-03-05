---
title: Xuất DGN dưới dạng một phần của DWG trong Aspose.CAD cho .NET
linktitle: Xuất DGN dưới dạng một phần của DWG
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách xuất DGN như một phần của DWG trong Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để tích hợp liền mạch.
type: docs
weight: 11
url: /vi/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Giới thiệu

Trong thế giới phát triển .NET, Aspose.CAD nổi bật như một thư viện mạnh mẽ để làm việc với các tệp Thiết kế hỗ trợ máy tính (CAD). Hướng dẫn này sẽ hướng dẫn bạn quy trình xuất tệp DGN (Thiết kế) như một phần của tệp DWG (Bản vẽ) bằng Aspose.CAD cho .NET. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn từng bước này sẽ giúp bạn khai thác các khả năng của Aspose.CAD để đạt được nhiệm vụ cụ thể này một cách hiệu quả.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD cho .NET. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Thiết lập môi trường phát triển .NET ưa thích của bạn, chẳng hạn như Visual Studio.

- Kiến thức cơ bản về C#: Làm quen với ngôn ngữ lập trình C#.

## Nhập không gian tên

Trong dự án C# của bạn, hãy bao gồm các vùng tên cần thiết để truy cập chức năng Aspose.CAD. Thêm các lệnh sử dụng sau vào đầu tệp mã của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Bây giờ, hãy chia mã được cung cấp thành nhiều bước:

## Bước 1: Xác định đường dẫn tệp

```csharp
//Đường dẫn tập tin đầu vào và đầu ra
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Bước 2: Tạo phiên bản PdfOptions

```csharp
// Tạo một phiên bản của lớp PdfOptions để xuất DWG sang PDF
PdfOptions exportOptions = new PdfOptions();
```

## Bước 3: Tải tệp DWG

```csharp
// Tải tệp DWG hiện có dưới dạng hình ảnh và chuyển đổi nó thành loại CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Bước 4: Lặp lại các thực thể

```csharp
// Lặp lại qua từng thực thể bên trong tệp DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Bước 5: Kiểm tra loại thực thể

```csharp
// Kiểm tra xem thực thể có phải là định nghĩa hình ảnh không
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Bước 6: Nhận đường dẫn lớp lót

```csharp
// Nếu đó là định nghĩa hình ảnh, hãy lấy tham chiếu bên ngoài đến đối tượng
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Bước 7: Xác định các tùy chọn rasterization

```csharp
// Xác định cài đặt cho đối tượng CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Bước 8: Xuất DWG sang PDF

```csharp
// Xuất DWG sang PDF bằng cách gọi phương thức Lưu
cadImage.Save(outPath, exportOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã thực hiện thành công quá trình xuất tệp DGN dưới dạng một phần của tệp DWG bằng Aspose.CAD cho .NET. Hướng dẫn này đã cung cấp cho bạn các bước cơ bản và đoạn mã để hoàn thành nhiệm vụ cụ thể này một cách liền mạch.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET trong các dự án thương mại của mình không?
 A1: Có, bạn có thể. Thăm nom[đây](https://purchase.aspose.com/buy) để khám phá các lựa chọn cấp phép.

### Câu hỏi 2: Có bất kỳ hạn chế nào về kích thước của tệp DWG mà tôi có thể xử lý không?
Câu trả lời 2: Aspose.CAD hỗ trợ xử lý các tệp DWG lớn nhưng có thể áp dụng các giới hạn về phần cứng.

### Câu 3: Có phiên bản dùng thử không?
A3: Có, bạn có thể dùng thử miễn phí[đây](https://releases.aspose.com/).

### Q4: Làm thế nào tôi có thể nhận được giấy phép tạm thời?
 A4: Có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể tìm kiếm sự hỗ trợ ở đâu nếu gặp vấn đề?
 Câu trả lời 5: Bạn có thể truy cập diễn đàn Aspose.CAD[đây](https://forum.aspose.com/c/cad/19) để hỗ trợ.