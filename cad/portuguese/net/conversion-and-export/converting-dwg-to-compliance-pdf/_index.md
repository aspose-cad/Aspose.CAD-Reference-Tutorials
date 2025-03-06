---
title: Convertendo DWG em PDF de conformidade - Tutorial Aspose.CAD
linktitle: Convertendo DWG em PDF de conformidade
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Converta DWG em PDF de conformidade com Aspose.CAD para .NET. Siga nosso tutorial para obter orientação passo a passo.
weight: 13
url: /pt/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertendo DWG em PDF de conformidade - Tutorial Aspose.CAD

## Introdução

Bem-vindo ao nosso tutorial passo a passo sobre como converter arquivos DWG em PDF de conformidade usando Aspose.CAD para .NET. Aspose.CAD é uma API .NET poderosa que permite aos desenvolvedores trabalhar com formatos de arquivo CAD sem esforço. Neste tutorial, orientaremos você no processo de conversão de um arquivo DWG em PDF de conformidade com exemplos e explicações detalhadas.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD para .NET: Certifique-se de ter a biblioteca Aspose.CAD integrada ao seu projeto .NET. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: tenha um ambiente de desenvolvimento .NET funcional instalado e certifique-se de que esteja configurado corretamente.

- Arquivo DWG de amostra: baixe um arquivo DWG de amostra que deseja converter em PDF de conformidade.

## Importar namespaces

Em seu projeto .NET, importe os namespaces necessários para utilizar as funcionalidades do Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Agora, vamos dividir o processo de conversão de um arquivo DWG em PDF de conformidade em várias etapas.

## Etapa 1: carregar o arquivo DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Etapa 2: definir opções de rasterização

 Crie uma instância de`CadRasterizationOptions` e configure suas propriedades, como cor de fundo, largura e altura da página.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Passo 3: Criar Opções de PDF

 Crie uma instância de`PdfOptions` e defina as opções de rasterização vetorial.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Etapa 4: Salvar como PDF (conformidade com A1a)

Salve a imagem CAD como PDF de conformidade com conformidade A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Etapa 5: Salvar como PDF (conformidade com A1b)

Altere o tipo de conformidade para A1b e salve a imagem CAD como PDF de conformidade.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Conclusão

Parabéns! Você converteu com sucesso um arquivo DWG em PDF de conformidade usando Aspose.CAD para .NET. Este tutorial fornece um guia completo para desenvolvedores que desejam integrar recursos de conversão CAD em seus aplicativos.

## Perguntas frequentes

### Q1: Posso converter outros formatos CAD em PDF de conformidade usando Aspose.CAD?

A1: Sim, o Aspose.CAD suporta vários formatos CAD, permitindo a conversão para PDF de conformidade.

### P2: O Aspose.CAD é compatível com .NET Core?

A2: Sim, Aspose.CAD é compatível com .NET Framework e .NET Core.

### Q3: Existe alguma opção de licenciamento para Aspose.CAD?

 A3: Sim, você pode explorar opções de licenciamento[aqui](https://purchase.aspose.com/buy).

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q5: Onde posso obter suporte para Aspose.CAD?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para quaisquer dúvidas relacionadas ao suporte.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
