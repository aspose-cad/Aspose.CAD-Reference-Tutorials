---
date: 2026-10-19
description: Aprenda a criar arquivos PNG thumbnail IFC com Aspose.CAD for Java em
  apenas algumas linhas de código.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exportar IFC para PNG
og_description: Crie arquivos PNG thumbnail IFC sem esforço usando Aspose.CAD for
  Java. Este guia passo a passo mostra como carregar, rasterizar e salvar modelos
  IFC como imagens PNG de alta qualidade.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Criar PNG thumbnail IFC com Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Como criar miniatura PNG IFC com Aspose.CAD for Java
url: /pt/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar IFC para PNG com Aspose.CAD para Java

## Introdução

Neste tutorial você aprenderá a **criar miniaturas PNG de arquivos IFC** com Aspose.CAD para Java. Seja para gerar pré‑visualizações rápidas para um portal BIM, gerar miniaturas para um sistema de gerenciamento de documentos ou automatizar conversões em lote, os passos abaixo permitem rasterizar um modelo IFC 3‑D em uma imagem PNG 2‑D nítida em apenas algumas linhas de código Java.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.CAD para Java.  
- **Posso criar uma miniatura PNG de IFC em poucas linhas de código?** Sim – todo o fluxo cabe em menos de 20 linhas.  
- **Preciso de licença para produção?** Uma licença temporária funciona para testes; uma licença completa é necessária para implantação comercial.  
- **A saída é escalável?** Você pode definir quaisquer dimensões em pixels, então o PNG escala para o tamanho que precisar.  
- **Qual versão do Java é suportada?** Java 8 ou superior.

## O que significa “converter IFC para PNG”?
Converter IFC (Industry Foundation Classes) para PNG significa rasterizar o modelo 3‑D do edifício em uma imagem bitmap 2‑D. Esse processo cria uma miniatura visual que pode ser exibida em navegadores, relatórios ou aplicativos móveis sem exigir um visualizador CAD completo.

## Por que usar Aspose.CAD para Java?
Aspose.CAD suporta **mais de 30 formatos CAD e BIM**, incluindo IFC, DWG, DXF e DGN, e pode processar arquivos de até **2 GB** sem carregar todo o documento na memória. A biblioteca é pura Java, tem **zero dependências externas** e roda em Windows, Linux e macOS, tornando‑a ideal para geração de imagens no lado do servidor.  
Ela oferece rasterização de alto desempenho, amplo suporte a formatos e fácil integração em aplicações Java.

## Pré‑requisitos

- **Biblioteca Aspose.CAD** – baixe o JAR mais recente a partir do [link de download](https://releases.aspose.com/cad/java/).  
- **Kit de Desenvolvimento Java** – JDK 8 ou mais recente instalado na sua máquina.  
- **Arquivo fonte IFC** – coloque o arquivo em uma pasta que você possa referenciar a partir do seu código.

## Importar namespaces

O pacote `com.aspose.cad` fornece todas as classes necessárias. `CadImage` é o ponto de entrada para carregar arquivos CAD, enquanto `PngOptions` configura as opções de rasterização.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Como criar miniatura PNG de IFC em Java?

Carregue o arquivo IFC, defina as opções de rasterização e salve o resultado como imagem PNG – esse é o fluxo completo de conversão. As seções a seguir detalham cada passo, para que você possa copiar‑colar os trechos no seu projeto e executá‑los imediatamente.

### Etapa 1: carregar o arquivo IFC
Primeiro, aponte para a pasta onde seu arquivo IFC está localizado e carregue‑o com `CadImage.load`.  
`CadImage.load` lê um arquivo CAD e devolve um objeto de imagem que pode ser rasterizado.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Por que isso importa:** Carregar o arquivo como um `CadImage` fornece acesso às opções de conversão vetor‑raster que controlam resolução, cor de fundo e espessura de linha.

### Etapa 2: definir opções de rasterização
Defina as dimensões de saída e quaisquer outras configurações relacionadas ao vetor através de `VectorRasterizationOptions`.  
`VectorRasterizationOptions` permite especificar tamanho de saída, cor de fundo e outros parâmetros de rasterização.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Ajuste `PageWidth` e `PageHeight` para controlar a resolução final do PNG, o que é essencial ao **salvar arquivos PNG java** para impressões de alta qualidade ou miniaturas web.

### Etapa 3: configurar opções PNG
Vincule as opções de rasterização ao exportador PNG criando uma instância de `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Etapa 4: salvar a imagem como PNG
Por fim, escreva a imagem rasterizada no disco usando o método `save`.  
`save` grava a imagem rasterizada no caminho de arquivo especificado no formato escolhido.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Após esta etapa você terá **criado uma miniatura PNG de IFC** e poderá usar o `example.png` resultante onde precisar de uma imagem raster.

## Casos de uso comuns
- **Gerar miniaturas** para modelos BIM em portais web.  
- **Incorporar capturas de plantas** em relatórios PDF ou Word.  
- **Conversão automática em lote** de grandes bibliotecas IFC para projetos de arquivamento ou migração.

## Solução de problemas e dicas
- **Problemas de memória:** Para arquivos IFC muito grandes, aumente o heap da JVM (`-Xmx2g` ou superior).  
- **Texturas ausentes:** Certifique‑se de que os recursos externos do arquivo IFC estejam acessíveis a partir do `dataDir`.  
- **Dica profissional:** Use `vectorOptions.setBackgroundColor(Color.getWhite())` se preferir um fundo branco em vez do padrão PNG transparente.

## Perguntas Frequentes

### Q1: O Aspose.CAD é compatível com todas as versões de arquivos IFC?
A1: Aspose.CAD suporta várias versões de IFC. Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações detalhadas de compatibilidade.

### Q2: Posso personalizar ainda mais as opções de rasterização?
A2: Absolutamente! Explore a [documentação](https://reference.aspose.com/cad/java/) para configurações avançadas, como controle de DPI, anti‑aliasing e espessura de linha.

### Q3: Existe uma versão de avaliação disponível?
A3: Sim, você pode baixar a avaliação gratuita a partir do [teste gratuito do Aspose.CAD](https://releases.aspose.com/).

### Q4: Como obter uma licença temporária para testes?
A4: Obtenha uma licença temporária na [página de licença temporária do Aspose.CAD](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso fazer perguntas ou relatar problemas?
A5: Participe da comunidade no [fórum do Aspose.CAD](https://forum.aspose.com/c/cad/19) para obter suporte de engenheiros da Aspose e de outros desenvolvedores.

## Perguntas frequentes

**P: Posso usar esta abordagem para converter outros formatos CAD para PNG?**  
R: Sim, Aspose.CAD suporta muitos formatos (DWG, DXF, DGN, etc.). Basta mudar a extensão do arquivo e carregar a classe de imagem apropriada.

**P: A biblioteca permite definir um DPI personalizado?**  
R: O DPI é controlado indiretamente via `PageWidth`/`PageHeight`. Ajuste esses valores em relação ao tamanho físico desejado para alcançar o DPI requerido.

**P: A saída PNG é sem perdas?**  
R: PNG é um formato sem perdas, portanto a imagem rasterizada mantém toda a fidelidade visual dos dados vetoriais originais.

## Conclusão

Agora você tem um método completo e pronto para produção de **criar miniaturas PNG de IFC** usando Aspose.CAD para Java. Integre esses passos em ferramentas desktop, serviços de servidor ou funções de nuvem para automatizar pipelines de visualização BIM e entregar miniaturas rápidas e de alta qualidade aos usuários finais.

---

**Última atualização:** 2026-10-19  
**Testado com:** Aspose.CAD para Java 24.11  
**Autor:** Aspose

## Tutoriais Relacionados

- [Como Converter STL para PNG com Aspose.CAD para Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Converter DWG para PNG – Salvar CAD como PNG Usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Exportar DWG para PDF em Java – Definir Tamanho da Página PDF com Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}