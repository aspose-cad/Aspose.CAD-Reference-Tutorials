---
date: 2026-01-12
description: Tìm hiểu cách thêm hình ảnh vào tệp DWG bằng Aspose.CAD cho Java và chuyển
  đổi DWG sang PDF. Thực hiện theo hướng dẫn từng bước của chúng tôi để phát triển
  hiệu quả.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Thêm hình ảnh vào tệp DWG một cách dễ dàng bằng Aspose.CAD Java
url: /vi/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm Hình Ảnh vào Tệp DWG Một Cách Dễ Dàng Sử Dụng Aspose.CAD Java

Trong các ứng dụng Java hiện đại, **việc thêm hình ảnh vào DWG** là một yêu cầu phổ biến—cho dù bạn đang xây dựng một trình xem CAD, tự động cập nhật bản vẽ, hoặc tạo tài liệu. Aspose.CAD cho Java cung cấp cho bạn một cách đơn giản, hiệu suất cao để nhúng hình ảnh raster trực tiếp vào bản vẽ DWG mà không cần một engine CAD đầy đủ. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn qua toàn bộ quy trình, từ việc tải DWG đến xuất kết quả dưới dạng PDF.

## Trả Lời Nhanh
- **Thư viện tôi cần là gì?** Aspose.CAD for Java  
- **Tôi cũng có thể xuất ra PDF không?** Có – sử dụng `PdfOptions` cùng với `CadRasterizationOptions`  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một việc nhập ảnh cơ bản

## “Thêm hình ảnh vào dwg” là gì?
Thêm một hình ảnh vào tệp DWG có nghĩa là chèn một bức tranh raster (PNG, JPEG, v.v.) dưới dạng đối tượng `CadRasterImage` vào không gian mô hình (model space) của bản vẽ. Hình ảnh sẽ trở thành một phần của cây thực thể CAD và có thể được định vị, thay đổi tỷ lệ và cắt xén giống như bất kỳ đối tượng CAD nào khác.

## Tại sao nên dùng Aspose.CAD cho Java để thêm hình ảnh vào dwg?
- **Không cần phần mềm CAD** – API tự xử lý việc phân tích DWG nội bộ.  
- **Kiểm soát chi tiết** vị trí chèn, vectơ tỷ lệ và cắt xén.  
- **Tích hợp chuyển đổi PDF** để bạn có thể tạo PDF có thể in trong cùng quy trình.  
- **Đa nền tảng** – hoạt động trên Windows, Linux và macOS.

## Yêu Cầu Trước
- Aspose.CAD for Java: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/cad/java/).  
- Môi Trường Phát Triển Java: JDK 8+ với IDE yêu thích của bạn (IntelliJ, Eclipse, VS Code, v.v.).

## Nhập Gói
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hướng Dẫn Từng Bước

### Bước 1: Tải Tệp DWG
Đầu tiên, chỉ đến thư mục chứa bản vẽ DWG của bạn và tải nó bằng `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Bước 2: Định Nghĩa Định Dạng Hình Raster
Tạo một `CadRasterImageDef` tham chiếu tới file PNG bên ngoài mà bạn muốn nhúng. Hàm khởi tạo nhận tên file ảnh và kích thước pixel của nó.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Bước 3: Đặt Điểm Chèn và Vectơ Tỷ Lệ
Điểm chèn xác định vị trí góc trái‑dưới của ảnh sẽ xuất hiện. Các vectơ **U** và **V** kiểm soát tỷ lệ theo chiều ngang và chiều dọc.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Bước 4: Tạo Đối Tượng CadRasterImage
Kết hợp định nghĩa, điểm chèn và các vectơ thành một `CadRasterImage`. Bạn cũng có thể đặt giới hạn cắt xén nếu chỉ muốn một phần của bức tranh hiển thị.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Bước 5: Thêm Ảnh Vào Model Space
Chèn hình raster vào khối `*Model_Space`, sau đó cập nhật bộ sưu tập đối tượng của bản vẽ để định nghĩa được lưu lại.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Bước 6: Cấu Hình Tùy Chọn Xuất PDF (Tùy Chọn)
Nếu bạn cũng cần một phiên bản PDF của bản vẽ, cấu hình `PdfOptions` cùng với `CadRasterizationOptions`. Bước này minh họa cách **chuyển đổi dwg sang pdf** trong cùng một luồng.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Bước 7: Lưu PDF Đã Được Chỉnh Sửa
Cuối cùng, xuất bản vẽ đã chỉnh sửa dưới dạng tệp PDF. Cùng một thể hiện `image` được sử dụng, vì vậy PDF sẽ phản ánh hình raster mới được thêm.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Bằng cách thực hiện các bước trên, bạn có thể **thêm hình ảnh vào dwg** một cách nhanh chóng và cũng **lưu dwg dưới dạng pdf** nếu cần.

## Các Vấn Đề Thường Gặp và Giải Pháp
- **Ảnh không hiển thị** – Kiểm tra lại đường dẫn file ảnh (`road-sign-custom.png`) có đúng không và kích thước ảnh có khớp với các giá trị truyền vào `CadRasterImageDef`.  
- **Tỷ lệ không đúng** – Điều chỉnh các vectơ U và V; chúng đại diện cho đơn vị bản vẽ trên mỗi pixel.  
- **PDF trống** – Đảm bảo `CadRasterizationOptions.setDrawType` được đặt thành `UseObjectColor` hoặc chế độ phù hợp khác.

## Câu Hỏi Thường Gặp

**H: Aspose.CAD cho Java có tương thích với mọi môi trường phát triển Java không?**  
Đ: Có, Aspose.CAD cho Java tương thích với hầu hết các môi trường phát triển Java.

**H: Tôi có thể sử dụng Aspose.CAD cho Java cho các dự án thương mại không?**  
Đ: Có, bạn có thể sử dụng Aspose.CAD cho Java cho các dự án thương mại. Tham khảo chi tiết giấy phép [tại đây](https://purchase.aspose.com/buy).

**H: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?**  
Đ: Có, bạn có thể truy cập bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**H: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho Java?**  
Đ: Bạn có thể tìm kiếm hỗ trợ trên [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

**H: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD cho Java không?**  
Đ: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

---

**Cập Nhật Lần Cuối:** 2026-01-12  
**Kiểm Tra Với:** Aspose.CAD for Java 24.11  
**Tác Giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}