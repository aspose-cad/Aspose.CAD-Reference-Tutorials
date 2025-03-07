---
title: Exporte DGN incorporado para PDF com Aspose.CAD para Java
linktitle: Exportar DGN incorporado
second_title: API Java Aspose.CAD
description: Explore o guia passo a passo sobre como exportar arquivos DGN incorporados para PDF usando Aspose.CAD for Java. Aprimore seus aplicativos Java com manipulação perfeita de arquivos CAD.
weight: 11
url: /pt/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporte DGN incorporado para PDF com Aspose.CAD para Java

## Introdução

Bem-vindo a este tutorial abrangente sobre exportação de arquivos DGN incorporados usando Aspose.CAD para Java. Aspose.CAD é uma biblioteca poderosa que permite aos desenvolvedores Java trabalhar com arquivos CAD perfeitamente. Neste tutorial, orientaremos você no processo de exportação de arquivos DGN incorporados para PDF usando instruções passo a passo. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este tutorial o ajudará a aproveitar os recursos do Aspose.CAD para aprimorar seus aplicativos Java.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos:
- Ambiente de Desenvolvimento Java: Certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.
-  Aspose.CAD para Java: Baixe e instale a biblioteca Aspose.CAD para Java em[aqui](https://releases.aspose.com/cad/java/).

## Importar pacotes

Para começar, você precisa importar os pacotes necessários em seu projeto Java. Adicione as seguintes instruções de importação ao seu código:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Agora, vamos dividir o código de exemplo em várias etapas:

## Etapa 1: configurar caminhos de entrada e saída

Defina o caminho do diretório onde seu documento está localizado e especifique o nome do arquivo DWG de entrada.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Etapa 2: carregar o arquivo DWG

 Carregue o arquivo DWG em um`Image` objeto usando Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Etapa 3: configurar opções de rasterização

Configure opções de rasterização, como layouts a serem incluídos na exportação.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Passo 4: Configurar Opções de PDF

Configure opções de PDF, incluindo opções de rasterização vetorial.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Passo 5: Salvar arquivo PDF

Salve o arquivo PDF com as opções configuradas.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusão

Parabéns! Você exportou com sucesso um arquivo DGN incorporado para PDF usando Aspose.CAD para Java. Este tutorial abordou as etapas essenciais para integrar o Aspose.CAD em seu aplicativo Java para uma manipulação eficiente de arquivos CAD.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java em um projeto comercial?

 A1: Sim, Aspose.CAD for Java é uma biblioteca comercial. Você pode obter uma licença de[aqui](https://purchase.aspose.com/buy).

### Q2: Existe um teste gratuito disponível?

 A2:Sim, você pode acessar uma avaliação gratuita do Aspose.CAD para Java[aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD para Java?

A3: Você pode buscar suporte da comunidade Aspose.CAD no[fórum](https://forum.aspose.com/c/cad/19).

### P4: E se eu precisar de uma licença temporária?

 A4: Você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Onde posso encontrar a documentação?

 A5: A documentação está disponível[aqui](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
