---
title: Guia de conversão de DGN para PDF - Aspose.CAD para Java
linktitle: Suporte para DGN V7
second_title: API Java Aspose.CAD
description: Converta facilmente arquivos DGN em PDF usando Aspose.CAD para Java. Siga nosso guia passo a passo para integração perfeita e fluxo de trabalho eficiente.
type: docs
weight: 11
url: /pt/java/other-cad-operations/support-for-dgn-v7/
---
## Introdução

No mundo dinâmico do CAD (Computer-Aided Design), a conversão eficiente de arquivos DGN (Design) em PDF (Portable Document Format) é um requisito crucial. Aspose.CAD for Java surge como uma solução poderosa, oferecendo integração perfeita e recursos robustos. Este guia passo a passo tem como objetivo orientá-lo no processo de exportação de arquivos DGN para PDF usando Aspose.CAD para Java, garantindo um fluxo de trabalho tranquilo e eficiente.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Biblioteca Aspose.CAD para Java: Baixe e instale a biblioteca do[Página de download do Aspose.CAD para Java](https://releases.aspose.com/cad/java/).
- Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.

## Importar pacotes

Comece importando os pacotes necessários para o seu projeto Java:

## Etapa 1: importar os pacotes necessários

Em seu projeto Java, importe os pacotes necessários para Aspose.CAD for Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Etapa 2: definir caminhos de arquivo

Defina os caminhos para o arquivo DGN de entrada e o arquivo PDF de saída.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Etapa 3: carregar imagem DGN

Carregue a imagem DGN usando a biblioteca Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Passo 4: Configurar opções de exportação de PDF

Configure opções de exportação para PDF, incluindo dimensões de página, dimensionamento automático de layout, cor de fundo e layouts específicos para exportação.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //exportar apenas 4 (1,2,3 e 9) visualizações
options.setVectorRasterizationOptions(vectorOptions);
```

## Passo 5: Salvar arquivo PDF

Salve a imagem DGN como um arquivo PDF com as opções especificadas.

```java
objImage.save(outFile, options);
```

Repita essas etapas para diferentes arquivos DGN, ajustando os caminhos e opções dos arquivos conforme necessário.

## Conclusão

Com Aspose.CAD for Java, a conversão de arquivos DGN em PDF torna-se um processo simples. Este guia fornece o conhecimento necessário para integrar perfeitamente a biblioteca em seus projetos Java, facilitando conversões eficientes de arquivos CAD.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, fornecendo funcionalidade versátil além da conversão de DGN para PDF.

### Q2: Há uma licença temporária disponível para Aspose.CAD for Java?

 A2: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/) para fins de teste.

### Q3: Como posso buscar suporte ou tirar dúvidas sobre o Aspose.CAD for Java?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19)para se conectar com a comunidade e buscar assistência.

### P4: Quais layouts posso exportar ao converter DGN para PDF?

 A4: Você pode especificar os layouts a serem exportados personalizando o`setLayouts` matriz no código.

### Q5: Onde posso encontrar documentação abrangente para Aspose.CAD for Java?

 A5: Consulte o[Documentação Aspose.CAD para Java](https://reference.aspose.com/cad/java/) para obter informações detalhadas.