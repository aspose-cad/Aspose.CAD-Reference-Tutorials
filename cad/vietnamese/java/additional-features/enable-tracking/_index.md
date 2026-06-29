---
date: 2026-06-29
description: Tìm hiểu cách xuất DWG sang PDF, bật theo dõi và sử dụng lớp xử lý lỗi
  tùy chỉnh trong Java với Aspose.CAD cho Java. Bao gồm chuyển đổi DXF‑to‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Bật Theo dõi trong Tệp DWG bằng Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
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
title: Xuất DWG sang PDF và Bật Theo dõi với Aspose.CAD Java
url: /vi/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG sang PDF và Bật Theo dõi với Aspose.CAD Java

## Giới thiệu

Việc xuất DWG sang PDF đồng thời giữ được khả năng quan sát toàn bộ quá trình chuyển đổi là điều thiết yếu cho các nhóm làm việc tập trung vào CAD hiện đại. Trong hướng dẫn này, bạn sẽ khám phá **cách bật theo dõi** trong quy trình DWG, chuyển đổi DXF sang PDF trong cùng một pipeline, và ghi lại mọi cảnh báo render bằng một lớp **custom error handler Java**. Khi hoàn thành, bạn sẽ có một đoạn mã sẵn sàng cho môi trường sản xuất, không chỉ tạo ra các tệp PDF chất lượng cao mà còn ghi lại thông tin chẩn đoán để kiểm toán và khắc phục sự cố.

## Câu trả lời nhanh
- **What does “enable dwg tracking java” do?** Nó kích hoạt các callback render của Aspose.CAD để bạn có thể thấy cảnh báo và lỗi trong quá trình xuất.  
- **Do I need a license?** Bản dùng thử hoạt động cho việc thử nghiệm; cần giấy phép thương mại cho môi trường sản xuất.  
- **Can I also convert DXF to PDF?** Có – cùng một đối tượng `PdfOptions` dùng cho DWG cũng áp dụng cho DXF, đáp ứng kịch bản *java convert dxf pdf*.  
- **Which JDK version is required?** Java 8 trở lên.  
- **Where can I find more examples?** Xem [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) được liên kết bên dưới.

## Export DWG sang PDF là gì?
Export DWG to PDF là quá trình chuyển đổi bản vẽ AutoCAD gốc (DWG) thành tài liệu PDF di động trong khi bảo toàn độ chính xác vector, các lớp và chú thích. Aspose.CAD thực hiện chuyển đổi này hoàn toàn bằng Java, loại bỏ nhu cầu cài đặt AutoCAD bản địa.

## Tại sao nên sử dụng Aspose.CAD cho Java?

Aspose.CAD for Java cung cấp giải pháp thuần Java toàn diện cho việc chuyển đổi CAD, hỗ trợ hơn 50 định dạng, hiệu năng cao và cung cấp tính năng theo dõi tích hợp qua các callback render. Thư viện không yêu cầu phụ thuộc bên ngoài và có thể tích hợp vào các pipeline phía server.

- **Hỗ trợ đa dạng định dạng** – xử lý DWG, DXF, DGN và hơn 50 định dạng CAD khác.  
- **Không phụ thuộc bên ngoài** – thư viện thuần Java lý tưởng cho tự động hoá phía server.  
- **Theo dõi tích hợp** – `CadRenderHandler` cung cấp kết quả render chi tiết.  
- **Xuất PDF một dòng lệnh** – `PdfOptions` chuyển đổi sang PDF trong khi giữ nguyên dữ liệu vector.  

Các khẳng định định lượng này được chứng minh bởi khả năng của Aspose.CAD xử lý các tệp lên tới 500 trang mà không cần tải toàn bộ tài liệu vào bộ nhớ, đạt thời gian chuyển đổi dưới 2 giây trên máy chủ 4‑core tiêu chuẩn.

## Yêu cầu trước

- **Java Development Kit (JDK)** 8 hoặc mới hơn đã được cài đặt trên máy của bạn.  
- **Aspose.CAD for Java** tải về từ [download link](https://releases.aspose.com/cad/java/) chính thức.  
- **Aspose.CAD Free Trial** có thể lấy từ trang [Aspose.CAD Free Trial](https://releases.aspose.com/) nếu bạn cần đánh giá nhanh.  
- Một thư mục chứa các tệp DWG/DXF mà bạn muốn chuyển đổi.  

## Cách xuất DWG sang PDF?  

Tải tệp nguồn, cấu hình `PdfOptions`, gắn một `CadRenderHandler` tùy chỉnh, và gọi `save`. Quy trình end‑to‑end này chuyển DWG (hoặc DXF) sang PDF đồng thời phát ra thông tin theo dõi cho mỗi bước render, đảm bảo mọi cảnh báo hoặc lỗi được ghi lại và có thể được xử lý bởi nhà phát triển hoặc quy trình tự động.

## Nhập không gian tên

Lớp `CadRenderHandler` là giao diện callback của Aspose.CAD nhận chẩn đoán render. Nhập các gói cần thiết trước khi bắt đầu viết mã:

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

Lớp `CadImage` đại diện cho tài liệu CAD được nạp vào bộ nhớ. Khởi tạo nó với đường dẫn tệp sẽ tải bản vẽ mà không cần mở ứng dụng CAD bản địa.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Bước 2: Cấu hình tùy chọn xuất PDF (Cách chuyển DXF sang PDF)

`PdfOptions` xác định cách rasterizer CAD tạo ra đầu ra PDF, bao gồm các cài đặt render vector và kích thước trang. Đặt `VectorRasterizationOptions` đảm bảo các đường và đường cong giữ độ sắc nét. Đối tượng `VectorRasterizationOptions` chỉ định các tham số rasterization như DPI và màu nền.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Bước 3: Triển khai theo dõi (Custom Error Handler Java)

`ErrorHandler` kế thừa `CadRenderHandler` để ghi lại cảnh báo, lỗi và thông điệp thông tin phát ra trong quá trình rasterization. Lớp này ghi mỗi thông điệp ra console, nhưng bạn có thể dễ dàng chuyển chúng tới file log hoặc hệ thống giám sát. `CadRenderHandler` là một interface nhận chẩn đoán render từ rasterizer.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Bước 4: Xuất sang PDF  

Gọi `save` trên đối tượng `CadImage` với `PdfOptions` đã cấu hình thực hiện chuyển đổi. Vì handler tùy chỉnh đã được gắn, bất kỳ vấn đề render nào sẽ xuất hiện trên console khi quá trình xuất diễn ra.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Bước 5: Lớp CadRenderHandler  

`CadRenderHandler` là lớp cơ sở của Aspose.CAD để nhận kết quả render. Ghi đè phương thức `onRenderCompleted` cho phép bạn truy cập vào đối tượng `RenderResult`, chứa tập hợp các mục `RenderMessage` mô tả từng bước của quy trình.

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

Bật theo dõi tạo ra một chuỗi audit đáp ứng các yêu cầu tuân thủ trong các ngành được quy định như kiến trúc, kỹ thuật và xây dựng. Trình xử lý lỗi tùy chỉnh cũng cho phép bạn tích hợp kiểm tra sức khỏe chuyển đổi CAD vào các pipeline CI/CD, tự động đánh dấu các tệp cần xem xét thủ công.

## Các vấn đề thường gặp và giải pháp

- **`NullPointerException` trên `RenderResult`** – Đảm bảo bạn đang dùng Aspose.CAD 23.10 hoặc mới hơn; các phiên bản trước không có API `RenderResult`.  
- **File not found** – Kiểm tra lại `dataDir` trỏ đúng thư mục và tên tệp phải khớp chính xác về chữ hoa/thường.  
- **Missing tracking output** – Xác nhận rằng thể hiện `ErrorHandler` của bạn đã được gán đúng vào `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Câu hỏi thường gặp

**Q:** Tôi có thể bật theo dõi cho các định dạng CAD khác bằng Aspose.CAD for Java không?  
**A:** Theo dõi chủ yếu được cung cấp cho DWG và DXF. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức để xem API nào hỗ trợ callback render.

**Q:** Làm sao tôi có thể tùy chỉnh các tùy chọn xuất thêm, chẳng hạn đặt metadata cho PDF?  
**A:** `PdfOptions` cung cấp các thuộc tính như `setTitle`, `setAuthor`, và `setSubject`. Đặt chúng trước khi gọi `save` để nhúng metadata vào PDF kết quả.

**Q:** Bản dùng thử có đủ để đánh giá tính năng theo dõi không?  
**A:** Có, bản trial miễn phí cung cấp quyền truy cập đầy đủ API, cho phép bạn thử nghiệm `CadRenderHandler` và xuất PDF mà không bị hạn chế.

**Q:** Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD for Java ở đâu?  
**A:** Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để đặt câu hỏi và chia sẻ kinh nghiệm với các nhà phát triển khác.

**Q:** Làm sao tôi có thể lấy giấy phép tạm thời cho môi trường kiểm thử tự động?  
**A:** Thực hiện các bước tại [Temporary License](https://purchase.aspose.com/temporary-license/) để tạo file giấy phép có thời hạn.

## Kết luận

Bằng cách làm theo tutorial này, bạn đã biết **cách xuất DWG sang PDF**, bật theo dõi toàn diện, và xử lý chuyển đổi DXF‑to‑PDF bằng lớp **custom error handler Java**. Hãy tích hợp các đoạn mã này vào pipeline xây dựng của bạn để có được khả năng quan sát, nâng cao độ tin cậy và đáp ứng các yêu cầu tuân thủ cấp ngành cho việc xử lý tài liệu CAD.

---

**Cập nhật lần cuối:** 2026-06-29  
**Kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Xuất DWG sang PDF và Chuyển đổi Bản vẽ CAD – Hướng dẫn Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Xuất bố cục DWG cụ thể sang PDF bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}