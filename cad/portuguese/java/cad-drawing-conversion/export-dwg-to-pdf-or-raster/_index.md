---
title: Exporte DWG para PDF ou Raster usando Aspose.CAD para Java
linktitle: Exportar DWG para PDF ou Raster
second_title: API Java Aspose.CAD
description: Explore o processo contínuo de exportação de arquivos DWG para PDF ou imagens raster em Java usando Aspose.CAD. Este guia passo a passo garante precisão e eficiência.
type: docs
weight: 13
url: /pt/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Introdução

No mundo dinâmico do projeto auxiliado por computador (CAD), o manuseio eficiente dos desenhos é crucial. Aspose.CAD for Java fornece uma solução poderosa para exportar arquivos DWG para PDF ou imagens raster. Este tutorial irá guiá-lo através do processo, garantindo que você aproveite todo o potencial do Aspose.CAD para Java.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter o seguinte:

- Compreensão básica de programação Java.
-  Biblioteca Aspose.CAD para Java instalada. Se não, baixe-o[aqui](https://releases.aspose.com/cad/java/).
- Um arquivo DWG para fins de teste. Você pode usar o arquivo "Bottom_plate.dwg" fornecido.

## Importar namespaces

No seu projeto Java, importe os namespaces necessários para iniciar o processo:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Etapa 1: carregar o arquivo DWG

 Comece carregando seu arquivo DWG usando Aspose.CAD`Image` aula:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Etapa 2: determinar o tipo de unidade

A seguir, verifique o tipo de unidade do arquivo DWG carregado:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Etapa 3: definir opções de rasterização

Com base no tipo de unidade, configure as opções de rasterização:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Unidades métricas
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // unidades imperiais
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Passo 4: Configurar Opções de PDF

Configure as opções de exportação de PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Passo 5: Salvar como PDF

Por fim, salve o arquivo DWG como PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

E aí está! Você exportou com sucesso um arquivo DWG para PDF usando Aspose.CAD para Java.

## Conclusão

Este tutorial forneceu um guia passo a passo sobre como aproveitar o Aspose.CAD for Java para exportar arquivos DWG para PDF ou imagens raster. Esta biblioteca simplifica o processo, permitindo que você manipule com eficiência desenhos CAD em seus aplicativos Java.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java com outras estruturas Java?

A1: Sim, o Aspose.CAD for Java integra-se perfeitamente com estruturas Java populares.

### Q2: Há uma licença temporária disponível para Aspose.CAD for Java?

 A2: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q3: Onde posso encontrar suporte para Aspose.CAD para Java?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para obter ajuda da comunidade.

### Q4: Como posso adquirir uma licença do Aspose.CAD para Java?

 A4: Você pode comprar uma licença[aqui](https://purchase.aspose.com/buy).

### Q5: Quais unidades o Aspose.CAD para Java suporta?

A5: Aspose.CAD for Java suporta unidades métricas e imperiais.