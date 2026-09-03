---
date: 2026-08-29
description: Aprenda como definir o tamanho da página PDF e converter CAD para PDF
  usando Aspose.CAD para Java, com dimensionamento automático de layout e exportação
  TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Definir tamanho da página PDF – converter CAD para PDF
og_description: Aprenda como definir o tamanho da página PDF ao converter desenhos
  CAD para PDF em Java usando Aspose.CAD. Este guia aborda dimensões da tela, dimensionamento
  automático de layout e exportação para TIFF de alta resolução.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Definir tamanho da página PDF – converter CAD para PDF com Aspose em Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Definir tamanho da página PDF – converter CAD para PDF (Java)
url: /pt/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir tamanho da página PDF – converter CAD para PDF (Java)

## Introdução

Se você precisa **definir o tamanho da página PDF** ao converter desenhos CAD para PDF, você está no lugar certo. Neste tutorial, mostraremos como usar Aspose.CAD para Java para definir dimensões exatas do canvas, habilitar o dimensionamento automático de layout e, em seguida, exportar o resultado tanto para PDF quanto para TIFF. Seja preparando esquemas de engenharia para impressão ou gerando miniaturas para uma galeria web, controlar o tamanho da página e a resolução de saída é essencial.

## Respostas rápidas
- **O que significa “converter CAD para PDF”?** Transformar um desenho CAD (por exemplo, DXF, DWG) em um documento PDF que pode ser visualizado em qualquer plataforma.  
- **Posso também exportar para TIFF?** Sim—use `TiffOptions` para criar imagens raster de alta resolução.  
- **Qual opção controla o tamanho do canvas em Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **O que é dimensionamento automático de layout?** Uma flag (`setAutomaticLayoutsScaling(true)`) que preserva as proporções originais do layout quando o tamanho do canvas muda.  
- **Preciso de uma licença para Aspose.CAD?** Uma licença temporária ou permanente é necessária para uso em produção.

## Como definir o tamanho da página PDF ao converter CAD para PDF em Java

Carregue seu arquivo CAD, configure `CadRasterizationOptions` com a largura e altura desejadas, habilite o dimensionamento automático de layout e, em seguida, salve o resultado como PDF. Essa abordagem em duas etapas permite que você controle as dimensões exatas da página de saída sem sacrificar a qualidade vetorial.

## O que é converter CAD para PDF?

Converter CAD para PDF significa pegar desenhos de engenharia baseados em vetores e renderizá‑los como páginas PDF, preservando linhas, camadas e geometria, ao mesmo tempo que torna o arquivo universalmente acessível. O processo rasteriza o desenho de acordo com as opções especificadas, produzindo um PDF que pode ser aberto em qualquer dispositivo sem necessidade de software CAD, e mantém a fidelidade visual do design original.

## Por que definir o tamanho do canvas em Java?

Definir o tamanho do canvas em Java permite que você estabeleça a resolução de saída e as dimensões da página, garantindo que o PDF ou TIFF resultante atenda aos requisitos de impressão ou exibição. Também oferece controle sobre o comportamento de dimensionamento, o que é essencial para desenhos de grande formato.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos configurados:

- Aspose.CAD para Java: Certifique‑se de que a biblioteca Aspose.CAD está instalada em seu ambiente Java. Você pode baixar a biblioteca Aspose.CAD para Java [aqui](https://releases.aspose.com/cad/java/).
- Diretório de documentos: Configure um diretório de documentos para armazenar seus arquivos CAD. Este diretório será referenciado nas etapas do tutorial.

Agora, vamos começar com o guia passo a passo.

## Importar namespaces

Nesta etapa, importaremos os namespaces necessários para iniciar seu projeto Aspose.CAD.

`Image` é a classe principal usada para carregar arquivos CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Etapa 1: importar classes Aspose.CAD

A classe `Image` fornece métodos para carregar e salvar desenhos CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Neste trecho, configuramos o caminho para o diretório de recursos e carregamos um arquivo DXF usando a classe `Image` da Aspose.CAD.

## Etapa 2: definir propriedades de CadRasterizationOptions (definir tamanho do canvas em Java)

`CadRasterizationOptions` especifica as configurações de rasterização, como tamanho da página e dimensionamento, para a conversão de CAD para raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Aqui, criamos uma instância de `CadRasterizationOptions` e configuramos propriedades como largura da página, altura da página e **dimensionamento automático de layout**. Este é o núcleo da **configuração do modo canvas** para sua conversão.

## Etapa 3: criar PdfOptions e definir vectorRasterizationOptions

`PdfOptions` define as configurações de saída PDF para a conversão.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Agora, criamos uma instância de `PdfOptions` e definimos sua propriedade `VectorRasterizationOptions` para a `CadRasterizationOptions` configurada anteriormente.

## Etapa 4: exportar para PDF (converter CAD para PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, salvamos a imagem CAD em um arquivo PDF usando as opções especificadas, concluindo o processo de **converter CAD para PDF**.

## Etapa 5: criar TiffOptions e definir vectorRasterizationOptions (exportar CAD para TIFF)

`TiffOptions` configura os parâmetros de saída TIFF, como compressão e resolução.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nesta etapa, configuramos uma instância de `TiffOptions` e definimos sua propriedade `VectorRasterizationOptions`.

## Etapa 6: exportar para TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finalmente, salvamos a imagem CAD em um arquivo TIFF usando as opções especificadas, demonstrando como **exportar CAD para TIFF** após configurar o tamanho do canvas.

## Problemas comuns e soluções

| Problema | Causa | Correção |
|----------|-------|----------|
| PDF de saída está em branco | `setNoScaling(true)` desabilita a renderização para alguns desenhos | Remova `setNoScaling(true)` ou defina como `false`. |
| Resolução do TIFF parece baixa | Largura/altura da página muito pequena | Aumente os valores de `setPageWidth` / `setPageHeight`. |
| Layout parece distorcido | Dimensionamento automático de layout desativado | Certifique‑se de que `setAutomaticLayoutsScaling(true)` está habilitado. |

## Por que ajustar o tamanho do canvas e DPI?

Alterar o tamanho do canvas influencia diretamente a resolução de rasterização da saída. Se você precisar **aumentar a resolução do TIFF**, basta elevar os valores de `setPageWidth` / `setPageHeight` ou chamar `rasterizationOptions.setResolution(300)` antes de criar o `TiffOptions`. Isso fornece imagens raster de alta qualidade adequadas para impressão ou inspeção detalhada.

## Perguntas frequentes

**Q1: posso usar Aspose.CAD para Java com outros frameworks Java?**  
A: Sim, Aspose.CAD foi projetado para integrar‑se perfeitamente com vários frameworks Java.

**Q2: há uma licença temporária disponível para Aspose.CAD?**  
A: Sim, você pode obter uma licença temporária na página [aqui](https://purchase.aspose.com/temporary-license/).

**Q3: onde posso obter suporte da comunidade para Aspose.CAD?**  
A: Visite o fórum Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**Q4: posso experimentar Aspose.CAD gratuitamente?**  
A: Absolutamente! Obtenha a página de download de avaliação gratuita [aqui](https://releases.aspose.com/).

**Q5: como faço para comprar Aspose.CAD para Java?**  
A: Compre Aspose.CAD para Java [aqui](https://purchase.aspose.com/buy).

**Q: o tamanho do canvas afeta a qualidade vetorial no PDF?**  
A: Não. O tamanho do canvas controla as dimensões da página; os dados vetoriais permanecem independentes de resolução, garantindo renderização nítida em qualquer nível de zoom.

**Q: posso definir um DPI diferente para a saída TIFF?**  
A: Sim. Ajuste `rasterizationOptions.setResolution(dpiValue)` antes de criar `TiffOptions`.

**Q: como posso alterar as dimensões do PDF para um PDF existente sem re‑renderizar o CAD?**  
A: Use Aspose.PDF para carregar o PDF gerado e chamar `pdf.getPages().setPageSize(PageSize.A4)` ou um tamanho personalizado.

**Q: qual é a melhor maneira de converter dxf para pdf preservando camadas?**  
A: Mantenha `setAutomaticLayoutsScaling(true)` e evite `setNoScaling(true)`; isso mantém a visibilidade das camadas e a fidelidade do layout.

## Conclusão

Parabéns! Você converteu CAD para PDF e exportou CAD para TIFF com sucesso, enquanto **definiu o tamanho do canvas em Java**, habilitando **dimensionamento automático de layout**, e aprendeu como **configurar o modo canvas** para saídas de alta qualidade. Este tutorial fornece uma base sólida para seus projetos de conversão CAD. Explore mais recursos e possibilidades na [documentação Aspose.CAD](https://reference.aspose.com/cad/java/).

**Última atualização:** 2026-08-29  
**Testado com:** Aspose.CAD para Java 24.12  
**Autor:** Aspose

## Tutoriais Relacionados

- [Definir Tamanho do Canvas – Recursos Avançados de CAD com Aspose.CAD para Java](/cad/java/advanced-cad-features/)
- [Exportar DWG para PDF em Java – Definir Tamanho da Página PDF com Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Definir Tamanho de Página Personalizado – PDF de CAD com Dimensionamento Automático de Layout](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}