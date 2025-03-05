---
title: Ajustando o tamanho do desenho CAD usando o tipo de unidade com Aspose.CAD para Java
linktitle: Ajustando o tamanho do desenho CAD usando o tipo de unidade
second_title: API Java Aspose.CAD
description: Explore o poder do Aspose.CAD para Java para ajustar tamanhos de desenhos CAD sem esforço. Siga nosso guia passo a passo para precisão e adaptabilidade.
type: docs
weight: 14
url: /pt/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## Introdução

No domínio em constante evolução do Design Assistido por Computador (CAD), a precisão e a adaptabilidade são fundamentais. Um requisito comum é ajustar o tamanho dos desenhos CAD com base em tipos de unidades específicas. Aspose.CAD for Java surge como um aliado poderoso, fornecendo recursos integrados para manipulação de arquivos CAD programaticamente.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Ambiente de Desenvolvimento Java: Certifique-se de ter um ambiente de desenvolvimento Java funcional configurado em sua máquina.

-  Biblioteca Aspose.CAD para Java: Baixe e integre a biblioteca Aspose.CAD ao seu projeto Java. Você pode obter a biblioteca[aqui](https://releases.aspose.com/cad/java/).

## Importar namespaces

Em seu código Java, inclua os namespaces necessários para acessar as funcionalidades do Aspose.CAD. Adicione as seguintes importações:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Agora, vamos dividir o processo de ajuste do tamanho do desenho CAD usando o tipo de unidade em etapas gerenciáveis:

## Etapa 1: definir o diretório de dados

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Defina o caminho do diretório onde seus arquivos CAD estão localizados.

## Etapa 2: carregar o desenho CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Carregue o desenho CAD usando Aspose.CAD`Image` aula.

## Etapa 3: criar opções de BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instancie o`BmpOptions` classe para exportar o layout CAD para o formato BMP.

## Etapa 4: configurar opções de rasterização

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Crie uma instância de`CadRasterizationOptions` e associá-lo ao`BmpOptions` para rasterização vetorial.

## Etapa 5: definir o tipo de unidade

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Especifique o tipo de unidade desejado para o desenho CAD. Neste exemplo, definimos como Centímetro.

## Etapa 6: definir layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Defina os layouts a serem considerados durante a exportação. Neste caso, selecionamos o layout “Modelo”.

## Passo 7: Exportar para BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Finalmente, salve o desenho CAD modificado em formato BMP.

## Conclusão

Com Aspose.CAD para Java, ajustar os tamanhos dos desenhos CAD torna-se muito fácil. Este tutorial orientou você ao longo do processo, enfatizando a importância de cada etapa na obtenção de resultados precisos.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for Java com outras linguagens de programação?

A1: Aspose.CAD suporta principalmente Java, mas existem versões disponíveis para outras linguagens como .NET.

### Q2: Existe alguma opção de licenciamento para Aspose.CAD?

 A2: Sim, você pode explorar as opções de licenciamento e comprar Aspose.CAD[aqui](https://purchase.aspose.com/buy).

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD?

 A3: Certamente, você pode acessar uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Como posso obter suporte para Aspose.CAD para Java?

 A4: Visite o fórum Aspose.CAD[aqui](https://forum.aspose.com/c/cad/19) para suporte abrangente.

### Q5: Posso obter uma licença temporária para Aspose.CAD?

 A5: Sim, você pode adquirir uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).