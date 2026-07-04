---
date: 2026-07-04
description: Aprenda como definir o tamanho da página PDF e exportar PDF a partir
  de imagens CAD 3D usando Aspose.CAD para .NET – um guia passo a passo para converter
  DWG em PDF e salvar CAD como PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Exportando imagens 3D para PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Definir tamanho da página PDF – Exportar imagens 3D para PDF com Aspose.CAD
url: /pt/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando Imagens 3D para PDF - Tutorial Aspose.CAD

## Introdução

Se você precisa **definir o tamanho da página PDF** ao converter um desenho CAD 3‑D para PDF, chegou ao lugar certo. Este tutorial mostra, passo a passo, como carregar um arquivo CAD, configurar as opções de rasterização—including dimensões de página personalizadas—e gerar um PDF de alta fidelidade usando Aspose.CAD para .NET. Ao final, você poderá **exportar PDF a partir de CAD**, **salvar CAD como PDF**, e controlar cada detalhe de layout sem instalar o AutoCAD.

## Respostas Rápidas
- **O que significa “exportar PDF a partir de CAD”?** Ele converte um desenho CAD (DWG, DXF, DGN, etc.) em um PDF que pode ser aberto em qualquer dispositivo.  
- **Qual biblioteca realiza a conversão?** Aspose.CAD for .NET fornece rasterização e exportação para PDF sem dependências externas.  
- **Preciso de uma licença?** É necessária uma licença temporária ou completa para produção; uma versão de avaliação gratuita está disponível.  
- **Posso definir dimensões de página personalizadas?** Sim—use `PageWidth` e `PageHeight` em `RasterizationOptions`.  
- **A geometria 3‑D será mantida?** As entidades 3‑D são rasterizadas; habilite `TypeOfEntities.Entities3D` para suporte total a 3‑D.

## O que é “exportar PDF” no contexto de CAD?

Exportar PDF a partir de CAD significa pegar um desenho CAD (DWG, DXF, DGN, etc.) e convertê‑lo em um arquivo PDF que pode conter gráficos vetoriais, visualizações 3‑D rasterizadas e informações precisas de layout de página, facilitando o compartilhamento com quem não possui software CAD.

## Por que usar Aspose.CAD para exportar PDF?

Aspose.CAD permite que você **defina o tamanho da página PDF** e exporte PDFs totalmente em código .NET gerenciado. Ele suporta mais de 50 formatos CAD, processa arquivos de até 2 GB sem carregar todo o documento na memória, e preserva espessuras de linha, cores e renderização opcional de entidades 3D com DPI de rasterização de até 1200. A biblioteca funciona em Windows, Linux e macOS, portanto os PDFs gerados funcionam em qualquer plataforma.

## Pré‑requisitos

- **Aspose.CAD for .NET** instalado. Baixe‑o na [página de download do Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- Uma pasta contendo os arquivos CAD que você deseja converter (por exemplo, `C:\CAD\`).  
- .NET 6.0 ou posterior (ou .NET Framework 4.7.2).  

## Importar Namespaces

As instruções `using` importam os namespaces Aspose.CAD necessários para trabalhar com opções de rasterização e PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Guia Passo a Passo

### Como definir o tamanho da página PDF ao exportar CAD para PDF?

Carregue seu arquivo CAD, configure as dimensões da página em `RasterizationOptions`, anexe essas opções a uma instância `PdfOptions` e chame `Save`. Esse fluxo de quatro etapas oferece controle total sobre o tamanho e a qualidade da saída, mantendo o código conciso.

### Etapa 1: Carregar a Imagem CAD

A classe `Image` representa um desenho CAD carregado na memória, pronto para rasterização.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Etapa 2: Configurar Opções de Rasterização (Salvar CAD como PDF)

A classe `RasterizationOptions` define como os dados CAD são rasterizados, incluindo tamanho da página, DPI e se as entidades 3‑D são renderizadas.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Etapa 3: Definir Opções de PDF (Criar PDF a partir de CAD)

A classe `PdfOptions` contém as configurações de formato de saída e vincula as opções de rasterização à geração de PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Etapa 4: Salvar como PDF (Gerar PDF a partir de Modelo 3D)

O método `Save` no objeto `Image` grava o conteúdo rasterizado no arquivo PDF especificado, produzindo um documento pronto para ser compartilhado.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Problemas Comuns e Soluções

| Problema | Motivo | Correção |
|----------|--------|----------|
| **PDF de saída está em branco** | Nome de layout errado ou layout `Model` ausente. | Verifique se `rasterizationOptions.Layouts` corresponde a um layout presente no arquivo CAD. |
| **Baixa resolução** | O DPI padrão de rasterização é baixo. | Defina `rasterizationOptions.Resolution = 300;` antes de salvar. |
| **Entidades 3D não exibidas** | `TypeOfEntities` está comentado. | Descomente `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Exceção de licença** | Usando uma avaliação sem licença. | Aplique uma licença temporária ou permanente via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Perguntas Frequentes

**P: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?**  
**R:** Sim, o Aspose.CAD suporta mais de 50 formatos de entrada e saída, incluindo DWG, DXF, DGN, STL e IFC, garantindo flexibilidade para qualquer projeto.

**P: Posso personalizar as dimensões da página ao exportar para PDF?**  
**R:** Absolutamente. Defina `PageWidth` e `PageHeight` em `RasterizationOptions` para qualquer tamanho em pontos, polegadas ou milímetros antes de chamar `Save`.

**P: Licenças temporárias estão disponíveis para Aspose.CAD?**  
**R:** Sim, você pode obter licenças temporárias para Aspose.CAD visitando [Temporary License](https://purchase.aspose.com/temporary-license/).

**P: Onde posso encontrar suporte adicional ou discussões da comunidade?**  
**R:** Acesse o [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) para ajuda especializada e conselhos entre pares.

**P: Existe uma versão de avaliação gratuita do Aspose.CAD?**  
**R:** Sim, você pode explorar os recursos do Aspose.CAD acessando a [versão de avaliação gratuita](https://releases.aspose.com/).

## Conclusão

Agora você tem um método completo e pronto para produção para **definir o tamanho da página PDF** e **exportar PDF a partir de imagens CAD 3D** usando Aspose.CAD para .NET. Ajustando as opções de rasterização, você pode afinar a resolução, o layout da página e a renderização de entidades 3D para atender a qualquer requisito de documentação. Experimente diferentes configurações de DPI e dimensões de página para alcançar o equilíbrio perfeito entre tamanho do arquivo e fidelidade visual.

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Exportando Layouts Específicos para PDF - Guia Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportando DWG para PDF ou Imagens Rasterizadas - Guia Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportar DGN para PDF no Aspose.CAD para .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Última atualização:** 2026-07-04  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose