---
title: Renderizando documentos DWG em C# - Guia Aspose.CAD
linktitle: Renderizando documentos DWG em C#
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como renderizar documentos DWG em C# usando Aspose.CAD. Este guia passo a passo aborda importação, configuração e salvamento com exemplos de código.
type: docs
weight: 17
url: /pt/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## Introdução

Bem-vindo ao guia completo sobre renderização de documentos DWG em C# usando Aspose.CAD. Quer você seja um desenvolvedor experiente ou esteja apenas começando com .NET, este tutorial irá orientá-lo no processo de aproveitamento do Aspose.CAD para renderizar arquivos DWG com eficiência. Aspose.CAD é uma API poderosa que fornece funcionalidades robustas para trabalhar com formatos de arquivo CAD, tornando-o uma escolha ideal para desenvolvedores que lidam com arquivos DWG.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos:

- Conhecimento básico da linguagem de programação C#.
- Visual Studio instalado em sua máquina.
-  Biblioteca Aspose.CAD integrada ao seu projeto. Você pode baixá-lo em[aqui](https://releases.aspose.com/cad/net/).
- Um arquivo DWG de amostra, como "Bottom_plate.dwg", para acompanhar os exemplos.

## Importar namespaces

Para começar, certifique-se de importar os namespaces necessários no início do seu código C#:

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

Agora, vamos dividir o exemplo fornecido em várias etapas:

## Etapa 1: carregar o arquivo DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Seu código para carregar o arquivo DWG vai aqui.
}
```

## Etapa 2: configurar opções de rasterização

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Configurações adicionais de rasterização podem ser adicionadas aqui.
```

## Etapa 3: definir a região a ser desenhada

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Etapa 4: crie uma nova viewport

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Etapa 5: substituir a viewport ativa

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

## Passo 6: Configurar Opções de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 7: salve o DWG renderizado como PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Conclusão

Parabéns! Você renderizou com sucesso um documento DWG em PDF usando Aspose.CAD em C#. Sinta-se à vontade para explorar mais recursos e personalizar o código com base em seus requisitos específicos.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DWF e muito mais.

### P2: O Aspose.CAD é compatível com .NET Core?

A2: Sim, Aspose.CAD é compatível com .NET Framework e .NET Core.

### Q3: Como posso lidar com diferentes layouts em um arquivo DWG?

 A3: Você pode especificar o layout desejado no`Layouts` propriedade de`CadRasterizationOptions`.

### Q4: Há alguma consideração de licenciamento para usar o Aspose.CAD?

 A4: Para obter detalhes de licenciamento, visite[aqui](https://purchase.aspose.com/buy).

### P5: Onde posso encontrar suporte adicional?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.