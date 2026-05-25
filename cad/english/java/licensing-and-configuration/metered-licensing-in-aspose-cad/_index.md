---
title: How to Set Metered Licensing in Aspose.CAD
linktitle: How to Set Metered Licensing in Aspose.CAD
second_title: Aspose.CAD Java API
description: Learn how to set metered licensing in Aspose.CAD for Java to optimize CAD processing, reduce costs, and track usage efficiently.
date: 2026-05-25
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
weight: 10
url: /java/licensing-and-configuration/metered-licensing-in-aspose-cad/
schemas:
- type: TechArticle
  headline: How to Set Metered Licensing in Aspose.CAD
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  dateModified: '2026-05-25'
  author: Aspose
- type: FAQPage
  questions:
  - question: What is metered licensing?
    answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
  - question: How many keys are required?
    answer: Two keys – a public and a private key – generated from your Aspose account.
  - question: Can I check usage programmatically?
    answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
  - question: Is a trial available?
    answer: A free trial license can be obtained from the Aspose website.
  - question: Which Java version is supported?
    answer: Java 8 through 17 are fully supported.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Metered Licensing in Aspose.CAD

## Introduction

Unlock the full potential of Aspose.CAD for Java with **how to set metered** licensing! This step‑by‑step guide walks you through every stage—from installing prerequisites, importing the right packages, to measuring consumption before and after processing. By the end you’ll know exactly **how to set metered** keys, read usage metrics, and keep your CAD workflow cost‑effective.

## Quick Answers
- **What is metered licensing?** A usage‑based model that tracks API calls and charges per consumption unit.  
- **How many keys are required?** Two keys – a public and a private key – generated from your Aspose account.  
- **Can I check usage programmatically?** Yes, call `License.getConsumptionQuantity()` before and after processing.  
- **Is a trial available?** A free trial license can be obtained from the Aspose website.  
- **Which Java version is supported?** Java 8 through 17 are fully supported.

## What is metered licensing in Aspose.CAD?
Metered licensing is Aspose.CAD’s pay‑as‑you‑go model that records each API call as a consumption unit. It enables you to monitor exact usage, avoid over‑provisioning, and only pay for what you actually consume.

## Why use metered licensing for CAD processing?
Aspose.CAD supports **50+** input and output formats—including DWG, DXF, DGN, and SVG—and can process files up to **2 GB** without loading the entire document into memory. This efficiency translates into lower server costs, especially when handling large batches of drawings.

## Prerequisites

Before diving into the world of metered licensing with Aspose.CAD, make sure you have the following in place:

### Java Development Kit (JDK) Installation

Ensure that you have the latest version of Java Development Kit installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.CAD for Java Library

Make sure to download and set up the Aspose.CAD for Java library. You can find the library [here](https://releases.aspose.com/cad/java/). You can also browse other Aspose releases [here](https://releases.aspose.com/).

## How to set metered licensing in Aspose.CAD for Java?

Load your public and private keys, call `License.setMeteredKey(publicKey, privateKey)`, and the library instantly switches to metered mode. This single call activates usage tracking for every subsequent API operation, allowing you to query consumption before and after any processing step.

## Import Packages

In order to use the library, import its core package:

`import com.aspose.cad.*;` brings the Aspose.CAD classes into your project.

```java
import com.aspose.cad;
```

## Step 1: Set Metered Key

`setMeteredKey` registers your public and private keys with the Aspose.CAD library.

Firstly, set the metered key using the `setMeteredKey` method. Replace `<valid public key>` and `<valid private key>` with your actual public and private keys.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## Step 2: Get Consumption Quantity Before Processing

`getConsumptionQuantity` returns the total number of consumption units recorded so far.

Retrieve the consumed quantity value before accessing the Aspose.CAD API to get an initial understanding.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## Step 3: Processing

Perform your desired CAD processing using Aspose.CAD functionalities. Uncomment the code snippet related to your specific task, such as loading a CAD image.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## Step 4: Get Consumption Quantity After Processing

After processing, obtain the consumed quantity value again to assess the impact.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

Repeat these steps for any additional processing or tasks as needed.

## Common Issues and Solutions

- **Invalid key error:** Double‑check that both keys are copied exactly as shown in your Aspose account; extra spaces cause authentication failures.  
- **Zero consumption reported:** Ensure you call `License.getConsumptionQuantity()` *after* the first API usage; the first call initializes the counter.  
- **Performance slowdown on large files:** Use `CadImage.load(..., LoadOptions)` with `LoadOptions.setLoadMode(LoadMode.Stream)` to avoid loading the full file into memory.

## Frequently Asked Questions

**Q1: Can I use metered licensing for evaluation purposes?**  
A1: Yes, you can obtain a free trial license [here](https://releases.aspose.com/).

**Q2: Where can I find detailed documentation for Aspose.CAD for Java?**  
A2: Refer to the documentation [here](https://reference.aspose.com/cad/java/).

**Q3: How do I purchase a license for Aspose.CAD for Java?**  
A3: Visit the purchase page [here](https://purchase.aspose.com/buy).

**Q4: Is there a temporary license option available?**  
A5: Yes, you can explore temporary licenses [here](https://purchase.aspose.com/temporary-license/).

**Q5: Need community support or have specific questions?**  
A5: Head to the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19).

**Q6: Does metered licensing work with cloud deployments?**  
A6: Absolutely. The same `setMeteredKey` call works in Docker, Kubernetes, or serverless environments.

**Q7: Can I reset the consumption counter?**  
A7: The counter resets automatically at the start of each new billing period; you cannot manually reset it.

## Conclusion

Congratulations! You've successfully mastered **how to set metered** licensing with Aspose.CAD for Java. By following this guide, you've set up and integrated metered licensing seamlessly into your Java project, ensuring efficient usage of Aspose.CAD capabilities while keeping costs transparent.

---

**Last Updated:** 2026-05-25  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Convert CAD to PDF with Aspose.CAD for Java – Full Tutorials](/cad/java/)
- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Set Canvas Size – Advanced CAD Features with Aspose.CAD for Java](/cad/java/advanced-cad-features/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}