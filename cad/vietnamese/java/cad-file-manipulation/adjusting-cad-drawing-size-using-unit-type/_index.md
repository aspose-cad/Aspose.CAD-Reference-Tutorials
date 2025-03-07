---
title: Điều chỉnh kích thước bản vẽ CAD bằng loại đơn vị với Aspose.CAD cho Java
linktitle: Điều chỉnh kích thước bản vẽ CAD bằng loại đơn vị
second_title: API Java Aspose.CAD
description: Khám phá sức mạnh của Aspose.CAD cho Java trong việc điều chỉnh kích thước bản vẽ CAD một cách dễ dàng. Hãy làm theo hướng dẫn từng bước của chúng tôi để có được độ chính xác và khả năng thích ứng.
weight: 14
url: /vi/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Điều chỉnh kích thước bản vẽ CAD bằng loại đơn vị với Aspose.CAD cho Java

## Giới thiệu

Trong lĩnh vực Thiết kế có sự hỗ trợ của máy tính (CAD) ngày càng phát triển, độ chính xác và khả năng thích ứng là điều tối quan trọng. Một yêu cầu chung là điều chỉnh kích thước bản vẽ CAD dựa trên các loại đơn vị cụ thể. Aspose.CAD cho Java nổi lên như một đồng minh mạnh mẽ, cung cấp khả năng liền mạch để thao tác các tệp CAD theo chương trình.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Môi trường phát triển Java: Đảm bảo rằng bạn đã thiết lập môi trường phát triển Java chức năng trên máy của mình.

-  Thư viện Aspose.CAD cho Java: Tải xuống và tích hợp thư viện Aspose.CAD vào dự án Java của bạn. Bạn có thể lấy thư viện[đây](https://releases.aspose.com/cad/java/).

## Nhập không gian tên

Trong mã Java của bạn, hãy bao gồm các vùng tên cần thiết để truy cập các chức năng của Aspose.CAD. Thêm các mục nhập sau:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bây giờ, hãy chia nhỏ quy trình điều chỉnh kích thước bản vẽ CAD bằng loại đơn vị thành các bước có thể quản lý:

## Bước 1: Xác định thư mục dữ liệu

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Đặt đường dẫn cho thư mục chứa tệp CAD của bạn.

## Bước 2: Tải bản vẽ CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Tải bản vẽ CAD bằng Aspose.CAD's`Image` lớp học.

## Bước 3: Tạo tùy chọn BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Khởi tạo`BmpOptions` lớp để xuất bố cục CAD sang định dạng BMP.

## Bước 4: Định cấu hình tùy chọn Rasterization

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Tạo một thể hiện của`CadRasterizationOptions` và liên kết nó với`BmpOptions` để rasterization vector.

## Bước 5: Đặt loại đơn vị

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Chỉ định loại đơn vị mong muốn cho bản vẽ CAD. Trong ví dụ này, chúng tôi đặt nó thành Centimet.

## Bước 6: Đặt bố cục

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Xác định bố cục sẽ được xem xét trong quá trình xuất. Trong trường hợp này, chúng tôi đã chọn bố cục "Mô hình".

## Bước 7: Xuất sang BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Cuối cùng, lưu bản vẽ CAD đã sửa đổi ở định dạng BMP.

## Phần kết luận

Với Aspose.CAD cho Java, việc điều chỉnh kích thước bản vẽ CAD trở nên dễ dàng. Hướng dẫn này đã hướng dẫn bạn thực hiện quy trình, nhấn mạnh tầm quan trọng của từng bước trong việc đạt được kết quả chính xác.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các ngôn ngữ lập trình khác không?

Câu trả lời 1: Aspose.CAD chủ yếu hỗ trợ Java, nhưng cũng có phiên bản dành cho các ngôn ngữ khác như .NET.

### Câu 2: Có bất kỳ tùy chọn cấp phép nào cho Aspose.CAD không?

 Câu trả lời 2: Có, bạn có thể khám phá các tùy chọn cấp phép và mua Aspose.CAD[đây](https://purchase.aspose.com/buy).

### Câu 3: Aspose.CAD có bản dùng thử miễn phí không?

 A3: Chắc chắn, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho Java?

 A4: Truy cập diễn đàn Aspose.CAD[đây](https://forum.aspose.com/c/cad/19) để được hỗ trợ toàn diện.

### Câu hỏi 5: Tôi có thể xin giấy phép tạm thời cho Aspose.CAD không?

 Câu trả lời 5: Có, bạn có thể lấy giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
