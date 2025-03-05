---
title: Exporte DGN como parte de DWG no Aspose.CAD para .NET
linktitle: Exportar DGN como parte do DWG
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como exportar DGN como parte de DWG no Aspose.CAD for .NET. Siga nosso guia passo a passo para uma integração perfeita.
type: docs
weight: 11
url: /pt/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Introdução

No mundo do desenvolvimento .NET, Aspose.CAD se destaca como uma biblioteca poderosa para trabalhar com arquivos Computer-Aided Design (CAD). Este tutorial irá guiá-lo através do processo de exportação de um arquivo DGN (Design) como parte de um arquivo DWG (Desenho) usando Aspose.CAD for .NET. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este guia passo a passo o ajudará a aproveitar os recursos do Aspose.CAD para realizar essa tarefa específica com eficiência.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD para .NET: Certifique-se de ter a biblioteca Aspose.CAD para .NET instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: configure seu ambiente de desenvolvimento .NET preferido, como Visual Studio.

- Conhecimento básico de C#: Familiarize-se com a linguagem de programação C#.

## Importar namespaces

Em seu projeto C#, inclua os namespaces necessários para acessar a funcionalidade Aspose.CAD. Adicione o seguinte usando diretivas no início do seu arquivo de código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Agora, vamos dividir o código fornecido em várias etapas:

## Etapa 1: definir caminhos de arquivo

```csharp
//Caminhos de arquivo de entrada e saída
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Passo 2: Criar Instância PdfOptions

```csharp
// Crie uma instância da classe PdfOptions para exportar DWG para PDF
PdfOptions exportOptions = new PdfOptions();
```

## Etapa 3: carregar o arquivo DWG

```csharp
// Carregue o arquivo DWG existente como uma imagem e converta-o para o tipo CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Etapa 4: iterar por meio de entidades

```csharp
// Iterar através de cada entidade dentro do arquivo DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Etapa 5: verifique o tipo de entidade

```csharp
// Verifique se a entidade é uma definição de imagem
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Etapa 6: obter o caminho subjacente

```csharp
// Se for uma definição de imagem, obtenha a referência externa ao objeto
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Etapa 7: Definir opções de rasterização

```csharp
// Definir configurações para o objeto CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Passo 8: Exportar DWG para PDF

```csharp
// Exporte o DWG para PDF chamando o método Save
cadImage.Save(outPath, exportOptions);
```

## Conclusão

Parabéns! Você percorreu com sucesso o processo de exportação de um arquivo DGN como parte de um arquivo DWG usando Aspose.CAD para .NET. Este tutorial forneceu as etapas fundamentais e trechos de código para realizar essa tarefa específica sem problemas.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET em meus projetos comerciais?
 A1: Sim, você pode. Visita[aqui](https://purchase.aspose.com/buy) para explorar opções de licenciamento.

### P2: Há alguma limitação no tamanho dos arquivos DWG que posso processar?
A2: Aspose.CAD suporta o manuseio de arquivos DWG grandes, mas podem ser aplicadas limitações de hardware.

### Q3: Existe uma versão de teste disponível?
A3: Sim, você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Como posso obter licenças temporárias?
 A4: Licenças temporárias podem ser obtidas[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Onde posso procurar assistência se tiver problemas?
 A5: Você pode visitar o fórum Aspose.CAD[aqui](https://forum.aspose.com/c/cad/19) para suporte.