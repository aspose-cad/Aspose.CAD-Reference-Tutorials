---
date: 2026-06-19
description: Tìm hiểu cách đặt thời gian chờ khi lưu bản vẽ CAD bằng Aspose.CAD cho
  Java. Tăng hiệu suất, tránh treo, và xuất CAD sang PDF một cách hiệu quả.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Đặt Thời Gian Chờ Khi Lưu
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cách Đặt Thời Gian Chờ Khi Lưu cho CAD với Aspose.CAD
url: /vi/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đặt Thời Gian Hết Hạn Khi Lưu cho CAD với Aspose.CAD

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách đặt thời gian chờ** khi lưu bản vẽ CAD bằng Aspose.CAD cho Java. Áp dụng thời gian chờ ngăn các thao tác lưu kéo dài làm treo ứng dụng của bạn, điều này đặc biệt quan trọng khi bạn cần **xuất CAD sang PDF** hoặc **chuyển DWG sang PDF** trong các kịch bản xử lý hàng loạt. Aspose.CAD cho Java hỗ trợ hơn 50 định dạng CAD và có thể xử lý các tệp hàng trăm trang mà không tải toàn bộ tài liệu vào bộ nhớ, mang lại hiệu năng và mức tiêu thụ tài nguyên dự đoán được.

## Câu trả lời nhanh
- **Thời gian chờ làm gì?** Nó hủy bỏ thao tác lưu sau một khoảng thời gian xác định, giải phóng luồng và ngăn rò rỉ tài nguyên.  
- **Lớp nào kiểm soát thời gian chờ?** `InterruptionTokenSource` cung cấp token hủy được sử dụng bởi quy trình lưu.  
- **Tôi vẫn có thể xuất CAD sang PDF sau khi hết thời gian chờ không?** Có – bạn có thể bắt ngoại lệ gián đoạn và thử lại hoặc ghi log lỗi.  
- **Tôi có cần giấy phép đặc biệt không?** Một giấy phép Aspose.CAD thông thường là đủ; tính năng thời gian chờ đã được tích hợp sẵn.  
- **Cách tiếp cận này có an toàn với đa luồng không?** Có, khi mỗi lần lưu chạy trong luồng riêng của nó với token riêng.

## Thời gian chờ là gì trong các thao tác lưu CAD?
Thời gian chờ là giới hạn thời gian có thể cấu hình, khi vượt quá sẽ buộc quá trình lưu dừng lại và ném ngoại lệ gián đoạn. Điều này bảo vệ ứng dụng Java của bạn khỏi việc treo vô hạn do các bản vẽ phức tạp hoặc tắc nghẽn I/O.

## Tại sao đặt thời gian chờ khi lưu tệp CAD?
Aspose.CAD có thể **chuyển DWG sang PDF** và **xuất CAD sang PDF** trong vòng chưa tới một giây cho các bản vẽ thông thường, nhưng các tệp cực lớn hoặc hỏng có thể mất vài phút. Bằng cách định nghĩa thời gian chờ, bạn đảm bảo bất kỳ lần lưu nào cũng không vượt quá, ví dụ, 30 giây, giữ cho năng suất xử lý hàng loạt ổn định và ngăn tình trạng thiếu tài nguyên luồng.

## Yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn bạn đã chuẩn bị các yêu cầu sau:
- **Thư viện Aspose.CAD cho Java** – Đảm bảo bạn đã tích hợp thư viện Aspose.CAD cho Java vào dự án. Bạn có thể tải thư viện từ [website](https://releases.aspose.com/cad/java/).
- **Môi trường phát triển** – Thiết lập môi trường phát triển Java với tất cả công cụ và phụ thuộc cần thiết.

## Nhập Gói

Để bắt đầu, nhập các gói cần thiết vào dự án Java của bạn. Thêm các dòng sau vào đầu tệp Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Bây giờ, hãy phân tích mã ví dụ thành các hướng dẫn từng bước:

## Cách đặt thời gian chờ khi lưu bản vẽ CAD?

Tải tệp CAD, tạo một `InterruptionTokenSource` với thời gian chờ mong muốn, và truyền token này vào tùy chọn lưu PDF. Nếu thao tác vượt quá thời gian chờ, Aspose.CAD sẽ ném `OperationCanceledException`, bạn có thể bắt ngoại lệ này để xử lý lỗi một cách nhẹ nhàng.

### Bước 1: Đặt Thư Mục Nguồn và Đầu Ra

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Đảm bảo bạn có các thư mục nguồn và đầu ra đúng cho các bản vẽ CAD của mình.

### Bước 2: Tạo Nguồn Token Gián Đoạn

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Khởi tạo một nguồn token gián đoạn để quản lý các gián đoạn trong quá trình lưu.

### Bước 3: Tải Bản Vẽ CAD

Lớp `CadImage` là đối tượng cốt lõi của Aspose.CAD đại diện cho một bản vẽ CAD trong bộ nhớ, cung cấp các phương thức để render và chuyển đổi.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Bước 4: Cấu Hình Tùy Chọn Rasterization

`CadRasterizationOptions` chỉ định cách bản vẽ CAD được raster hóa thành hình ảnh.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Cấu hình các tùy chọn rasterization cho bản vẽ CAD.

### Bước 5: Cấu Hình Tùy Chọn PDF

`PdfOptions` định nghĩa các cài đặt để lưu bản vẽ CAD dưới dạng tài liệu PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Thiết lập tùy chọn PDF với các tùy chọn rasterization vector và token gián đoạn.

### Bước 6: Lưu Bản Vẽ với Thời Gian Hết Hạn

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Lưu bản vẽ CAD thành tệp PDF với thời gian chờ đã chỉ định.

### Bước 7: Xử Lý Gián Đoạn

`OperationCanceledException` được ném khi một thao tác lưu vượt quá thời gian chờ đã đặt.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Tạo một luồng để thực hiện thao tác lưu và ngắt nó sau thời gian chờ xác định.

## Vấn đề Thường Gặp và Giải Pháp

- **Thời gian chờ quá ngắn** – Nếu bạn nhận được nhiều gián đoạn, tăng giá trị thời gian chờ để đáp ứng các bản vẽ lớn hơn.  
- **InterruptedException không được bắt** – Luôn bao bọc lời gọi lưu trong khối try‑catch cho `OperationCanceledException` để tránh ứng dụng bị sập.  
- **Tiêu thụ bộ nhớ** – Sử dụng `PdfOptions.setVectorRasterizationOptions` để stream đầu ra thay vì tải toàn bộ tệp vào bộ nhớ.

## Câu Hỏi Thường Gặp

**H: Tôi có thể dùng tính năng này để chuyển DWG sang PDF trong công việc batch không?**  
Đ: Có, bao gói mỗi chuyển đổi trong một luồng riêng với token gián đoạn riêng để áp dụng giới hạn thời gian cho từng tệp.

**H: Thời gian chờ có hoạt động trên mọi định dạng đầu ra không?**  
Đ: Cơ chế thời gian chờ gắn với `InterruptionTokenSource` và hoạt động với bất kỳ định dạng nào tôn trọng token, bao gồm PDF, PNG và SVG.

**H: Điều gì xảy ra với các tệp bị ghi một phần sau khi hết thời gian chờ?**  
Đ: Aspose.CAD tự động loại bỏ đầu ra không hoàn chỉnh, vì vậy bạn sẽ không có các PDF bị hỏng.

**H: Có cần giấy phép cho việc sử dụng trong môi trường production không?**  
Đ: Có, cần một giấy phép Aspose.CAD hợp lệ cho các triển khai thương mại; bản dùng thử miễn phí có sẵn để đánh giá.

**H: Tôi có thể tìm thêm ví dụ về việc sử dụng token gián đoạn ở đâu?**  
Đ: Tài liệu chính thức của Aspose.CAD cung cấp các đoạn mã bổ sung và hướng dẫn thực hành tốt.

## Tài Nguyên Bổ Sung

- [releases page](https://releases.aspose.com/cad/java/) – Trang tải trực tiếp các bản phát hành mới nhất của Aspose.CAD cho Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Tham chiếu API đầy đủ và hướng dẫn cho nhà phát triển.  
- [this link](https://releases.aspose.com/) – Các bản phát hành sản phẩm Aspose chung.  
- [here](https://purchase.aspose.com/temporary-license/) – Nhận giấy phép tạm thời để thử nghiệm.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Hỗ trợ cộng đồng và thảo luận.

## Kết Luận

Bạn đã nắm vững **cách đặt thời gian chờ** cho việc lưu bản vẽ CAD với Aspose.CAD cho Java. Bằng cách tích hợp `InterruptionTokenSource` vào quy trình làm việc, bạn có thể **xuất CAD sang PDF** hoặc **chuyển DWG sang PDF** một cách đáng tin cậy mà không lo ngại các thao tác kéo dài, giữ cho ứng dụng của bạn luôn phản hồi và mở rộng.

---

**Cập nhật lần cuối:** 2026-06-19  
**Kiểm tra với:** Aspose.CAD cho Java 24.12  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng Dẫn Liên Quan

- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Xuất Bố Cục DWG Cụ Thể sang PDF bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Chuyển DWG sang PNG và Các Định Dạng Raster Khác bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}