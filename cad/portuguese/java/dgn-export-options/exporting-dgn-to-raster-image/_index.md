---
title: Conversão de Java DGN para JPEG com tutorial Aspose.CAD
linktitle: Exportando DGN no formato AutoCAD para formato de imagem raster
second_title: API Java Aspose.CAD
description: Aprenda como exportar arquivos DGN para imagens JPEG em Java usando Aspose.CAD. Este tutorial passo a passo orienta você durante o processo sem esforço.
type: docs
weight: 13
url: /pt/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Introdução

Bem-vindo a este tutorial abrangente sobre exportação de arquivos DGN (Design) para formato de imagem raster usando Aspose.CAD para Java. Aspose.CAD é uma biblioteca poderosa que permite aos desenvolvedores Java trabalhar com arquivos CAD perfeitamente. Neste tutorial, orientaremos você no processo de conversão de arquivos DGN em imagens JPEG, fornecendo instruções passo a passo e exemplos de código.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
1.  Biblioteca Aspose.CAD: Certifique-se de ter a biblioteca Aspose.CAD para Java instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Certifique-se de ter o Java instalado em sua máquina.
3. Ambiente de Desenvolvimento Integrado (IDE): Use um IDE compatível com Java, como IntelliJ ou Eclipse.

## Importar pacotes

No seu projeto Java, importe os pacotes necessários para Aspose.CAD. Adicione as seguintes linhas ao seu código:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Etapa 1: carregar o arquivo DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Etapa 2: Criar objeto JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Etapa 3: atribuir opções de rasterização

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Etapa 4: salve a imagem convertida

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Repita essas etapas para seus arquivos DGN específicos, ajustando os caminhos dos arquivos de acordo.

## Conclusão

Parabéns! Você aprendeu com sucesso como exportar arquivos DGN para formato de imagem raster usando Aspose.CAD para Java. Este tutorial equipou você com o conhecimento para incorporar essa funcionalidade em seus aplicativos Java.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, fornecendo uma solução versátil para desenvolvedores Java.

### Q2: Existe uma avaliação gratuita disponível para Aspose.CAD for Java?

 A2: Sim, você pode acessar uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q3: Onde posso encontrar documentação para Aspose.CAD for Java?

 A3: Consulte a documentação[aqui](https://reference.aspose.com/cad/java/).

### Q4: Como posso obter suporte para Aspose.CAD para Java?

 A4: Visite o fórum de suporte[aqui](https://forum.aspose.com/c/cad/19).

### P5: Onde posso adquirir uma licença do Aspose.CAD para Java?

 A5: Você pode comprar uma licença[aqui](https://purchase.aspose.com/buy).