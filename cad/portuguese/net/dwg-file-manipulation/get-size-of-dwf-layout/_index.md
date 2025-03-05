---
title: Trabalhando com arquivos DWG em C# – Obtenha o tamanho do layout DWF
linktitle: Trabalhando com arquivos DWG em C# – Obtenha o tamanho do layout DWF
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore o poder do Aspose.CAD for .NET no manuseio de arquivos DWG. Aprenda a extrair tamanhos de layout DWF sem esforço usando C#.
type: docs
weight: 10
url: /pt/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Introdução

No domínio do design auxiliado por computador (CAD) e do desenvolvimento .NET, o Aspose.CAD se destaca como uma ferramenta poderosa para lidar com arquivos DWG. Este tutorial irá guiá-lo através do processo de trabalhar com arquivos DWG em C# e extrair o tamanho de um layout DWF. Antes de mergulharmos no código, vamos garantir que você tenha tudo configurado para embarcar nesta jornada.

## Pré-requisitos

Para seguir este tutorial perfeitamente, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD for .NET: Certifique-se de ter o Aspose.CAD for .NET instalado. Você pode baixá-lo no[Página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

Agora que você tem as ferramentas necessárias, vamos entrar na área de codificação.

## Importar namespaces

Antes de começarmos a trabalhar com o código, vamos importar os namespaces necessários:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Esses namespaces fornecerão as classes e métodos essenciais para lidar com arquivos CAD com Aspose.CAD em seu aplicativo C#.

## Etapa 1: configure seu ambiente

Comece garantindo que você tenha o ambiente correto configurado para o seu projeto. Faça referência à biblioteca Aspose.CAD em seu projeto C#.

## Etapa 2: definir caminhos de arquivo

Defina os caminhos para o seu arquivo DWG e o diretório de saída dos arquivos JPG gerados:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Etapa 3: carregar a imagem DWF

Carregue a imagem DWF usando Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // O código para etapas adicionais irá aqui
}
```

## Etapa 4: iterar pelas páginas

Itere pelas páginas da imagem DWF:

```csharp
foreach (var page in image.Pages)
{
    // O código para etapas adicionais irá aqui
}
```

## Etapa 5: Obtenha informações de layout

Obtenha informações de layout de cada página:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Etapa 6: configurar opções de JPG

Configure opções para salvar o layout como arquivo JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // O código para etapas adicionais irá aqui
}
```

## Etapa 7: determinar o tamanho da página

Determine o tamanho do layout DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// O código para etapas adicionais irá aqui
```

## Etapa 8: configurar as dimensões da página

Configure as dimensões da página com base no tipo de unidade:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Etapa 9: salve o arquivo JPG

Salve o arquivo JPG com as opções especificadas:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Agora você extraiu com sucesso o tamanho do layout DWF do arquivo DWG usando Aspose.CAD em C#. Sinta-se à vontade para explorar mais recursos e funcionalidades que Aspose.CAD oferece para desenvolvimento .NET.

## Conclusão

Neste tutorial, percorremos o processo de trabalhar com arquivos DWG em C# usando Aspose.CAD. Seguindo essas etapas, você pode não apenas obter o tamanho de um layout DWF, mas também aproveitar os recursos do Aspose.CAD para várias tarefas relacionadas a CAD em seus projetos .NET.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com os formatos de arquivo DWG mais recentes?

 A1: Aspose.CAD suporta vários formatos de arquivo DWG, incluindo as versões mais recentes. Consulte o[documentação](https://reference.aspose.com/cad/net/) para obter detalhes específicos de compatibilidade.

### Q2: Posso usar o Aspose.CAD para projetos comerciais e pessoais?

 A2: Sim, Aspose.CAD oferece opções de licenciamento flexíveis para uso comercial e pessoal. Visite a[página de compra](https://purchase.aspose.com/buy) para mais detalhes.

### Q3: Como posso obter uma licença temporária para Aspose.CAD?

 A3: Você pode obter uma licença temporária de[aqui](https://purchase.aspose.com/temporary-license/) para fins de avaliação.

### Q4: Onde posso encontrar suporte para Aspose.CAD?

A4: Para qualquer dúvida ou assistência, visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Existe uma avaliação gratuita disponível para Aspose.CAD?

 A5: Sim, você pode acessar uma versão de teste gratuita do Aspose.CAD[aqui](https://releases.aspose.com/).