---
date: 2025-12-28
description: Tìm hiểu cách tạo PDF từ DWG, lưu DWG dưới dạng PDF và thêm văn bản vào
  bản vẽ DWG bằng Aspose.CAD cho Java — hướng dẫn từng bước.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Tạo PDF từ DWG và Thêm Văn bản bằng Aspose.CAD cho Java
url: /vi/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ DWG và Thêm Văn Bản Sử Dụng Aspose.CAD cho Java

## Giới thiệu

Nếu bạn cần **tạo PDF từ DWG** và đồng thời chèn văn bản tùy chỉnh, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn toàn bộ quy trình — tải bản vẽ DWG, thêm chú thích văn bản, và cuối cùng lưu kết quả dưới dạng PDF bằng Aspose.CAD cho Java. Khi kết thúc, bạn sẽ hiểu cách **lưu DWG dưới dạng PDF**, tùy chỉnh chiều cao văn bản, và thậm chí thêm các chú thích cơ bản.

## Câu trả lời nhanh
- **Có thể chuyển DWG sang PDF trong Java không?** Yes, Aspose.CAD for Java provides a straightforward API.  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** A commercial license is required; a free trial is available.  
- **Phương pháp nào thêm văn bản vào DWG?** Use the `CadText` object and add it to the model space.  
- **Tôi có thể đặt chiều cao văn bản không?** Absolutely—use `setTextHeight()` on the `CadText` instance.  
- **Kết quả có phải dựa trên vector không?** When rasterization options are set to `UseObjectColor`, the PDF retains high‑quality vector data.

## Yêu cầu trước

Before diving into the tutorial, ensure you have the following prerequisites in place:

- **Thư viện Aspose.CAD cho Java:** Download and install the library from the [trang Aspose.CAD cho Java](https://releases.aspose.com/cad/java/).

- **Bộ công cụ phát triển Java (JDK):** Make sure you have the latest JDK installed on your system.

- **Bản vẽ DWG:** Prepare a DWG drawing file where you want to add text.

## Nhập không gian tên

In your Java code, import the necessary namespaces for Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, chúng ta sẽ phân tích đoạn mã được cung cấp thành nhiều bước:

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

## Bước 7: Lưu DWG đã chỉnh sửa dưới dạng PDF (dwg sang pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Bằng cách thực hiện các bước này, bạn sẽ có thể **tạo PDF từ DWG**, thêm văn bản tùy chỉnh và kiểm soát chiều cao văn bản — chỉ với vài dòng mã Java.

## Tại sao cần Thêm Văn bản vào DWG và Chuyển đổi sang PDF?

Adding text directly to a DWG file is useful for:

- **Ghi chú thiết kế** with notes or part numbers.
- **Tạo tài liệu có thể in** where the PDF serves as a read‑only, widely supported format.
- **Tự động hoá xử lý hàng loạt** of large CAD libraries without manual editing.

## Vấn đề Thường gặp & Mẹo

- **Văn bản không hiển thị?** Verify the X/Y coordinates are within the drawing extents and that the layer is visible.
- **Chiều cao văn bản không đúng?** Adjust `setTextHeight()`; the value is in the drawing’s unit system.
- **PDF trông bị raster hoá?** Ensure `CadDrawTypeMode.UseObjectColor` is set to keep vector information.
- **Hiệu năng trên tệp lớn?** Increase `pageHeight`/`pageWidth` only as needed; larger values consume more memory.

## Câu hỏi Thường gặp

**Q: Aspose.CAD có tương thích với mọi phiên bản của tệp DWG không?**  
A: Aspose.CAD supports various versions of DWG files, ensuring compatibility with a wide range of CAD software.

**Q: Tôi có thể tùy chỉnh phông chữ và định dạng của văn bản đã thêm không?**  
A: Yes, you can customize the font, style, and other formatting options for the text added to DWG files using Aspose.CAD.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?**  
A: Yes, you can explore the features of Aspose.CAD by obtaining a free trial from [đây](https://releases.aspose.com/).

**Q: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho Java ở đâu?**  
A: Refer to the documentation [tại đây](https://reference.aspose.com/cad/java/) for in-depth information and examples.

**Q: Làm thế nào tôi có thể nhận hỗ trợ hoặc tìm kiếm trợ giúp cho Aspose.CAD?**  
A: Visit the [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) to get assistance and connect with the community.

---

**Cập nhật lần cuối:** 2025-12-28  
**Được kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}