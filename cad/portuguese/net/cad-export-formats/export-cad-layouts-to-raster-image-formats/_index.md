---
date: 2026-03-21
description: Aprenda como converter dxf para png e outros formatos raster usando Aspose.CAD
  para .NET. Siga nosso guia passo a passo para exportação de camadas CAD sem interrupções.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DXF para PNG com Aspose.CAD para .NET
url: /pt/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar Layouts CAD para Formatos de Imagem Raster no Aspose.CAD para .NET

## Introdução

Você está procurando converter **dxf para png** e outros formatos de imagem raster de forma eficiente usando Aspose.CAD para .NET? Este guia passo a passo o conduzirá pelo processo, fornecendo instruções detalhadas e trechos de código para tornar a tarefa fluida. Seja você um desenvolvedor experiente ou um recém‑chegado ao Aspose.CAD, este tutorial atende a todos os níveis de especialização.

### Respostas Rápidas
- **Qual biblioteca lida com a conversão?** Aspose.CAD for .NET  
- **Formato principal suportado nativamente?** JPEG, PNG, BMP, and TIFF raster images  
- **Posso exportar camadas CAD específicas?** Yes – use `CadRasterizationOptions.Layers` to target individual layers  
- **Preciso de uma licença para produção?** A valid Aspose.CAD license is required for non‑trial use  
- **Versões .NET suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## O que é **convert dxf to png**?

Converter um arquivo DXF (Drawing Exchange Format) para PNG significa rasterizar dados CAD baseados em vetor em uma imagem baseada em pixels. Isso é útil quando você precisa incorporar desenhos CAD em páginas da web, relatórios ou qualquer ambiente que suporte apenas gráficos raster.

## Por que exportar camadas CAD separadamente?

Exportar camadas CAD individualmente oferece controle granular sobre a saída visual, reduz o tamanho do arquivo de cada imagem e permite aplicar estilos ou pós‑processamento específicos de camada. Isso é especialmente útil para grandes desenhos de engenharia onde apenas um subconjunto de camadas é relevante para um determinado público.

## Pré-requisitos

- **Aspose.CAD for .NET Library** – baixe-a no [site da Aspose.CAD](https://releases.aspose.com/cad/net/).  
- **CAD Drawing File** – um arquivo DXF (por exemplo, `conic_pyramid.dxf`) que você deseja converter para formatos raster.  

## Importar Namespaces

Em seu projeto .NET, importe os namespaces necessários para aproveitar as funcionalidades do Aspose.CAD. Inclua os seguintes namespaces no início do seu código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Como **convert dxf to png** – Guia Passo a Passo

### Etapa 1: Carregar Desenho CAD

Primeiro, carregue o arquivo DXF em um objeto `Image`. Este objeto representa todo o desenho CAD na memória.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Etapa 2: Criar `CadRasterizationOptions`

Configure as opções de rasterização, como dimensões de saída e resolução. Essas opções controlam como os dados vetoriais são rasterizados.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Etapa 3: Especificar Camadas (Exportar Camadas CAD)

Se você precisar apenas de uma camada específica, liste seu nome aqui. Isso demonstra **export cad layers** individualmente.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Etapa 4: Escolher um Formato de Imagem – Salvar CAD como PNG (ou JPEG)

Crie um objeto de opções específico para o formato de imagem. Substitua `JpegOptions` por `PngOptions` quando quiser **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Dica profissional:** Para gerar arquivos PNG, basta instanciar `new PngOptions()` em vez de `JpegOptions`.

### Etapa 5: Exportar para Formato JPEG (ou PNG)

Finalmente, salve a imagem rasterizada no disco. A extensão do arquivo determina o formato de saída.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Quando você substituir `JpegOptions` por `PngOptions`, o mesmo código **convert dxf to png** e produzirá um arquivo `.png`.

### Etapa Adicional: Converter Todas as Camadas

Se você precisar **convert cad to raster** para cada camada do desenho, chame o método auxiliar abaixo. Ele itera sobre todas as camadas e salva cada uma como uma imagem separada.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Observação:* A implementação de `ConvertAllLayersToRasterImageFormats` faz parte do conjunto completo de exemplos Aspose.CAD e demonstra o processamento em lote de camadas.

## Problemas Comuns & Solução de Problemas

| Sintoma | Causa Provável | Solução |
|---------|----------------|---------|
| Imagem em branco ou branca | Opções de rasterização não definidas (ex.: `PageWidth`/`PageHeight` = 0) | Certifique‑se de que `PageWidth` e `PageHeight` tenham valores positivos |
| Camadas ausentes | Nome de camada incorreto no array `Layers` | Verifique o nome exato da camada no arquivo CAD (sensível a maiúsculas/minúsculas) |
| PNG de baixa qualidade | DPI padrão está baixo | Defina `rasterizationOptions.Resolution = 300;` para maior qualidade |

## Perguntas Frequentes (Original)

### Q1: Posso usar outros formatos de imagem para exportação?
A1: Sim, você pode. Basta substituir `JpegOptions` pelas opções do formato desejado, como `PngOptions` ou `BmpOptions`.

### Q2: Existe uma versão de avaliação disponível?
A2: Sim, você pode explorar a funcionalidade do Aspose.CAD baixando a versão de avaliação [aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD?
A3: Visite o [fórum](https://forum.aspose.com/c/cad/19) do Aspose.CAD para suporte da comunidade ou considere adquirir uma licença para suporte dedicado.

### Q4: Licenças temporárias estão disponíveis?
A4: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso encontrar a documentação?
A5: Consulte a documentação detalhada [aqui](https://reference.aspose.com/cad/net/).

## FAQ Adicional

**Q: Posso exportar todas as camadas em um único comando?**  
A: Sim, use o método `ConvertAllLayersToRasterImageFormats` mostrado acima.

**Q: O Aspose.CAD suporta formatos vetoriais como SVG?**  
A: Ele foca principalmente em formatos raster, mas você pode exportar para PDF que mantém os dados vetoriais.

**Q: Como controlo a cor de fundo do PNG exportado?**  
A: Defina `rasterizationOptions.BackgroundColor` para a `Color` desejada antes de salvar.

**Q: É possível exportar um único layout em vez de todo o desenho?**  
A: Sim, configure `rasterizationOptions.Layouts` para especificar o(s) nome(s) de layout que você deseja rasterizar.

## Conclusão

Você aprendeu agora como **convert dxf to png**, **export cad layers**, e **save cad as png** ou JPEG usando Aspose.CAD para .NET. Ajustando `CadRasterizationOptions` e trocando as opções de formato de imagem, você pode adaptar a conversão a praticamente qualquer saída raster que precisar. Explore as outras opções de formato na API Aspose.CAD para ampliar seu fluxo de trabalho CAD‑para‑raster.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}