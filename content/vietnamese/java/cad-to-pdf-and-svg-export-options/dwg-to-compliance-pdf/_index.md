---
title: DWG sang PDF tuân thủ bằng Aspose.CAD cho Java
linktitle: DWG sang PDF tuân thủ
second_title: API Java Aspose.CAD
description: Dễ dàng chuyển đổi các bản vẽ DWG thành các tệp tương thích PDF/A1a và PDF/A1b bằng Aspose.CAD cho Java. Hợp lý hóa quy trình làm việc của bạn một cách chính xác và dễ dàng.
type: docs
weight: 11
url: /vi/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## Giới thiệu

Trong thế giới thiết kế kỹ thuật số ngày càng phát triển, nhu cầu chuyển đổi bản vẽ DWG sang định dạng PDF tuân thủ là rất quan trọng để cộng tác liền mạch và tài liệu được tiêu chuẩn hóa. Aspose.CAD cho Java nổi lên như một công cụ mạnh mẽ, mang lại hiệu quả và độ chính xác trong quy trình này. Trong hướng dẫn này, chúng ta sẽ khám phá cách sử dụng Aspose.CAD cho Java để dễ dàng chuyển đổi các tệp DWG thành các tệp PDF tuân thủ, đảm bảo tuân thủ các tiêu chuẩn PDF/A1a và PDF/A1b.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java đang hoạt động trên hệ thống của mình.
-  Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ[Liên kết tải xuống](https://releases.aspose.com/cad/java/).
- Thư mục tài liệu: Tạo một thư mục để lưu trữ các bản vẽ DWG của bạn.

## Nhập không gian tên

Trong dự án Java của bạn, hãy nhập các vùng tên cần thiết để truy cập các chức năng của Aspose.CAD. Thêm các dòng sau vào đầu tệp Java của bạn:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Bước 1: Đặt thư mục tài nguyên

Xác định đường dẫn đến thư mục tài nguyên của bạn nơi lưu trữ các bản vẽ DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Bước 2: Tải tệp DWG

Tải tệp DWG bằng thư viện Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Bước 3: Tạo tùy chọn PDF

Tạo một phiên bản của PdfOptions và đặt các tùy chọn rasterization vector.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Bước 4: Đặt tùy chọn PDF cốt lõi

Đặt các tùy chọn PDF cốt lõi, chỉ định tiêu chuẩn tuân thủ (PDF/A1a hoặc PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Bước 5: Lưu PDF với Tuân thủ A1a

Lưu tệp PDF tuân thủ A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Bước 6: Thay đổi Tuân thủ thành A1b

Thay đổi tuân thủ thành PDF/A1b và lưu tệp PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Lặp lại các bước này cho mỗi tệp DWG mà bạn muốn chuyển đổi.

## Phần kết luận

Tóm lại, Aspose.CAD cho Java cung cấp một giải pháp mạnh mẽ để chuyển đổi tệp DWG thành tệp PDF tuân thủ. Bằng cách làm theo hướng dẫn từng bước này, bạn có thể hợp lý hóa quy trình chuyển đổi và đảm bảo rằng tài liệu của bạn tuân thủ các tiêu chuẩn ngành.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các phiên bản của tệp DWG không?

 Câu trả lời 1: Aspose.CAD hỗ trợ nhiều phiên bản khác nhau của tệp DWG, bao gồm cả phiên bản mới nhất. Tham khảo đến[tài liệu](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết về khả năng tương thích.

### Câu hỏi 2: Tôi có thể tùy chỉnh cài đặt đầu ra PDF bằng Aspose.CAD không?

A2: Chắc chắn rồi! Aspose.CAD cung cấp nhiều tùy chọn để tùy chỉnh, cho phép bạn điều chỉnh đầu ra PDF theo yêu cầu cụ thể của mình.

### Câu hỏi 3: Aspose.CAD có giấy phép tạm thời không?

 Câu trả lời 3: Có, bạn có thể xin giấy phép tạm thời cho mục đích thử nghiệm từ[liên kết này](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 4: Tôi có thể tìm kiếm sự hỗ trợ hoặc tương tác với cộng đồng cho Aspose.CAD ở đâu?

 A4: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 5: Tôi có thể dùng thử Aspose.CAD miễn phí trước khi mua hàng không?

 A5: Chắc chắn rồi! Tải xuống phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/) để tìm hiểu khả năng trước khi đưa ra quyết định.