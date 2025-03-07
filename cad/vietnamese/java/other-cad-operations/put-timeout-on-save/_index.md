---
title: Hết thời gian lưu cho CAD với Aspose.CAD
linktitle: Đặt thời gian chờ để lưu
second_title: API Java Aspose.CAD
description: Tìm hiểu cách tăng hiệu suất ứng dụng Java của bạn với Aspose.CAD. Đặt thời gian chờ để lưu bản vẽ CAD. Thực hiện theo hướng dẫn từng bước của chúng tôi.
weight: 15
url: /vi/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hết thời gian lưu cho CAD với Aspose.CAD

## Giới thiệu

Chào mừng bạn đến với hướng dẫn về cách đặt thời gian chờ khi lưu bằng Aspose.CAD cho Java. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình đặt thời gian chờ để lưu bản vẽ CAD nhằm nâng cao hiệu suất ứng dụng của bạn. Aspose.CAD cho Java là một thư viện mạnh mẽ cho phép bạn làm việc liền mạch với các tệp CAD trong ứng dụng Java của mình.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
-  Thư viện Aspose.CAD cho Java: Đảm bảo rằng bạn đã tích hợp thư viện Aspose.CAD cho Java vào dự án của mình. Bạn có thể tải xuống thư viện từ[trang mạng](https://releases.aspose.com/cad/java/).
- Môi trường phát triển: Thiết lập môi trường phát triển Java của bạn với tất cả các công cụ và phụ thuộc cần thiết.

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Thêm các dòng sau vào đầu tệp Java của bạn:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Bây giờ, hãy chia mã ví dụ thành các hướng dẫn từng bước:

## Bước 1: Đặt thư mục nguồn và đầu ra

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Đảm bảo bạn có đúng thư mục nguồn và đầu ra cho bản vẽ CAD của mình.

## Bước 2: Tạo nguồn mã thông báo gián đoạn

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Khởi tạo nguồn mã thông báo gián đoạn để quản lý các gián đoạn trong quá trình lưu.

## Bước 3: Tải bản vẽ CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Tải bản vẽ CAD vào một`CadImage` sự vật.

## Bước 4: Định cấu hình tùy chọn Rasterization

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Định cấu hình các tùy chọn rasterization cho bản vẽ CAD.

## Bước 5: Định cấu hình tùy chọn PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Thiết lập các tùy chọn PDF với các tùy chọn tạo điểm ảnh vector và mã thông báo gián đoạn.

## Bước 6: Lưu bản vẽ với thời gian chờ

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Lưu bản vẽ CAD vào tệp PDF với thời gian chờ được chỉ định.

## Bước 7: Xử lý sự gián đoạn

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Tạo một luồng để xử lý thao tác lưu và ngắt nó sau một khoảng thời gian chờ được chỉ định.

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách đặt thời gian chờ khi lưu bằng Aspose.CAD cho Java. Tính năng này có thể nâng cao đáng kể hiệu quả của các ứng dụng liên quan đến CAD của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Làm cách nào tôi có thể tải xuống Aspose.CAD cho Java?

 A1: Bạn có thể tải xuống từ[trang phát hành](https://releases.aspose.com/cad/java/).

### Câu hỏi 2: Tôi có thể tìm tài liệu về Aspose.CAD cho Java ở đâu?

 A2: Tham khảo[tài liệu](https://reference.aspose.com/cad/java/) để biết thông tin toàn diện.

### Câu 3: Có bản dùng thử miễn phí không?

Câu trả lời 3: Có, bạn có thể dùng thử miễn phí từ[liên kết này](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào để có được giấy phép tạm thời?

 A4: Thăm quan[đây](https://purchase.aspose.com/temporary-license/) để biết chi tiết giấy phép tạm thời.

### Câu 5: Cần trợ giúp hoặc có thắc mắc?

 A5: Đi tới[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
