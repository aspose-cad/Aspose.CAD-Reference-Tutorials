---
title: Exportando arquivos DGN incorporados - Tutorial Aspose.CAD
linktitle: Exportando arquivos DGN incorporados
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore o poder do Aspose.CAD para .NET. Aprenda a exportar arquivos DGN incorporados para PDF sem esforço com este tutorial passo a passo.
type: docs
weight: 14
url: /pt/net/export-techniques/exporting-embedded-dgn-files/
---
## Introdução

No mundo dinâmico do desenvolvimento de software, Aspose.CAD for .NET se destaca como uma ferramenta poderosa para lidar com arquivos de Design Auxiliado por Computador (CAD). Este tutorial irá guiá-lo através do processo de exportação de arquivos DGN incorporados usando Aspose.CAD for .NET. Quer você seja um desenvolvedor experiente ou um iniciante curioso, este guia passo a passo o ajudará a aproveitar os recursos do Aspose.CAD de maneira eficaz.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

1.  Aspose.CAD para .NET: Baixe e instale a biblioteca em[Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

2. Ambiente de desenvolvimento: configure um ambiente de desenvolvimento .NET com Visual Studio ou qualquer outro IDE preferido.

3. Exemplo de arquivo DXF: Para este tutorial, usaremos o arquivo "conic_pyramid.dxf". Certifique-se de tê-lo disponível no diretório de documentos designado.

## Importar namespaces

No seu código C#, certifique-se de importar os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Passo 1: Carregue o arquivo DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Seu código para etapas adicionais irá aqui
}
```

## Etapa 2: definir opções de rasterização

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Passo 3: Definir opções de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 4: Salvar como PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Etapa 5: exibir mensagem de sucesso

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusão

Parabéns! Você exportou com sucesso um arquivo DGN incorporado para PDF usando Aspose.CAD for .NET. Este tutorial abordou as etapas essenciais, fornecendo uma base para explorar funcionalidades mais avançadas oferecidas pelo Aspose.CAD.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET com outras linguagens de programação?

A1: Aspose.CAD oferece suporte principalmente a .NET, mas Aspose fornece bibliotecas para várias linguagens, incluindo Java e Python.

### Q2: Existe uma avaliação gratuita disponível para Aspose.CAD for .NET?

 A2: Sim, você pode obter uma avaliação gratuita em[aqui](https://releases.aspose.com/).

### Q3: Onde posso encontrar documentação abrangente para Aspose.CAD for .NET?

 A3: Consulte a documentação[aqui](https://reference.aspose.com/cad/net/).

### Q4: Como obtenho licenciamento temporário para Aspose.CAD for .NET?

 A4: Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Precisa de assistência ou deseja interagir com a comunidade?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões.