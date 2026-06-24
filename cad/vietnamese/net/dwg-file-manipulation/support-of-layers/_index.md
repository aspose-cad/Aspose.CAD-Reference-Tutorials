---
date: 2026-04-09
description: Tìm hiểu cách xuất các lớp DWG, chuyển đổi hình ảnh DWG và lưu DWG dưới
  dạng JPEG bằng C# với Aspose.CAD cho .NET. Hướng dẫn từng bước để thao tác tệp CAD
  hiệu quả.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Xử lý các lớp trong tệp DWG bằng C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Xuất các lớp DWG bằng C# – Hướng dẫn Aspose.CAD
url: /vi/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất các lớp DWG bằng C# – Hướng dẫn Aspose.CAD

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách xuất các lớp DWG** bằng C# và thư viện Aspose.CAD. Cho dù bạn cần **chuyển đổi định dạng ảnh DWG**, kiểm soát **tính hiển thị lớp DWG**, hoặc chỉ đơn giản **lưu tệp DWG JPEG**, các bước dưới đây sẽ chỉ cho bạn cách thực hiện một cách hiệu quả. Khi kết thúc hướng dẫn, bạn sẽ có một đoạn mã sẵn sàng chạy, tách một lớp cụ thể và render nó thành JPEG chất lượng cao.

## Câu trả lời nhanh
- **“export dwg layers” có nghĩa là gì?** Nó có nghĩa là raster hoá các lớp đã chọn của tệp DWG thành định dạng ảnh như JPEG hoặc PNG.  
- **Thư viện nào là tốt nhất cho nhiệm vụ này?** Aspose.CAD cho .NET cung cấp hỗ trợ đầy đủ mà không cần AutoCAD.  
- **Tôi có thể xuất nhiều lớp cùng lúc không?** Có – truyền một mảng tên lớp vào tùy chọn raster hoá.  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Cần giấy phép thương mại; bản dùng thử miễn phí có sẵn để đánh giá.  
- **Các định dạng đầu ra nào được hỗ trợ?** JPEG, PNG, BMP, TIFF và một số định dạng khác thông qua các lớp ImageOptions.

## Export dwg layers là gì?
Xuất các lớp DWG có nghĩa là lấy dữ liệu vector thuộc về một hoặc nhiều lớp trong bản vẽ DWG và raster hoá chúng thành ảnh bitmap. Điều này hữu ích khi bạn muốn chia sẻ một phần cụ thể của bản vẽ mà không tiết lộ toàn bộ tệp CAD.

## Tại sao cần kiểm soát tính hiển thị lớp DWG?
- Tạo các tài sản hình ảnh sạch sẽ cho bài thuyết trình hoặc tài liệu.  
- Giảm kích thước tệp bằng cách chỉ xuất geometry cần thiết.  
- Bảo vệ chi tiết thiết kế sở hữu bằng cách ẩn các lớp bí mật.  

## Yêu cầu trước

Trước khi chúng ta bắt đầu, hãy xác nhận rằng bạn đã có:

- Kiến thức cơ bản về ngôn ngữ lập trình C#.  
- Visual Studio đã được cài đặt trên máy của bạn.  
- Thư viện Aspose.CAD cho .NET, bạn có thể tải xuống từ [trang web Aspose.CAD](https://releases.aspose.com/cad/net/).

## Nhập không gian tên

Để bắt đầu, nhập các không gian tên cho phép bạn truy cập các tính năng raster hoá và xuất ảnh.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Bước 1: Tải tệp DWG

Tải tệp DWG (hoặc DWF) nguồn vào một đối tượng `Image`. Đối tượng này đại diện cho toàn bộ bản vẽ trong bộ nhớ.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Tại sao điều này quan trọng:* Việc tải tệp một lần cho phép bạn tái sử dụng cùng một thể hiện `image` cho bất kỳ số lượng xuất theo lớp nào, cải thiện hiệu năng.

## Bước 2: Cấu hình tùy chọn raster hoá

Tạo một thể hiện `CadRasterizationOptions` để chỉ cho Aspose.CAD cách render bản vẽ. Ở đây chúng ta đặt độ phân giải cao (1600 × 1600) để đảm bảo JPEG xuất ra sắc nét.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Bạn cũng có thể điều chỉnh màu nền, tỷ lệ độ dày đường, hoặc cài đặt khử răng cưa nếu cần.

## Bước 3: Chỉ định các lớp (DWG Layer Visibility)

Thêm các lớp mà bạn muốn **export dwg layers**. Trong ví dụ này chúng ta chỉ xuất “LayerA”. Để xuất nhiều lớp, chỉ cần liệt kê chúng trong mảng.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Mẹo chuyên nghiệp:* Sử dụng tên lớp chính xác như trong bản vẽ; tên lớp phân biệt chữ hoa và chữ thường.

## Bước 4: Cấu hình tùy chọn xuất ảnh

Chọn định dạng ảnh bạn muốn tạo. Chúng ta sẽ sử dụng `JpegOptions` vì JPEG cung cấp cân bằng tốt giữa chất lượng và kích thước tệp, lý tưởng khi bạn cần **save dwg jpeg** cho việc xem trước trên web.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Nếu bạn cần **convert dwg image** sang PNG hoặc TIFF, hãy thay `JpegOptions` bằng lớp tùy chọn tương ứng.

## Bước 5: Lưu ảnh đã xuất

Xác định đường dẫn tệp đầu ra và gọi `Save`. Engine raster hoá sẽ tôn trọng danh sách lớp bạn cung cấp, vì vậy chỉ “LayerA” xuất hiện trong JPEG cuối cùng.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Sau khi dòng này chạy, bạn sẽ thấy `for_layers_test.jpg` trong thư mục tài liệu của mình, chỉ chứa lớp đã chọn.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|------------|
| **Tên lớp không tồn tại** | Xác minh chính xác chính tả và chữ hoa/chữ thường của lớp trong DWG gốc. Sử dụng trình xem CAD để liệt kê tên các lớp. |
| **Ảnh đầu ra trống** | Đảm bảo tùy chọn raster hoá có nền không trong suốt và các lớp đã chọn thực sự chứa geometry. |
| **Đầu ra độ phân giải thấp** | Tăng `PageWidth` và `PageHeight` hoặc đặt `Resolution` trong `CadRasterizationOptions`. |
| **Phiên bản DWG không được hỗ trợ** | Cập nhật lên phiên bản Aspose.CAD mới nhất; nó thêm hỗ trợ cho các bản phát hành AutoCAD mới hơn. |

## Câu hỏi thường gặp

### Câu 1: Tôi có thể xử lý nhiều lớp đồng thời không?
A1: Có, bạn có thể. Chỉ cần thêm tên các lớp vào mảng `rasterizationOptions.Layers`.

### Câu 2: Có phiên bản dùng thử của Aspose.CAD không?
A2: Có, bạn có thể lấy phiên bản dùng thử miễn phí từ [tại đây](https://releases.aspose.com/).

### Câu 3: Tôi có thể tìm tài liệu ở đâu?
A3: Tài liệu có sẵn [tại đây](https://reference.aspose.com/cad/net/).

### Câu 4: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD?
A4: Bạn có thể tìm hỗ trợ trên [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Câu 5: Các tùy chọn cấp phép cho Aspose.CAD là gì?
A5: Bạn có thể khám phá các tùy chọn cấp phép và chi tiết mua hàng [tại đây](https://purchase.aspose.com/buy).

**Câu hỏi bổ sung**

**Q: Tôi có thể xuất bản vẽ sang PNG thay vì JPEG không?**  
A: Chắc chắn. Thay `JpegOptions` bằng `PngOptions` và điều chỉnh phần mở rộng tệp cho phù hợp.

**Q: Thư viện có giữ nguyên kiểu đường và màu không?**  
A: Có. Tất cả các thuộc tính vector đều được render chính xác trong quá trình raster hoá.

---

**Cập nhật lần cuối:** 2026-04-09  
**Kiểm tra với:** Aspose.CAD cho .NET (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}