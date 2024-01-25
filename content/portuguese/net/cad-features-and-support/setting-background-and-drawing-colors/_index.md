---
title: Configurando cores de fundo e de desenho no Aspose.CAD para .NET
linktitle: Definir cores de fundo e de desenho
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Domine Aspose.CAD para .NET. Defina as cores do plano de fundo e do desenho sem esforço. Siga nosso guia passo a passo.
type: docs
weight: 15
url: /pt/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## Introdução

No mundo dinâmico do desenvolvimento .NET, o Aspose.CAD surge como uma ferramenta poderosa para lidar com arquivos de Design Auxiliado por Computador (CAD). Se você deseja aprimorar suas habilidades na manipulação de desenhos CAD, este tutorial é a sua porta de entrada. Iremos nos aprofundar nos meandros da configuração de cores de fundo e desenho usando Aspose.CAD for .NET, fornecendo um guia passo a passo que garante clareza e eficácia.

## Pré-requisitos

Antes de embarcarmos nesta jornada, certifique-se de ter os seguintes pré-requisitos em vigor:

- Compreensão básica do desenvolvimento .NET.
-  Instalação do Aspose.CAD para .NET. Se você ainda não fez isso, você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).
- Um arquivo CAD de amostra para experimentação. Você pode encontrar um em seu diretório de documentos.

## Importar namespaces

No seu projeto .NET, comece importando os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o arquivo CAD

Comece carregando o arquivo CAD com o qual deseja trabalhar usando o seguinte trecho de código:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Seu código para processamento posterior vai aqui
}
```

## Etapa 2: configurar opções de rasterização

 Crie uma instância de`CadRasterizationOptions` e defina suas propriedades para configuração de fundo e cor do desenho:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## Passo 3: Exportar para PDF

 Crie uma instância de`PdfOptions` e definir o`VectorRasterizationOptions` propriedade:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// Exportar CAD para PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Etapa 4: exportar para TIFF

 Crie uma instância de`TiffOptions` e definir o`VectorRasterizationOptions` propriedade:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// Exportar CAD para TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como definir cores de fundo e de desenho no Aspose.CAD for .NET. Este tutorial fornece habilidades para manipular arquivos CAD sem esforço.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET com qualquer tipo de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF e DGN.

### Q2: Há uma avaliação gratuita disponível para Aspose.CAD for .NET?

 A2: Sim, você pode explorar uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q3: Onde posso encontrar documentação detalhada do Aspose.CAD for .NET?

 A3: Consulte a documentação[aqui](https://reference.aspose.com/cad/net/).

### Q4: Como posso obter licenciamento temporário para Aspose.CAD?

 A4: Licenças temporárias podem ser obtidas[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Precisa de ajuda ou deseja se conectar com a comunidade?

 A5: Visite o fórum de suporte[aqui](https://forum.aspose.com/c/cad/19).
