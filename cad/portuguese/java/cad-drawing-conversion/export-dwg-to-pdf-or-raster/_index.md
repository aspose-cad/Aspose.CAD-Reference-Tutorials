---
date: 2026-10-14
description: Saiba como a biblioteca Java CAD Aspose.CAD for Java pode exportar DWG
  para PDF ou imagens raster de forma rápida e precisa.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Exportar DWG para PDF e imagens raster
og_description: Exporte DWG para PDF rapidamente com Aspose.CAD for Java. Aprenda
  conversão de PDF de alta qualidade, opções raster e licenciamento neste guia passo
  a passo.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Exportar DWG para PDF e imagens raster usando a biblioteca Java CAD Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Exportar DWG para PDF e imagens raster usando a biblioteca Java CAD Aspose.CAD
url: /pt/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG PDF e imagens raster usando a biblioteca Java CAD Aspose.CAD

## Introdução

Exportar DWG para PDF é uma necessidade frequente para engenheiros, arquitetos e qualquer pessoa que precise compartilhar desenhos CAD sem expor o formato de arquivo nativo. Com **Aspose.CAD for Java**, você pode **export dwg pdf** — ou imagens raster — em apenas algumas linhas de código Java, mantendo a fidelidade vetorial e a precisão do layout. Este tutorial orienta você a carregar um arquivo DWG, configurar a rasterização e salvar o resultado como um PDF ou imagem de alta qualidade. Você também verá por que o Aspose.CAD é a biblioteca Java CAD preferida para conversões confiáveis e multiplataforma.

Para um guia focado apenas na conversão para PDF, veja o [Tutorial de Exportação DWG para PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Respostas rápidas
- **O que este tutorial cobre?** Exportação de arquivos DWG para PDF ou imagens raster usando Aspose.CAD for Java.  
- **Preciso de uma licença?** Uma licença temporária gratuita está disponível para avaliação; uma licença completa é necessária para produção.  
- **Qual versão do Java é suportada?** Qualquer runtime Java 8+ funciona com a API mais recente do Aspose.CAD Java.  
- **Posso converter DWG para outros formatos de imagem?** Sim – as mesmas opções de rasterização permitem gerar PNG, JPEG, BMP, etc.  
- **Quanto tempo leva a conversão?** Normalmente menos de um segundo para desenhos padrão; arquivos maiores podem levar alguns segundos.

## Por que a biblioteca Java CAD é a melhor escolha para conversão de DWG?

Aspose.CAD for Java é a melhor escolha porque oferece uma implementação pura‑Java que não requer DLLs nativas, detecta automaticamente unidades métricas ou imperiais, entrega saída rasterizada de até 1200 DPI e gera PDFs que preservam vetores sem dependências externas. A biblioteca também oferece um modelo de licenciamento flexível que permite iniciar com uma licença temporária e escalar para uso empresarial.

## O que é “export dwg to pdf”?

`Export dwg pdf` é o processo de converter um arquivo de desenho DWG nativo em um documento PDF enquanto preserva dados vetoriais, camadas e escala. Essa conversão produz um arquivo independente de dispositivo que pode ser visualizado em qualquer plataforma sem a necessidade do AutoCAD. Como o PDF mantém informações vetoriais, o texto permanece pesquisável e os gráficos ficam nítidos em qualquer nível de zoom, tornando‑o ideal para documentação, revisão de clientes e armazenamento arquivístico.

## Por que usar Aspose.CAD Java para esta conversão?

Você deve usar Aspose.CAD Java porque a biblioteca trata da conversão de unidades, rasterização e incorporação de PDF internamente, eliminando a necessidade de ferramentas de terceiros ou pipelines complexos de linha de comando. Sua API foi projetada para desenvolvedores: um único objeto `Image` representa o desenho, e alguns objetos de configuração permitem ajustar DPI, tamanho da página e compressão. O resultado é uma saída consistente e repetível em ambientes Windows, Linux e macOS.

## Pré‑requisitos

Antes de mergulhar no código, certifique‑se de que você tem:

- Conhecimento básico de programação Java.  
- Biblioteca Aspose.CAD for Java instalada. Se ainda não a baixou, obtenha **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Um arquivo DWG para teste – o exemplo **Bottom_plate.dwg** é usado neste guia.  

## Importar namespaces

No seu projeto Java, importe as classes necessárias para iniciar a conversão:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guia passo a passo

### Etapa 1: Carregar o arquivo DWG

Primeiro, carregue seu desenho DWG usando a classe `Image`. Isso cria uma representação em memória que o Aspose.CAD pode manipular.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Etapa 2: Determinar o tipo de unidade

Entender se o desenho usa unidades métricas ou imperiais é essencial para a escala correta. O método auxiliar `IsMetric` (implementação omitida para brevidade) retorna um sinalizador booleano.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Etapa 3: Definir opções de rasterização

A classe `CadRasterizationOptions` define parâmetros de rasterização como DPI, tamanho da página e conversão de unidades. Com base no sistema de unidades, configure o tamanho da página, a escala e o tipo de unidade de destino. Essas opções determinam como o DWG será rasterizado antes de ser incorporado a um PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Etapa 4: Configurar opções PDF (pdf options cad)

A classe `PdfOptions` especifica configurações específicas de PDF, incluindo compressão e metadados. Crie uma instância de `PdfOptions` e anexe as configurações de rasterização. Isso indica ao Aspose.CAD como incorporar o conteúdo rasterizado ao PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Etapa 5: Salvar como PDF

O método `save` grava a imagem no caminho de arquivo fornecido usando as opções especificadas. Finalmente, exporte o desenho para um arquivo PDF. O método `save` recebe o caminho de saída e o `PdfOptions` configurado.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Quando o código terminar, você encontrará **Saved.pdf** na sua pasta `DWGDrawings`, pronto para distribuição ou arquivamento.

## Como converter imagens raster DWG com a biblioteca Java CAD?

Você pode converter DWG para formatos raster trocando `PdfOptions` por uma classe de opções específica de raster, como `PngOptions` ou `JpegOptions`. Reutilize a mesma instância de `CadRasterizationOptions`, ajuste o formato de saída e chame o método `save` com o novo objeto de opções. Essa abordagem permite gerar arquivos PNG, JPEG, BMP ou TIFF com uma única alteração de linha, mantendo o fluxo de trabalho consistente.

## Como gerar PDF DWG usando opções PDF CAD?

O exemplo acima já **gera pdf dwg**. Para ajustar o tamanho do PDF, habilite a compressão chamando `pdfOptions.setCompress(true)`. Você também pode incorporar metadados personalizados, definir a versão do PDF ou adicionar proteção por senha através de propriedades adicionais de `PdfOptions`. Essas personalizações dão controle total sobre o PDF final sem sair do código Java.

## Problemas comuns e dicas

- **Tamanho de página incorreto** – Verifique a lógica de conversão de unidades; coeficientes incompatíveis podem gerar páginas excessivamente grandes.  
- **Fontes ou espessuras de linha ausentes** – Certifique‑se de que o DWG referencia quaisquer recursos externos antes da conversão.  
- **Desempenho em desenhos grandes** – Aumente a configuração `DPI` em `CadRasterizationOptions` somente quando for necessária qualidade superior; DPI menor acelera o processamento.  
- **Questões de licença** – Para avaliação você pode usar uma **licença temporária Aspose**; uma licença completa é necessária para implantações em produção.

## Perguntas frequentes

**Q: Posso usar Aspose.CAD for Java com outros frameworks Java?**  
A: Sim, Aspose.CAD for Java integra‑se perfeitamente com frameworks Java populares como Spring, Jakarta EE e Android.

**Q: Uma licença temporária está disponível para Aspose.CAD for Java?**  
A: Sim, você pode obter uma **[obter uma licença temporária](https://purchase.aspose.com/temporary-license/)**.

**Q: Onde posso encontrar suporte para Aspose.CAD for Java?**  
A: Visite o **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** para assistência da comunidade e dos engenheiros da Aspose.

**Q: Como posso comprar uma licença para Aspose.CAD for Java?**  
A: Você pode comprar uma licença **[adquirir uma licença](https://purchase.aspose.com/buy)**.

**Q: Quais unidades o Aspose.CAD for Java suporta?**  
A: Aspose.CAD for Java suporta unidades métricas e imperiais, detectando automaticamente o sistema de unidades do desenho.

**Q: Posso converter DWG para outros formatos de imagem (por exemplo, PNG, JPEG) usando a mesma API?**  
A: Absolutamente. Substitua `PdfOptions` pelas opções de imagem raster apropriadas (por exemplo, `PngOptions`) e reutilize o mesmo `CadRasterizationOptions`.

## Conclusão

Este tutorial demonstrou como **export dwg pdf** e imagens raster usando a **biblioteca java cad** Aspose.CAD for Java. Ao seguir o guia passo a passo, você pode integrar conversões CAD confiáveis em qualquer aplicação Java, seja para PDFs de documentação ou imagens raster para exibição na web. A natureza pura‑Java da biblioteca, a saída de alta qualidade e o licenciamento flexível a tornam uma escolha sólida tanto para utilitários pequenos quanto para pipelines empresariais de grande escala.

---

**Última atualização:** 2026-10-14  
**Testado com:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Tutoriais relacionados

- [Exportar DWG para PDF: Layout específico usando Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG para PDF em Java – Definir tamanho da página PDF com Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportar DWG para PDF com linhas ocultas – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}