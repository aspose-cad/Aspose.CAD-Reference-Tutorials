---
title: Exporte IFC para PNG com Aspose.CAD para Java
linktitle: Exportar IFC para PNG
second_title: API Java Aspose.CAD
description: Converta IFC para PNG sem esforço com Aspose.CAD para Java. Siga nosso tutorial passo a passo.
type: docs
weight: 18
url: /pt/java/cad-export-options/export-ifc-to-png/
---
## Introdução

Bem-vindo a este tutorial passo a passo sobre como exportar IFC (Industry Foundation Classes) para PNG usando Aspose.CAD para Java. Aspose.CAD é uma biblioteca Java poderosa que oferece amplos recursos para trabalhar com arquivos CAD, incluindo o formato IFC. Neste tutorial, orientaremos você no processo de conversão de um arquivo IFC em uma imagem PNG com explicações detalhadas em cada etapa.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD para Java do[Link para Download](https://releases.aspose.com/cad/java/).

- Diretório de Documentos: Prepare um diretório em seu sistema onde seu arquivo IFC está localizado.

## Importar namespaces

Em seu projeto Java, importe os namespaces necessários conforme mostrado abaixo:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Etapa 1: carregar o arquivo IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Esta etapa envolve carregar o arquivo IFC usando Aspose.CAD.

## Etapa 2: definir opções de vetor

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Configure opções de vetor para rasterização, especificando a largura e a altura da página.

## Etapa 3: definir opções de PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Defina opções de PNG, incluindo opções de rasterização vetorial.

## Etapa 4: salvar como PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Salve a imagem processada no formato PNG.

## Conclusão

Parabéns! Você converteu com sucesso um arquivo IFC para PNG usando Aspose.CAD para Java. Este tutorial forneceu um guia completo, garantindo que você possa integrar perfeitamente essa funcionalidade em seus projetos.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todas as versões de arquivos IFC?

 A1: Aspose.CAD suporta várias versões de arquivos IFC. Consulte o[documentação](https://reference.aspose.com/cad/java/) para detalhes de compatibilidade.

### P2: Posso personalizar ainda mais as opções de rasterização?

 A2: Com certeza! Explore o[documentação](https://reference.aspose.com/cad/java/) para opções de personalização avançadas.

### Q3: Existe uma versão de teste disponível?

A3: Sim, você pode acessar a versão de avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Como posso obter licenciamento temporário para Aspose.CAD?

 A4: Obtenha uma licença temporária de[esse link](https://purchase.aspose.com/temporary-license/).

### P5: Onde posso procurar ajuda ou discutir problemas?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.
