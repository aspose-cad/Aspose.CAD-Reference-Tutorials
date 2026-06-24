---
date: 2026-02-28
description: Tìm hiểu cách tạo PDF từ DWG, lưu DWG dưới dạng PDF và thêm văn bản vào
  bản vẽ DWG với Aspose.CAD cho Java—hướng dẫn từng bước.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Tạo PDF từ DWG và Thêm Văn bản bằng Aspose.CAD cho Java
url: /vi/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ DWG và Thêm Văn Bản bằng Aspose.CAD cho Java

## Giới thiệu

Nếu bạn cần **tạo PDF từ các tệp DWG** đồng thời chèn văn bản tùy chỉnh, bạn đang ở đúng nơi. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — tải bản vẽ DWG, thêm chú thích văn bản, và cuối cùng lưu kết quả dưới dạng PDF bằng Aspose.CAD cho Java. Khi hoàn thành, bạn sẽ hiểu cách **lưu DWG dưới dạng PDF**, tùy chỉnh chiều cao văn bản, và thậm chí thêm các chú thích cơ bản.

## Câu trả lời nhanh
- **Có thể chuyển DWG sang PDF trong Java không?** Có, Aspose.CAD cho Java cung cấp API đơn giản.  
- **Có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Cần giấy phép thương mại; bản dùng thử miễn phí có sẵn.  
- **Phương pháp nào để thêm văn bản vào DWG?** Sử dụng đối tượng `CadText` và thêm nó vào không gian mô hình.  
- **Có thể đặt chiều cao văn bản không?** Chắc chắn — dùng `setTextHeight()` trên thể hiện `CadText`.  
- **Kết quả có phải là dạng vector không?** Khi tùy chọn rasterization được đặt thành `UseObjectColor`, PDF vẫn giữ dữ liệu vector chất lượng cao.

## “tạo PDF từ DWG” là gì?
Tạo PDF từ một bản vẽ DWG có nghĩa là chuyển đổi định dạng CAD gốc sang một tài liệu đọc‑chỉ được hỗ trợ rộng rãi, đồng thời bảo tồn hình học gốc. Việc chuyển đổi này rất cần thiết khi bạn muốn chia sẻ thiết kế với các bên liên quan không có phần mềm CAD.

## Tại sao nên dùng Aspose.CAD cho Java để chuyển DWG sang PDF?
Aspose.CAD cung cấp giải pháp thuần Java không yêu cầu cài đặt CAD bên ngoài. Nó hỗ trợ **chuyển DWG sang PDF**, duy trì độ trung thực vector, và cho phép bạn lập trình thêm các chú thích như văn bản, kích thước, hoặc đồ họa tùy chỉnh trước khi chuyển đổi.

## Yêu cầu trước

Trước khi bắt đầu hướng dẫn, hãy đảm bảo bạn đã chuẩn bị các yêu cầu sau:

- Thư viện Aspose.CAD cho Java: Tải và cài đặt thư viện từ [trang Aspose.CAD cho Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Đảm bảo bạn đã cài đặt JDK mới nhất trên hệ thống.

- Bản vẽ DWG: Chuẩn bị một tệp DWG mà bạn muốn thêm văn bản.

## Nhập không gian tên

Trong mã Java của bạn, nhập các không gian tên cần thiết cho Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, chúng ta sẽ phân tích đoạn mã mẫu thành nhiều bước:

## Bước 1: Thiết lập Thư mục Tài liệu và Đường dẫn Tệp DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Bước 2: Tải ảnh DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Bước 3: Tạo Đối tượng CadText (Thêm Văn bản vào DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Bước 4: Thêm Văn bản vào CadImage (Chèn Chú thích)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Bước 5: Thiết lập Tùy chọn PDF (Chuẩn bị tạo PDF từ DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Bước 6: Cấu hình CadRasterizationOptions (Kiểm soát việc render PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Bước 7: Lưu DWG đã chỉnh sửa dưới dạng PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Bằng cách thực hiện các bước này, bạn sẽ có thể **tạo PDF từ DWG**, thêm văn bản tùy chỉnh, và kiểm soát chiều cao văn bản — tất cả chỉ với vài dòng mã Java.

## Làm sao để chuyển DWG sang PDF trong Java ở quy mô lớn?
Nếu bạn cần **chuyển hàng loạt DWG sang PDF**, hãy bao bọc đoạn mã trên trong một vòng lặp duyệt qua thư mục chứa các bản vẽ DWG. Điều chỉnh `pageHeight`/`pageWidth` chỉ khi cần thiết để giảm mức tiêu thụ bộ nhớ, và tái sử dụng cùng một thể hiện `PdfOptions` cho mỗi tệp để cải thiện hiệu năng.

## Các vấn đề thường gặp & Mẹo

- **Văn bản không hiển thị?** Kiểm tra tọa độ X/Y có nằm trong phạm vi bản vẽ và lớp (layer) có được hiển thị không.
- **Chiều cao văn bản không đúng?** Điều chỉnh `setTextHeight()`; giá trị dựa trên hệ thống đơn vị của bản vẽ.
- **PDF trông như raster?** Đảm bảo `CadDrawTypeMode.UseObjectColor` được đặt để giữ thông tin vector.
- **Hiệu năng với tệp lớn?** Tăng `pageHeight`/`pageWidth` chỉ khi cần; giá trị lớn hơn sẽ tiêu tốn nhiều bộ nhớ hơn.

## Câu hỏi thường gặp

**H: Aspose.CAD có tương thích với mọi phiên bản tệp DWG không?**  
Đ: Aspose.CAD hỗ trợ nhiều phiên bản tệp DWG, đảm bảo tương thích với đa số phần mềm CAD.

**H: Tôi có thể tùy chỉnh phông chữ và định dạng của văn bản đã thêm không?**  
Đ: Có, bạn có thể tùy chỉnh phông, kiểu và các tùy chọn định dạng khác cho văn bản được thêm vào tệp DWG bằng Aspose.CAD.

**H: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?**  
Đ: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng cách nhận bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).

**H: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho Java ở đâu?**  
Đ: Tham khảo tài liệu [tại đây](https://reference.aspose.com/cad/java/) để biết thông tin sâu hơn và các ví dụ.

**H: Làm sao tôi có thể nhận hỗ trợ hoặc trợ giúp với Aspose.CAD?**  
Đ: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được hỗ trợ và kết nối với cộng đồng.

---

**Cập nhật lần cuối:** 2026-02-28  
**Đã kiểm tra với:** Aspose.CAD cho Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}