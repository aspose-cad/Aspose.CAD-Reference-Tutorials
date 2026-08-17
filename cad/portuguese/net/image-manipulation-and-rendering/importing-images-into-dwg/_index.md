---
date: 2026-08-17
description: Aprenda como adicionar imagem a arquivos dwg usando C# e Aspose.CAD para
  .NET. Este guia orienta você na importação de imagens, definição de pontos de inserção
  e exportação para PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importando Imagens em Arquivos DWG com C#
og_description: Aprenda como adicionar imagem a arquivos dwg usando C#. Este tutorial
  cobre a importação de imagens, definição de pontos de inserção e conversão de dwg
  para pdf com Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Como adicionar imagem a arquivos dwg com C# usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Como adicionar imagem a arquivos dwg com C# usando Aspose.CAD
url: /pt/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como adicionar imagem a arquivos dwg com C# usando Aspose.CAD

## Introdução

Adicionar uma imagem a um arquivo DWG é uma necessidade rotineira quando você precisa enriquecer desenhos CAD com logotipos, fotos ou gráficos raster. Neste tutorial você aprenderá como **add image to dwg** programaticamente usando C# e Aspose.CAD para .NET, e opcionalmente converter o resultado para PDF. As etapas são divididas para que você possa copiar‑colar cada seção em seu próprio projeto.

## Respostas rápidas
- **Qual biblioteca realiza o trabalho?** Aspose.CAD for .NET.
- **Posso incorporar arquivos PNG?** Sim – PNG, JPEG, BMP e outros formatos raster são suportados.
- **Preciso de uma licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para produção.
- **A exportação para PDF é suportada?** Absolutamente – você pode converter o DWG atualizado para PDF em uma linha.
- **Quais versões do .NET são compatíveis?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## O que é um arquivo DWG?

Um arquivo DWG é o formato binário nativo para desenhos Autodesk AutoCAD, armazenando geometria vetorial, camadas e metadados. É amplamente usado em arquitetura, engenharia e construção, e o Aspose.CAD pode ler e gravar esse formato sem necessidade de AutoCAD instalado.

## Por que adicionar imagem a dwg com Aspose.CAD?

O Aspose.CAD suporta **50+ input and output formats**, pode processar arquivos maiores que 500 MB sem carregar todo o documento na memória, e fornece uma API determinística que funciona em ambientes de servidor sem interface gráfica. Isso torna o processamento em lote de desenhos DWG rápido e confiável.

## Pré-requisitos
- Conhecimento básico de programação C#.
- Aspose.CAD for .NET instalado. Você pode baixá-lo na [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). Você também pode explorar outros produtos Aspose na [Aspose releases page](https://releases.aspose.com/).
- Um ambiente de desenvolvimento como Visual Studio 2022 ou posterior.

## Como adicionar imagem a dwg usando Aspose.CAD?

Carregue o DWG de destino, crie um objeto de imagem raster que descreva a foto que você deseja incorporar, defina o ponto de inserção e os vetores de escala, e então anexe a imagem ao desenho. Por fim, salve o DWG modificado ou exporte-o diretamente para PDF. Todo o fluxo de trabalho requer apenas algumas chamadas de API e é executado em menos de um segundo para desenhos típicos de 2 páginas.

### Importar namespaces
Inclua os namespaces que expõem as classes CAD de que você precisará.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Etapa 1: configurar seu diretório de documentos
Prepare a pasta que contém o DWG fonte e a imagem que você deseja incorporar.

```csharp
string MyDir = "Your Document Directory";
```

### Etapa 2: carregar o arquivo dwg
A classe `CadImage` representa um desenho DWG e fornece acesso às suas entidades, camadas e metadados.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Etapa 3: definir as propriedades da imagem
Crie um objeto `Image` que aponte para o arquivo raster (por exemplo, PNG) e especifique seu formato.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Etapa 4: definir ponto de inserção dwg e vetores
Especifique onde a imagem deve aparecer dentro do desenho e como ela deve ser dimensionada. O ponto de inserção é definido por uma coordenada 2‑D, enquanto os vetores controlam a largura e a altura.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Etapa 5: criar e configurar a imagem raster
Instancie um objeto `RasterImage`, atribua os dados da imagem e defina quaisquer opções adicionais de renderização.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Etapa 6: adicionar imagem ao arquivo dwg
Insira a imagem raster configurada na coleção de entidades do DWG para que ela se torne parte do desenho.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Etapa 7: salvar como pdf (exportar dwg para pdf)
Depois de incorporar a imagem, você pode **convert dwg to pdf** ou **save dwg as pdf** com uma única chamada. Isso é útil para compartilhar o desenho com partes interessadas que não possuem software CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Como converter dwg para pdf após incorporar uma imagem?

Chame o método `Save` na instância `CadImage`, passando `SaveFormat.Pdf` e, opcionalmente, um objeto `PdfOptions` para controlar o tamanho da página, rasterização e metadados. O Aspose.CAD preserva a imagem raster incorporada, camadas e espessuras de linha, produzindo uma representação PDF fiel que pode ser aberta em qualquer visualizador. Essa conversão é realizada em uma única linha de código.

## Problemas comuns e soluções
- **A imagem aparece no local errado** – verifique novamente as coordenadas do ponto de inserção e os vetores de direção; eles são relativos à origem do desenho.
- **Imagens grandes causam picos de memória** – use a opção `Resize` na imagem raster antes da inserção, ou trabalhe com uma cópia de resolução mais baixa.
- **A exportação para PDF perde a qualidade vetorial** – certifique-se de salvar com `PdfOptions` que preservem os dados vetoriais; imagens raster são sempre incorporadas como estão.

## Perguntas frequentes

**Q: Posso usar Aspose.CAD para .NET com outras linguagens de programação?**  
A: A biblioteca principal é específica para .NET, mas a Aspose oferece APIs equivalentes para Java, Python e outras plataformas.

**Q: Existe um teste gratuito disponível para Aspose.CAD?**  
A: Sim, você pode explorar um teste gratuito na [Aspose free trial page](https://releases.aspose.com/).

**Q: Onde posso encontrar documentação detalhada para Aspose.CAD?**  
A: A documentação está disponível na [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Como obtenho uma licença temporária para Aspose.CAD?**  
A: Visite a [temporary license page](https://purchase.aspose.com/temporary-license/) para obter uma licença temporária.

**Q: Existem fóruns da comunidade para suporte ao Aspose.CAD?**  
A: Sim, você pode buscar suporte e interagir com a comunidade no [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Última atualização:** 2026-08-17  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriais relacionados

- [Exportando DWG para PDF ou Imagens Raster - Guia Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportando DWG para Formato DXF em C# - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exportando Layouts Específicos para PDF - Guia Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}