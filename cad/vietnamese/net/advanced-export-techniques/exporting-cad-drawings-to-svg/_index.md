---
date: 2026-03-07
description: Tìm hiểu cách xuất CAD sang SVG bằng Aspose.CAD cho .NET, tùy chỉnh màu
  SVG và chuyển đổi DWG sang SVG một cách hiệu quả.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Xuất CAD sang SVG – Xuất bản vẽ CAD sang định dạng SVG - Hướng dẫn Aspose.CAD
url: /vi/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất CAD sang SVG – Xuất Bản Vẽ CAD sang Định Dạng SVG

## Giới thiệu

Xuất bản vẽ CAD sang SVG là một yêu cầu phổ biến khi bạn cần đồ họa không phụ thuộc vào độ phân giải cho các trang web, báo cáo hoặc trực quan hoá tương tác. Trong hướng dẫn này, bạn sẽ học **cách xuất CAD sang SVG** với Aspose.CAD cho .NET, khám phá các tùy chọn để **tùy chỉnh màu SVG**, và xem cách **chuyển DWG sang SVG** (hoặc DXF sang SVG) chỉ trong vài dòng mã. Các bước nhanh gọn, API trực quan, và các tệp SVG tạo ra sẽ phóng to hoàn hảo trên bất kỳ thiết bị nào.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc chuyển đổi?** Aspose.CAD cho .NET.  
- **Tôi có thể thay đổi chế độ màu không?** Có – sử dụng `SvgColorMode` để đặt grayscale, đen‑trắng, hoặc full‑color.  
- **Các định dạng CAD nào được hỗ trợ?** DWG, DXF và nhiều định dạng khác (xem tài liệu Aspose.CAD).  
- **Tôi có cần giấy phép cho việc phát triển không?** Một giấy phép tạm thời có sẵn để thử nghiệm.  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho các bản vẽ tiêu chuẩn.

## “Xuất CAD sang SVG” là gì?
Xuất CAD sang SVG có nghĩa là lấy một tệp CAD gốc (như DWG hoặc DXF) và render nó thành định dạng Scalable Vector Graphics. SVG dựa trên XML, nhẹ, và có thể được style bằng CSS—làm cho nó trở nên lý tưởng cho các ứng dụng web và di động hiện đại.

## Tại sao nên sử dụng Aspose.CAD để xuất CAD sang SVG?
- **Không phụ thuộc bên ngoài** – API .NET thuần, không cần cài đặt AutoCAD.  
- **Kiểm soát chi tiết** – bạn có thể **tùy chỉnh màu SVG**, quyết định liệu văn bản có được giữ dưới dạng hình dạng hay không, và chọn các tùy chọn rasterization.  
- **Hỗ trợ đa định dạng** – cùng một đoạn mã hoạt động cho **chuyển DWG sang SVG**, **chuyển DXF sang SVG**, và các định dạng khác, giúp đơn giản hoá cơ sở mã của bạn.  
- **Hiệu năng cao** – được tối ưu cho tốc độ và sử dụng bộ nhớ thấp, phù hợp cho xử lý hàng loạt.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Aspose.CAD cho .NET** đã được cài đặt. Bạn có thể tải thư viện [tại đây](https://releases.aspose.com/cad/net/).  
- Môi trường phát triển .NET (Visual Studio, Rider, hoặc .NET CLI).  
- Một tệp CAD (DWG hoặc DXF) mà bạn muốn chuyển đổi.

## Nhập các Namespace

Đầu tiên, đưa các namespace cần thiết vào dự án của bạn để các lớp có thể được sử dụng.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Hướng dẫn từng bước

### Bước 1: Đặt Thư mục Tài liệu  
Xác định thư mục nơi tệp CAD nguồn của bạn nằm và nơi tệp SVG sẽ được lưu.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Bước 2: Tải Bản vẽ CAD  
Sử dụng `Image.Load` để đọc tệp DWG (hoặc DXF). Điều này hoạt động cho các kịch bản **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Bước 3: Cấu hình tùy chọn xuất SVG  
Điều chỉnh các cài đặt xuất để phù hợp với nhu cầu của bạn. Ở đây chúng ta đặt chế độ màu thành grayscale và buộc tất cả văn bản được render dưới dạng hình vector.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Bước 4: Lưu tệp SVG  
Cuối cùng, ghi tệp SVG ra đĩa. Bước này **lưu CAD dưới dạng SVG** và hoàn thành quá trình chuyển đổi.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Bằng cách làm theo bốn bước ngắn gọn này, bạn có thể **chuyển DWG sang SVG** (hoặc **chuyển DXF sang SVG**) với kiểm soát đầy đủ đối với giao diện đầu ra.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Kết quả SVG trống** | Đường dẫn tệp nguồn không đúng hoặc tệp bị hỏng. | Kiểm tra `MyDir` và đảm bảo tệp CAD mở mà không có lỗi. |
| **Màu sắc hiển thị sai** | `SvgColorMode` được đặt thành Grayscale một cách không cố ý. | Thay đổi `options.ColorType` thành `SvgColorMode.FullColor` để giữ nguyên màu gốc. |
| **Thiếu văn bản** | `TextAsShapes` được đặt thành `false` và trình xem không hỗ trợ phông chữ nhúng. | Giữ `TextAsShapes = true` hoặc nhúng phông chữ cần thiết vào SVG. |

## Câu hỏi thường gặp

### Q1: Aspose.CAD có tương thích với tất cả các định dạng CAD không?

A1: Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG và DXF, đảm bảo tính tương thích rộng rãi.

### Q2: Tôi có thể tùy chỉnh chế độ màu khi xuất sang SVG không?

A2: Có, Aspose.CAD cho phép bạn chọn chế độ màu, cung cấp sự linh hoạt trong đầu ra.

### Q3: Có giấy phép tạm thời để thử nghiệm không?

A3: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/) để đánh giá.

### Q4: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD ở đâu?

A4: Tài liệu có sẵn [tại đây](https://reference.aspose.com/cad/net/).

### Q5: Làm sao tôi có thể nhận hỗ trợ hoặc đặt câu hỏi liên quan đến Aspose.CAD?

A5: Truy cập diễn đàn cộng đồng [tại đây](https://forum.aspose.com/c/cad/19) để được hỗ trợ và thảo luận.

## Các câu hỏi thường gặp

**Q: Tôi có thể dùng đoạn mã này với .NET Core hoặc .NET 6 không?**  
A: Chắc chắn. Aspose.CAD cho .NET tương thích với .NET Framework, .NET Core và .NET 5/6+.

**Q: Có thể xuất chỉ một layout hoặc layer cụ thể không?**  
A: Có. Sử dụng `SvgOptions` để đặt `PageIndex` hoặc lọc các layer trước khi lưu.

**Q: Làm sao tôi nhúng các style CSS tùy chỉnh vào SVG đã tạo?**  
A: Sau khi lưu, bạn có thể xử lý hậu kỳ XML của SVG để chèn phần tử `<style>`, hoặc sử dụng `options.CustomCss` nếu phiên bản mới hỗ trợ.

**Q: Giới hạn kích thước cho tệp CAD nguồn là bao nhiêu?**  
A: Thư viện xử lý các tệp lớn, nhưng mức tiêu thụ bộ nhớ tăng theo độ phức tạp. Đối với các bản vẽ rất lớn, hãy cân nhắc xử lý từng trang riêng biệt.

**Q: Quá trình chuyển đổi có giữ nguyên độ dày và kiểu đường nét không?**  
A: Mặc định, độ dày đường nét được giữ nguyên. Bạn có thể điều chỉnh các tùy chọn render trong `SvgOptions` để kiểm soát chi tiết hơn.

---

**Cập nhật lần cuối:** 2026-03-07  
**Kiểm thử với:** Aspose.CAD cho .NET 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}