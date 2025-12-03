---
date: 2025-12-03
description: Tìm hiểu cách đặt kích thước trang PDF khi chuyển đổi DWG sang PDF và
  bật tính năng theo dõi trong các tệp DWG bằng Aspose.CAD cho Java – hướng dẫn toàn
  diện để xuất bản vẽ CAD sang PDF một cách chính xác.
language: vi
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Đặt kích thước trang PDF và bật theo dõi trong tệp DWG bằng Aspose.CAD trong
  Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kích Thước Trang PDF và Bật Theo Dõi trong Tệp DWG Sử Dụng Aspose.CAD trong Java

## Giới thiệu

Nếu bạn cần **set PDF page size** khi bạn *convert DWG to PDF* và cũng muốn theo dõi bất kỳ vấn đề render nào, Aspose.CAD for Java cung cấp cho bạn một cách sạch sẽ, lập trình để thực hiện cả hai. Trong tutorial này chúng ta sẽ đi qua các bước chính xác để cấu hình kích thước trang, bật theo dõi và xuất bản vẽ CAD ra PDF—tất cả từ Java. Khi kết thúc, bạn sẽ hiểu vì sao việc đặt kích thước trang đúng quan trọng đối với bản vẽ CAD và cách ghi lại thông tin theo dõi chi tiết trong quá trình xuất.

## Câu trả lời nhanh
- **What does “set PDF page size” affect?** Nó xác định chiều rộng và chiều cao của canvas PDF kết quả, đảm bảo bản vẽ của bạn vừa vặn hoàn hảo.  
- **Do I need a license to use this feature?** Bản trial hoạt động cho việc thử nghiệm; cần giấy phép thương mại cho môi trường sản xuất.  
- **Which Aspose.CAD version is required?** Bất kỳ phiên bản gần đây nào hỗ trợ `CadRasterizationOptions`.  
- **Can I use this with other CAD formats?** Ví dụ minh họa DWG/DXF, nhưng cùng cách tiếp cận hoạt động cho hầu hết các định dạng được hỗ trợ.  
- **How long does the conversion take?** Thông thường dưới một giây cho các tệp vừa; các bản vẽ lớn hơn có thể mất lâu hơn.

## “set PDF page size” là gì trong ngữ cảnh xuất CAD?
Đặt kích thước trang PDF cho renderer biết chính xác kích thước (theo pixel hoặc point) của canvas đầu ra. Điều này đặc biệt quan trọng đối với bản vẽ kỹ thuật, nơi tỷ lệ và bố cục phải được giữ nguyên. Nếu không có cài đặt kích thước trang rõ ràng, PDF có thể mặc định thành kích thước gây cắt hoặc biến dạng bản vẽ.

## Tại sao phải đặt kích thước trang PDF khi xuất bản vẽ CAD?
- **Preserve scale** – Kỹ sư dựa vào các bản in đúng tỷ lệ.  
- **Fit to paper** – Chọn A4, Letter, hoặc kích thước tùy chỉnh phù hợp với yêu cầu dự án.  
- **Improve readability** – Trang lớn hơn có thể hiển thị chi tiết mịn mà không cần phóng to.  
- **Consistent output** – Các pipeline tự động tạo PDF với kích thước giống hệt nhau mỗi lần chạy.

## Cách đặt kích thước trang PDF khi chuyển DWG sang PDF?
Dưới đây chúng ta sẽ cấu hình `CadRasterizationOptions` với các giá trị chiều rộng và chiều cao tùy chỉnh trước khi xuất. Bước này trực tiếp đáp ứng từ khóa chính **set PDF page size**.

## Yêu cầu trước

- **Java Development Kit (JDK)** – Java 8 hoặc mới hơn đã được cài đặt trên máy của bạn.  
- **Aspose.CAD for Java** – Tải về từ trang [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – Thư mục chứa các tệp DWG/DXF bạn muốn xử lý.

## Nhập các Namespace

Đầu tiên, nhập các lớp bạn sẽ cần. Khối mã không thay đổi so với tutorial gốc.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Bước 1: Tải tệp DWG/DXF

Tải bản vẽ nguồn của bạn. Điều chỉnh đường dẫn để trỏ tới tệp của bạn.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Bước 2: Cấu hình tùy chọn xuất PDF (bao gồm kích thước trang)

Ở đây chúng ta đặt chiều rộng và chiều cao trang—đây là nơi chúng ta **set PDF page size**. Các giá trị tính bằng pixel; bạn có thể chuyển đổi từ inch hoặc milimet tùy nhu cầu.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Nếu bạn muốn sử dụng các kích thước giấy tiêu chuẩn, hãy dùng phép chuyển đổi `1 inch = 72 points`. Đối với trang A4 (8.27 × 11.69 in), đặt `pageWidth = 595` và `pageHeight = 842`.

## Bước 3: Triển khai Theo dõi

Theo dõi ghi lại bất kỳ vấn đề render nào. Chúng ta gắn một handler tùy chỉnh sẽ được gọi sau khi xuất.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Bước 4: Xuất ra PDF

Bây giờ thực hiện chuyển đổi. PDF sẽ được tạo với kích thước bạn đã chỉ định, và bất kỳ thông tin theo dõi nào sẽ được in ra console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Bước 5: Lớp CadRenderHandler

Handler in ra bất kỳ lỗi nào xảy ra trong quá trình render. Điều này giúp bạn gỡ lỗi khi **exporting CAD drawing PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **Blank PDF** | Page size được đặt thành 0 hoặc quá nhỏ | Kiểm tra `setPageWidth` và `setPageHeight` có giá trị dương. |
| **Missing geometry** | Lỗi render được handler ghi lại | Xem lại đầu ra console từ `ErrorHandler` và xử lý `RenderCode` cụ thể. |
| **File not found** | Đường dẫn `dataDir` không đúng | Sử dụng đường dẫn tuyệt đối hoặc đảm bảo thư mục tồn tại. |
| **License exception** | Dùng trial mà không có giấy phép hợp lệ cho tệp lớn | Áp dụng giấy phép Aspose.CAD trước khi tải ảnh. |

## Câu hỏi thường gặp

**Q: Can I enable tracking for other CAD file formats using Aspose.CAD for Java?**  
A: Aspose.CAD chủ yếu hỗ trợ DWG/DXF cho việc theo dõi. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức.

**Q: How can I handle additional export options in Aspose.CAD for Java?**  
A: Thư viện cung cấp nhiều tùy chọn như DPI, màu nền và rasterization vector. Xem [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) để biết chi tiết.

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: Có, bạn có thể tải bản trial miễn phí từ [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q: Where can I seek assistance or discuss issues related to Aspose.CAD for Java?**  
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và câu trả lời chính thức.

**Q: How do I obtain a temporary license for Aspose.CAD for Java?**  
A: Thực hiện các bước được mô tả trên trang [Temporary License](https://purchase.aspose.com/temporary-license/).

**Last Updated:** 2025-12-03  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}