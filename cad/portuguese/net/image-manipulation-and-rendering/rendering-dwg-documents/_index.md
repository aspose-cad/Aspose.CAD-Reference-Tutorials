---
date: 2026-08-23
description: Aprenda como criar viewport dwg c# usando Aspose.CAD. Este guia cobre
  loading de um arquivo DWG, configurando rasterization, definindo um viewport e saving
  do resultado como PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Renderizando documentos DWG em C#
og_description: Aprenda como criar viewport dwg c# usando Aspose.CAD em .NET. Este
  guia passo a passo mostra loading, rasterization, definição de viewports e saving
  em PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Como criar viewport dwg c# com Aspose.CAD para .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Como criar viewport dwg c# com Aspose.CAD para .NET
url: /pt/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderizando documentos DWG em C# – tutorial de criação de viewport dwg c# tutorial

## Introdução

Neste tutorial abrangente, você aprenderá a **criar viewport dwg c#** com Aspose.CAD e renderizar um arquivo DWG para PDF. Seja para extrair um layout específico, gerar uma folha imprimível ou incorporar uma visualização CAD em um relatório, controlar o viewport oferece controle preciso de renderização. Aspose.CAD suporta **mais de 20 formatos CAD** e pode processar arquivos com milhares de entidades sem carregar todo o documento na memória, tornando‑o ideal para aplicações .NET de alto desempenho.

## Respostas rápidas
- **Qual é o primeiro passo?** Carregue o arquivo DWG com `CadImage.Load`.
- **Qual classe define a área de visualização?** `Viewport` dentro de `CadRasterizationOptions`.
- **Posso gerar saída em PDF?** Sim, usando `PdfOptions` após a rasterização.
- **Preciso de licença para produção?** É necessária uma licença comercial; uma avaliação gratuita funciona para testes.
- **O .NET Core é suportado?** Absolutamente – Aspose.CAD funciona com .NET Framework, .NET Core e .NET 5/6.

## Pré-requisitos

Antes de mergulhar no código, certifique‑se de que você tem:

- Conhecimento básico de programação em C#.
- Visual Studio (qualquer edição recente) instalado.
- Biblioteca Aspose.CAD adicionada ao seu projeto. Você pode baixá‑la na [página de download do Aspose.CAD](https://releases.aspose.com/cad/net/).
- Um arquivo DWG de exemplo, como **Bottom_plate.dwg**, para acompanhar.

## Importar namespaces

Adicione as diretivas `using` necessárias no início do seu arquivo C# para que o compilador possa localizar os tipos do Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Agora que o ambiente está pronto, vamos percorrer a implementação passo a passo.

## Como criar viewport dwg c#?

Para criar um viewport personalizado, primeiro carregue o arquivo DWG em um objeto `CadImage`, depois configure `CadRasterizationOptions` com o layout e a escala desejados. Defina a região que deseja exibir, instancie um `CadVportTableObject` com o centro, altura e proporção calculados, substitua o viewport ativo, defina as opções de PDF e, finalmente, salve o resultado.

## Etapa 1: carregar o arquivo dwg

`CadImage.Load` carrega um arquivo DWG em um objeto `CadImage`, que representa o desenho CAD na memória.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Etapa 2: configurar opções de rasterização

`CadRasterizationOptions` especifica como o desenho CAD é rasterizado, incluindo seleção de layout, escala e tamanho de saída.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Etapa 3: definir a região a desenhar

`Point` define as coordenadas X e Y do canto superior esquerdo da região a ser renderizada.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Etapa 4: criar um novo viewport

`CadVportTableObject` representa um objeto viewport que controla a área visível e a proporção do desenho renderizado.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Etapa 5: substituir o viewport ativo

O loop substitui o viewport ativo pelo recém‑criado para aplicar as configurações de visualização personalizadas.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Etapa 6: configurar opções de PDF

`PdfOptions` configura parâmetros de saída PDF, como compressão e metadados.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 7: salvar o dwg renderizado como PDF

`image.Save` grava a imagem renderizada em um arquivo usando as opções de formato especificadas.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Por que usar um viewport personalizado ao renderizar DWG?

Um viewport personalizado permite isolar um layout ou região específica, reduzindo o tamanho do arquivo e melhorando a velocidade de renderização. Aspose.CAD pode renderizar um DWG de 300 páginas em menos de 2 segundos quando um viewport focado é usado, comparado à renderização completa do desenho, que pode levar vários segundos a mais.

## Problemas comuns e soluções

- **Saída em branco** – Certifique‑se de que as coordenadas do viewport estejam dentro dos limites do desenho; use `CadImage.Size` para verificar os limites.
- **Camadas ausentes** – Defina `CadRasterizationOptions.Layouts` para o nome correto do layout; caso contrário, o layout padrão pode estar vazio.
- **Desempenho reduzido** – Desative o anti‑aliasing em `CadRasterizationOptions` se você precisar apenas de uma pré‑visualização rápida.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos, incluindo DWG, DXF, DWF e mais de 20 tipos CAD adicionais.

### Q2: O Aspose.CAD é compatível com .NET Core?

A2: Sim, Aspose.CAD funciona com .NET Framework, .NET Core e as versões mais recentes do .NET.

### Q3: Como posso lidar com diferentes layouts em um arquivo DWG?

A3: Especifique o layout desejado usando a propriedade `Layouts` de `CadRasterizationOptions` antes da renderização.

### Q4: Existem considerações de licenciamento ao usar o Aspose.CAD?

A4: Para detalhes de licenciamento, visite a [página de licenciamento do Aspose.CAD](https://purchase.aspose.com/buy).

### Q5: Onde posso encontrar suporte adicional?

A5: Visite o [fórum do Aspose.CAD](https://forum.aspose.com/c/cad/19) para ajuda da comunidade e discussões.

### Q6: Posso renderizar diretamente para PNG em vez de PDF?

A6: Sim, altere `PdfOptions` para `PngOptions` e chame `image.Save("output.png", pngOptions)`.

### Q7: Como incorporo a imagem renderizada em uma aplicação Windows Forms?

A7: Carregue a imagem salva em um controle `PictureBox` usando `Image.FromFile("output.png")`.

## Conclusão

Agora você sabe como **criar viewport dwg c#** e renderizar um arquivo DWG para PDF (ou outros formatos raster) usando Aspose.CAD. Ao dominar a manipulação de viewport, você obtém controle detalhado sobre a saída visual, essencial para gerar desenhos de engenharia precisos, relatórios ou miniaturas. Explore configurações adicionais de rasterização, experimente diferentes formatos de saída e integre o código em serviços .NET maiores ou utilitários de desktop.

---

**Last Updated:** 2026-08-23  
**Tested with:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Tutoriais Relacionados

- [Como definir Viewport ao converter DWG para PDF com coordenadas em C# - Tutorial Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Aprenda a definir opções de rasterização CAD – Exportar layouts específicos para PDF com Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Como converter DWG para PDF e imagens raster usando Aspose.CAD para .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}