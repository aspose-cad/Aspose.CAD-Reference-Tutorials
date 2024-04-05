---
title: Ajustando o tamanho do desenho CAD no Aspose.CAD para .NET
linktitle: Ajustando o tamanho do desenho CAD
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como ajustar facilmente os tamanhos dos desenhos CAD no .NET usando Aspose.CAD. Siga nosso guia passo a passo para redimensionar perfeitamente.
type: docs
weight: 10
url: /pt/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Introdução

Você deseja ajustar perfeitamente o tamanho dos desenhos CAD em seus aplicativos .NET? Aspose.CAD for .NET fornece uma solução robusta, permitindo que você lide facilmente com o redimensionamento de desenhos CAD. Neste tutorial, orientaremos você através do processo, detalhando cada etapa para garantir que você compreenda os meandros do redimensionamento de desenhos CAD usando Aspose.CAD.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Biblioteca Aspose.CAD for .NET: Baixe e instale a biblioteca do[Página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Exemplo de desenho CAD: Certifique-se de ter um arquivo de exemplo de desenho CAD (por exemplo, "sample.dwg") em seu diretório de documentos.

## Importar namespaces

Comece importando os namespaces necessários para seu aplicativo .NET. Esta etapa é crucial para acessar as funcionalidades disponibilizadas pelo Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o desenho CAD

Comece carregando o desenho CAD em uma instância da classe Aspose.CAD.Image. Certifique-se de ter o caminho de arquivo correto para seu desenho de amostra.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Carregar um desenho CAD em uma instância de imagem
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Seu código aqui...
}
```

## Etapa 2: criar opções Bmp

Crie uma instância da classe BmpOptions, responsável por especificar opções ao salvar o desenho CAD como um arquivo BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Etapa 3: definir opções de CadRasterization

Instancie a classe CadRasterizationOptions e configure suas propriedades para rasterização vetorial.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Etapa 4: definir a propriedade UnitType

Defina a propriedade UnitType de CadRasterizationOptions para especificar o tipo de unidade para redimensionamento. Neste exemplo, está definido como Centímetro.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Etapa 5: definir propriedade de layouts

Especifique os layouts que deseja incluir no desenho redimensionado definindo a propriedade Layouts.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Passo 6: Exportar para BMP

Por fim, salve o layout redimensionado como um arquivo BMP usando o método Salvar.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Agora você ajustou com sucesso o tamanho do seu desenho CAD usando Aspose.CAD for .NET!

## Conclusão

Neste tutorial, percorremos o processo de redimensionamento de desenhos CAD em .NET usando Aspose.CAD. Seguindo essas etapas, você pode integrar perfeitamente essa funcionalidade em seus aplicativos, proporcionando uma experiência de usuário tranquila.

## Perguntas frequentes

### Q1: O Aspose.CAD for .NET é compatível com todos os formatos CAD?

 A1: Aspose.CAD for .NET suporta uma ampla variedade de formatos CAD, incluindo DWG, DXF, DWF e muito mais. Verifica a[documentação](https://reference.aspose.com/cad/net/) para a lista completa.

### P2: Posso redimensionar vários layouts simultaneamente?

A2: Sim, você pode redimensionar vários layouts ajustando a matriz de layouts em CadRasterizationOptions.

### Q3: Onde posso obter suporte para Aspose.CAD for .NET?

 A3: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e assistência comunitária.

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode explorar um[teste grátis](https://releases.aspose.com/) para avaliar os recursos do Aspose.CAD for .NET.

### Q5: Como posso obter uma licença temporária do Aspose.CAD for .NET?

 A5: Obtenha uma licença temporária para fins de teste[aqui](https://purchase.aspose.com/temporary-license/).