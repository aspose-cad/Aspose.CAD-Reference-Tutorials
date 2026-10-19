---
date: 2026-10-19
description: Aprenda como converter DWG para PDF em Java com Aspose.CAD. Este guia
  passo a passo mostra como exportar PDF do AutoCAD, salvar CAD como PDF e aplicar
  uma licença.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Exportar imagens do AutoCAD para PDF
og_description: Aprenda como converter DWG para PDF em Java com Aspose.CAD. Este guia
  orienta você na exportação de PDF do AutoCAD, no salvamento de CAD como PDF e no
  licenciamento.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Converter DWG para PDF em Java usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Converter DWG para PDF em Java usando Aspose.CAD
url: /pt/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PDF do AutoCAD – exportar imagens AutoCAD para PDF com Aspose.CAD para Java

## Introdução

Se você precisa **converter DWG para PDF em Java**, está no lugar certo. Este tutorial mostra como exportar imagens AutoCAD para PDF usando Aspose.CAD para Java, uma biblioteca pura‑Java que manipula DWG, DXF, DWF e muitos outros formatos CAD sem dependências nativas. Ao final, você será capaz de **salvar CAD como PDF**, ajustar opções de rasterização como tamanho da página e aplicar corretamente uma **licença Aspose CAD** para uso em produção.

## Respostas rápidas
- **Posso converter DWG para PDF com Java?** Sim – Aspose.CAD para Java suporta nativamente DWG, DXF e dezenas de outros formatos CAD.  
- **Preciso de uma licença?** Uma **licença Aspose CAD** permanente remove todas as restrições de avaliação; uma licença temporária está disponível para testes.  
- **Quais versões do Java são suportadas?** Java 8 e superiores são totalmente suportados.  
- **Posso controlar as dimensões da página PDF?** Absolutamente – defina `pageWidth` e `pageHeight` nas opções de rasterização.  
- **É possível renderização 3‑D?** Sim – habilite `TypeOfEntities.Entities3D` para rasterizar entidades 3‑D.

## O que é exportar PDF do AutoCAD?

Exportar PDF do AutoCAD é o processo de transformar desenhos CAD vetoriais em um documento PDF portátil. Ele preserva camadas, espessuras de linha, cores e, opcionalmente, geometria 3‑D, facilitando o compartilhamento de projetos com clientes ou o arquivamento deles sem a necessidade de software CAD.

## Por que converter DWG para PDF com Aspose.CAD para Java?

Aspose.CAD suporta **mais de 50 formatos de entrada e saída**, processa desenhos com centenas de páginas sem carregar o arquivo inteiro na memória e funciona em qualquer plataforma que suporte Java 8+. A biblioteca oferece controle total sobre DPI, tamanho da página e layout, permitindo que você **personalize o tamanho da página PDF** para corresponder às especificações exatas do projeto, tudo sem instalar DLLs nativas.

## Pré-requisitos

- **Java Development Kit** – JDK 8 ou posterior instalado em sua estação de trabalho.  
- **Aspose.CAD para Java** – faça o download do JAR mais recente a partir do [link de download](https://releases.aspose.com/cad/java/).  
- **Diretório de trabalho** – uma pasta onde seus arquivos DWG de origem e os PDFs gerados serão armazenados.

## Importar namespaces

A classe `Image` representa qualquer desenho CAD rasterizável, enquanto `RasterizationOptions` e `PdfOptions` permitem ajustar finamente a conversão.

A classe `Image` é o objeto de nível superior do Aspose.CAD que mantém um desenho CAD na memória.  
A classe `RasterizationOptions` define como os dados vetoriais são rasterizados antes de serem gravados em PDF.  
A classe `PdfOptions` agrupa as configurações de rasterização com parâmetros de saída específicos para PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Agora vamos percorrer o código passo a passo.

## Como converter DWG para PDF com Aspose.CAD para Java?

Para converter um arquivo DWG para PDF com Aspose.CAD para Java, carregue o desenho usando a classe Image, configure CadRasterizationOptions (como DPI, tamanho da página e tipos de entidade), envolva essas opções em PdfOptions e, em seguida, chame o método save especificando um nome de arquivo .pdf. Essa sequência garante que os dados vetoriais sejam rasterizados corretamente e que o PDF resultante corresponda aos requisitos de layout.

### Etapa 1: definir o caminho do diretório de recursos

Substitua `"Your Document Directory"` pelo caminho absoluto da pasta que você criou nos pré-requisitos.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Dica profissional:** Use `Paths.get(...).toAbsolutePath()` para evitar erros relacionados a caminhos em diferentes sistemas operacionais.

### Etapa 2: carregar a imagem CAD

Carregar o arquivo CAD em um objeto `Image` fornece acesso total ao mecanismo de rasterização do Aspose.CAD.

A classe `Image` carrega o arquivo DWG e o prepara para a conversão.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Por que isso importa:** Uma vez que o desenho está na memória, você pode consultar seus layouts, camadas e metadados antes de rasterizar.

### Etapa 3: definir opções de rasterização

Ajuste `pageWidth` e `pageHeight` para **personalizar o tamanho da página PDF**. Habilitar `setTypeOfEntities(TypeOfEntities.Entities3D)` permite renderização 3‑D completa quando necessário.

O objeto `RasterizationOptions` controla DPI, dimensões da página e tipos de entidade para a saída.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` são medidos em pontos (1 pt = 1/72 pol).  
- Descomente a linha `setTypeOfEntities` para rasterização 3‑D.  
- `setLayouts` seleciona qual layout (Model, Layout1, etc.) renderizar.

### Etapa 4: configurar opções de PDF

Vincule as configurações de rasterização à saída PDF, garantindo que os dados vetoriais sejam transformados corretamente.

A classe `PdfOptions` vincula a configuração de rasterização ao arquivo PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Etapa 5: salvar o PDF

O arquivo resultante, `Export3DImagestoPDF_out_.pdf`, é uma representação **salvar cad como pdf** do seu desenho AutoCAD original.

O método `save` grava a imagem rasterizada em um arquivo PDF no disco.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Problemas comuns & soluções

| Sintoma | Causa provável | Solução |
|---------|----------------|---------|
| Saída PDF em branco | Opções de rasterização não definidas ou layout incompatível | Verifique se `setLayouts` corresponde ao nome do layout no seu arquivo CAD. |
| Imagem de baixa resolução | `pageWidth`/`pageHeight` muito pequenos | Aumente as dimensões ou defina um DPI maior via `rasterizationOptions.setResolution(...)`. |
| Exceção de licença | Nenhuma licença válida aplicada | Aplique uma **licença Aspose CAD** ou use uma licença temporária para testes. |

## Perguntas frequentes

**Q: Posso usar Aspose.CAD para Java com outros formatos de arquivo CAD?**  
A: Sim – a biblioteca suporta DWG, DXF, DWF, DGN e mais de 30 formatos adicionais, oferecendo flexibilidade em diferentes projetos.

**Q: Como obtenho uma licença temporária para Aspose.CAD para Java?**  
A: Visite a [página de licença temporária](https://purchase.aspose.com/temporary-license/) para solicitar uma licença de tempo limitado para avaliação.

**Q: Existem opções de layout para rasterização?**  
A: Absolutamente. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc., para escolher qual visualização será renderizada no PDF.

**Q: Posso alterar o tamanho do arquivo PDF de saída?**  
A: Sim – modifique `pageWidth` e `pageHeight` nas opções de rasterização para corresponder a quaisquer dimensões de página necessárias.

**Q: Onde posso obter ajuda se encontrar problemas?**  
A: A comunidade dedicada está disponível no [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) onde você pode fazer perguntas e compartilhar soluções.

---

**Última atualização:** 2026-10-19  
**Testado com:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Tutoriais Relacionados

- [Exportar DWG para PDF em Java – Definir tamanho da página PDF com Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportar DWG para PDF: Layout específico usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG para PDF e habilitar rastreamento com Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}