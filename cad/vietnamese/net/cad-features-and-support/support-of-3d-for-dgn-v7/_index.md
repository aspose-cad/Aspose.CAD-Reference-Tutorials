---
date: 2026-03-29
description: Tìm hiểu cách cấu hình các tùy chọn raster hóa CAD và xuất DGN sang PDF
  với hỗ trợ 3D bằng Aspose.CAD cho .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cấu hình các tùy chọn raster hóa CAD cho DGN V7 3D
url: /vi/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cấu hình tùy chọn raster hóa CAD cho DGN V7 3D

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách cấu hình tùy chọn raster hóa CAD** để xuất tệp DGN V7 3‑D sang PDF bằng Aspose.CAD cho .NET. Dù bạn đang xây dựng một trình xem CAD, một công cụ báo cáo, hay một quy trình chuyển đổi tự động, việc nắm vững các cài đặt này sẽ cho phép bạn kiểm soát chính xác kích thước trang, tỷ lệ bố cục, màu nền và các góc nhìn cụ thể mà bạn muốn render. Hãy cùng đi qua quy trình từng bước.

## Câu trả lời nhanh
- **Câu hỏi: “configure CAD rasterization options” có nghĩa là gì?**  
  Nó đề cập đến việc thiết lập các thuộc tính như kích thước trang, tỷ lệ, màu nền và lựa chọn bố cục trước khi chuyển đổi tệp CAD sang định dạng raster (ví dụ: PDF).
- **Cách xuất DGN sang PDF với hỗ trợ 3‑D?**  
  Tải DGN bằng `DgnImage`, định nghĩa `PdfOptions` + `CadRasterizationOptions`, sau đó gọi `Save`.
- **Có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?**  
  Có – cần giấy phép thương mại để triển khai; bản dùng thử miễn phí có sẵn.
- **Các phiên bản .NET nào được hỗ trợ?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Có thể chọn các góc nhìn cụ thể để xuất không?**  
  Chắc chắn – đặt mảng `Layouts` trong tùy chọn raster hóa.

## “configure CAD rasterization options” là gì?

Cấu hình tùy chọn raster hóa CAD có nghĩa là tùy chỉnh cách một bản vẽ CAD được raster hóa (chuyển từ vector sang bitmap hoặc PDF). Bằng cách điều chỉnh các cài đặt này, bạn kiểm soát đầu ra hình ảnh, hiệu năng và kích thước tệp của tài liệu kết quả.

## Tại sao nên sử dụng Aspose.CAD để xuất DGN V7 3‑D?

- **Full .NET integration** – không cần COM hoặc DLL gốc.  
- **Supports 3‑D geometry** – giữ lại thông tin độ sâu khi render sang PDF.  
- **Fine‑grained control** – chọn chính xác bố cục, tỷ lệ và màu nền.  
- **Cross‑platform** – hoạt động trên Windows, Linux và macOS với .NET Core.

## Yêu cầu trước

- **Aspose.CAD for .NET** – tải về từ [tại đây](https://releases.aspose.com/cad/net/).  
- **Visual Studio** hoặc bất kỳ IDE .NET nào tương thích.  
- **A sample DGN file** – trong hướng dẫn này chúng ta sẽ dùng `Nikon_D90_Camera.dgn` (được bao gồm trong gói mẫu Aspose).  

Bây giờ mọi thứ đã sẵn sàng, hãy bắt đầu với mã.

## Nhập không gian tên

Trong dự án .NET của bạn, nhập các không gian tên cần thiết:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Bước 1: Thiết lập thư mục tài liệu của bạn

Tạo một biến trỏ tới thư mục chứa DGN nguồn và các tệp đầu ra.

```csharp
string MyDir = "Your Document Directory";
```

## Bước 2: Tải tệp DGN

Tải tệp DGN dưới dạng `DgnImage`. Đối tượng này cung cấp quyền truy cập vào dữ liệu CAD và quy trình raster hóa.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Bước 3: Cấu hình tùy chọn xuất PDF (Configure CAD Rasterization Options)

Ở đây chúng ta **cấu hình tùy chọn raster hóa CAD** để quyết định cách mô hình 3‑D được render sang PDF. Bạn có thể điều chỉnh kích thước trang, bật tự động tỷ lệ bố cục, đặt màu nền và chọn các bố cục (góc nhìn) cụ thể để xuất.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Bước 4: Lưu ảnh raster

Cuối cùng, xuất DGN sang tệp PDF bằng các tùy chọn vừa cấu hình.

```csharp
dgnImage.Save(outFile, options);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Blank PDF output** | Xác minh rằng mảng `Layouts` chứa các định danh góc nhìn đúng có trong tệp DGN. |
| **Incorrect colors** | Đảm bảo `BackgroundColor` được đặt giá trị mong muốn; sử dụng `Color.White` cho nền sáng. |
| **Performance bottleneck on large files** | Bật `AutomaticLayoutsScaling` và cân nhắc giảm `PageWidth/PageHeight` để giảm độ phân giải raster. |
| **License exception** | Cài đặt giấy phép Aspose.CAD hợp lệ trước khi tải ảnh để tránh dấu nước bản dùng thử. |

## Câu hỏi thường gặp

**Q: Có thể sử dụng Aspose.CAD cho .NET với các định dạng tệp CAD khác không?**  
A: Có, Aspose.CAD hỗ trợ DWG, DXF, DWF, DGN và nhiều định dạng khác.

**Q: Làm sao xử lý ngoại lệ khi làm việc với Aspose.CAD?**  
A: Bao quanh mã bằng khối `try‑catch` và kiểm tra `Aspose.CAD.CADException` để có thông tin chi tiết về lỗi.

**Q: Aspose.CAD có phù hợp cho dự án thương mại không?**  
A: Chắc chắn. Bạn có thể mua giấy phép [tại đây](https://purchase.aspose.com/buy).

**Q: Có thể dùng thử Aspose.CAD cho .NET trước khi mua không?**  
A: Có, bản dùng thử miễn phí có sẵn [tại đây](https://releases.aspose.com/).

**Q: Tôi có thể tìm hỗ trợ cộng đồng cho Aspose.CAD ở đâu?**  
A: Tham gia diễn đàn thảo luận [tại đây](https://forum.aspose.com/c/cad/19).

---

**Cập nhật lần cuối:** 2026-03-29  
**Kiểm tra với:** Aspose.CAD 24.11 for .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}