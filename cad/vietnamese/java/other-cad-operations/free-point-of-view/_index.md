---
title: Kết xuất quan điểm miễn phí với Aspose.CAD cho Java
linktitle: Quan điểm miễn phí
second_title: API Java Aspose.CAD
description: Khám phá sức mạnh của Aspose.CAD cho Java trong hướng dẫn này để đạt được khả năng hiển thị quan điểm miễn phí cho các bản vẽ CAD. Giải phóng tiềm năng của Aspose.CAD.
weight: 14
url: /vi/java/other-cad-operations/free-point-of-view/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kết xuất quan điểm miễn phí với Aspose.CAD cho Java

## Giới thiệu

Chào mừng bạn đến với "Hướng dẫn quan điểm miễn phí - Aspose.CAD cho Java." Trong hướng dẫn toàn diện này, chúng tôi sẽ hướng dẫn bạn quy trình tận dụng Aspose.CAD cho Java để đạt được khả năng hiển thị quan điểm miễn phí cho các bản vẽ CAD. Aspose.CAD là một thư viện Java mạnh mẽ cung cấp nhiều tính năng để làm việc với các tệp Thiết kế hỗ trợ máy tính (CAD). Hướng dẫn sẽ bao gồm các điều kiện tiên quyết cần thiết, nhập các gói thiết yếu và chia nhỏ từng ví dụ thành hướng dẫn từng bước.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
-  Thư viện Aspose.CAD cho Java: Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ[Liên kết tải xuống](https://releases.aspose.com/cad/java/).
- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt Java trên máy của mình.

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Thêm các dòng mã sau vào đầu tệp Java của bạn:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

Các gói này rất cần thiết để làm việc với các tệp CAD và tùy chỉnh các tùy chọn kết xuất.

Bây giờ, hãy chia ví dụ được cung cấp thành nhiều bước:

## Bước 1: Thiết lập thư mục tài liệu của bạn

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Thay thế "Thư mục tài liệu của bạn" bằng đường dẫn đến thư mục tài liệu thực tế của bạn.

## Bước 2: Tải bản vẽ CAD

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

Chỉ định đường dẫn đến bản vẽ CAD của bạn và tải nó bằng cách sử dụng`Image` lớp học.

## Bước 3: Định cấu hình tùy chọn Rasterization CAD

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

Tùy chỉnh các tùy chọn tạo điểm ảnh CAD theo yêu cầu của bạn, chẳng hạn như chiều cao và chiều rộng của trang.

## Bước 4: Thiết lập JpegOptions

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Tạo một thể hiện của`JpegOptions` và liên kết nó với các tùy chọn rasterization đã được cấu hình trước đó.

## Bước 5: Xác định góc quay

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

Chỉ định các góc xoay dọc theo trục X, Y và Z để hiển thị điểm nhìn tự do.

## Bước 6: Lưu hình ảnh được hiển thị

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

Lưu hình ảnh được hiển thị với các tùy chọn đã chỉ định vào vị trí mong muốn.

Lặp lại các bước này cho trường hợp sử dụng cụ thể của bạn, đảm bảo hiển thị quan điểm miễn phí cho bản vẽ CAD của bạn.

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách triển khai kết xuất quan điểm miễn phí bằng Aspose.CAD cho Java. Hướng dẫn này bao gồm các bước cần thiết, từ thiết lập các điều kiện tiên quyết đến tùy chỉnh các tùy chọn kết xuất và lưu hình ảnh đầu ra.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java trên nhiều nền tảng không?

Câu trả lời 1: Có, Aspose.CAD cho Java độc lập với nền tảng và có thể được sử dụng trên nhiều hệ điều hành khác nhau.

### Câu hỏi 2: Có bất kỳ tùy chọn cấp phép nào cho Aspose.CAD cho Java không?

 Câu trả lời 2: Có, bạn có thể khám phá các tùy chọn cấp phép và mua hàng[đây](https://purchase.aspose.com/buy).

### Câu 3: Có bản dùng thử miễn phí không?

 Câu trả lời 3: Có, bạn có thể truy cập phiên bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể tìm hỗ trợ cho Aspose.CAD cho Java ở đâu?

 A4: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 5: Làm cách nào để có được giấy phép tạm thời?

 A5: Xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
