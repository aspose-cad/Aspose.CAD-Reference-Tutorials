---
date: 2026-04-06
description: Tìm hiểu cách chuyển đổi DWG sang PDF và thêm văn bản tùy chỉnh bằng
  C# và Aspose.CAD. Hướng dẫn từng bước này bao gồm việc tạo PDF từ DWG, chèn một
  thực thể văn bản và thay đổi phông chữ văn bản trong DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Thêm văn bản vào tệp DWG trong C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Chuyển đổi DWG sang PDF và Thêm Văn bản trong C# – Hướng dẫn Aspose.CAD
url: /vi/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển DWG sang PDF và Thêm Văn bản trong C# – Hướng dẫn Aspose.CAD

## Giới thiệu

Trong thế giới CAD và phát triển .NET đang phát triển nhanh, **chuyển DWG sang PDF** đồng thời chèn chú thích tùy chỉnh là một yêu cầu thường gặp. Cho dù bạn cần tạo bản vẽ có thể in cho khách hàng hoặc nhúng ghi chú động trực tiếp vào DWG, Aspose.CAD giúp công việc trở nên đơn giản. Trong hướng dẫn này, bạn sẽ học cách **chuyển DWG sang PDF**, **thêm một thực thể văn bản**, và thậm chí **thay đổi phông chữ văn bản DWG** bằng C#.

## Câu trả lời nhanh
- **Thư viện nào là tốt nhất cho việc chuyển DWG sang PDF?** Aspose.CAD for .NET  
- **Tôi có thể thêm văn bản tùy chỉnh khi chuyển đổi không?** Yes – create a `CadText` entity and add it before saving.  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** A commercial license is required; a free trial is available.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Có thể thay đổi phông chữ của văn bản không?** Yes, adjust the `CadText` properties such as `StyleType` and `TextHeight`.

## DWG chuyển sang PDF là gì?

Việc chuyển đổi tệp DWG sang PDF biến một bản vẽ CAD dựa trên vector thành tài liệu có thể chia sẻ rộng rãi, không phụ thuộc vào thiết bị. PDF giữ nguyên hình học và các lớp gốc, đồng thời cho phép bạn nhúng chú thích, văn bản hoặc siêu dữ liệu khác. Aspose.CAD tự động xử lý rasterization và render vector, vì vậy bạn không cần phần mềm CAD bên thứ ba trên máy chủ.

## Tại sao phải thêm văn bản vào DWG trước khi chuyển đổi?

Nhúng văn bản trực tiếp vào DWG cho phép bạn kiểm soát hoàn toàn vị trí, kiểu dáng và phân lớp. Khi tệp sau này được chuyển sang PDF, văn bản sẽ xuất hiện chính xác ở vị trí bạn đã đặt, bảo toàn ý định thiết kế và loại bỏ nhu cầu xử lý sau trong trình chỉnh sửa PDF.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Aspose.CAD Library** – download it from the [download link](https://releases.aspose.com/cad/net/).  
- **Môi trường .NET hoạt động** (Visual Studio 2022, .NET 6, hoặc bất kỳ phiên bản tương thích nào).  
- **Thư mục cho các tệp thử nghiệm của bạn** – chúng tôi sẽ gọi nó là `MyDir` trong toàn bộ hướng dẫn.

Bây giờ, hãy cùng đi qua quy trình từng bước.

## Nhập không gian tên

Thêm các câu lệnh `using` cần thiết để bạn có thể truy cập các lớp của Aspose.CAD.

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

Tải tệp DWG nguồn của bạn vào một đối tượng `Image`. Đối tượng này cho phép bạn truy cập các thực thể CAD bên dưới.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Bước 2: Tạo đối tượng CadText (Chèn thực thể Văn bản)

Lớp `CadText` đại diện cho một dòng văn bản trong DWG. Ở đây chúng ta thiết lập kiểu, giá trị, màu, lớp và vị trí. Điều chỉnh `StyleType` hoặc `TextHeight` để **thay đổi phông chữ văn bản DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Bước 3: Thêm thực thể Văn bản vào Model Space

Model space của DWG chứa hầu hết các thực thể vẽ. Bằng cách thêm `CadText` của chúng ta vào khối `*Model_Space`, văn bản sẽ trở thành một phần của bản vẽ.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Bước 4: Cấu hình tùy chọn PDF (Tạo PDF từ DWG)

Thiết lập các tùy chọn rasterization kiểm soát cách DWG được render thành PDF. Bạn có thể tinh chỉnh kích thước trang, kiểu vẽ và bố cục.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Bước 5: Lưu DWG đã chỉnh sửa dưới dạng PDF

Cuối cùng, xuất bản vẽ đã chỉnh sửa. PDF kết quả sẽ bao gồm văn bản mới được chèn.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Mẹo chuyên nghiệp:** Nếu bạn cần PDF có độ phân giải cao hơn, tăng `PageHeight` và `PageWidth` một cách tỷ lệ.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| Văn bản không hiển thị trong PDF | Lớp hoặc ID màu sai | Đảm bảo `LayerName` tồn tại và `ColorId` được đặt thành màu có thể nhìn thấy (ví dụ, 7 cho màu trắng). |
| Văn bản bị đặt sai vị trí | Tọa độ căn chỉnh không đúng | Xác minh giá trị `FirstAlignment.X/Y` tương đối với đơn vị của bản vẽ. |
| PDF trống | Chưa thiết lập tùy chọn rasterization | Đặt `DrawType` thành `UseObjectColor` hoặc `UseObjectLineWeight`. |

## Câu hỏi thường gặp (Hiện có)

### Q1: Aspose.CAD có tương thích với mọi phiên bản tệp DWG không?

A1: Aspose.CAD supports a wide range of DWG file versions, ensuring compatibility with various CAD software.

### Q2: Tôi có thể thêm nhiều thực thể văn bản vào một tệp DWG duy nhất bằng Aspose.CAD không?

A2: Yes, you can add multiple text entities to a DWG file by repeating the process outlined in the tutorial.

### Q3: Làm thế nào để thay đổi phông chữ và kiểu chữ của văn bản trong Aspose.CAD?

A3: To modify text font and style, adjust the properties of the `CadText` object before adding it to the DWG file.

### Q4: Có những lưu ý nào về giấy phép khi sử dụng Aspose.CAD trong dự án thương mại không?

A5: Yes, ensure compliance with Aspose.CAD licensing terms. Refer to [Aspose.CAD Purchase](https://purchase.aspose.com/buy) for details.

### Q5: Tôi có thể tìm kiếm trợ giúp hoặc thảo luận các câu hỏi liên quan đến Aspose.CAD ở đâu?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and get support.

## Câu hỏi bổ sung

**Q: Làm thế nào để tạo PDF từ DWG mà không thêm văn bản?**  
A: Skip the `CadText` creation step and directly configure `PdfOptions` before calling `image.Save(...)`.

**Q: Tôi có thể thay đổi màu văn bản bằng lập trình không?**  
A: Yes, set `cadText.ColorId` to a specific ACI color number (e.g., 1 for red).

**Q: Có thể chèn văn bản đa dòng không?**  
A: Use `CadMText` for multiline text blocks; the approach is similar to `CadText`.

**Q: Aspose.CAD có hỗ trợ chuyển đổi hàng loạt nhiều tệp DWG không?**  
A: Absolutely – loop through a directory of DWG files, apply the same steps, and save each as PDF.

## Kết luận

Bạn đã có một quy trình hoàn chỉnh, sẵn sàng cho môi trường sản xuất để **chuyển DWG sang PDF**, **thêm văn bản tùy chỉnh**, và **tùy chỉnh giao diện văn bản** bằng C# và Aspose.CAD. Kỹ thuật này lý tưởng cho việc tự động tạo bản vẽ, quy trình báo cáo, hoặc bất kỳ kịch bản nào mà bạn cần làm phong phú các tệp CAD một cách nhanh chóng.

---

**Cập nhật lần cuối:** 2026-04-06  
**Kiểm thử với:** Aspose.CAD 24.11 for .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}