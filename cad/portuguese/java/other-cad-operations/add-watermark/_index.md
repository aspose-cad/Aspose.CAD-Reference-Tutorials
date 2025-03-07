---
title: Adicionar marcas d'água a desenhos CAD - Tutorial Aspose.CAD para Java
linktitle: Adicione uma Marca D'água
second_title: API Java Aspose.CAD
description: Aprimore seus desenhos CAD com marcas d’água personalizadas usando Aspose.CAD para Java. Siga nosso guia passo a passo para uma integração perfeita.
weight: 12
url: /pt/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar marcas d'água a desenhos CAD - Tutorial Aspose.CAD para Java

## Introdução

Bem-vindo a este guia completo sobre como adicionar marcas d'água a desenhos CAD usando Aspose.CAD for Java. Neste tutorial, você aprenderá como integrar marcas d'água de forma eficiente, aprimorando seus documentos CAD com mensagens ou marcas personalizadas. Aspose.CAD for Java fornece um poderoso conjunto de recursos, tornando o processo de adição de marca d'água simples.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos:

-  Aspose.CAD para Java: Certifique-se de ter a biblioteca Aspose.CAD instalada em seu ambiente Java. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Certifique-se de ter a versão mais recente do JDK instalada em seu sistema.

## Importar pacotes

Em seu projeto Java, importe os pacotes Aspose.CAD necessários para começar:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Etapa 1: adicionar novo MTEXT

```java
//adicionar novo MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Etapa 2: adicionar entidade simples como texto

Você também pode adicionar uma entidade mais simples, como texto:

```java
// ou adicione uma entidade mais simples como Texto
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Passo 3: Exportar para PDF

Exporte o desenho CAD com a marca d'água adicionada para um arquivo PDF:

```java
// exportar para pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Conclusão

Parabéns! Você adicionou marcas d'água aos seus desenhos CAD com sucesso usando Aspose.CAD for Java. Este processo simples, mas poderoso, permite que você personalize seus designs ou proteja-os com sua marca.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

A1: Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DWT e DWF.

### P2: Posso personalizar a aparência do texto da marca d'água?

R2: Sim, você tem controle total sobre a aparência da marca d'água, incluindo tamanho, cor e posição do texto.

### Q3: Existe uma versão de teste disponível para Aspose.CAD for Java?

 A3: Sim, você pode baixar a versão de teste[aqui](https://releases.aspose.com/).

### Q4: Como posso obter suporte para Aspose.CAD?

 A4: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.

### Q5: Onde posso encontrar a documentação completa do Aspose.CAD for Java?

 A5: Consulte o[documentação](https://reference.aspose.com/cad/java/) para obter informações detalhadas.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
