---
title: Criação de PDF único com layouts diferentes - Guia Aspose.CAD
linktitle: Criação de PDF único com layouts diferentes
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Crie um único PDF com diferentes layouts usando Aspose.CAD for .NET. Siga nosso guia passo a passo para integração perfeita e geração eficiente de PDF.
type: docs
weight: 13
url: /pt/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Introdução

Você deseja gerar um único documento PDF a partir de um desenho CAD com diferentes layouts usando Aspose.CAD for .NET? Este guia passo a passo orientará você durante o processo, ajudando você a obter uma integração perfeita e uma criação eficiente de PDF. Aspose.CAD for .NET fornece recursos poderosos para manipular desenhos CAD programaticamente e, neste tutorial, nos concentraremos na criação de um único PDF com diferentes layouts.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos:

-  Aspose.CAD para .NET: Certifique-se de ter o Aspose.CAD para .NET instalado. Você pode baixá-lo em[aqui](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: Configure um ambiente de desenvolvimento .NET e tenha um conhecimento básico de programação C#.

## Importar namespaces

Em seu projeto C#, inclua os namespaces necessários para aproveitar as funcionalidades do Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Etapa 1: carregar a imagem CAD

```csharp
// O caminho para o diretório de documentos.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Seu código para a Etapa 1 vai aqui
}
```

## Etapa 2: personalizar opções de rasterização

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Tamanhos personalizados para vários layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Passo 3: Definir Opções de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Passo 4: Salvar como PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Agora você criou com sucesso um único documento PDF com diferentes layouts usando Aspose.CAD for .NET. Sinta-se à vontade para explorar mais recursos e personalizar o código de acordo com seus requisitos específicos.

## Conclusão

Neste tutorial, abordamos o processo de criação de um único PDF a partir de um desenho CAD com diferentes layouts usando Aspose.CAD for .NET. Esta poderosa biblioteca simplifica as tarefas de manipulação de CAD e oferece flexibilidade para vários cenários.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET com outros formatos CAD?

A1: Sim, Aspose.CAD for .NET suporta vários formatos CAD, como DWG, DXF, DGN e muito mais.

### P2: Existe um teste gratuito disponível?

 A2: Sim, você pode explorar uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD for .NET?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.

### P4: Onde posso encontrar documentação detalhada?

 A4: Consulte a documentação[aqui](https://reference.aspose.com/cad/net/).

### Q5: Posso comprar uma licença do Aspose.CAD for .NET?

 A5: Sim, você pode comprar uma licença[aqui](https://purchase.aspose.com/buy).