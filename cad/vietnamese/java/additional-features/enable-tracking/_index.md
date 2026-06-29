---
date: 2026-02-10
description: Hướng dẫn từng bước cách bật tính năng theo dõi trong các tệp DWG bằng
  Aspose.CAD cho Java và cách chuyển đổi DXF sang PDF với trình xử lý lỗi tùy chỉnh.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Cách kích hoạt theo dõi trong các tệp DWG bằng Aspose.CAD trong Java
url: /vi/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách bật theo dõi trong DWG tệp bằng Aspose.CAD trong Java

## Giới thiệu

Nếu bạn đang làm việc trên hợp đồng CAD dự án, việc **cách bật theo dõi** trong DWG quy trình của bạn là một bước thay đổi cuộc chơi. Nó cung cấp cho bạn cái nhìn thời gian thực hiện các vấn đề kết xuất, giúp bạn phát hiện sớm các chuyển đổi lỗi và giữ cho mọi bên liên quan được thông báo. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn chi tiết các bước để theo dõi Aspose.CAD cho Java và chúng tôi cũng sẽ trình diễn **cách chuyển đổi DXF sang PDF** như một phần của cùng một đường dẫn. Khi hoàn thành, bạn sẽ có một đoạn mã hoàn chỉnh, sẵn sàng cho sản phẩm xuất bản, báo cáo lỗi qua một lớp **trình xử lý lỗi tùy chỉnh Java** trong khi xuất bản vẽ.

## Trả lời nhanh
- **Câu hỏi “bật dwg theo dõi java” có tác dụng gì?** Nó kích hoạt lỗi xử lý gọi lại của Aspose.CAD để bạn có thể tìm thấy các vấn đề hiển thị trong quá trình xuất.
- **Tôi có cần giấy phép không?** Bản dùng thử hoạt động thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Tôi có thể chuyển đổi DXF sang PDF không?** Có – cùng một `PdfOptions` dùng cho DWG cũng hoạt động cho DXF, đáp ứng kịch bản *java chuyển đổi dxf pdf*.
- **Yêu cầu phiên bản JDK nào?** Java 8 trở lên.
- **Tôi có thể tìm thêm ví dụ ở đâu?** Kiểm tra tài liệu Aspose.CAD Java được liên kết bên dưới.

## Cách bật tính năng theo dõi trong tệp DWG bằng Aspose.CAD

Kích hoạt DWG theo dõi trong một ứng dụng Java có nghĩa là gắn một trình xử lý kết xuất tùy chỉnh để ghi lại cảnh báo, lỗi và các thông tin mong đợi khác khi CAD tệp được rasterization hoặc xuất. Tính năng này giúp các nhà phát triển gỡ lỗi chuyển đổi đường ống và đảm bảo sản phẩm cuối cùng có chất lượng cao hơn.

## Tại sao nên sử dụng Aspose.CAD cho Java?

- **Hỗ trợ CAD đầy đủ tính năng** – DWG, DXF, DGN, và hơn thế nữa.
- **Không phụ thuộc bên ngoài** – thư viện tím Java, lý tưởng cho tự động hóa máy chủ.
- **Theo dõi tích hợp** – kết quả hiển thị chi tiết qua `CadRenderHandler`.
- **Xuất PDF dễ dàng** – chuyển đổi một dòng lệnh trong khi giữ vectơ dữ liệu.

## Điều kiện tiên quyết

Trước khi chúng tôi thực hiện phần thực thi, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Bộ công cụ phát triển Java (JDK): Đảm bảo rằng Java đã được cài đặt trên hệ thống của bạn.
- Aspose.CAD for Java: Tải và cài đặt Aspose.CAD for Java từ [link tải xuống](https://releases.aspose.com/cad/java/).
- Document Directory: Chuẩn bị một thư mục chứa các tệp DWG của bạn.

## Nhập không gian tên

Trong dự án Java của bạn, hãy bắt đầu bằng cách nhập các không gian tên cần thiết để tận dụng các chức năng của Aspose.CAD:

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

## Bước 1: Tải tập tin DWG

Bắt đầu bằng việc tải tệp DWG (hoặc DXF) vào ứng dụng Java của bạn. Điều chỉnh đường dẫn tệp cho phù hợp:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Bước 2: Cấu hình các tùy chọn xuất PDF (Cách chuyển đổi DXF sang PDF)

Thiết lập các tùy chọn xuất PDF, chỉ định các tùy chọn rasterization vector cho CAD. Điều này cũng trình diễn khả năng *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Bước 3: Triển khai theo dõi (Trình xử lý lỗi tùy chỉnh bằng Java)

Triển khai theo dõi bằng một lớp xử lý lỗi tùy chỉnh. Lớp này sẽ ghi lại các vấn đề render và hiển thị chúng trên console:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Bước 4: Xuất sang PDF

Khởi chạy quá trình xuất để chuyển đổi tệp DWG/DXF sang PDF với tính năng theo dõi đã bật:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Bước 5: Lớp CadRenderHandler

Định nghĩa lớp `ErrorHandler` (kế thừa `CadRenderHandler`) để xử lý kết quả render và xuất thông tin theo dõi:

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

## Tại sao điều này lại quan trọng

Bằng cách bật theo dõi, bạn có thể xóa kiểm tra chuỗi cho mỗi chuyển đổi bước. Điều đặc biệt này có giá trị trong các ngành công nghiệp được quy định (kiến trúc, kỹ thuật, xây dựng) ở nơi mà bằng chứng về việc kết xuất chính xác là điều cần thiết cho các cuộc kiểm tra chiến thuật. Tùy chọn xử lý lỗi lớp cũng cung cấp một kết nối để ghi đăng nhập vào hệ thống giám sát hoặc kích hoạt tự động thử lại.

## Các vấn đề thường gặp và giải pháp

- **`NullPointerException` trên `RenderResult`** – Đảm bảo bạn đang sử dụng Aspose.CAD phiên bản 23.10 trở lên; các phiên bản cũ hơn không có API `RenderResult`.
- **Không tìm thấy tệp** – Kiểm tra lại thư mục `dataDir` đúng thư mục và tên tệp phải khớp chính xác, kể cả chữ hoa/chữ thông thường.
- **Thiếu đầu ra theo dõi** – Xác nhận rằng tùy chọn chỉnh sửa `ErrorHandler` đã được phân bổ đúng cho `cadRasterizationOptions.RenderResult`.

## Câu hỏi thường gặp

**Q:** Tôi có thể bật theo dõi các dạng CAD khác bằng Aspose.CAD cho Java không?
A: Aspose.CAD chủ yếu hỗ trợ theo dõi DWG. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức.

**Q:** Làm cách nào để xử lý các tùy chọn xuất ra trong Aspose.CAD cho Java?
A: Khám phá tài liệu chi tiết tại [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**Q:** Có phiên bản nào được dùng thử cho Aspose.CAD cho Java không?
A: Có, bạn có thể truy cập phiên bản dùng thử tại [Bản dùng thử miễn phí Aspose.CAD](https://releases.aspose.com/).

**Q:** Tôi có thể tìm hỗ trợ hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho Java ở đâu?
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận cộng đồng hỗ trợ.

**Q:** Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho Java?
A: Thực hiện quy trình được mô tả tại [Giấy phép tạm thời](https://purchase.aspose.com/temporary-license/).

## Phần kết luận

Kích hoạt DWG theo dõi trong Java với Aspose.CAD không cung cấp chỉ cho bạn khả năng giám sát các chuyển đổi vấn đề mà còn hợp tác thiết kế tối ưu hóa. Bằng cách thực hiện theo các bước trên, bạn có thể **bật theo dõi**, chuyển đổi DXF sang PDF và xử lý mọi vấn đề hiển thị một cách nhẹ nhàng.

---

**Cập nhật lần cuối:** 10/02/2026
**Đã kiểm thử với:** Aspose.CAD for Java 24.12
**Tác giả:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}