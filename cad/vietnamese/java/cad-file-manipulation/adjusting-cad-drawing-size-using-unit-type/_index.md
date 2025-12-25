---
date: 2025-12-25
description: Tìm hiểu cách xuất DWG sang BMP bằng Aspose.CAD cho Java. Hướng dẫn từng
  bước này cho thấy cách điều chỉnh kích thước bản vẽ CAD và chuyển đổi CAD sang BMP
  một cách hiệu quả.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Xuất DWG sang BMP – Điều chỉnh kích thước CAD bằng loại đơn vị (Java)
url: /vi/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG sang BMP – Điều chỉnh kích thước bản vẽ CAD bằng Loại Đơn vị với Aspose.CAD cho Java

## Giới thiệu

Khi bạn cần **xuất DWG sang BMP**, việc kiểm soát kích thước và đơn vị đo của kết quả là rất quan trọng cho các quy trình xử lý tiếp theo hoặc in ấn. Trong hướng dẫn này, bạn sẽ học cách điều chỉnh kích thước bản vẽ CAD và chuyển đổi CAD sang BMP với Aspose.CAD cho Java, sử dụng thuộc tính `UnitType` để xác định đơn vị đo. Các bước được giải thích bằng ngôn ngữ đơn giản, vì vậy ngay cả khi bạn mới bắt đầu với thư viện cũng có thể theo dõi.

## Câu trả lời nhanh
- **“Xuất DWG sang BMP” có nghĩa là gì?** Chuyển đổi một bản vẽ DWG thành ảnh raster BMP.  
- **Thuộc tính nào kiểm soát kích thước đầu ra?** `CadRasterizationOptions.setUnitType()` đặt đơn vị (ví dụ: centimet).  
- **Tôi có cần giấy phép để chạy mã không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép cần thiết cho môi trường sản xuất.  
- **Tôi có thể chọn các layout khác không?** Có, dùng `setLayouts()` để chỉ định layout không gian mô hình hoặc không gian giấy.  
- **Các định dạng đầu ra nào được hỗ trợ?** Ngoài BMP, bạn có thể xuất sang PNG, JPEG, TIFF, v.v., bằng cách thay đổi lớp tùy chọn.

## **Xuất DWG sang BMP** là gì?

Xuất DWG sang BMP có nghĩa là raster hoá một tệp DWG dựa trên vector thành một ảnh bitmap (BMP). Điều này hữu ích khi bạn cần một biểu diễn pixel‑perfect cho các hệ thống kế thừa, quy trình xử lý ảnh, hoặc các trường hợp hiển thị đơn giản.

## Tại sao cần điều chỉnh kích thước bản vẽ CAD bằng **Loại Đơn vị**?

Việc đặt loại đơn vị cho phép bạn kiểm soát kích thước thực tế của ảnh xuất ra mà không phải tính toán các hệ số tỉ lệ thủ công. Điều này đảm bảo bitmap khớp với các đo lường thực tế (ví dụ: centimet), rất quan trọng đối với bản vẽ kỹ thuật và tài liệu in ấn.

## Yêu cầu trước

Trước khi bắt đầu hướng dẫn, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- **Môi trường phát triển Java** – Một JDK hoạt động (phiên bản 8 trở lên) và một IDE hoặc công cụ xây dựng (Maven/Gradle).  
- **Thư viện Aspose.CAD cho Java** – Tải xuống và tích hợp thư viện Aspose.CAD vào dự án Java của bạn. Bạn có thể lấy thư viện [tại đây](https://releases.aspose.com/cad/java/).

## Nhập các namespace

Trong mã Java của bạn, bao gồm các namespace cần thiết để truy cập các chức năng của Aspose.CAD. Thêm các import sau:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bây giờ, chúng ta sẽ phân tích quy trình điều chỉnh kích thước bản vẽ CAD bằng loại đơn vị thành các bước dễ quản lý:

## Bước 1: Xác định thư mục dữ liệu

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Đặt đường dẫn cho thư mục chứa các tệp CAD của bạn.

## Bước 2: Tải bản vẽ CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Tải bản vẽ CAD bằng lớp `Image` của Aspose.CAD.

## Bước 3: Tạo tùy chọn BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Khởi tạo lớp `BmpOptions` để xuất layout CAD sang định dạng BMP.

## Bước 4: Cấu hình tùy chọn raster hoá

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Tạo một thể hiện của `CadRasterizationOptions` và liên kết nó với `BmpOptions` để raster hoá vector.

## Bước 5: Đặt Loại Đơn vị

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Chỉ định loại đơn vị mong muốn cho bản vẽ CAD. Trong ví dụ này, chúng tôi đã đặt **Centimeter**, ảnh hưởng trực tiếp đến kích thước ảnh xuất ra khi bạn **điều chỉnh kích thước bản vẽ CAD**.

## Bước 6: Đặt Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Xác định các layout sẽ được xem xét trong quá trình xuất. Trong trường hợp này, chúng tôi đã chọn layout **"Model"**, nhưng bạn có thể chuyển sang layout không gian giấy nếu cần.

## Bước 7: Xuất sang BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Cuối cùng, lưu bản vẽ CAD đã chỉnh sửa dưới dạng BMP. Bước này hoàn thành quy trình **xuất DWG sang BMP** đồng thời giữ lại các điều chỉnh kích thước bạn đã cấu hình.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **Ảnh đầu ra quá nhỏ** | Loại đơn vị chưa được đặt hoặc mặc định (pixel) | Gọi `setUnitType()` với đơn vị mong muốn (ví dụ: `UnitType.Centimeter`). |
| **Xuất sai layout** | Tên layout bị lỗi chính tả | Kiểm tra tên layout bằng phần mềm xem CAD; sử dụng chuỗi chính xác trong `setLayouts()`. |
| **Lỗi giấy phép** | Chạy mà không có giấy phép hợp lệ trong môi trường sản xuất | Áp dụng giấy phép tạm thời hoặc vĩnh viễn như mô tả trong FAQ. |

## Câu hỏi thường gặp (Mở rộng)

**H: Tôi có thể dùng Aspose.CAD cho Java với các ngôn ngữ lập trình khác không?**  
Đ: Aspose.CAD chủ yếu hỗ trợ Java, nhưng cũng có các phiên bản cho các ngôn ngữ khác như .NET.

**H: Có các tùy chọn giấy phép nào cho Aspose.CAD không?**  
Đ: Có, bạn có thể khám phá các tùy chọn giấy phép và mua Aspose.CAD [tại đây](https://purchase.aspose.com/buy).

**H: Có bản dùng thử miễn phí cho Aspose.CAD không?**  
Đ: Chắc chắn, bạn có thể truy cập bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**H: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho Java?**  
Đ: Truy cập diễn đàn Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19) để được hỗ trợ toàn diện.

**H: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD không?**  
Đ: Có, bạn có thể mua giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2025-12-25  
**Được kiểm tra với:** Aspose.CAD cho Java 24.10  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}