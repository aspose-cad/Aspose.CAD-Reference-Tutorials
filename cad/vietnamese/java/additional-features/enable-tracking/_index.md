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

# Cách bật theo dõi trong tệp DWG bằng Aspose.CAD trong Java

## Introduction

Nếu bạn đang làm việc trên các dự án CAD hợp tác, việc biết **cách bật theo dõi** trong quy trình DWG của bạn là một bước thay đổi cuộc chơi. Nó cung cấp cho bạn cái nhìn thời gian thực về các vấn đề render, giúp bạn phát hiện sớm các lỗi chuyển đổi, và giữ cho mọi bên liên quan được thông báo. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn chi tiết các bước để bật theo dõi với Aspose.CAD cho Java, và chúng tôi cũng sẽ trình diễn **cách chuyển đổi DXF sang PDF** như một phần của cùng một pipeline. Khi hoàn thành, bạn sẽ có một đoạn mã hoàn chỉnh, sẵn sàng cho sản xuất, báo cáo lỗi qua một lớp **custom error handler Java** trong khi xuất bản vẽ.

## Quick Answers
- **Câu hỏi “enable dwg tracking java” làm gì?** Nó kích hoạt các callback xử lý lỗi của Aspose.CAD để bạn có thể thấy các vấn đề render trong quá trình xuất.  
- **Tôi có cần giấy phép không?** Bản dùng thử hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể chuyển đổi DXF sang PDF không?** Có – cùng một `PdfOptions` dùng cho DWG cũng hoạt động cho DXF, đáp ứng kịch bản *java convert dxf pdf*.  
- **Yêu cầu phiên bản JDK nào?** Java 8 trở lên.  
- **Tôi có thể tìm thêm ví dụ ở đâu?** Kiểm tra tài liệu Aspose.CAD Java được liên kết bên dưới.

## How to Enable Tracking in DWG Files Using Aspose.CAD

Bật theo dõi DWG trong một ứng dụng Java có nghĩa là gắn một custom render handler để ghi lại cảnh báo, lỗi và các thông tin chẩn đoán khác trong khi tệp CAD đang được raster hóa hoặc xuất. Sự hiện diện này giúp các nhà phát triển gỡ lỗi pipeline chuyển đổi và đảm bảo sản phẩm cuối có chất lượng cao hơn.

## Why Use Aspose.CAD for Java?

- **Full‑feature CAD support** – DWG, DXF, DGN, và hơn thế nữa.  
- **No external dependencies** – thư viện thuần Java, lý tưởng cho tự động hoá phía server.  
- **Built‑in tracking** – kết quả render chi tiết qua `CadRenderHandler`.  
- **Easy PDF export** – chuyển đổi một dòng lệnh trong khi giữ dữ liệu vector.  

## Prerequisites

Trước khi chúng ta đi vào phần thực thi, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Java Development Kit (JDK): Đảm bảo rằng Java đã được cài đặt trên hệ thống của bạn.  
- Aspose.CAD for Java: Tải và cài đặt Aspose.CAD for Java từ [download link](https://releases.aspose.com/cad/java/).  
- Document Directory: Chuẩn bị một thư mục chứa các tệp DWG của bạn.

## Import Namespaces

Trong dự án Java của bạn, bắt đầu bằng việc import các namespace cần thiết để tận dụng các chức năng của Aspose.CAD:

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

## Step 1: Load the DWG File

Bắt đầu bằng việc tải tệp DWG (hoặc DXF) vào ứng dụng Java của bạn. Điều chỉnh đường dẫn tệp cho phù hợp:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (How to Convert DXF to PDF)

Thiết lập các tùy chọn xuất PDF, chỉ định các tùy chọn rasterization vector cho CAD. Điều này cũng trình diễn khả năng *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Step 3: Implement Tracking (Custom Error Handler Java)

Triển khai theo dõi bằng một lớp xử lý lỗi tùy chỉnh. Lớp này sẽ ghi lại các vấn đề render và hiển thị chúng trên console:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Khởi chạy quá trình xuất để chuyển đổi tệp DWG/DXF sang PDF với tính năng theo dõi đã bật:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

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

## Why This Matters

Bằng cách bật theo dõi, bạn có được một chuỗi audit rõ ràng cho mỗi bước chuyển đổi. Điều này đặc biệt có giá trị trong các ngành công nghiệp được quy định (kiến trúc, kỹ thuật, xây dựng) nơi mà bằng chứng về việc render chính xác là cần thiết cho các cuộc kiểm toán tuân thủ. Lớp xử lý lỗi tùy chỉnh cũng cung cấp một điểm nối để ghi log vào hệ thống giám sát hoặc kích hoạt các retry tự động.

## Common Issues and Solutions

- **`NullPointerException` on `RenderResult`** – Đảm bảo bạn đang sử dụng Aspose.CAD phiên bản 23.10 trở lên; các phiên bản cũ hơn không có API `RenderResult`.  
- **File not found** – Kiểm tra lại `dataDir` trỏ đúng thư mục và tên tệp phải khớp chính xác, kể cả chữ hoa/chữ thường.  
- **Missing tracking output** – Xác nhận rằng `ErrorHandler` tùy chỉnh đã được gán đúng cho `cadRasterizationOptions.RenderResult`.

## Frequently Asked Questions

**Q:** Tôi có thể bật theo dõi cho các định dạng CAD khác bằng Aspose.CAD cho Java không?  
A: Aspose.CAD chủ yếu hỗ trợ theo dõi DWG. Đối với các định dạng khác, hãy tham khảo tài liệu chính thức.

**Q:** Làm thế nào để xử lý các tùy chọn xuất bổ sung trong Aspose.CAD cho Java?  
A: Khám phá tài liệu chi tiết tại [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**Q:** Có phiên bản dùng thử cho Aspose.CAD cho Java không?  
A: Có, bạn có thể truy cập phiên bản dùng thử tại [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q:** Tôi có thể tìm hỗ trợ hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho Java ở đâu?  
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng.

**Q:** Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho Java?  
A: Thực hiện quy trình được mô tả tại [Temporary License](https://purchase.aspose.com/temporary-license/).

## Conclusion

Bật theo dõi DWG trong Java với Aspose.CAD không chỉ cung cấp cho bạn khả năng quan sát các vấn đề chuyển đổi mà còn tối ưu hoá quy trình thiết kế hợp tác. Bằng cách làm theo các bước trên, bạn có thể **bật theo dõi**, chuyển đổi DXF sang PDF, và xử lý mọi vấn đề render một cách nhẹ nhàng.

---

**Last Updated:** 2026-02-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}