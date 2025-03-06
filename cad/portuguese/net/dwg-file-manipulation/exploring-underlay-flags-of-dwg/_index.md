---
title: Explorando sinalizadores de subposição de arquivos DWG - Tutorial Aspose.CAD
linktitle: Explorando sinalizadores subjacentes de arquivos DWG
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Desbloqueie o poder do Aspose.CAD for .NET ao explorar sinalizadores de subjacência de arquivos DWG. Siga nosso guia passo a passo.
weight: 13
url: /pt/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Explorando sinalizadores de subposição de arquivos DWG - Tutorial Aspose.CAD

## Introdução

Se você está mergulhando no intrincado mundo dos arquivos CAD, especificamente dos arquivos DWG, e deseja desvendar os mistérios das bandeiras subjacentes, você está no lugar certo. Este tutorial irá guiá-lo através do processo de exploração de sinalizadores de subjacência em arquivos DWG usando a poderosa biblioteca Aspose.CAD for .NET.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter o seguinte:

- Uma compreensão básica de programação C# e .NET.
-  Biblioteca Aspose.CAD para .NET instalada. Se não, você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).
- Um arquivo DWG para teste. Você pode usar o arquivo de amostra "BlockRefDgn.dwg" fornecido no tutorial.

## Importar namespaces

Para começar, você precisa importar os namespaces necessários. Aqui está um trecho para ajudá-lo:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Etapa 1: carregar o arquivo DWG e converter para CadImage

Comece carregando o arquivo DWG existente e convertendo-o em um CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Carregue o arquivo DWG e converta para CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Seu código para as etapas subsequentes irá aqui
}
```

## Etapa 2: iterar por meio de entidades

Em seguida, percorra cada entidade dentro do arquivo DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Seu código para as etapas subsequentes irá aqui
}
```

## Etapa 3: verifique o tipo CadDgnUnderlay

Verifique se a entidade é do tipo CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // Seu código para as etapas subsequentes irá aqui
}
```

## Etapa 4: acessar sinalizadores de subjacência

Acesse diferentes sinalizadores de underlay e extraia informações relevantes:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Conclusão

Parabéns! Você explorou com sucesso os sinalizadores subjacentes de arquivos DWG usando Aspose.CAD para .NET. Este tutorial equipou você com o conhecimento necessário para navegar pelas entidades e extrair informações cruciais sobre subjacências.

## Perguntas frequentes

### Q1: Posso usar o Aspose.CAD for .NET com outros formatos de arquivo CAD?

A1: Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DGN e muito mais. Verifique a documentação para a lista completa.

### Q2: Há uma licença temporária disponível para Aspose.CAD for .NET?

 A2: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q3: Onde posso encontrar suporte para Aspose.CAD for .NET?

 A3: Visite o fórum de suporte[aqui](https://forum.aspose.com/c/cad/19) para assistência.

### Q4: Como posso comprar o Aspose.CAD para .NET?

A4: Compre a biblioteca[aqui](https://purchase.aspose.com/buy).

### Q5: Existe um teste gratuito disponível?

 A5: Sim, você pode acessar a avaliação gratuita[aqui](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
