---
title: Xuất DGN sang DWG bằng Aspose.CAD cho Java
linktitle: Xuất DGN dưới dạng một phần của DWG
second_title: API Java Aspose.CAD
description: Khám phá cách xuất DGN như một phần của DWG bằng Aspose.CAD cho Java. Thực hiện theo hướng dẫn từng bước của chúng tôi để thao tác tệp CAD hiệu quả.
weight: 10
url: /vi/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DGN sang DWG bằng Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách sử dụng Aspose.CAD cho Java để xuất tệp DGN (MicroStation Design) dưới dạng một phần của tệp DWG (Bản vẽ AutoCAD). Aspose.CAD là một thư viện mạnh mẽ cung cấp chức năng toàn diện để làm việc với các định dạng tệp CAD. Hướng dẫn từng bước này sẽ giúp bạn hiểu quy trình xuất DGN như một phần của DWG bằng Java.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
1. Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tìm thấy thư viện[đây](https://releases.aspose.com/cad/java/).
2. Bộ công cụ phát triển Java (JDK): Đảm bảo rằng bạn đã cài đặt Java trên hệ thống của mình.
3. Môi trường phát triển tích hợp (IDE): Chọn Java IDE như Eclipse hoặc IntelliJ để có trải nghiệm phát triển mượt mà hơn.

## Gói nhập khẩu

Trong dự án Java của bạn, hãy nhập các gói Aspose.CAD cần thiết để cho phép thao tác với tệp CAD. Đây là một ví dụ:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Bước 1: Đặt đường dẫn tệp

 Xác định đường dẫn tệp đầu vào và đầu ra cho tệp DWG. Cập nhật`dataDir`, `fileName` , Và`outPath` các biến tương ứng.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Bước 2: Tạo phiên bản PdfOptions

 Tạo một thể hiện của`PdfOptions` class, vì chúng tôi đang xuất tệp DWG sang định dạng PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Bước 3: Tải tệp DWG

 Tải tệp DWG hiện có dưới dạng hình ảnh và chuyển đổi nó thành`CadImage` kiểu.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Bước 4: Lặp lại các thực thể

Đi qua từng thực thể bên trong tệp DWG và kiểm tra xem đó có phải là định nghĩa hình ảnh hay không. Nếu có, hãy truy xuất tham chiếu bên ngoài tới đối tượng.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Bước 5: Xác định các tùy chọn rasterization

 Xác định các cài đặt cho`CadRasterizationOptions`đối tượng, bao gồm chiều rộng, chiều cao, bố cục và màu nền của trang.

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

## Bước 6: Đặt tùy chọn Rasterization Vector

Đặt các tùy chọn rasterization vector để xuất.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Bước 7: Xuất DWG sang PDF

 Cuối cùng, xuất DWG sang PDF bằng cách gọi`save` phương pháp.

```java
cadImage.save(outPath, exportOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách xuất tệp DGN dưới dạng một phần của tệp DWG bằng Aspose.CAD cho Java. Thư viện mạnh mẽ này cung cấp các khả năng mở rộng để làm việc với các tệp CAD, giúp các tác vụ thao tác tệp CAD của bạn trở nên hiệu quả và đơn giản.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu về Aspose.CAD cho Java ở đâu?

 A1: Tài liệu có thể được tìm thấy[đây](https://reference.aspose.com/cad/java/).

### Câu hỏi 2: Làm cách nào tôi có thể tải xuống thư viện Aspose.CAD cho Java?

 A2: Bạn có thể tải xuống thư viện từ[liên kết này](https://releases.aspose.com/cad/java/).

### Câu hỏi 3: Có bản dùng thử miễn phí dành cho Aspose.CAD cho Java không?

 Câu trả lời 3: Có, bạn có thể tìm bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD cho Java ở đâu?

 A4: Xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 5: Cần trợ giúp hoặc có thắc mắc?

 A5: Truy cập diễn đàn hỗ trợ cộng đồng Aspose.CAD[đây](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
