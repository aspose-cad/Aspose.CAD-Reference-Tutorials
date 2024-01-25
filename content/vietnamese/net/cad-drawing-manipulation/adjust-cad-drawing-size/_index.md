---
title: Điều chỉnh kích thước bản vẽ CAD trong Aspose.CAD cho .NET
linktitle: Điều chỉnh kích thước bản vẽ CAD
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách dễ dàng điều chỉnh kích thước bản vẽ CAD trong .NET bằng Aspose.CAD. Hãy làm theo hướng dẫn từng bước của chúng tôi để thay đổi kích thước liền mạch.
type: docs
weight: 10
url: /vi/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Giới thiệu

Bạn đang tìm cách điều chỉnh liền mạch kích thước của bản vẽ CAD trong các ứng dụng .NET của mình? Aspose.CAD cho .NET cung cấp một giải pháp mạnh mẽ, cho phép bạn dễ dàng xử lý việc thay đổi kích thước bản vẽ CAD. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn thực hiện quy trình, chia nhỏ từng bước để đảm bảo bạn nắm bắt được sự phức tạp của việc thay đổi kích thước bản vẽ CAD bằng Aspose.CAD.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Aspose.CAD for .NET Library: Tải xuống và cài đặt thư viện từ[Trang tải xuống Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).
- Bản vẽ CAD mẫu: Đảm bảo bạn có tệp bản vẽ CAD mẫu (ví dụ: "sample.dwg") trong thư mục tài liệu của bạn.

## Nhập không gian tên

Bắt đầu bằng cách nhập các vùng tên cần thiết vào ứng dụng .NET của bạn. Bước này rất quan trọng để truy cập các chức năng do Aspose.CAD cung cấp cho .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải bản vẽ CAD

Bắt đầu bằng cách tải bản vẽ CAD vào một phiên bản của lớp Aspose.CAD.Image. Đảm bảo bạn có đường dẫn tệp chính xác cho bản vẽ mẫu của mình.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Tải bản vẽ CAD trong phiên bản của Hình ảnh
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Mã của bạn ở đây...
}
```

## Bước 2: Tạo BmpOptions

Tạo một thể hiện của lớp BmpOptions, lớp này chịu trách nhiệm chỉ định các tùy chọn khi lưu bản vẽ CAD dưới dạng tệp BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Bước 3: Đặt tùy chọn CadRasterization

Khởi tạo lớp CadRasterizationOptions và định cấu hình các thuộc tính của nó cho quá trình rasterization vector.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Bước 4: Đặt thuộc tính UnitType

Đặt thuộc tính UnitType của CadRasterizationOptions để chỉ định loại đơn vị cần thay đổi kích thước. Trong ví dụ này, nó được đặt thành Centimet.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Bước 5: Đặt thuộc tính bố cục

Chỉ định bố cục bạn muốn đưa vào bản vẽ đã thay đổi kích thước bằng cách đặt thuộc tính Bố cục.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Bước 6: Xuất sang BMP

Cuối cùng, lưu bố cục đã thay đổi kích thước dưới dạng tệp BMP bằng phương pháp Lưu.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Bây giờ bạn đã điều chỉnh thành công kích thước bản vẽ CAD của mình bằng Aspose.CAD cho .NET!

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã hướng dẫn quy trình thay đổi kích thước bản vẽ CAD trong .NET bằng Aspose.CAD. Bằng cách làm theo các bước này, bạn có thể tích hợp liền mạch chức năng này vào các ứng dụng của mình, mang lại trải nghiệm mượt mà cho người dùng.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD cho .NET có tương thích với tất cả các định dạng CAD không?

 Câu trả lời 1: Aspose.CAD cho .NET hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DWF, v.v. Kiểm tra[tài liệu](https://reference.aspose.com/cad/net/) để có danh sách đầy đủ.

### Câu hỏi 2: Tôi có thể thay đổi kích thước nhiều bố cục cùng một lúc không?

Câu trả lời 2: Có, bạn có thể thay đổi kích thước nhiều bố cục bằng cách điều chỉnh mảng bố cục trong CadRasterizationOptions.

### Câu hỏi 3: Tôi có thể nhận hỗ trợ cho Aspose.CAD cho .NET ở đâu?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và giúp đỡ.

### Q4: Có bản dùng thử miễn phí không?

 Đ4: Có, bạn có thể khám phá một[dùng thử miễn phí](https://releases.aspose.com/) để đánh giá các tính năng của Aspose.CAD cho .NET.

### Câu hỏi 5: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD cho .NET?

 A5: Xin giấy phép tạm thời cho mục đích thử nghiệm[đây](https://purchase.aspose.com/temporary-license/).