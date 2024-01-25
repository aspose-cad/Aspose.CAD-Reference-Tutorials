---
title: Exportando objetos OLE de arquivos DWG - Tutorial Aspose.CAD
linktitle: Exportando objetos OLE de arquivos DWG
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore o guia passo a passo sobre como exportar objetos OLE de arquivos DWG usando Aspose.CAD for .NET. Aprimore suas habilidades de manipulação de arquivos CAD sem esforço.
type: docs
weight: 12
url: /pt/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## Introdução

Você deseja extrair objetos OLE de arquivos DWG com facilidade? Aspose.CAD for .NET está aqui para agilizar o processo para você. Neste tutorial, orientaremos você na exportação de objetos OLE passo a passo, garantindo que você aproveite ao máximo esta poderosa biblioteca .NET. 

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.CAD for .NET: Certifique-se de ter a biblioteca instalada. Você pode baixá-lo no[Página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

-  Diretório de documentos: configure um diretório onde seus arquivos DWG serão armazenados. Substituir`"Your Document Directory"` no trecho de código fornecido com o caminho real.

## Importar namespaces

Em seu projeto .NET, você precisará importar os namespaces necessários para aproveitar as funcionalidades do Aspose.CAD. Use o seguinte trecho de código:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Etapa 1: definir o diretório de documentos

```csharp
string MyDir = "Your Document Directory";
```

 Substituir`"Your Document Directory"` com o caminho onde seus arquivos DWG estão localizados.

## Etapa 2: especificar arquivos DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Liste os arquivos DWG que você deseja processar na matriz.

## Etapa 3: configurar opções de exportação

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Personalize as opções de exportação com base nas suas necessidades. Neste exemplo, configuramos a exportação de PNG com um layout especificado.

## Etapa 4: iterar por meio de arquivos e exportar

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Itere pelos arquivos DWG especificados, carregue cada um deles e salve o arquivo PNG exportado com as opções definidas.

## Conclusão

Parabéns! Você exportou com sucesso objetos OLE de arquivos DWG usando Aspose.CAD for .NET. Esta poderosa biblioteca simplifica tarefas complexas, proporcionando eficiência e flexibilidade na manipulação de arquivos CAD.

## Perguntas frequentes

### Q1: O Aspose.CAD for .NET é adequado para arquivos CAD juniores e seniores?

A1: Sim, o Aspose.CAD for .NET é versátil e pode lidar com uma ampla variedade de arquivos CAD, incluindo variantes júnior e sênior.

### P2: Posso personalizar opções de exportação para diferentes layouts?

A2: Com certeza! Conforme mostrado no tutorial, você pode personalizar as opções de exportação, incluindo layouts, para atender às suas necessidades específicas.

### Q3: Onde posso encontrar documentação detalhada do Aspose.CAD for .NET?

 A3: Explore o[Documentação do Aspose.CAD para .NET](https://reference.aspose.com/cad/net/) para obter informações detalhadas e exemplos.

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode experimentar os recursos do Aspose.CAD for .NET com uma avaliação gratuita. Visita[esse link](https://releases.aspose.com/) para começar.

### P5: Como posso obter suporte ou me conectar com a comunidade?

 A5: Para apoio e envolvimento da comunidade, visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).