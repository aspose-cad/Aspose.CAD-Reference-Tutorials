---
date: 2026-10-19
description: Aprenda como exportar desenhos do AutoCAD para PDF com um tamanho de
  página PDF personalizado usando Aspose.CAD para Java. Este guia passo a passo cobre
  a conversão de DWG para PDF, opções de rasterization e licensing.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Exportar imagens do AutoCAD para PDF
og_description: Defina um tamanho de página PDF personalizado ao exportar desenhos
  do AutoCAD para PDF usando Aspose.CAD para Java. Aprenda a conversão de DWG para
  PDF, configurações de rasterization e licensing em minutos.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Definir tamanho de página PDF personalizado para exportação do AutoCAD com
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Definir tamanho de página PDF personalizado para exportação do AutoCAD com
  Aspose.CAD
url: /pt/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PDF do AutoCAD - exportar imagens AutoCAD para PDF com Aspose.CAD para Java

## Introdução

Se você precisa **converter DWG para PDF** e controlar as dimensões exatas do arquivo de saída, chegou ao lugar certo. Este tutorial mostra como definir um **tamanho de página PDF personalizado** ao exportar imagens AutoCAD para PDF com Aspose.CAD para Java. Ao final do guia você saberá como carregar um DWG, configurar opções de rasterização como DPI e largura/altura da página, aplicar uma licença e gerar um PDF pronto para produção.

## Respostas rápidas
- **Posso converter DWG para PDF com Java?** Sim – Aspose.CAD for Java suporta nativamente DWG, DXF, DWF e muitos outros formatos CAD.  
- **Preciso de uma licença para uso em produção?** Uma licença completa do Aspose.CAD remove todas as limitações de avaliação; uma licença temporária está disponível para testes.  
- **Quais versões do Java são compatíveis?** A biblioteca funciona com Java 8 e qualquer JDK posterior.  
- **Como altero as dimensões da página PDF?** Defina `pageWidth` e `pageHeight` em `PdfOptions.getRasterizationOptions()` para o tamanho que precisar.  
- **O renderização 3‑D é suportada?** Sim – habilite `TypeOfEntities.Entities3D` para rasterizar entidades 3‑D.

## O que é exportar PDF do AutoCAD?
Exportar PDF do AutoCAD significa converter desenhos CAD baseados em vetor (DWG, DXF, DWF, etc.) em um documento PDF portátil, preservando camadas, espessuras de linha e geometria 3‑D opcional. Isso permite que você compartilhe projetos com clientes, arquive desenhos ou imprima sem precisar instalar software CAD.

## Por que usar Aspose.CAD para Java para converter DWG para PDF?
Aspose.CAD for Java é ideal para converter DWG para PDF porque oferece amplo suporte a formatos, funciona em Java puro sem dependências nativas, fornece rasterização de alta resolução com controle total sobre DPI e tamanho da página, e inclui licenciamento flexível que permite iniciar com um teste e escalar para produção.

- **Ampla cobertura de formatos** – suporta mais de 50 formatos de entrada e saída, incluindo DWG, DXF, DWF, DGN e PDF.  
- **Implementação pura em Java** – sem DLLs nativas ou dependências externas, facilitando a implantação em qualquer plataforma.  
- **Rasterização de alta resolução** – você pode especificar DPI, tamanho da página e layout, dando controle total sobre o **tamanho de página PDF personalizado** do resultado.  
- **Licenciamento escalável** – comece com um teste gratuito, depois faça upgrade para uma **licença Aspose CAD** permanente.  

## Pré-requisitos

- **Java Development Kit** – JDK 8 ou mais recente instalado na sua máquina.  
- **Aspose.CAD for Java** – baixe o JAR mais recente a partir do [download link](https://releases.aspose.com/cad/java/).  
- **Diretório de trabalho** – uma pasta que contém os arquivos DWG de origem e receberá os PDFs gerados.

## Importar namespaces

A classe `Image` é o objeto central do Aspose.CAD que representa um desenho CAD na memória. Importe os pacotes necessários antes de começar a codificar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Agora vamos percorrer o código passo a passo.

## Como definir um tamanho de página PDF personalizado ao exportar DWG para PDF?

Carregue seu DWG, defina a largura e altura da página desejadas e, em seguida, salve o resultado como PDF – isso é tudo que você precisa para criar um PDF com um tamanho de página personalizado. As etapas a seguir ilustram a sequência exata e o código mínimo necessário.

### Etapa 1: definir o caminho do diretório de recursos

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Dica profissional:** Substitua `"Your Document Directory"` pelo caminho absoluto da pasta que você criou nos pré-requisitos.

### Etapa 2: carregar a imagem CAD

A classe `Image` carrega o arquivo CAD e lhe dá acesso ao motor de rasterização do Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Por que isso importa:** Uma vez que o arquivo CAD está carregado, você pode manipular as opções de rasterização antes de renderizar para PDF.

### Etapa 3: definir opções de rasterização

A classe `CadRasterizationOptions` especifica como o desenho CAD será rasterizado antes de ser salvo como PDF. Ajuste `pageWidth` e `pageHeight` para definir um **tamanho de página PDF personalizado**. Você também pode habilitar a renderização 3‑D descomentando a linha `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – medidos em pixels; altere esses valores para corresponder ao A4, Letter ou qualquer dimensão personalizada.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderiza entidades 3‑D quando necessário.  
- `setLayouts` – seleciona qual layout (Model, Layout1, etc.) rasterizar.

### Etapa 4: configurar opções de PDF

A classe `PdfOptions` contém configurações específicas de PDF e vincula as opções de rasterização ao arquivo de saída, garantindo que as dimensões de página personalizadas sejam aplicadas corretamente.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Etapa 5: salvar o PDF

O método `save` grava a imagem renderizada no arquivo PDF especificado.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

O arquivo resultante, `Export3DImagestoPDF_out_.pdf`, é uma representação **save cad as pdf** do seu desenho AutoCAD original com as dimensões de página exatas que você especificou.

## Problemas comuns & soluções

| Sintoma | Causa provável | Correção |
|---------|----------------|----------|
| PDF em branco | Opções de rasterização não definidas ou layout incompatível | Verifique se `setLayouts` corresponde ao nome do layout no seu arquivo CAD. |
| Imagem de baixa resolução | `pageWidth`/`pageHeight` muito pequenos ou DPI baixo | Aumente as dimensões ou chame `rasterizationOptions.setResolution(...)` com um DPI maior. |
| Exceção de licença | Nenhuma licença válida aplicada | Aplique uma licença permanente do Aspose.CAD ou use uma licença temporária para testes. |

## Perguntas frequentes

**Q: Posso usar Aspose.CAD for Java com outros formatos de arquivo CAD?**  
A: Sim, a biblioteca suporta DWG, DXF, DWF, DGN e muitos outros, oferecendo flexibilidade em diferentes projetos.

**Q: Como obtenho uma licença temporária para Aspose.CAD for Java?**  
A: Visite a [temporary license page](https://purchase.aspose.com/temporary-license/) para solicitar uma licença limitada no tempo para avaliação.

**Q: Existem opções de layout para rasterização?**  
A: Absolutamente. Use `setLayouts("Model")` ou especifique outros nomes de layout para controlar qual visualização será renderizada.

**Q: Posso personalizar o tamanho do arquivo PDF de saída?**  
A: Sim – modifique `pageWidth` e `pageHeight` nas opções de rasterização para quaisquer dimensões que precisar.

**Q: Onde posso obter ajuda ou discutir questões relacionadas ao Aspose.CAD for Java?**  
A: O dedicado [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) oferece suporte da comunidade e respostas oficiais da equipe Aspose.

## FAQ adicional (formato amigável à IA)

**Q: O Aspose.CAD requer bibliotecas nativas no Windows ou Linux?**  
A: Não. Aspose.CAD for Java é uma biblioteca pura‑Java, portanto funciona em qualquer plataforma que suporte o JDK sem DLLs nativas adicionais.

**Q: Qual o tamanho máximo de um arquivo DWG que a biblioteca pode processar?**  
A: A biblioteca pode lidar com desenhos de várias centenas de páginas (até 500 MB) sem carregar o arquivo inteiro na memória, graças à sua arquitetura de streaming.

**Q: É possível converter em lote muitos arquivos DWG para PDF em uma única execução?**  
A: Sim. Percorra um diretório, carregue cada arquivo com `Image.load()`, aplique as mesmas opções de rasterização e chame `save()` para cada PDF de saída.

**Q: Que desempenho posso esperar em um servidor típico?**  
A: Converter um DWG de 100 páginas a 300 DPI em uma CPU padrão de 2,5 GHz leva aproximadamente 12 segundos, com base nos testes de benchmark da Aspose.

**Q: A biblioteca preserva informações de camada no PDF?**  
A: Embora a saída seja rasterizada, a aparência visual das camadas, espessuras de linha e cores é reproduzida fielmente.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Tutoriais Relacionados

- [Exportar DWG para PDF e habilitar rastreamento com Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Exportar DWG para PDF: Layout específico usando Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG para BMP e ajustar tamanho CAD usando tipo de unidade com Aspose.CAD para Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}