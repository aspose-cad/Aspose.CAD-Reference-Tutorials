---
title: Exporte DGN para PDF em Aspose.CAD para .NET
linktitle: Exportar DGN para PDF
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como exportar arquivos DGN para PDF sem esforço com Aspose.CAD for .NET. Um guia passo a passo para manipulação perfeita de arquivos CAD.
type: docs
weight: 12
url: /pt/net/cad-export-formats/export-dgn-to-pdf/
---
## Introdução

No mundo do desenvolvimento .NET, Aspose.CAD é uma biblioteca poderosa que facilita a manipulação e conversão de arquivos CAD. Uma tarefa comum que os desenvolvedores costumam encontrar é exportar arquivos DGN para o formato PDF. Neste tutorial, percorreremos o processo passo a passo, usando Aspose.CAD for .NET.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter o seguinte em vigor:

- Conhecimento prático de C# e do framework .NET.
-  Biblioteca Aspose.CAD para .NET instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/cad/net/).
- Um arquivo DGN de amostra, por exemplo, "Nikon_D90_Camera.dgn" para este tutorial.

## Importar namespaces

No seu projeto C#, comece importando os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o arquivo DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Seu código aqui...
}
```

## Etapa 2: configurar opções de rasterização

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Passo 3: Criar Opções de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 4: Salvar como PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusão

Parabéns! Você exportou com sucesso um arquivo DGN para PDF usando Aspose.CAD for .NET. Este tutorial abordou as etapas essenciais, desde o carregamento do arquivo DGN até a configuração das opções de rasterização e o salvamento da saída como PDF.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET sem conhecimento prévio de CAD?

A1: Com certeza! Aspose.CAD simplifica tarefas complexas de CAD, tornando-o acessível para desenvolvedores com diversas experiências.

### Q2: Onde posso encontrar mais exemplos e documentação para Aspose.CAD?

 A2: Explore o[documentação](https://reference.aspose.com/cad/net/) para guias e exemplos completos.

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD?

A3: Sim, você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Como posso obter licenças temporárias para Aspose.CAD?

 A4: Obtenha licenças temporárias[aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Precisa de ajuda ou tem dúvidas?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.