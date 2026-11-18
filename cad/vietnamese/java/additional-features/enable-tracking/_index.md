---
date: 2026-11-18
description: Tìm hiểu cách xuất DWG sang PDF, bật theo dõi và sử dụng lớp Java xử
  lý lỗi tùy chỉnh với Aspose.CAD cho Java. Bao gồm chuyển đổi DXF sang PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Bật Theo dõi trong Tệp DWG bằng Java
og_description: Xuất DWG sang PDF và bật theo dõi đầy đủ trong Java với Aspose.CAD.
  Tìm hiểu cách sử dụng trình xử lý lỗi tùy chỉnh, chuyển đổi DXF sang PDF và ghi
  lại các cảnh báo render.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Xuất DWG sang PDF với tính năng theo dõi bằng Aspose.CAD cho Java
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: Xuất DWG sang PDF và Bật Theo dõi với Aspose.CAD Java
url: /vi/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG sang PDF và bật theo dõi với Aspose.CAD Java

## Giới thiệu

Việc xuất DWG sang PDF đồng thời duy trì khả năng quan sát đầy đủ quá trình chuyển đổi là điều cần thiết cho các đội ngũ tập trung vào CAD hiện đại. Trong hướng dẫn này, bạn sẽ khám phá **cách bật theo dõi** trong quy trình DWG, chuyển đổi DXF sang PDF trong cùng một pipeline, và ghi lại mọi cảnh báo khi render bằng lớp **custom error handler Java**. Khi kết thúc, bạn sẽ có một đoạn mã sẵn sàng cho sản xuất, không chỉ tạo ra các PDF chất lượng cao mà còn ghi lại thông tin chẩn đoán để kiểm tra và khắc phục.

## Câu trả lời nhanh
- **Công việc của “enable dwg tracking java” là gì?** Nó kích hoạt các callback render của Aspose.CAD để bạn có thể thấy cảnh báo và lỗi trong quá trình xuất.  
- **Tôi có cần giấy phép không?** Bản dùng thử hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể cũng chuyển đổi DXF sang PDF không?** Có – cùng một đối tượng `PdfOptions` được dùng cho DWG cũng hoạt động cho DXF, bao phủ kịch bản *java convert dxf pdf*.  
- **Yêu cầu phiên bản JDK nào?** Java 8 hoặc cao hơn.  
- **Tôi có thể tìm thêm ví dụ ở đâu?** Xem [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) được liên kết bên dưới.

## Export DWG sang PDF là gì?

Export DWG to PDF là quá trình chuyển đổi bản vẽ AutoCAD gốc (DWG) thành tài liệu PDF di động trong khi giữ nguyên độ chính xác vector, các lớp và chú thích. **Aspose.CAD chuyển đổi DWG sang PDF bằng Java thuần, vì vậy bạn không bao giờ cần cài đặt AutoCAD có giấy phép.** Việc chuyển đổi này giữ nguyên trọng lượng đường, kiểu chữ và hình học bố cục, làm cho PDF phù hợp cho việc xem xét của khách hàng, lưu trữ hoặc xử lý tiếp theo.

## Tại sao nên dùng Aspose.CAD cho Java?

Aspose.CAD cho Java cung cấp một giải pháp toàn diện, thuần Java cho việc chuyển đổi CAD, hỗ trợ hơn 50 định dạng, mang lại hiệu suất cao và cung cấp tính năng theo dõi tích hợp thông qua các callback render. Nó không yêu cầu phụ thuộc bên ngoài và có thể được tích hợp vào các pipeline phía máy chủ. Thư viện còn bao gồm xử lý tiết kiệm bộ nhớ, cho phép chuyển đổi các tệp lên tới 500 trang mà không cần tải toàn bộ tài liệu vào RAM.

## Yêu cầu trước

- **Java Development Kit (JDK)** 8 hoặc mới hơn được cài đặt trên máy của bạn.  
- **Aspose.CAD for Java** tải xuống từ [download link](https://releases.aspose.com/cad/java/) chính thức.  
- **Aspose.CAD Free Trial** có thể lấy từ trang [Aspose.CAD Free Trial](https://releases.aspose.com/) nếu bạn cần đánh giá nhanh.  
- Một thư mục chứa các tệp DWG/DXF bạn muốn chuyển đổi.  

## Cách xuất DWG sang PDF?

Tải tệp nguồn của bạn, cấu hình `PdfOptions`, gắn một `CadRenderHandler` tùy chỉnh, và gọi `save`. Quy trình end‑to‑end này chuyển đổi DWG (hoặc DXF) sang PDF đồng thời phát ra thông tin theo dõi cho mỗi bước render, đảm bảo mọi cảnh báo hoặc lỗi được ghi lại và có thể được xử lý bởi các nhà phát triển hoặc quy trình tự động.

## Nhập không gian tên

Giao diện `CadRenderHandler` nhận các chẩn đoán render như cảnh báo và lỗi trong quá trình chuyển đổi.  
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

## Bước 1: tải tệp dwg/dxf  

`CadImage` đại diện cho một bản vẽ CAD được tải vào bộ nhớ và cung cấp quyền truy cập vào các trang và lớp của nó.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Bước 2: cấu hình tùy chọn xuất pdf (cách chuyển đổi dxf sang pdf)

`PdfOptions` định nghĩa các cài đặt đầu ra PDF, trong khi `VectorRasterizationOptions` kiểm soát các tham số rasterization như DPI và màu nền.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Bước 3: triển khai theo dõi (custom error handler java)

`ErrorHandler` mở rộng `CadRenderHandler` để bắt và ghi lại các thông điệp render được phát ra trong quá trình chuyển đổi.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Bước 4: xuất sang pdf  

Gọi phương thức `save` trên đối tượng `CadImage` sẽ ghi PDF đã render vào đường dẫn đầu ra đã chỉ định.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Bước 5: lớp cadrenderhandler  

`CadRenderHandler` là lớp callback cơ bản nhận một `RenderResult` chứa các thông điệp chi tiết sau khi render hoàn tất.  
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

## Tại sao điều này quan trọng

Bật theo dõi tạo ra một chuỗi kiểm toán đáp ứng các yêu cầu tuân thủ trong các lĩnh vực được quy định như kiến trúc, kỹ thuật và xây dựng. Lớp error handler tùy chỉnh cũng cho phép bạn tích hợp kiểm tra sức khỏe chuyển đổi CAD vào các pipeline CI/CD, tự động đánh dấu các tệp cần xem xét thủ công.

## Các vấn đề thường gặp và giải pháp

- **`NullPointerException` trên `RenderResult`** – Đảm bảo bạn đang sử dụng Aspose.CAD 23.10 hoặc mới hơn; các phiên bản trước thiếu API `RenderResult`.  
- **File not found** – Kiểm tra lại rằng `dataDir` trỏ tới thư mục đúng và tên tệp khớp chính xác về chữ hoa/thường.  
- **Missing tracking output** – Xác nhận rằng thể hiện `ErrorHandler` của bạn đã được gán đúng cho `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Câu hỏi thường gặp

**Q:** Tôi có thể bật theo dõi cho các định dạng tệp CAD khác bằng Aspose.CAD cho Java không?  
**A:** Theo dõi chủ yếu được cung cấp cho DWG và DXF. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức để xem API nào cung cấp callback render.  

**Q:** Làm thế nào tôi có thể tùy chỉnh các tùy chọn xuất bổ sung, chẳng hạn đặt siêu dữ liệu PDF?  
**A:** `PdfOptions` cung cấp các thuộc tính như `setTitle`, `setAuthor`, và `setSubject`. Đặt chúng trước khi gọi `save` để nhúng siêu dữ liệu vào PDF kết quả.  

**Q:** Phiên bản dùng thử có đủ để đánh giá các tính năng theo dõi không?  
**A:** Có, bản dùng thử miễn phí bao gồm toàn bộ quyền truy cập API, cho phép bạn thử nghiệm `CadRenderHandler` và xuất PDF mà không bị hạn chế.  

**Q:** Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD cho Java ở đâu?  
**A:** Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để đặt câu hỏi và chia sẻ kinh nghiệm với các nhà phát triển khác.  

**Q:** Làm thế nào tôi có thể lấy giấy phép tạm thời cho môi trường kiểm thử tự động?  
**A:** Thực hiện các bước tại [Temporary License](https://purchase.aspose.com/temporary-license/) để tạo tệp giấy phép có thời hạn.  

## Kết luận

Bằng cách làm theo hướng dẫn này, bạn đã biết cách **xuất DWG sang PDF**, bật theo dõi toàn bộ quy trình, và xử lý chuyển đổi DXF‑to‑PDF với lớp **custom error handler Java**. Hãy tích hợp các đoạn mã này vào pipeline xây dựng của bạn để có được khả năng quan sát, cải thiện độ tin cậy và đáp ứng các tiêu chuẩn tuân thủ ngành cho việc xử lý tài liệu CAD.

---

**Cập nhật lần cuối:** 2026-11-18  
**Kiểm thử với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

## Hướng dẫn liên quan

- [Xuất DWG sang PDF và Chuyển đổi Bản vẽ CAD – Hướng dẫn Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Xuất Bố cục DWG Cụ thể sang PDF bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}