---
date: 2025-12-22
description: Tìm hiểu cách xuất bản vẽ CAD và chuyển đổi DWG sang BMP trong Java với
  Aspose.CAD. Hãy làm theo hướng dẫn từng bước này để thao tác tệp CAD một cách hiệu
  quả.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Cách xuất bản vẽ CAD sang BMP bằng Aspose.CAD cho Java
url: /vi/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất CAD Drawing sang BMP bằng Aspise.CAD cho Java

## Introduction

Nếu bạn đang tìm kiếm một cách rõ ràng, đáng tin cậy để **how to export cad** files từ Java, bạn đã đến đúng nơi. Với Aspose.CAD cho Java bạn không chỉ có thể tự động điều chỉnh kích thước bản vẽ mà còn **convert DWG to BMP** chỉ trong vài dòng code. Hướng dẫn này sẽ dẫn bạn qua toàn bộ quá trình, từ thiết lập môi trường đến tạo ảnh BMP giữ nguyên bố cục CAD gốc.

## Quick Answers
- **What does “how to export cad” mean?** Nó đề cập đến việc chuyển đổi các tệp CAD (DWG, DXF, v.v.) sang định dạng khác như BMP, PNG hoặc PDF.  
- **Which library handles the conversion?** Aspose.CAD for Java cung cấp một API đơn giản cho nhiệm vụ này.  
- **Do I need a license?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **Can I export multiple layouts at once?** Có – bằng cách đặt thuộc tính `Layouts` bạn có thể chỉ định các layout cần render.  
- **Is BMP the only output format?** Không – bạn cũng có thể xuất sang PNG, JPEG, TIFF và nhiều định dạng khác.

## What is “how to export cad” with Aspose.CAD?
Xuất CAD có nghĩa là lấy một bản vẽ CAD gốc (ví dụ: tệp DWG) và render nó hình ảnh raster hoặc một định dạng vector khác. Aspose.CAD thực hiện toàn bộ công việc nặng: phân tích cấu trúc CAD, raster hóa các thực thể vector, và ghi kết quả vào định dạng ảnh bạn chọn.

## Why use Aspose.CAD for Java to **convert DWG to BMP**?
- **Không phụ thuộc bên ngoài** – thuần Java, không cần DLL native.  
- **Hỗ trợ đầy đủ cho DWG, DXF, DGN và các định dạng khác**.  
- **Kiểm soát chi tiết** các tùy chọn raster hóa như lựa chọn layout, tỷ lệ, và màu nền.  
- **Hiệu năng cao** phù hợp cho xử lý batch trên máy chủ.

## Prerequisites

Trước khi bắt đầu, hãy chắc chắn bạn có các mục sau:

1. **Java Development Kit** – tải về [here](https://www.java.com/en/download/).  
2. **Aspose.CAD for Java library** – lấy JAR mới nhất từ [here](https://releases.aspose.com/cad/java/).  
3. **Sample CAD file** – một tệp DWG (ví dụ `sample.dwg`) đặt trong thư mục tài liệu của dự án.

## Import Namespaces

Trong ứng dụng Java của bạn, bao gồm các namespace cần thiết để sử dụng chức năng Aspose.CAD. Dưới đây là một ví dụ:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bây giờ, hãy phân tích quy trình **how to export cad** thành các bước dễ quản lý.

## Step‑by‑Step Guide

### Step 1: Load the CAD Drawing

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Chúng ta tải tệp DWG nguồn vào một đối tượng `Image`, đây là điểm khởi đầu cho mọi thao tác tiếp theo.

### Step 2: Create `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` sẽ chứa các cài đặt raster hóa đặc thù cho đầu ra BMP.

### Step 3: Configure Rasterization Settings

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Ở đây chúng ta liên kết các tùy chọn rasterization với `BmpOptions`, cho phép kiểm soát cách các thực thể CAD được render.

### Step 4: Set the Layout(s) to Export

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Thuộc tính `Layouts` cho Aspose.CAD biết nên bao gồm những layout nào. Trong hầu hết các trường hợp, `"Model"` là layout chính bạn muốn chuyển đổi.

### Step 5: Export to BMP Format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Gọi `save` với `BmpOptions` đã cấu hình sẽ ghi tệp BMP ra đĩa. Đây là bước hoàn tất quy trình **convert DWG to BMP**.

## Common Issues and Solutions

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|------------|----------------|
| Hình ảnh đầu ra trắng | Tên layout không đúng hoặc thiếu layout | Xác minh tên layout khớp với tệp CAD (ví dụ, `"Model"`). |
| Độ phân giải thấp | DPI mặc định quá thấp | Đặt `cadRasterizationOptions.setResolution(300);` trước khi lưu. |
| Lỗi out‑of‑memory cho tệp lớn | Các bản vẽ lớn cần nhiều heap | Tăng kích thước heap JVM (`-Xmx2g`) hoặc xử lý từng trang riêng biệt. |

## Frequently Asked Questions

**Q: Aspose.CAD có tương thích với các định dạng tệp CAD khác nhau không?**  
A: Có, Aspose.CAD hỗ trợ DWG, DXF, DGN và nhiều định dạng khác.

**Q: Tôi có thể sử dụng Aspose.CAD cho các dự án thương mại không?**  
A: Hoàn toàn được. Mua giấy phép [here](https://purchase.aspose.com/buy) để sử dụng trong môi trường sản xuất.

**Q: Làm sao để lấy giấy phép tạm thời cho việc thử nghiệm?**  
A: Bạn có thể nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

**Q: Tôi có thể tìm hỗ trợ cộng đồng ở đâu?**  
A: Tham gia diễn đàn cộng đồng Aspose.CAD tại [forum](https://forum.aspose.com/c/cad/19).

**Q: Có bản dùng thử miễn phí cho Aspose.CAD for Java không?**  
A: Có, tải bản dùng thử miễn phí [here](https://releases.aspose.com/).

## Conclusion

Trong hướng dẫn này chúng tôi đã trình bày **how to export cad** từ Java và **convert DWG to BMP** bằng Aspose.CAD. Bằng cách thực hiện năm bước trên, bạn có thể tích hợp chuyển đổi CAD‑to‑image vào bất kỳ ứng dụng Java nào, dù là công cụ desktop, dịch vụ web, hay pipeline xử lý batch. Khám phá các định dạng đầu ra khác (PNG, JPEG, PDF) bằng cách thay đổi lớp options, và tận dụng bộ tính năng phong phú của Aspose.CAD để đáp ứng mọi nhu cầu thao tác CAD của bạn.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}