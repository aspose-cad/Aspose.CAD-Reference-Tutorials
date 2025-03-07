---
title: Convertendo DWG em PDF com coordenadas em C# - Tutorial Aspose.CAD
linktitle: Convertendo DWG para PDF com coordenadas em C#
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como converter DWG para PDF com coordenadas específicas em C# usando Aspose.CAD. Siga nosso guia passo a passo para conversões de arquivos CAD precisas e eficientes.
weight: 11
url: /pt/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertendo DWG em PDF com coordenadas em C# - Tutorial Aspose.CAD

## Introdução

Bem-vindo a este tutorial abrangente sobre como converter arquivos DWG em PDF com coordenadas especificadas usando Aspose.CAD for .NET. Aspose.CAD é uma biblioteca poderosa que permite aos desenvolvedores trabalhar perfeitamente com formatos de arquivo CAD em seus aplicativos .NET. Neste tutorial, orientaremos você no processo de conversão de um arquivo DWG em PDF e, ao mesmo tempo, forneceremos coordenadas específicas para aumentar a precisão.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:

- Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD para .NET. Você pode encontrar a biblioteca[aqui](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: certifique-se de ter um ambiente de desenvolvimento compatível configurado, incluindo Visual Studio ou qualquer outro IDE preferido.

- Arquivo DWG: Tenha um arquivo DWG pronto para conversão. Você pode usar o arquivo de exemplo fornecido ou seu arquivo DWG personalizado.

## Importar namespaces

No seu projeto C#, importe os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Vamos dividir o código em um guia passo a passo para uma melhor compreensão:

## Etapa 1: definir o diretório de documentos

```csharp
string MyDir = "Your Document Directory";
```

## Etapa 2: definir o caminho do arquivo DWG de origem

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Etapa 3: carregar o arquivo DWG e configurar as opções de rasterização

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Etapa 4: definir coordenadas e viewport

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Etapa 5: aplicar configurações de viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Passo 6: Configurar Opções de PDF e Exportar

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Etapa 7: exibir mensagem de sucesso

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusão

Parabéns! Você converteu com sucesso um arquivo DWG em PDF com coordenadas especificadas usando Aspose.CAD for .NET. Este tutorial abordou etapas essenciais e forneceu um guia claro para desenvolvedores.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DWF e muito mais.

### P2: Como posso lidar com erros durante o processo de conversão?

A2: Implemente mecanismos de tratamento de erros usando blocos try-catch para capturar e gerenciar exceções.

### Q3: O Aspose.CAD é adequado para ambientes Windows e Linux?

A3: Sim, Aspose.CAD é compatível com plataformas Windows e Linux.

### Q4: Posso personalizar ainda mais a saída do PDF?

A4: Certamente! Explore as amplas opções fornecidas pelo Aspose.CAD para adaptar a saída do PDF às suas necessidades específicas.

### P5: Onde posso encontrar suporte adicional ou discussões na comunidade?

A5: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
