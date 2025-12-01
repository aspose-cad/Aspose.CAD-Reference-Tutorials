---
date: 2025-12-01
description: Tìm hiểu cách đặt kích thước trang PDF, chuyển đổi DWG sang PDF và bật
  theo dõi các thay đổi của DWG bằng Aspose.CAD cho Java.
language: vi
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Đặt kích thước trang PDF và theo dõi DWG với Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kích Thước Trang PDF và Theo Dõi DWG với Aspose.CAD Java

## Giới thiệu

Khi cộng tác trong các dự án CAD, bạn thường cần **đặt kích thước trang PDF** để có bố cục nhất quán, **chuyển DWG sang PDF**, và theo dõi mọi thay đổi được thực hiện trên bản vẽ. Aspose.CAD for Java giúp thực hiện tất cả những điều này trong một quy trình làm việc liền mạch. Trong hướng dẫn này, chúng ta sẽ đi qua các bước chính để **đặt kích thước trang PDF**, bật **theo dõi các thay đổi DWG**, và xuất bản vẽ dưới dạng PDF—tất cả đều sử dụng Java.

## Câu trả lời nhanh
- **Làm thế nào để đặt kích thước trang PDF?** Sử dụng `CadRasterizationOptions.setPageWidth()` và `setPageHeight()` trước khi xuất.  
- **Tôi có thể theo dõi các thay đổi khi xuất không?** Có – triển khai một `CadRenderHandler` tùy chỉnh để ghi nhận kết quả theo dõi.  
- **Phương pháp nào chuyển DWG sang PDF?** Gọi `image.save(stream, pdfOptions)` sau khi cấu hình các tùy chọn.  
- **Các yêu cầu chính là gì?** JDK, Aspose.CAD for Java, và một thư mục chứa các tệp DWG/DXF.  
- **Cần giấy phép cho môi trường sản xuất không?** Có, cần một giấy phép Aspose.CAD hợp lệ cho các triển khai không dùng bản thử nghiệm.

## “Đặt kích thước trang PDF” trong ngữ cảnh xuất DWG là gì?

Đặt kích thước trang PDF xác định kích thước của canvas PDF kết quả (rộng × cao tính bằng pixel). Điều này rất quan trọng khi bạn muốn bản vẽ xuất ra phù hợp với một kích thước giấy cụ thể hoặc bố cục màn hình, đảm bảo mọi yếu tố xuất hiện đúng vị trí mong muốn.

## Tại sao cần bật theo dõi khi xuất tệp DWG?

Theo dõi (hoặc change‑tracking) ghi lại bất kỳ vấn đề nào trong quá trình render, như thiếu phông chữ hoặc các thực thể không được hỗ trợ. Bằng cách nắm bắt thông tin này, bạn có thể:

- Nhanh chóng xác định các vấn đề cần khắc phục trước khi giao hàng cuối cùng.  
- Cung cấp phản hồi rõ ràng cho các thành viên trong nhóm về những gì đã bị thay đổi hoặc bỏ qua.  
- Duy trì một bản ghi audit cho các ngành công nghiệp yêu cầu tuân thủ nghiêm ngặt.

## Yêu cầu trước

- **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (8+).  
- **Aspose.CAD for Java** – tải xuống từ trang [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Thư mục tài liệu** – một thư mục chứa các tệp DWG/DXF bạn muốn xử lý.

## Nhập không gian tên

Bắt đầu bằng cách nhập các lớp Aspose.CAD cần thiết và các lớp I/O chuẩn của Java.

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

## Bước 1: Tải tệp DWG (hoặc DXF)

Tải bản vẽ nguồn của bạn vào một đối tượng `Image`. Điều chỉnh đường dẫn để trỏ tới thư mục của bạn.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Bước 2: Cấu hình tùy chọn xuất PDF (bao gồm kích thước trang)

Ở đây chúng ta thiết lập các tùy chọn PDF và **đặt kích thước trang PDF** thành 800 × 600 pixel. Đây là nơi từ khóa chính được áp dụng.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Bước 3: Triển khai theo dõi

Tạo một trình xử lý lỗi tùy chỉnh sẽ nhận thông tin theo dõi trong quá trình chuyển đổi.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Bước 4: Xuất ra PDF

Với các tùy chọn và trình xử lý theo dõi đã sẵn sàng, xuất bản vẽ. Bước này **chuyển DWG sang PDF** (hoặc DXF sang PDF trong ví dụ của chúng ta).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Bước 5: Lớp CadRenderHandler – Ghi nhận kết quả theo dõi

Lớp `ErrorHandler` mở rộng `CadRenderHandler` và in ra bất kỳ vấn đề render nào xảy ra khi **theo dõi các thay đổi DWG**.

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

## Các vấn đề thường gặp & Cách khắc phục

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Missing fonts** | Tệp CAD tham chiếu các phông chữ chưa được cài đặt trên máy chủ. | Cài đặt các phông chữ cần thiết hoặc nhúng chúng vào bản vẽ nguồn. |
| **Unsupported entities** | Một số thực thể DWG chưa được Aspose.CAD hỗ trợ. | Sử dụng đầu ra theo dõi để xác định chúng và đơn giản hoá bản vẽ. |
| **Incorrect page size** | `setPageWidth/Height` chưa được gọi trước khi xuất. | Đảm bảo kích thước trang được đặt trong `CadRasterizationOptions` như hướng dẫn ở trên. |

## Câu hỏi thường gặp

### Q1: Tôi có thể bật theo dõi cho các định dạng tệp CAD khác bằng Aspose.CAD cho Java không?

A1: Aspose.CAD chủ yếu hỗ trợ theo dõi cho các tệp DWG/DXF. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức để xem tính năng nào khả dụng.

### Q2: Làm thế nào tôi có thể xử lý các tùy chọn xuất bổ sung trong Aspose.CAD cho Java?

A2: Thư viện cung cấp nhiều tùy chọn như DPI, màu nền, và rasterization vector. Khám phá chúng trong [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3: Có phiên bản dùng thử cho Aspose.CAD cho Java không?

A3: Có, bạn có thể tải bản dùng thử miễn phí từ [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Tôi có thể tìm kiếm hỗ trợ hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho Java ở đâu?

A4: Diễn đàn cộng đồng tại [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) là nơi tuyệt vời để đặt câu hỏi và chia sẻ kinh nghiệm.

### Q5: Làm thế nào để tôi nhận được giấy phép tạm thời cho Aspose.CAD cho Java?

A5: Thực hiện các bước được mô tả trên trang [Temporary License](https://purchase.aspose.com/temporary-license/) để yêu cầu giấy phép có thời hạn cho việc đánh giá.

### Q6: Tôi có thể **chuyển DWG sang PDF** trong khi giữ nguyên các lớp không?

A6: Có. Bằng cách cấu hình `CadRasterizationOptions` bạn có thể bảo tồn thông tin lớp trong PDF kết quả.

### Q7: Cách tốt nhất để **xuất DWG dưới dạng PDF** với kích thước trang tùy chỉnh là gì?

A7: Đặt chiều rộng và chiều cao mong muốn bằng `setPageWidth` và `setPageHeight` trước khi gọi `image.save()` – chính xác như đã minh họa ở Bước 2.

## Kết luận

Bằng cách thực hiện các bước trên, bạn có thể **đặt kích thước trang PDF**, **chuyển DWG sang PDF**, và **theo dõi các thay đổi trong tệp DWG** sử dụng Aspose.CAD for Java. Quy trình này cho phép bạn kiểm soát hoàn toàn bố cục đầu ra đồng thời cung cấp các chẩn đoán quan trọng giúp quá trình cộng tác CAD của bạn diễn ra suôn sẻ và không lỗi. Hãy khám phá thêm các tùy chọn render và tích hợp mã này vào các pipeline tự động lớn hơn.

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}