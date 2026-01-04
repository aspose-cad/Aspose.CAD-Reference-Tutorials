---
date: 2026-01-04
description: Tìm hiểu cách **lưu CAD dưới dạng PNG** và xuất các đối tượng OLE một
  cách dễ dàng từ các tệp CAD bằng Aspose.CAD cho Java. Thiết lập nhanh, mẫu mã đầy
  đủ và các mẹo thực hành tốt nhất.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Lưu CAD dưới dạng PNG và Xuất các Đối tượng OLE với Aspose.CAD cho Java
url: /vi/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu CAD dưới dạng PNG và Xuất các Đối tượng OLE với Aspose.CAD cho Java

## Giới thiệu

Trong thế giới thiết kế hỗ trợ máy tính (CAD) đang phát triển nhanh, khả năng **lưu CAD dưới dạng PNG** đồng thời trích xuất các đối tượng OLE (Object Linking and Embedding) nhúng có thể giúp tối ưu hoá quy trình làm việc của bạn một cách đáng kể. Dù bạn đang xây dựng công cụ chuyển đổi hàng loạt, tạo thumbnail cho cổng thông tin web, hay chỉ cần lưu trữ nội dung OLE, Aspose.CAD cho Java cung cấp cách tiếp cận sạch sẽ, lập trình được. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình, từ thiết lập dự án đến việc xuất mỗi đối tượng OLE dưới dạng ảnh PNG.

## Câu trả lời nhanh
- **Có thể xuất trực tiếp các đối tượng OLE sang PNG không?** Có – Aspose.CAD tải file CAD và cho phép bạn raster hoá mỗi layout thành PNG.  
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc mới hơn.  
- **Cần giấy phép cho tính năng này không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép cần thiết cho môi trường sản xuất.  
- **Dữ liệu vector có được giữ lại không?** Quá trình raster hoá PNG giữ độ trung thực hình ảnh, nhưng kết quả là raster, không phải vector.  
- **Có hỗ trợ xử lý hàng loạt không?** Chắc chắn – lặp qua mảng các file như trong ví dụ mã nguồn.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- **Java Development Kit (JDK)** – Cài đặt và cấu hình Java 8+.  
- **Aspose.CAD cho Java** – Tải thư viện mới nhất từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  
- **Các file nguồn CAD** – Bất kỳ file DWG/DXF/DGN nào chứa các đối tượng OLE mà bạn muốn xuất.

## Nhập các Namespace

Để làm việc với file CAD, bạn cần nhập các lớp cốt lõi của Aspose.CAD. Giữ nguyên khối import như sau – nó cung cấp các lớp sẽ được dùng sau này trong hướng dẫn.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Cách Lưu CAD dưới dạng PNG

Dưới đây là hướng dẫn ngắn gọn, từng bước, cho thấy **cách xuất các đối tượng OLE và lưu CAD dưới dạng PNG**. Mỗi bước bao gồm một giải thích ngắn và đoạn mã chính xác bạn cần sao chép vào dự án.

### Bước 1: Đặt Thư Mục Tài Liệu

Xác định thư mục chứa các bản vẽ CAD của bạn. Thay thế placeholder bằng đường dẫn thực tế trên máy của bạn.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Bước 2: Định Nghĩa Tên File CAD

Liệt kê mọi file CAD bạn muốn xử lý. Bạn có thể thêm bao nhiêu mục tùy thích.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Bước 3: Thiết Lập Tùy Chọn Xuất PNG

Cấu hình các thiết lập raster hoá. Ở đây chúng ta mục tiêu vào một layout cụ thể (`Layout1`) và sử dụng các tùy chọn PNG mặc định.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Bước 4: Lặp Qua Các File CAD và Lưu dưới dạng PNG

Tải mỗi file CAD, raster hoá các đối tượng OLE, và ghi file PNG đầu ra. Hậu tố `_out.png` giúp bạn nhận diện các ảnh đã tạo.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Các Vấn Đề Thường Gặp và Giải Pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|--------|-------------|-----------|
| **`Image.load` gây ra `FileNotFoundException`** | Đường dẫn `dataDir` không đúng hoặc tên file bị sai. | Kiểm tra lại chuỗi thư mục và đảm bảo tên file khớp chính xác, kể cả khoảng trắng. |
| **PNG đầu ra bị trắng** | Tên layout không tồn tại trong file CAD nguồn. | Dùng `cadImage.getLayouts()` để liệt kê các layout có sẵn, sau đó cập nhật `rasterizationOptions.setLayouts(...)`. |
| **File CAD lớn gây OutOfMemoryError** | Raster hoá ảnh độ phân giải cao tiêu tốn nhiều bộ nhớ heap. | Tăng kích thước heap JVM (`-Xmx2g`) hoặc giảm độ phân giải raster hoá bằng `rasterizationOptions.setResolution(...)`. |

## Câu Hỏi Thường Gặp

### Q1: Aspose.CAD có tương thích với mọi định dạng file CAD không?

A1: Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF và DGN. Tham khảo [tài liệu](https://reference.aspose.com/cad/java/) để biết danh sách đầy đủ.

### Q2: Tôi có thể tùy chỉnh các thiết lập xuất cho các đối tượng OLE không?

A2: Có, Aspose.CAD cung cấp nhiều tùy chọn để tùy chỉnh thiết lập xuất, cho phép bạn điều chỉnh đầu ra theo yêu cầu cụ thể.

### Q3: Có bản dùng thử miễn phí cho Aspose.CAD không?

A3: Có, bạn có thể khám phá khả năng của Aspose.CAD bằng cách lấy bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).

### Q4: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD ở đâu?

A4: Tham gia cộng đồng Aspose.CAD tại [diễn đàn](https://forum.aspose.com/c/cad/19) để nhận trợ giúp và chia sẻ kinh nghiệm.

### Q5: Làm sao để mua giấy phép cho Aspose.CAD?

A5: Truy cập [trang mua hàng](https://purchase.aspose.com/buy) để mua giấy phép phù hợp với nhu cầu phát triển của bạn.

## Kết luận

Bằng cách thực hiện năm bước đơn giản này, bạn có thể **lưu CAD dưới dạng PNG** và trích xuất mọi đối tượng OLE nhúng chỉ với vài dòng mã Java. Cách tiếp cận này lý tưởng cho việc chuyển đổi hàng loạt, báo cáo tự động, hoặc bất kỳ kịch bản nào cần ảnh raster của nội dung CAD mà không cần xuất thủ công. Hãy thoải mái thử nghiệm các tùy chọn raster hoá khác nhau để đáp ứng yêu cầu về chất lượng và hiệu năng của bạn.

---

**Cập nhật lần cuối:** 2026-01-04  
**Đã kiểm tra với:** Aspose.CAD cho Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}