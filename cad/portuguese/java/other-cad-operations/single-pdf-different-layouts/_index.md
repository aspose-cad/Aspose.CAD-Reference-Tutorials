---
date: 2026-06-29
description: Aprenda como criar PDF a partir de DWG e personalizar o layout do PDF
  usando Aspose.CAD para Java. Integração fácil para desenvolvedores Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: PDF único com diferentes layouts
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Criar PDF a partir de DWG com Aspose.CAD para Java
url: /pt/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar PDF a partir de DWG com Aspose.CAD para Java

## Introdução

Neste tutorial você **criará PDF a partir de DWG** e aplicará vários layouts de tamanho de página usando Aspose.CAD para Java. Seja para gerar plantas de construção, esquemas de engenharia ou PDFs prontos para marketing, as etapas abaixo mostram como converter desenhos CAD para PDF, personalizar as dimensões de cada layout e produzir um único documento de várias páginas — tudo sem sair do seu ambiente Java.

## Respostas Rápidas
- **O que o tutorial cobre?** Conversão de um desenho DWG para um único PDF com múltiplos tamanhos de página.  
- **Qual biblioteca é necessária?** Aspose.CAD para Java (versão mais recente).  
- **Preciso de licença?** Uma versão de avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Posso exportar outros formatos?** Sim — a API também suporta exportação para PNG, JPEG e SVG.  
- **O Java 8 é suficiente?** A biblioteca funciona com Java 8 e runtimes mais recentes.

## O que é “criar pdf a partir de dwg”?

**Criar PDF a partir de DWG** significa converter um arquivo nativo AutoCAD DWG em um documento PDF, preservando a fidelidade vetorial, camadas e espessura de linhas, e permitindo a personalização do layout. Aspose.CAD realiza essa conversão totalmente na memória, portanto nenhum software CAD externo é necessário, e o PDF resultante pode ser editado ou impresso diretamente.

## Por que personalizar o layout de PDF a partir de DWG?

Aspose.CAD suporta **mais de 30 formatos CAD** e pode gerar PDFs de até **500 MB** sem carregar todo o arquivo na memória. Ao definir tamanhos de página individuais para cada layout, você pode produzir folhas imprimíveis que correspondem a dimensões ISO, ANSI ou personalizadas — um benefício mensurável que economiza tempo e elimina o pós‑processamento manual.

## Pré-requisitos

Antes de iniciarmos esta jornada, certifique-se de que você tem os seguintes pré-requisitos configurados:
- Ambiente Java: Certifique-se de que o Java está instalado em sua máquina.  
- Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD para Java a partir do [link de download](https://releases.aspose.com/cad/java/).  
- Diretório de Documentos: Crie um diretório para seus desenhos DWG.

## Importar Pacotes

A classe `CadImage` é o objeto central do Aspose.CAD que representa um desenho CAD na memória. Importe os namespaces necessários antes de começar:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Etapa 1: Carregar Desenho CAD

`CadImage` carrega o arquivo DWG e fornece acesso aos seus dados vetoriais. Comece carregando seu desenho CAD em um objeto `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Etapa 2: Configurar Opções de Rasterização

`RasterizationOptions` define como os vetores CAD são rasterizados antes de serem inseridos no PDF. Configure as opções de rasterização para a imagem CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Etapa 3: Personalizar Tamanhos de Página do Layout

`PdfOptions` permite atribuir dimensões de página distintas a cada layout dentro do DWG. Defina tamanhos personalizados para vários layouts no desenho CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Etapa 4: Definir Opções de PDF

`PdfOptions` é o contêiner que combina as configurações de rasterização e as definições de layout. Configure as opções de PDF, incorporando as configurações de rasterização:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Etapa 5: Salvar como PDF

`PdfSaveOptions` finaliza a conversão e grava o arquivo de saída. Salve a imagem CAD processada como PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Parabéns! Você **criou pdf a partir de dwg** com diferentes tamanhos de página usando Aspose.CAD para Java.

## Problemas Comuns e Soluções

- **Páginas em branco no PDF de saída** – Certifique-se de que os valores de `PageSize` correspondam às dimensões reais do layout no arquivo DWG.  
- **Erros de falta de memória em desenhos grandes** – Use `CadImage.load(..., LoadOptions)` com `LoadOptions.setLoadMode(LoadMode.Memory)` para transmitir o arquivo em vez de carregá-lo completamente.  
- **Escala incorreta** – Ajuste `RasterizationOptions.setPageWidth` e `setPageHeight` para corresponder ao DPI desejado (pontos por polegada).

## Perguntas Frequentes

**Q: Posso usar Aspose.CAD para Java com outras bibliotecas Java?**  
A: Sim, Aspose.CAD para Java integra-se perfeitamente com bibliotecas como Apache POI, Jackson ou Spring Boot.

**Q: Existe uma versão de avaliação disponível?**  
A: Absolutamente! Você pode acessar uma versão de avaliação gratuita [aqui](https://releases.aspose.com/).

**Q: Onde posso encontrar suporte adicional?**  
A: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**Q: Como obtenho uma licença temporária?**  
A: Você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso comprar a versão completa?**  
A: Compre a versão completa do Aspose.CAD para Java [aqui](https://purchase.aspose.com/buy).

---

**Last Updated:** 2026-06-29  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Tutoriais Relacionados

- [Exportar DWG para PDF ou Raster usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Exportar Layouts CAD para PDF com Aspose.CAD para Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Exportar Layout DWG específico para PDF usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}