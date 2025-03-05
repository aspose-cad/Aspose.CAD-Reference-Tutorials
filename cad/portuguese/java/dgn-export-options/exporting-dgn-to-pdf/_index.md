---
title: Exportação fácil de DGN para AutoCAD PDF com Aspose.CAD para Java
linktitle: Exportando DGN no formato AutoCAD para PDF
second_title: API Java Aspose.CAD
description: Explore o guia passo a passo sobre como exportar arquivos DGN para o formato AutoCAD em PDF usando Aspose.CAD para Java. Eleve os recursos de manipulação de CAD do seu aplicativo Java sem esforço.
type: docs
weight: 12
url: /pt/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Introdução

Bem-vindo a este tutorial abrangente sobre como usar Aspose.CAD for Java para exportar arquivos DGN no formato AutoCAD para PDF. Se você deseja aprimorar a capacidade do seu aplicativo Java de lidar com arquivos CAD, o Aspose.CAD é uma excelente escolha. Neste tutorial, orientaremos você passo a passo no processo de exportação de arquivos DGN.


## Pré-requisitos
Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos:
-  Biblioteca Aspose.CAD: Certifique-se de ter a biblioteca Aspose.CAD para Java instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/java/).
- Diretório de documentos: Configure um diretório de documentos onde seus arquivos de entrada e saída serão armazenados.

## Importar pacotes

Em seu projeto Java, importe os pacotes necessários para acessar as funcionalidades do Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Agora, vamos dividir o código de exemplo em várias etapas:

## Etapa 1: definir caminhos de arquivo

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Certifique-se de substituir “Seu diretório de documentos” pelo caminho real onde seus arquivos estão localizados.

## Etapa 2: carregar imagem DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Carregue o arquivo DGN usando Aspose.CAD.

## Passo 3: Definir opções de exportação de PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Exportar visualizações específicas
options.setVectorRasterizationOptions(vectorOptions);
```

Defina as opções de exportação de PDF, incluindo dimensões de página e preferências de layout.

## Passo 4: Salvar arquivo PDF

```java
objImage.save(outFile, options);
```

Salve o arquivo PDF exportado.

Repita essas etapas para quaisquer arquivos DGN adicionais que você deseja converter. Parabéns! Você exportou com sucesso arquivos DGN para o formato AutoCAD em PDF usando Aspose.CAD para Java.

## Conclusão

Neste tutorial, exploramos como aproveitar o Aspose.CAD for Java para aprimorar os recursos de manipulação de arquivos CAD do seu aplicativo. Com etapas fáceis de seguir e exemplos de código, agora você pode exportar facilmente arquivos DGN para o formato AutoCAD em PDF.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

A1: Sim, o Aspose.CAD suporta uma ampla variedade de formatos CAD, garantindo versatilidade no manuseio de vários tipos de arquivos.

### P2: Posso personalizar as configurações de exportação de PDF?

A2: Absolutamente. Conforme mostrado no tutorial, você pode ajustar opções como dimensões de página e layouts para atender às suas necessidades.

### P3: Onde posso encontrar suporte ou assistência adicional?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode acessar a avaliação gratuita[aqui](https://releases.aspose.com/).

### P5: Como posso obter uma licença temporária?

 A5: Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).