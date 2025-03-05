---
title: Adicionando marcas d'água a desenhos CAD - Guia Aspose.CAD
linktitle: Adicionando marcas d'água a desenhos CAD
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprimore seus desenhos CAD com marcas d'água profissionais usando Aspose.CAD for .NET. Siga nosso guia passo a passo para designs personalizados e envolventes.
type: docs
weight: 11
url: /pt/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Introdução

Você deseja aprimorar seus desenhos CAD adicionando marcas d’água profissionais? Aspose.CAD for .NET fornece uma solução robusta para integrar marcas d'água perfeitamente em seus arquivos CAD. Neste guia passo a passo, orientaremos você no processo de adição de marcas d'água usando Aspose.CAD, garantindo que seus desenhos não apenas transmitam informações críticas, mas também carreguem sua marca exclusiva.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter o seguinte:
-  Aspose.CAD para .NET: Certifique-se de ter a biblioteca Aspose.CAD instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).
- Seu diretório de documentos: configure um diretório para armazenar seus desenhos CAD.
Agora, vamos começar a adicionar marcas d'água aos seus desenhos CAD!

## Importar namespaces

Comece importando os namespaces necessários para o seu projeto .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Etapa 1: carregar o desenho CAD

```csharp
// O caminho para o diretório de documentos.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Etapa 2: adicionar marca d'água como MTEXT

```csharp
// Adicionar novo MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Etapa 3: ou adicione marca d'água como texto

```csharp
// Alternativamente, adicione uma entidade mais simples como Texto
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Passo 4: Exportar para PDF

```csharp
// Exporte o desenho CAD com marca d'água para PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Repita essas etapas para desenhos diferentes e você terá arquivos CAD com marca d'água com aparência profissional rapidamente!

## Conclusão

Parabéns! Você aprendeu com sucesso como adicionar marcas d’água aos seus desenhos CAD usando Aspose.CAD for .NET. Este processo simples, mas poderoso, permite que você personalize seus projetos enquanto mantém a integridade de seus desenhos técnicos.

## Perguntas frequentes

### Q1: Posso personalizar a aparência da marca d'água?

A1: Sim, você pode personalizar o texto, a fonte, o tamanho e a posição da marca d'água de acordo com suas preferências.

### Q2: O Aspose.CAD é compatível com diferentes formatos de arquivo CAD?

A2: Aspose.CAD suporta vários formatos de arquivo CAD, incluindo DWG e DXF, garantindo ampla compatibilidade.

### Q3: Posso adicionar várias marcas d'água a um único desenho CAD?

A3: Com certeza! Você pode adicionar quantas marcas d'água forem necessárias, proporcionando flexibilidade para diferentes casos de uso.

### Q4: O Aspose.CAD oferece uma avaliação gratuita?

A4: Sim, você pode explorar os recursos do Aspose.CAD com uma avaliação gratuita. Pegue[aqui](https://releases.aspose.com/).

### Q5: Onde posso encontrar suporte para Aspose.CAD?

 A5: Para qualquer dúvida ou assistência, visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).