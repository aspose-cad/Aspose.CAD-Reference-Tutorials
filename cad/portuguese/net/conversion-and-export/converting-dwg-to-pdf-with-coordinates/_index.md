---
date: 2026-04-03
description: Aprenda como definir a viewport e converter DWG para PDF em C# usando
  Aspose.CAD. Este tutorial de DWG para PDF mostra exportação precisa com coordenadas.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Convertendo DWG para PDF com Coordenadas em C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Como definir a viewport ao converter DWG para PDF com coordenadas em C# – Tutorial
  Aspose.CAD
url: /pt/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertendo DWG para PDF com Coordenadas em C# - Tutorial Aspose.CAD

## Introdução

Bem-vindo a este tutorial abrangente sobre **how to set viewport** ao converter arquivos DWG para PDF com coordenadas especificadas usando Aspose.CAD para .NET. Ao controlar o viewport, você obtém PDFs pixel‑perfeitos que correspondem exatamente à área que você precisa — perfeito para desenhos de construção, pré‑visualizações de plantas baixas ou qualquer fluxo de trabalho BIM.

## Respostas Rápidas
- **What does “set viewport” mean?** Ele define a região visível e a escala do desenho CAD durante a rasterização.  
- **Which library handles the conversion?** Aspose.CAD for .NET.  
- **Do I need a license?** Um teste gratuito funciona para avaliação; uma licença comercial é necessária para produção.  
- **Supported platforms?** Windows, Linux e macOS com .NET 5/6/7 ou .NET Framework 4.6+.  
- **Typical implementation time?** Cerca de 10‑15 minutos para uma conversão básica.

## Pré-requisitos

Antes de começarmos, certifique‑se de que você possui os seguintes pré‑requisitos:

- **Aspose.CAD Library** – Baixe e instale a biblioteca Aspose.CAD para .NET. Você pode encontrar a biblioteca [aqui](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider ou qualquer IDE que suporte desenvolvimento .NET.
- **DWG File** – Tenha um arquivo DWG pronto para conversão. Você pode usar o arquivo de exemplo fornecido ou seu próprio arquivo DWG personalizado.

## Como Definir o Viewport para Exportação Precisa de PDF

Definir o viewport é a etapa central que permite especificar a área exata do desenho que você deseja renderizar. No código abaixo criamos um novo `CadVportTableObject`, posicionamos com a coordenada superior‑esquerda e calculamos largura, altura e proporção. Esta é a implementação de **how to set viewport** que conduz o restante da conversão.

## Importar Namespaces

Em seu projeto C#, importe os namespaces necessários:

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

Vamos dividir o código em um guia passo a passo para melhor compreensão:

## Etapa 1: Definir o Diretório do Documento

```csharp
string MyDir = "Your Document Directory";
```

## Etapa 2: Definir o Caminho do Arquivo DWG Fonte

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Etapa 3: Carregar o Arquivo DWG e Configurar as Opções de Rasterização

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Etapa 4: Definir Coordenadas e Viewport  

Aqui realmente **set the viewport** (how to set viewport) especificando o canto superior‑esquerdo, largura e altura da área que você deseja exportar.

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

## Etapa 5: Aplicar Configurações de Viewport

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

## Etapa 6: Configurar Opções de PDF e Exportar  

Agora juntamos tudo e **convert DWG to PDF** usando as opções de rasterização que preparamos.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Etapa 7: Exibir Mensagem de Sucesso

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Casos de Uso Comuns

- **Construction documentation** – Gere PDFs imprimíveis de seções específicas de plantas baixas.  
- **BIM coordination** – Exporte apenas a área de interesse para detecção de conflitos.  
- **Client presentations** – Forneça um PDF limpo de um cômodo ou elevação selecionada sem expor todo o desenho.

## Conclusão

Parabéns! Você converteu **DWG to PDF** com coordenadas precisas e aprendeu **how to set viewport** usando Aspose.CAD para .NET. Este **dwg to pdf tutorial** demonstra como **create pdf from dwg** e **export dwg as pdf c#** mantendo controle total sobre a área de saída.

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DWF e outros.

### Q2: Como posso tratar erros durante o processo de conversão?

A2: Implemente mecanismos de tratamento de erros usando blocos try‑catch para capturar e gerenciar exceções.

### Q3: O Aspose.CAD é adequado para ambientes Windows e Linux?

A3: Sim, Aspose.CAD é compatível com plataformas Windows e Linux.

### Q4: Posso personalizar ainda mais a saída PDF?

A4: Certamente! Explore as extensas opções fornecidas pelo Aspose.CAD para adaptar a saída PDF aos seus requisitos específicos.

### Q5: Onde posso encontrar suporte adicional ou discussões da comunidade?

A5: Visite o [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

## Perguntas Frequentes Adicionais

**Q: Essa abordagem funciona com arquivos DWG grandes (centenas de MB)?**  
A: Sim. A rasterização é realizada página por página, e você pode ajustar `rasterizationOptions` (por exemplo, `Resolution`) para equilibrar qualidade e uso de memória.

**Q: Posso exportar múltiplos viewports em páginas PDF separadas?**  
A: Você pode percorrer `cadImage.ViewPorts`, definir cada um como ativo e chamar `Save` para cada página, depois mesclar os PDFs usando Aspose.PDF.

**Q: É possível adicionar uma marca d'água ao PDF gerado?**  
A: Após salvar o PDF, você pode reabri‑lo com Aspose.PDF e aplicar uma marca d'água de texto ou imagem antes de entregá‑lo ao usuário.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}