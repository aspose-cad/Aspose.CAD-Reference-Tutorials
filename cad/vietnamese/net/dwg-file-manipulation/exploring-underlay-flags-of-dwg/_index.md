---
date: 2026-04-09
description: Tìm hiểu cách chuyển đổi DWG sang hình ảnh và cách đọc các cờ underlay
  bằng Aspose.CAD cho .NET trong hướng dẫn từng bước này.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Khám phá các cờ nền của tệp DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Chuyển đổi DWG sang hình ảnh – Khám phá các cờ Underlay của tệp DWG - Hướng
  dẫn Aspose.CAD
url: /vi/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Khám phá các cờ Underlay của tệp DWG - Hướng dẫn Aspose.CAD

## Giới thiệu

Nếu bạn đang khám phá thế giới phức tạp của các tệp CAD, cụ thể là tệp DWG, và muốn **chuyển đổi DWG sang hình ảnh** đồng thời khám phá **cách đọc các cờ underlay**, bạn đã đến đúng nơi. Hướng dẫn này sẽ dẫn bạn qua từng bước sử dụng thư viện mạnh mẽ Aspose.CAD cho .NET, giúp bạn trích xuất thông tin underlay và render bản vẽ thành hình ảnh một cách tự tin.

## Câu trả lời nhanh
- **“convert DWG to image” có nghĩa là gì?**  
  Nó có nghĩa là render một bản vẽ DWG thành định dạng raster (PNG, JPEG, v.v.) bằng Aspose.CAD.
- **Phương thức nào tiết lộ các cờ underlay?**  
  Truy cập thuộc tính `Flags` của đối tượng `CadUnderlay` sau khi tải DWG.
- **Tôi có cần giấy phép cho Aspose.CAD không?**  
  Một giấy phép tạm thời có sẵn để đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.
- **Các phiên bản .NET nào được hỗ trợ?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 và các phiên bản sau.
- **Tôi có thể trích xuất hình học underlay không?**  
  Có – đường dẫn underlay, điểm chèn, tỉ lệ, góc quay và trạng thái cờ đều có thể truy cập.

## “convert DWG to image” là gì và tại sao nó quan trọng?

Việc chuyển đổi tệp DWG sang hình ảnh cho phép bạn hiển thị bản vẽ CAD trong trình duyệt, nhúng chúng vào báo cáo, hoặc chia sẻ với các bên liên quan không có trình xem CAD. Khi render, bạn thường cần kiểm tra các đối tượng **underlay** (ví dụ: tham chiếu DGN) để đảm bảo chúng hiển thị đúng. Hiểu các cờ underlay giúp bạn khắc phục các vấn đề cắt, render đơn sắc và hiển thị trước khi tạo ra hình ảnh cuối cùng.

## Yêu cầu trước

- Kiến thức cơ bản về lập trình C# và .NET.  
- Thư viện **Aspose.CAD for .NET** đã được cài đặt. Nếu bạn chưa có, tải về **[tại đây](https://releases.aspose.com/cad/net/)**.  
- Một tệp DWG để thử nghiệm – tệp mẫu **“BlockRefDgn.dwg”** được sử dụng xuyên suốt hướng dẫn này.

## Nhập không gian tên

Để bắt đầu, nhập các không gian tên cần thiết:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DWG và Chuyển đổi sang `CadImage`

Đầu tiên, tải tệp DWG và ép kiểu nó thành một `CadImage`. Đối tượng này cho phép bạn truy cập tất cả các thực thể trong bản vẽ, bao gồm cả underlay.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Bước 2: Duyệt qua các thực thể

Tiếp theo, lặp qua mọi thực thể trong bản vẽ. Đây là nơi bạn sẽ tìm các đối tượng underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Bước 3: Kiểm tra Kiểu `CadDgnUnderlay`

Xác định các thực thể underlay bằng cách kiểm tra kiểu chạy thời gian thực của chúng. Lớp `CadDgnUnderlay` đại diện cho các underlay DGN được nhúng trong DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Bước 4: Truy cập các Cờ Underlay

Khi bạn có một `CadDgnUnderlay`, ép kiểu nó thành `CadUnderlay` để đọc các thuộc tính và trạng thái cờ. Các cờ cho biết underlay có hiển thị, bị cắt hay được render ở chế độ đơn sắc hay không.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Những gì đầu ra cho bạn biết

- **UnderlayPath / UnderlayName** – vị trí của tệp DGN bên ngoài.  
- **InsertionPoint (X, Y)** – tọa độ nơi underlay được đặt trong không gian DWG.  
- **RotationAngle** – góc quay được áp dụng cho underlay.  
- **ScaleX / ScaleY / ScaleZ** – hệ số tỉ lệ cho mỗi trục.  
- **Flags** – các giá trị boolean cho thấy trạng thái hiển thị (`UnderlayIsOn`), cắt (`ClippingIsOn`) và render đơn sắc (`Monochrome`).

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| Không có đầu ra cho kiểm tra cờ | Các cờ underlay mặc định là 0 khi underlay bị tắt. | Đảm bảo DWG thực sự chứa một underlay hoạt động hoặc bật lại tính năng hiển thị trong tệp CAD nguồn. |
| Ngoại lệ `Invalid cast` | Thực thể không phải là `CadDgnUnderlay`. | Kiểm tra điều kiện `if (entity is CadDgnUnderlay)` trước khi ép kiểu. |
| Render hình ảnh thất bại sau khi trích xuất cờ | Underlay có thể bị cắt hoặc tắt, dẫn đến khu vực trống. | Điều chỉnh các cờ (`UnderlayIsOn = true`, `ClippingIsOn = false`) trước khi render hình ảnh cuối cùng. |

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET với các định dạng tệp CAD khác không?

A1: Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DGN và nhiều hơn nữa. Kiểm tra tài liệu để biết danh sách đầy đủ.

### Câu hỏi 2: Có giấy phép tạm thời cho Aspose.CAD cho .NET không?

A2: Có, bạn có thể nhận giấy phép tạm thời **[tại đây](https://purchase.aspose.com/temporary-license/)**.

### Câu hỏi 3: Tôi có thể tìm hỗ trợ cho Aspose.CAD cho .NET ở đâu?

A3: Truy cập diễn đàn hỗ trợ **[tại đây](https://forum.aspose.com/c/cad/19)** để được trợ giúp.

### Câu hỏi 4: Làm thế nào để mua Aspose.CAD cho .NET?

A4: Mua thư viện **[tại đây](https://purchase.aspose.com/buy)**.

### Câu hỏi 5: Có bản dùng thử miễn phí không?

A5: Có, bạn có thể truy cập bản dùng thử miễn phí **[tại đây](https://releases.aspose.com/)**.

## Kết luận

Chúc mừng! Bạn đã học cách **chuyển đổi DWG sang hình ảnh** đồng thời nắm vững **cách đọc các cờ underlay** bằng Aspose.CAD cho .NET. Với kiến thức này, bạn có thể:

- Render bản vẽ DWG thành hình ảnh raster cho các kịch bản web hoặc báo cáo.  
- Kiểm tra và thao tác các thuộc tính underlay để đảm bảo hiển thị chính xác.  
- Gỡ lỗi các vấn đề về hiển thị, cắt và render đơn sắc trước khi tạo hình ảnh cuối cùng.

Hãy khám phá các tính năng khác của Aspose.CAD như quản lý lớp, trích xuất văn bản và chuyển đổi hàng loạt để mở rộng quy trình tự động hóa CAD của bạn.

---

**Cập nhật lần cuối:** 2026-04-09  
**Kiểm tra với:** Aspose.CAD for .NET 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}