---
title: Configurando o tamanho e o modo da tela no Aspose.CAD para .NET
linktitle: Configurando o tamanho e o modo da tela
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore o guia passo a passo sobre como definir o tamanho e o modo da tela no Aspose.CAD for .NET. Otimize sua renderização CAD com facilidade usando este tutorial abrangente.
type: docs
weight: 16
url: /pt/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Introdução

Você está pronto para desbloquear todo o potencial do Aspose.CAD for .NET e revolucionar sua experiência de renderização CAD? Neste tutorial passo a passo, nos aprofundaremos nas complexidades da configuração do tamanho e modo da tela usando a poderosa biblioteca Aspose.CAD. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este guia irá orientá-lo durante o processo, garantindo que você aproveite os recursos do Aspose.CAD de maneira eficaz.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD do[Site Aspose.CAD](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: certifique-se de ter um ambiente de desenvolvimento .NET configurado em sua máquina.

-  Arquivo CAD de amostra: Para este tutorial, usaremos um arquivo DXF de amostra. Você pode encontrar um no[Documentação Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importar namespaces

Para começar, importe os namespaces necessários no início do seu aplicativo .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passo 1: Carregar arquivo CAD

Comece carregando o arquivo CAD usando o seguinte código:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Seu código para etapas adicionais irá aqui
}
```

## Etapa 2: Criar CadRasterizationOptions

 Crie uma instância de`CadRasterizationOptions` e defina suas propriedades:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Etapa 3: criar opções de PDF

 Crie uma instância de`PdfOptions` e definir seu`VectorRasterizationOptions` propriedade:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 4: Exportar para PDF

Exporte o arquivo CAD para PDF usando as opções configuradas:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Etapa 5: criar opções Tiff

 Crie uma instância de`TiffOptions` e definir seu`VectorRasterizationOptions` propriedade:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 6: exportar para TIFF

Exporte o arquivo CAD para TIFF usando as opções configuradas:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusão

Parabéns! Você definiu com sucesso o tamanho e o modo da tela no Aspose.CAD for .NET. Este poderoso recurso abre um mundo de possibilidades para renderização CAD. Experimente diferentes opções e descubra todo o potencial do Aspose.CAD em suas aplicações .NET.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD com outras bibliotecas .NET?

A1: Sim, o Aspose.CAD integra-se perfeitamente com outras bibliotecas .NET, fornecendo recursos aprimorados para manipulação de CAD.

### Q2: Há uma avaliação gratuita disponível para Aspose.CAD?

 A2: Sim, você pode explorar os recursos do Aspose.CAD com uma avaliação gratuita. Visita[aqui](https://releases.aspose.com/) para começar.

### Q3: Como posso obter suporte para Aspose.CAD?

 A3: Para suporte e discussões, visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Onde posso encontrar documentação abrangente para Aspose.CAD?

 A4: Consulte o[Documentação Aspose.CAD](https://reference.aspose.com/cad/net/) para obter informações detalhadas e exemplos.

### Q5: Como faço para adquirir o Aspose.CAD para .NET?

 A5: Para adquirir o Aspose.CAD, visite o[página de compra](https://purchase.aspose.com/buy).