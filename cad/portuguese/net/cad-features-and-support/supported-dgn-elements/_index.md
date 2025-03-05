---
title: Elementos DGN suportados em Aspose.CAD para .NET
linktitle: Elementos DGN suportados
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore os recursos poderosos do Aspose.CAD for .NET para lidar com arquivos DGN. Siga nosso guia passo a passo para trabalhar perfeitamente com elementos 2D e 3D.
type: docs
weight: 18
url: /pt/net/cad-features-and-support/supported-dgn-elements/
---
## Introdução

Você é um desenvolvedor .NET que deseja trabalhar perfeitamente com arquivos DGN? Aspose.CAD for .NET fornece uma solução robusta para lidar com arquivos DGN com eficiência. Neste tutorial, nos aprofundaremos nos elementos DGN suportados, orientando você no processo de trabalho com Aspose.CAD for .NET.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

- Conhecimento básico de programação .NET.
- Visual Studio instalado em sua máquina.
-  Biblioteca Aspose.CAD para .NET, que você pode baixar[aqui](https://releases.aspose.com/cad/net/).

## Importar namespaces

Para iniciar seu projeto, importe os namespaces necessários para seu aplicativo .NET. Esta etapa garante que você tenha acesso às funcionalidades fornecidas pelo Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Etapa 1: carregar o arquivo DGN

Comece carregando um arquivo DGN existente como CadImage em seu aplicativo .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Seu código aqui
}
```

## Etapa 2: iterar por meio de elementos DGN

Itere através dos elementos DGN usando um loop foreach. Aspose.CAD for .NET fornece uma variedade de tipos de elementos DGN com os quais você pode trabalhar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Seu código aqui
}
```

## Etapa 3: lidar com entidades suportadas anteriormente

Manipule as entidades 2D anteriormente suportadas, que agora também são suportadas para 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Casos adicionais
        {
            // Seu código aqui
            break;
        }
}
```

## Etapa 4: lidar com entidades 3D suportadas

Lide com as entidades 3D suportadas fornecidas pelo Aspose.CAD for .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Seu código aqui
            break;
        }
}
```

## Etapa 5: exportar e salvar

Por fim, exporte o arquivo DGN modificado para uma imagem raster e salve-o no diretório especificado.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusão

Neste tutorial, exploramos os recursos do Aspose.CAD for .NET no manuseio e manipulação de arquivos DGN. Seguindo o guia passo a passo, você pode trabalhar de forma eficiente com elementos DGN suportados, sejam eles entidades 2D ou 3D. Aspose.CAD for .NET permite que você integre perfeitamente o processamento de arquivos DGN em seus aplicativos .NET.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.CAD for .NET?

 A1: Você pode encontrar a documentação[aqui](https://reference.aspose.com/cad/net/).

### Q2: Como faço o download do Aspose.CAD para .NET?

 A2: Você pode baixar a biblioteca[aqui](https://releases.aspose.com/cad/net/).

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD for .NET?

 A3: Sim, você pode acessar a avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Onde posso obter licenças temporárias do Aspose.CAD for .NET?

 A4: Licenças temporárias estão disponíveis[aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Precisa de ajuda ou tem dúvidas?

 A5: Visite a comunidade Aspose.CAD for .NET[Fórum de suporte](https://forum.aspose.com/c/cad/19).