---
date: 2026-10-04
description: Aprenda a converter rapidamente DWG para PNG e exportar CAD como PNG
  ou outros formatos raster usando Aspose.CAD for Java. Obtenha resultados de alta
  qualidade rapidamente.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Converter Layout CAD para Formato de Imagem Raster
og_description: Converta DWG para PNG rapidamente com Aspose.CAD for Java. Aprenda
  passo a passo como exportar CAD como PNG, JPEG, TIFF e muito mais.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Converter DWG para PNG e outros formatos raster usando Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Converter DWG para PNG e outros formatos raster usando Aspose.CAD for Java
url: /pt/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DWG para PNG e outros formatos raster usando Aspose.CAD para Java

## Introdução

`Aspose.CAD for Java` é uma biblioteca que permite a conversão programática de arquivos CAD para imagens raster como PNG, JPEG e TIFF. Converter DWG para PNG (ou outros formatos de imagem raster) é uma necessidade comum quando você precisa compartilhar desenhos CAD com colegas que não têm um visualizador CAD, incorporar designs na documentação ou gerar miniaturas para galerias da web. Neste guia você aprenderá como converter dwg para png de forma rápida e confiável, seja trabalhando com um arquivo de desenho completo ou apenas com um layout específico. Você também pode precisar **converter CAD para raster** para pré‑visualizações web, ferramentas de relatório ou aplicativos móveis.

## Respostas rápidas
- **Qual biblioteca manipula DWG para PNG?** Aspose.CAD for Java provides the conversion engine.  
- **Quais formatos raster posso exportar?** PNG, JPEG, TIFF, PDF, BMP, and more than 30 additional formats.  
- **Preciso de licença para testes?** A free trial works for development; a commercial license is required for production.  
- **Posso escolher um layout específico?** Yes – use `setLayouts` to target “Model”, “Layout1”, etc.  
- **É possível saída em alta resolução?** Absolutely – adjust `setPageWidth` and `setPageHeight` (or `setResolution`) to control DPI.

## O que significa “convert dwg to png”?

Converter dwg para png significa transformar um desenho vetorial DWG em uma imagem PNG baseada em pixels que pode ser exibida por qualquer visualizador de imagens padrão. Esse processo rasteriza entidades vetoriais, preservando espessura de linha, cores e camadas ao traduzi‑las para um bitmap de resolução fixa. O resultado é ideal para incorporação em PDFs, documentos Word ou páginas da web onde o suporte a vetores é limitado.

## Por que exportar CAD como PNG (ou outros formatos raster)?

Exportar CAD como PNG oferece compatibilidade universal, carregamento rápido e fácil incorporação em todas as principais plataformas. Imagens raster carregam instantaneamente comparado à abertura de um arquivo DWG pesado, e a compressão sem perdas do PNG garante fidelidade visual. Ao controlar resolução, cor de fundo e layout, você garante que todos os interessados vejam a mesma aparência, seja o arquivo visualizado em um desktop, dispositivo móvel ou dentro de um navegador.

## Casos de uso comuns

| Cenário | Por que a saída raster ajuda |
|----------|------------------------|
| **Documentação de projeto** | Incorporar PNGs em PDFs ou documentos Word evita a necessidade de software CAD para revisores. |
| **Portais web** | Miniaturas geradas a partir de arquivos DWG carregam instantaneamente e melhoram a experiência do usuário. |
| **Aplicativos móveis** | Imagens raster exibem corretamente em dispositivos que não possuem visualizadores CAD. |
| **Relatórios automatizados** | Converter em lote vários layouts para PNG/JPEG para inclusão em gráficos ou painéis. |

## Pré-requisitos

1. **Ambiente de desenvolvimento Java** – JDK 8 ou mais recente instalado e configurado.  
2. **Aspose.CAD for Java** – Baixe o JAR mais recente da [documentação Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Importar namespaces

`com.aspose.cad.Image` é a classe central que representa qualquer arquivo CAD na memória. `com.aspose.cad.imageoptions.*` fornece objetos de opções para cada formato raster. Importe as classes que você precisará para carregar um desenho, configurar a rasterização e salvar a saída.

> **Dica profissional:** Se você pretende **exportar CAD como PNG** em vez de TIFF, substitua `TiffOptions` por `PngOptions` (encontrado em `com.aspose.cad.imageoptions.PngOptions`).

## Guia passo a passo

### Etapa 1: configurar o diretório de recursos

Substitua `"Your Document Directory"` pelo caminho absoluto onde seus arquivos CAD estão armazenados. Este diretório será usado tanto para arquivos de entrada quanto de saída.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Etapa 2: carregar o arquivo CAD

`Image.load` analisa o arquivo de origem e cria uma representação em memória que você pode rasterizar. Você pode carregar qualquer formato suportado (DWG, DXF, DGN, etc.) – esta é a parte de **como converter cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Etapa 3: configurar opções de rasterização

`CadRasterizationOptions` define como os dados vetoriais são transformados em pixels. `setPageWidth` e `setPageHeight` controlam a resolução de saída (valores maiores = DPI mais alto). `setLayouts` permite **converter CAD para raster** para layouts específicos; omita‑o para rasterizar o desenho completo.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Etapa 4: definir opções de imagem

`TiffOptions` (ou `PngOptions` para PNG) informa ao Aspose qual formato raster gerar e permite ajustar finamente compressão, profundidade de cor e outras configurações específicas do formato. Escolha a classe de opções que corresponde à saída desejada.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Etapa 5: salvar a imagem resultante

Chame `save` na instância `Image`, passando o nome do arquivo de saída e o objeto de opções. Altere a extensão do arquivo para `.png` (e use `PngOptions`) para **salvar CAD como PNG**. O mesmo padrão funciona para JPEG, BMP ou PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Armadilha comum:** Esquecer de corresponder a extensão do arquivo com a classe de opções causará um `UnsupportedFormatException`. Sempre mantenha‑os sincronizados.

## Problemas comuns e soluções

| Problema | Solução |
|----------|----------|
| **Imagem de saída em branco** | Verifique se os nomes de layout em `setLayouts` correspondem exatamente aos do arquivo CAD de origem. |
| **PNG de baixa resolução** | Aumente `setPageWidth` / `setPageHeight` ou defina `setResolution` nas opções de rasterização. |
| **Versão DWG não suportada** | Certifique-se de estar usando a versão mais recente do Aspose.CAD; versões mais antigas podem não suportar versões mais recentes do DWG. |
| **Erros de memória em arquivos grandes** | Processar páginas uma de cada vez ou aumentar o heap da JVM (`-Xmx2g`). |

## Perguntas frequentes

**Q: O Aspose.CAD é compatível com diferentes formatos de arquivo CAD?**  
A: Sim, ele suporta mais de 30 formatos CAD e raster, incluindo DWG, DXF, DGN e SVG.

**Q: Posso personalizar a resolução da imagem raster de saída?**  
A: Absolutamente. Ajuste `setPageWidth`, `setPageHeight` ou `setResolution` em `CadRasterizationOptions` para alcançar o DPI desejado.

**Q: Como posso converter vários layouts CAD em uma única execução?**  
A: Forneça um array com todos os nomes de layout para `setLayouts`, por exemplo, `new String[]{"Model","Layout1","Layout2"}`.

**Q: Existem formatos de saída além do TIFF suportados?**  
A: Sim—PNG, JPEG, BMP, PDF e outros estão disponíveis através de suas respectivas classes `*Options`.

**Q: Onde posso obter ajuda ou compartilhar minha experiência com Aspose.CAD?**  
A: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e assistência oficial.

## Conclusão

Seguindo estas etapas, você pode **converter DWG para PNG**, **exportar CAD como PNG**, **salvar CAD como JPEG**, ou gerar qualquer outro formato raster que precisar. Aspose.CAD para Java cuida do trabalho pesado, permitindo que você se concentre em integrar imagens de alta qualidade em suas aplicações, documentação ou portais web. O suporte da biblioteca a mais de 30 formatos e sua capacidade de renderizar desenhos com centenas de páginas sem carregar o arquivo inteiro na memória a tornam uma escolha robusta para rasterização CAD de nível empresarial.

---

**Última atualização:** 2026-10-04  
**Testado com:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Tutoriais relacionados

- [Exportar rapidamente DWG para PDF ou Raster usando a biblioteca Java CAD Aspose.CAD](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Converter DWG para BMP com Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Exportar DWG para PDF: Layout específico usando Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}