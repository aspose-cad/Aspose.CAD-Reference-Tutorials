---
title: Definir tamanho e modo da tela
linktitle: Definir tamanho e modo da tela
second_title: API Java Aspose.CAD
description: Explore o poder do Aspose.CAD para Java com nosso guia passo a passo sobre como definir o tamanho e o modo da tela. Converta facilmente arquivos CAD para formatos PDF e TIFF.
weight: 16
url: /pt/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir tamanho e modo da tela

## Introdução

Você está procurando aproveitar o poder do Aspose.CAD for Java para aprimorar seu processo de conversão de CAD? Este guia completo irá orientá-lo nas etapas de configuração do tamanho e modo da tela usando Aspose.CAD para Java. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este tutorial fornecerá os insights necessários.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD para Java: Certifique-se de ter a biblioteca Aspose.CAD instalada em seu ambiente Java. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/java/).

- Diretório de documentos: Configure um diretório de documentos para armazenar seus arquivos CAD. Este diretório será referenciado nas etapas do tutorial.

Agora, vamos começar com o guia passo a passo.

## Importar namespaces

Nesta etapa, importaremos os namespaces necessários para iniciar seu projeto Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Etapa 1: importar classes Aspose.CAD

```java
// O caminho para o diretório de recursos.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Neste trecho, configuramos o caminho para o diretório de recursos e carregamos um arquivo DXF usando o Aspose.CAD`Image` aula.

## Etapa 2: definir propriedades de CadRasterizationOptions

```java
// Crie uma instância de CadRasterizationOptions e defina suas diversas propriedades
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Aqui, criamos uma instância de`CadRasterizationOptions` e configure propriedades como largura e altura da página e opções de escala.

## Etapa 3: criar PdfOptions e definir VectorRasterizationOptions

```java
// Crie uma instância de PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Defina a propriedade VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Agora, criamos um`PdfOptions` instância e definir seu`VectorRasterizationOptions` propriedade para o configurado anteriormente`CadRasterizationOptions`.

## Passo 4: Exportar para PDF

```java
// Exportar CAD para PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, salvamos a imagem CAD em um arquivo PDF usando as opções especificadas.

## Etapa 5: criar TiffOptions e definir VectorRasterizationOptions

```java
// Crie uma instância de TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Defina a propriedade VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nesta etapa montamos um`TiffOptions` instância e configurar seu`VectorRasterizationOptions` propriedade.

## Etapa 6: exportar para TIFF

```java
// Exportar CAD para TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finalmente, salvamos a imagem CAD em um arquivo TIFF usando as opções especificadas.

## Conclusão

 Parabéns! Você definiu com sucesso o tamanho e o modo da tela usando Aspose.CAD para Java. Este tutorial fornece uma base sólida para seus projetos de conversão de CAD. Explore mais recursos e possibilidades no[Documentação Aspose.CAD](https://reference.aspose.com/cad/java/).

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java com outras estruturas Java?

A1: Sim, o Aspose.CAD foi projetado para integração perfeita com várias estruturas Java.

### Q2: Há uma licença temporária disponível para Aspose.CAD?

 A2: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q3: Onde posso obter suporte da comunidade para Aspose.CAD?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### Q4: Posso experimentar o Aspose.CAD gratuitamente?

 A4: Com certeza! Faça um teste gratuito[aqui](https://releases.aspose.com/).

### Q5: Como faço para adquirir o Aspose.CAD para Java?

 A5: Compre o produto[aqui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
