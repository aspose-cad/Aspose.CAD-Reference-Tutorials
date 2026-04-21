---
date: 2026-03-29
description: Aprenda como converter DGN para PNG usando Aspose.CAD para .NET. Este
  guia também aborda o suporte ao formato de arquivo CAD e o conjunto completo de
  elementos DGN suportados.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DGN para PNG com Aspose.CAD para .NET
url: /pt/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DGN para PNG com Aspose.CAD para .NET

## Introdução

Você é um desenvolvedor .NET que deseja **converter DGN para PNG** de forma simples? O Aspose.CAD para .NET oferece uma solução robusta para manipular arquivos DGN com eficiência. Neste tutorial, exploraremos os elementos DGN suportados, orientando‑o no uso do Aspose.CAD para .NET e mostrando exatamente como exportar esses elementos para imagens PNG.

## Respostas Rápidas
- **O que o Aspose.CAD faz?** Ele lê, modifica e converte arquivos CAD/BIM (incluindo DGN) para formatos raster como PNG.  
- **Posso converter elementos DGN 2D e 3D?** Sim – tanto entidades 2‑D quanto 3‑D são suportadas.  
- **Quais versões do .NET são necessárias?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Preciso de licença para testes?** Existe uma avaliação gratuita; uma licença é necessária para produção.  
- **Onde obtenho a biblioteca?** Baixe-a no site oficial da Aspose (link abaixo).

## O que significa “converter DGN para PNG”?
Converter DGN para PNG significa renderizar o desenho vetorial DGN (2‑D ou 3‑D) em um formato de imagem raster (PNG). Isso é útil quando você precisa exibir desenhos CAD na web, incorporá‑los em relatórios ou gerar miniaturas sem exigir um visualizador CAD.

## Por que usar Aspose.CAD para .NET para suporte a formatos de arquivos CAD?
- **Suporte total a formatos CAD** – DGN, DWG, DXF, DWF e muito mais.  
- **Sem dependências externas** – biblioteca pura .NET, sem necessidade de instalações CAD nativas.  
- **Renderização de alta fidelidade** – preserva espessuras de linha, cores e geometria 3‑D.  
- **Processamento em lote** – percorra facilmente muitos arquivos em uma aplicação server‑side.

## Pré‑requisitos

Antes de começar, certifique‑se de que você possui:

- Conhecimento básico de programação .NET.  
- Visual Studio instalado na sua máquina.  
- Biblioteca Aspose.CAD para .NET, que pode ser baixada [aqui](https://releases.aspose.com/cad/net/).

## Importar Namespaces

Para iniciar seu projeto, importe os namespaces necessários ao seu aplicativo .NET. Esta etapa garante acesso às funcionalidades fornecidas pelo Aspose.CAD para .NET.

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

## Como Converter DGN para PNG

A seguir, um guia passo a passo que mostra como carregar um arquivo DGN, percorrer seus elementos, manipular entidades 2‑D e 3‑D e, finalmente, exportar o resultado para uma imagem raster PNG.

### Etapa 1: Carregar o Arquivo DGN

Comece carregando um arquivo DGN existente como um `DgnImage` em sua aplicação .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Etapa 2: Percorrer os Elementos DGN

Percorra os elementos DGN usando um loop `foreach`. O Aspose.CAD para .NET oferece diversos tipos de elementos DGN com os quais você pode trabalhar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Etapa 3: Manipular Entidades 2‑D Suportadas Anteriormente

Essas entidades agora também são suportadas para renderização 3‑D. A instrução switch permite ramificar a lógica com base no tipo de elemento.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Etapa 4: Manipular Entidades 3‑D Suportadas

O Aspose.CAD adiciona suporte total a várias entidades DGN 3‑D. Expanda o switch para processá‑las conforme necessário.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Etapa 5: Exportar e Salvar como PNG

Após as manipulações necessárias, exporte o desenho DGN para uma imagem raster PNG e salve‑a no diretório especificado.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Dica profissional:** Use `Image.Save` com `new PngOptions()` para controlar resolução, cor de fundo e outras configurações específicas do PNG.

## Visão Geral do Suporte a Formatos de Arquivo CAD

O Aspose.CAD para .NET não se limita ao DGN. Ele também oferece suporte a DWG, DXF, DWF e muitos outros formatos CAD, proporcionando uma única API para lidar com um amplo espectro de desenhos de engenharia. Isso o torna ideal para projetos que exigem **suporte a formatos de arquivo CAD** em vários padrões.

## Problemas Comuns & Soluções

| Problema | Motivo | Solução |
|----------|--------|---------|
| **Imagem aparece em branco** | Exportado com DPI zero | Defina `ResolutionX` e `ResolutionY` em `PngOptions`. |
| **Geometria 3‑D ausente** | Tipo de elemento não tratado no switch | Adicione o caso `DgnElementType` ausente e renderize adequadamente. |
| **Falha por falta de memória em arquivos grandes** | Carregamento do arquivo inteiro de uma vez | Processe os elementos em lotes ou use streaming quando possível. |

## Perguntas Frequentes

### Q1: Onde encontro a documentação do Aspose.CAD para .NET?
A1: Você pode acessar a documentação [aqui](https://reference.aspose.com/cad/net/).

### Q2: Como faço o download do Aspose.CAD para .NET?
A2: Baixe a biblioteca [aqui](https://releases.aspose.com/cad/net/).

### Q3: Existe uma avaliação gratuita disponível para o Aspose.CAD para .NET?
A3: Sim, você pode acessar a avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Onde obtenho licenças temporárias para o Aspose.CAD para .NET?
A4: Licenças temporárias estão disponíveis [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Precisa de ajuda ou tem dúvidas?
A5: Visite o fórum da comunidade Aspose.CAD para .NET [support forum](https://forum.aspose.com/c/cad/19).

---

**Última atualização:** 2026-03-29  
**Testado com:** Aspose.CAD para .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}