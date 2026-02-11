---
date: 2026-01-10
description: Tìm hiểu cách xuất DGN sang DWG và chuyển đổi MicroStation DGN sang AutoCAD
  DWG bằng Aspose.CAD cho Java. Hướng dẫn từng bước.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Xuất DGN sang DWG bằng Aspose.CAD cho Java
url: /vi/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN to DWG with Aspose.CAD for Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **export dgn to dwg** và nhúng một thiết kế MicroStation DGN vào trong tệp AutoCAD DWG bằng thư viện Aspose.CAD cho Java. Dù bạn đang di chuyển các bản vẽ MicroStation cũ hoặc cần kết hợp các DGN underlay với bố cục DWG, hướng dẫn này sẽ dẫn bạn qua từng bước — từ thiết lập môi trường đến tạo bản xem trước PDF của DWG cuối cùng.

## Câu trả lời nhanh
- **Việc “export dgn to dwg” đạt được gì?** Nó nhúng một DGN underlay vào DWG, cho phép xem liền mạch trong AutoCAD.  
- **Tôi có thể xuất kết quả sang định dạng nào để xem nhanh?** Bạn có thể **export cad file to pdf** bằng cách sử dụng `PdfOptions`.  
- **Có cần giấy phép để chạy mã không?** Cần một giấy phép Aspose.CAD tạm thời hoặc trả phí cho việc sử dụng trong môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên hoạt động với phiên bản mới nhất của Aspose.CAD for Java.  
- **Có bản dùng thử miễn phí không?** Có — tải bản dùng thử từ trang web Aspose.

## Export dgn to dwg là gì?
Export DGN to DWG có nghĩa là chuyển đổi hoặc nhúng một thiết kế MicroStation DGN dưới dạng underlay bên trong bản vẽ AutoCAD DWG. Điều này cho phép các chuyên gia CAD tận dụng các tài sản DGN hiện có mà không cần tạo lại hình học từ đầu.

## Tại sao chuyển đổi MicroStation DGN sang AutoCAD DWG?
- **Collaboration:** Các nhóm sử dụng AutoCAD có thể xem và chỉnh sửa nội dung DGN trực tiếp.  
- **Standardization:** DWG là định dạng chuẩn de‑facto cho nhiều quy trình downstream (ví dụ: tạo PDF, render 3D).  
- **Preservation:** Giữ nguyên các tham chiếu DGN gốc, giảm thiểu mất mát dữ liệu.

## Yêu cầu trước

Trước khi bắt đầu hướng dẫn, hãy đảm bảo bạn đã chuẩn bị các yêu cầu sau:
1. **Aspose.CAD Library:** Tải và cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tìm thư viện [tại đây](https://releases.aspose.com/cad/java/).  
2. **Java Development Kit (JDK):** Đảm bảo Java đã được cài đặt trên hệ thống của bạn.  
3. **Integrated Development Environment (IDE):** Chọn một IDE Java như Eclipse hoặc IntelliJ để có trải nghiệm phát triển mượt mà hơn.

## Nhập gói

Trong dự án Java của bạn, nhập các gói Aspose.CAD cần thiết để thao tác với tệp CAD. Dưới đây là một ví dụ:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Bước 1: Đặt đường dẫn tệp

Xác định các đường dẫn tệp đầu vào và đầu ra cho tệp DWG. Cập nhật các biến `dataDir`, `fileName` và `outPath` cho phù hợp.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Bước 2: Tạo thể hiện PdfOptions

Tạo một thể hiện của lớp `PdfOptions`, vì chúng ta đang **exporting the CAD file to PDF** để kiểm tra nhanh.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Bước 3: Tải tệp DWG

Tải tệp DWG hiện có dưới dạng hình ảnh và chuyển đổi nó sang kiểu `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Bước 4: Duyệt qua các thực thể

Duyệt qua mỗi thực thể trong tệp DWG và kiểm tra xem nó có phải là một định nghĩa hình ảnh không. Nếu có, lấy tham chiếu bên ngoài tới đối tượng.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Bước 5: Định nghĩa tùy chọn rasterization

Định nghĩa các thiết lập cho đối tượng `CadRasterizationOptions`, bao gồm chiều rộng trang, chiều cao, bố cục và màu nền.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Bước 6: Đặt tùy chọn rasterization vector

Đặt các tùy chọn rasterization vector cho quá trình xuất.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Bước 7: Xuất DWG sang PDF

Cuối cùng, xuất DWG sang PDF bằng cách gọi phương thức `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **No DGN underlay appears** | The DWG does not contain a `DGNUNDERLAY` entity. | Verify that the source DWG includes a DGN reference. |
| **PDF is blank** | Rasterization options set to zero size or wrong layout. | Ensure `setPageWidth`/`setPageHeight` are positive and `setLayouts` matches the DWG layout name. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply a temporary or purchased license before calling any API methods. |

## Câu hỏi thường gặp

### Q1: Bạn có thể tìm tài liệu cho Aspose.CAD cho Java ở đâu?

A1: Tài liệu có thể được tìm thấy [tại đây](https://reference.aspose.com/cad/java/).

### Q2: Làm sao để tải thư viện Aspose.CAD cho Java?

A2: Bạn có thể tải thư viện từ [liên kết này](https://releases.aspose.com/cad/java/).

### Q3: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?

A3: Có, bạn có thể tìm bản dùng thử [tại đây](https://releases.aspose.com/).

### Q4: Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho Java?

A4: Nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q5: Cần trợ giúp hoặc có câu hỏi?

A5: Tham khảo diễn đàn hỗ trợ cộng đồng Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19).

### Q6: Tôi có thể chuyển PDF kết quả lại thành DWG không?

A6: PDF chỉ là bản xem trước raster; việc chuyển lại sang DWG đòi hỏi một công cụ reverse‑engineering riêng.

### Q7: Phương pháp này có hoạt động với các định dạng CAD khác như DWF hoặc DXF không?

A7: Có, Aspose.CAD hỗ trợ nhiều định dạng; bạn chỉ cần điều chỉnh phần mở rộng tệp và các thiết lập rasterization cho phù hợp.

**Cập nhật lần cuối:** 2026-01-10  
**Kiểm tra với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}