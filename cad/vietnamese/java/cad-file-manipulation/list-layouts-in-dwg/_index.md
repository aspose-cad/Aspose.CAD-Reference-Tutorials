---
date: 2026-02-28
description: Tìm hiểu cách đọc tệp DWG bằng Aspose.CAD cho Java và dễ dàng liệt kê
  các bố cục trong tệp DWG. Tích hợp chức năng CAD mạnh mẽ vào các ứng dụng Java của
  bạn.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Cách đọc DWG và liệt kê bố cục trong DWG bằng Aspose.CAD cho Java
url: /vi/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

 exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đọc DWG và Liệt Kê Các Bố Cục trong DWG Sử Dụng Aspose.CAD cho Java

## Giới thiệu

Nếu bạn đang tìm kiếm một cách đáng tin cậy **cách đọc dwg** các tệp một cách lập trình, Aspose.CAD cho Java cung cấp một API sạch sẽ, đa nền tảng cho phép bạn tải bản vẽ và trích xuất bất kỳ thông tin nào bạn cần — chẳng hạn như tên của tất cả các bố cục bên trong tệp. Trong hướng dẫn chi tiết này, chúng tôi sẽ chỉ cho bạn **cách đọc DWG** và liệt kê mọi bố cục có trong một tệp DWG (hoặc DXF), để bạn có thể tích hợp khả năng này vào bất kỳ ứng dụng Java nào làm việc với dữ liệu CAD.

## Câu trả lời nhanh
- **Thư viện nào được yêu cầu?** Aspose.CAD cho Java.  
- **Tôi có thể đọc file DWG trên bất kỳ hệ điều hành nào không?** Có – Java là đa nền tảng, vì vậy bạn có thể **đọc dwg trên linux** dễ dàng như trên Windows.  
- **Tôi có cần giấy phép để chạy mẫu không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép cần thiết cho môi trường sản xuất.  
- **Các định dạng CAD nào được hỗ trợ?** DWG, DXF, DWF và các định dạng khác.  
- **Mã có tương thích với Java 8+ không?** Hoàn toàn.

## “cách đọc dwg” trong Java là gì?

Đọc một tệp DWG có nghĩa là tải dữ liệu CAD nhị phân vào một mô hình đối tượng mà bạn có thể truy vấn. Aspose.CAD trừu tượng hoá cấu trúc DWG phức tạp phía sau các lớp Java đơn giản, cho phép bạn tập trung vào thông tin cần thiết — trong trường hợp này là tên các bố cục.

## Tại sao cần liệt kê các bố cục trong file DWG?

Một DWG có thể chứa nhiều bố cục (paper space, model space, các sheet tùy chỉnh). Biết tên các bố cục giúp bạn:

- Tạo báo cáo cho mỗi bố cục.  
- Xuất các bố cục cụ thể ra hình ảnh hoặc PDF.  
- Tự động hoá xử lý hàng loạt bản vẽ.  

## Yêu cầu trước

Trước khi chúng ta đi vào mã, hãy xác nhận rằng bạn đã có:

- **Aspose.CAD cho Java Library** – tải JAR mới nhất từ [website](https://releases.aspose.com/cad/java/).  
- **Môi trường phát triển Java** – JDK 8 trở lên, và một IDE hoặc công cụ build mà bạn lựa chọn.

## Nhập các Namespace

Trong tệp nguồn Java của bạn, nhập các lớp Aspose.CAD cần thiết:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Bước 1: Thiết lập Thư mục Tài liệu của Bạn

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Thay **“Your Document Directory”** bằng đường dẫn tuyệt đối nơi các tệp CAD của bạn nằm. Trên Linux bạn có thể dùng đường dẫn như `/home/user/cad/`.

## Bước 2: Tải File DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Phương thức `Image.load` tự động phát hiện định dạng tệp, vì vậy cùng một đoạn mã hoạt động cho cả các tệp **DWG** và **DXF**.

## Bước 3: Lấy Các Bố Cục và In Tên

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Vòng lặp duyệt qua mỗi đối tượng bố cục và in tên của nó ra console – một cách đơn giản để xác nhận rằng bạn đã **đọc DWG** thành công và trích xuất thông tin bố cục.

## Cách Chuyển Đổi DWG sang PDF trên Linux

Nếu sau này bạn cần chuyển một bố cục cụ thể thành PDF, Aspose.CAD có thể render bố cục thành hình ảnh và sau đó bạn có thể dùng Aspose.PDF (hoặc bất kỳ thư viện PDF nào khác) để nhúng hình ảnh đó vào tài liệu PDF. Mã chuyển đổi giống hệt trên Linux vì API thuần Java.

## Những Cạm Bẫy Thường Gặp & Mẹo

- **Đường dẫn tệp không đúng** – Kiểm tra lại rằng `dataDir` kết thúc bằng dấu phân cách (`/` hoặc `\\`) phù hợp với hệ điều hành của bạn.  
- **Phiên bản DWG không được hỗ trợ** – Đảm bảo bạn đang dùng phiên bản Aspose.CAD mới; các phiên bản DWG cũ có thể cần chuyển đổi.  
- **Tiêu thụ bộ nhớ** – Các bản vẽ lớn có thể tiêu tốn nhiều bộ nhớ. Giải phóng đối tượng `CadImage` khi hoàn thành: `cadImage.dispose();`.  
- **Chạy trên máy chủ không giao diện** – Không cần thành phần UI, vì vậy mã chạy được trên máy chủ Linux không có môi trường đồ họa.

## Kết luận

Chúc mừng! Bạn đã biết **cách đọc dwg** và liệt kê các bố cục của nó bằng Aspose.CAD cho Java. Kỹ thuật này là nền tảng cho các tự động hoá CAD nâng cao hơn, chẳng hạn như xuất các bố cục cụ thể ra hình ảnh, PDF, hoặc thậm chí chuyển DWG sang PDF trên Linux. Để khám phá sâu hơn, tham khảo [tài liệu chính thức](https://reference.aspose.com/cad/java/).

## Câu Hỏi Thường Gặp

**Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng CAD khác không?**  
Có, Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DWF và các định dạng khác.

**Câu hỏi 2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?**  
Có, bạn có thể lấy bản dùng thử miễn phí từ [here](https://releases.aspose.com/).

**Câu hỏi 3: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD cho Java ở đâu?**  
Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng.

**Câu hỏi 4: Làm thế nào để mua giấy phép cho Aspose.CAD cho Java?**  
Bạn có thể mua giấy phép từ [purchase page](https://purchase.aspose.com/buy).

**Câu hỏi 5: Tôi có thể sử dụng giấy phép tạm thời để thử nghiệm không?**  
Có, bạn có thể lấy giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

**Câu hỏi: Phương pháp này có hoạt động để đọc file DWG trên Linux không?**  
Chắc chắn. Vì giải pháp thuần Java, nó chạy trên bất kỳ hệ điều hành nào có JDK tương thích.

**Câu hỏi: Tôi có thể đọc file DWG mà không tải toàn bộ bản vẽ vào bộ nhớ không?**  
Aspose.CAD tải bản vẽ vào bộ nhớ; đối với các tệp rất lớn, hãy cân nhắc xử lý chúng trong các luồng riêng hoặc sử dụng API streaming nếu có trong các phiên bản tương lai.

**Câu hỏi: Có cách nào để lọc các bố cục theo tên không?**  
Có – sau khi lấy `CadLayoutDictionary`, bạn có thể kiểm tra `layout.getLayoutName().equalsIgnoreCase("MyLayout")` trước khi xử lý.

**Last Updated:** 2026-02-28  
**Tested With:** Aspose.CAD cho Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}