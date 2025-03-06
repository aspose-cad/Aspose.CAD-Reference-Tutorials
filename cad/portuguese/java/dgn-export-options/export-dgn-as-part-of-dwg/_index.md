---
title: Exporte DGN para DWG com Aspose.CAD para Java
linktitle: Exportar DGN como parte do DWG
second_title: API Java Aspose.CAD
description: Explore como exportar DGN como parte de DWG usando Aspose.CAD para Java. Siga nosso guia passo a passo para manipulação eficiente de arquivos CAD.
weight: 10
url: /pt/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporte DGN para DWG com Aspose.CAD para Java

## Introdução

Neste tutorial, exploraremos como usar Aspose.CAD for Java para exportar um arquivo DGN (MicroStation Design) como parte de um arquivo DWG (AutoCAD Drawing). Aspose.CAD é uma biblioteca poderosa que oferece funcionalidade abrangente para trabalhar com formatos de arquivo CAD. Este guia passo a passo ajudará você a entender o processo de exportação de DGN como parte de DWG usando Java.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
1. Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD para Java. Você pode encontrar a biblioteca[aqui](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Certifique-se de ter o Java instalado em seu sistema.
3. Ambiente de Desenvolvimento Integrado (IDE): Escolha um IDE Java como Eclipse ou IntelliJ para uma experiência de desenvolvimento mais tranquila.

## Importar pacotes

Em seu projeto Java, importe os pacotes Aspose.CAD necessários para permitir a manipulação de arquivos CAD. Aqui está um exemplo:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Etapa 1: definir caminhos de arquivo

 Defina os caminhos dos arquivos de entrada e saída para o arquivo DWG. Atualize o`dataDir`, `fileName` , e`outPath` variáveis de acordo.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Passo 2: Criar Instância PdfOptions

 Crie uma instância do`PdfOptions` class, pois estamos exportando o arquivo DWG para o formato PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Etapa 3: carregar o arquivo DWG

 Carregue o arquivo DWG existente como uma imagem e converta-o para o formato`CadImage` tipo.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Etapa 4: iterar por meio de entidades

Percorra cada entidade dentro do arquivo DWG e verifique se é uma definição de imagem. Se for, recupere a referência externa ao objeto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Etapa 5: definir opções de rasterização

 Definir configurações para o`CadRasterizationOptions`objeto, incluindo largura da página, altura, layouts e cor de fundo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Etapa 6: definir opções de rasterização vetorial

Defina as opções de rasterização vetorial para exportação.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Passo 7: Exportar DWG para PDF

 Finalmente, exporte o DWG para PDF chamando o`save` método.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como exportar um arquivo DGN como parte de um arquivo DWG usando Aspose.CAD para Java. Esta poderosa biblioteca oferece amplos recursos para trabalhar com arquivos CAD, tornando suas tarefas de manipulação de arquivos CAD eficientes e diretas.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.CAD para Java?

 A1: A documentação pode ser encontrada[aqui](https://reference.aspose.com/cad/java/).

### Q2: Como posso baixar a biblioteca Aspose.CAD para Java?

 A2: Você pode baixar a biblioteca de[esse link](https://releases.aspose.com/cad/java/).

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD para Java?

 A3: Sim, você pode encontrar a versão de avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Onde posso obter uma licença temporária do Aspose.CAD para Java?

 A4: Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Precisa de ajuda ou tem dúvidas?

 A5: Visite o fórum de suporte da comunidade Aspose.CAD[aqui](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
