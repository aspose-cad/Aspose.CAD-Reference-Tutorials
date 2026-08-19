---
date: 2026-03-19
description: Tìm hiểu cách thay đổi kích thước bản vẽ CAD trong .NET với Aspose.CAD,
  bao gồm cách thu phóng đơn vị bản vẽ CAD và điều chỉnh kích thước bố cục. Hãy theo
  dõi hướng dẫn từng bước của chúng tôi.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách thay đổi kích thước bản vẽ CAD bằng Aspose.CAD cho .NET
url: /vi/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thay đổi kích thước bản vẽ CAD với Aspose.CAD cho .NET

## Giới thiệu

Nếu bạn cần **cách thay đổi kích thước CAD** trực tiếp từ ứng dụng .NET của mình, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách thay đổi cài đặt đơn vị CAD, tỷ lệ các kích thước bản vẽ CAD, và điều chỉnh kích thước CAD một cách lập trình bằng Aspose.CAD cho .NET. Khi kết thúc, bạn sẽ có một giải pháp vững chắc, sẵn sàng cho môi trường sản xuất để thay đổi kích thước bất kỳ định dạng CAD nào được hỗ trợ.

## Câu trả lời nhanh
- **Thư viện nào cần thiết?** Aspose.CAD cho .NET  
- **Tôi có thể thay đổi loại đơn vị không?** Có – đặt `UnitType` trong `CadRasterizationOptions`  
- **Cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép Aspose.CAD hợp lệ cho việc sử dụng không phải thử nghiệm  
- **Định dạng ảnh mà ví dụ xuất ra là gì?** BMP (nhưng bất kỳ định dạng raster nào được hỗ trợ cũng hoạt động)  
- **Có bao nhiêu dòng mã?** Ít hơn 30 dòng cho một thao tác thay đổi kích thước hoàn chỉnh  

## Thực tế “cách thay đổi kích thước CAD” là gì?
Thay đổi kích thước một bản vẽ CAD có nghĩa là chuyển đổi dữ liệu vector thành ảnh raster ở một tỷ lệ hoặc đơn vị cụ thể (ví dụ: centimet, inch). Điều này hữu ích khi bạn cần nhúng bản vẽ vào báo cáo, tạo hình thu nhỏ, hoặc tích hợp hình ảnh CAD vào các trang web.

## Tại sao điều chỉnh kích thước CAD với Aspose.CAD?
- **Không cần phần mềm CAD bên ngoài** – mọi thứ chạy bên trong mã .NET của bạn.  
- **Kiểm soát chi tiết** đối với đơn vị, bố cục và các tùy chọn raster hóa.  
- **Hỗ trợ đa định dạng** – cùng một đoạn mã hoạt động cho DWG, DXF, DWF và nhiều định dạng khác.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- Thư viện Aspose.CAD cho .NET: Tải xuống và cài đặt thư viện từ [trang tải Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).  
- Bản vẽ CAD mẫu: Một tệp như `sample.dwg` được đặt trong thư mục tài liệu của dự án.  

## Nhập không gian tên

Đầu tiên, nhập các không gian tên cho phép bạn truy cập các lớp của Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải bản vẽ CAD

Tải tệp nguồn vào một đối tượng `Image`. Đối tượng này đại diện cho bản vẽ CAD trong bộ nhớ và sẽ là cơ sở cho mọi thao tác tiếp theo.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Bước 2: Tạo BmpOptions (hoặc bất kỳ định dạng raster nào khác)

`BmpOptions` cho Aspose.CAD biết cách render dữ liệu vector khi bạn lưu nó dưới dạng bitmap. Bạn có thể thay thế bằng `PngOptions`, `JpegOptions`, v.v., tùy thuộc vào định dạng mục tiêu.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Bước 3: Đặt CadRasterizationOptions

`CadRasterizationOptions` chứa các cài đặt cốt lõi cho việc tỷ lệ, chuyển đổi đơn vị và lựa chọn bố cục. Liên kết nó với thuộc tính `VectorRasterizationOptions` của `BmpOptions` đảm bảo rasterizer sử dụng các cài đặt tùy chỉnh của bạn.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Bước 4: Đặt UnitType (thay đổi đơn vị CAD)

Ở đây chúng ta thay đổi đơn vị CAD từ mặc định sang centimet. Đây là nơi từ khóa **change cad unit** xuất hiện, và nó ảnh hưởng trực tiếp đến kích thước ảnh cuối cùng.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Bước 5: Chọn Layouts (đặt bố cục CAD)

Nếu bản vẽ của bạn chứa nhiều bố cục (ví dụ: Model, Sheet1), hãy chỉ định những bố cục nào bạn muốn raster hóa. Việc chọn đúng bố cục là rất quan trọng khi bạn **set cad layouts** cho đầu ra đã thay đổi kích thước.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Bước 6: Xuất ra BMP (thay đổi kích thước bản vẽ CAD)

Cuối cùng, lưu ảnh đã raster hóa. Tệp đầu ra phản ánh kích thước, đơn vị và bố cục mới mà bạn đã cấu hình—hiệu quả hoàn thành thao tác **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Bây giờ bạn có một tệp BMP đại diện cho bản vẽ CAD đã thay đổi kích thước, sẵn sàng cho các xử lý hoặc hiển thị tiếp theo.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| Ảnh đầu ra mờ | DPI (dots per inch) mặc định quá thấp | Đặt `cadRasterizationOptions.Resolution = 300;` trước khi lưu |
| Bố cục sai | Tên bố cục bị lỗi chính tả | Kiểm tra tên bố cục chính xác bằng trình xem CAD hoặc bộ sưu tập `Layouts` |
| Chuyển đổi đơn vị không đúng | Trộn lẫn đơn vị mét và inch | Đảm bảo `UnitType` khớp với hệ đo mong muốn |

## Câu hỏi thường gặp

### Q1: Aspose.CAD cho .NET có tương thích với tất cả các định dạng CAD không?

A1: Aspose.CAD cho .NET hỗ trợ một loạt các định dạng CAD, bao gồm DWG, DXF, DWF và nhiều hơn nữa. Kiểm tra [tài liệu](https://reference.aspose.com/cad/net/) để biết danh sách đầy đủ.

### Q2: Tôi có thể thay đổi kích thước nhiều bố cục cùng lúc không?

A2: Có, bạn có thể thay đổi kích thước nhiều bố cục bằng cách điều chỉnh mảng `Layouts` trong `CadRasterizationOptions`.

### Q3: Tôi có thể nhận hỗ trợ cho Aspose.CAD cho .NET ở đâu?

A3: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và trợ giúp.

### Q4: Có bản dùng thử miễn phí không?

A4: Có, bạn có thể khám phá một [bản dùng thử miễn phí](https://releases.aspose.com/) để đánh giá các tính năng của Aspose.CAD cho .NET.

### Q5: Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho .NET?

A5: Nhận giấy phép tạm thời cho mục đích thử nghiệm [tại đây](https://purchase.aspose.com/temporary-license/).

## Các câu hỏi thường gặp khác

**Hỏi: Làm sao tôi có thể phóng to một bản vẽ CAD mà không thay đổi loại đơn vị?**  
Đáp: Điều chỉnh thuộc tính `Zoom` của `CadRasterizationOptions` (ví dụ: `cadRasterizationOptions.Zoom = 2.0;`) để gấp đôi kích thước trong khi giữ nguyên đơn vị gốc.

**Hỏi: Tôi có thể xuất ra các định dạng khác ngoài BMP không?**  
Đáp: Chắc chắn. Thay thế `BmpOptions` bằng `PngOptions`, `JpegOptions`, hoặc bất kỳ lớp định dạng raster nào khác được hỗ trợ.

**Hỏi: Có thể xử lý hàng loạt một thư mục các bản vẽ không?**  
Đáp: Có. Duyệt qua các tệp trong thư mục, áp dụng cùng logic raster hóa và lưu mỗi đầu ra với tên duy nhất.

---

**Cập nhật lần cuối:** 2026-03-19  
**Kiểm tra với:** Aspose.CAD cho .NET 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}