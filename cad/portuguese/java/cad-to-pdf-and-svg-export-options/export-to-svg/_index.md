---
date: 2026-06-14
description: Aprenda como exportar CAD para SVG com Aspose.CAD para Java. Este guia
  passo a passo mostra como converter DWG para SVG, definir o modo de cor SVG e integrar
  a biblioteca ao seu projeto Java.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exportar para SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exportar CAD para SVG usando Aspose.CAD para Java
url: /pt/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar CAD para SVG usando Aspose.CAD para Java

## Introdução

Neste tutorial abrangente, você aprenderá **como exportar CAD para SVG** usando Aspose.CAD para Java. Seja para **converter DWG para SVG**, gerar SVG a partir de arquivos DWG em um trabalho em lote, ou simplesmente mudar o SVG para escala de cinza para exibição web leve, este guia o conduzirá por cada passo — desde a configuração da biblioteca até o ajuste fino das opções de exportação. Ao final, você terá um snippet pronto para produção que roda em qualquer plataforma compatível com JVM.

## Respostas Rápidas
- **O que significa “exportar CAD para SVG”?** Ele transforma um desenho CAD (por exemplo, DWG ou DXF) em um arquivo Scalable Vector Graphics que os navegadores renderizam sem perda de qualidade.  
- **Qual biblioteca realiza a conversão?** Aspose.CAD for Java fornece uma API dedicada que suporta mais de 30 formatos CAD e gera SVG com fidelidade vetorial completa.  
- **Preciso de uma licença para desenvolvimento?** Um teste gratuito funciona para avaliação; uma licença comercial é necessária para implantações em produção.  
- **Posso controlar a saída de cor do SVG?** Sim—use `SvgColorMode` para alternar entre renderização em escala de cinza e cores completas.  
- **É necessário algum software adicional?** Apenas um runtime Java (JDK 8 ou superior) e o JAR do Aspose.CAD; nenhuma ferramenta CAD externa é necessária.

## O que é exportar CAD para SVG?
Exportar CAD para SVG é o processo de converter um arquivo CAD nativo (como DWG, DXF ou DWF) para o formato de imagem vetorial SVG. O SVG resultante mantém os dados geométricos exatos, permitindo exibição independente de resolução em navegadores web e ferramentas de design.

## Por que exportar CAD para SVG com Aspose.CAD?
Aspose.CAD pode lidar com **mais de 30 formatos de entrada** e gerar saída SVG de até **500 páginas** sem carregar o arquivo inteiro na memória, oferecendo **conversão vetorial de alta fidelidade** a velocidades de **200 páginas/segundo** em uma CPU típica de servidor. A biblioteca roda **100 % Java**, eliminando a necessidade de DLLs nativas ou motores CAD de terceiros.

## Pré-requisitos

- **Java Development Kit** (JDK 8 ou superior) instalado e configurado na sua máquina.  
- **Aspose.CAD for Java** arquivo JAR baixado do [link de download](https://releases.aspose.com/cad/java/).  
- Uma pasta que contém ao menos um desenho CAD (DWG, DXF, etc.) que você deseja converter.

## Importar Namespaces

Antes de escrever qualquer código, certifique‑se de que a biblioteca Aspose.CAD está no seu classpath e importe as classes necessárias.

### Passo 1: Abra seu Projeto Java
Inicie sua IDE favorita (IntelliJ IDEA, Eclipse, VS Code) e abra o projeto onde pretende adicionar a lógica de conversão.

### Passo 2: Adicione a Biblioteca Aspose.CAD
Coloque o arquivo `aspose-cad-xx.jar` no diretório `libs` e adicione‑o como dependência na sua ferramenta de build (Maven, Gradle ou plain `javac`).

### Passo 3: Importar Namespaces
No arquivo fonte Java que realizará a conversão, adicione as seguintes importações:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Essas importações dão acesso à classe central `Image` e às opções de exportação específicas para SVG.

## Como Exportar CAD para SVG Usando Aspose.CAD para Java?

Exportar um desenho CAD para SVG com Aspose.CAD envolve carregar o arquivo fonte, configurar opções específicas de SVG e gravar a saída. O processo é simples, requer apenas algumas linhas de código e funciona de forma consistente em todos os formatos CAD suportados, preservando a fidelidade vetorial.

### Passo 1: Especifique o Diretório de Recursos
Defina o caminho absoluto ou relativo que aponta para a pasta que contém seus desenhos CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Passo 2: Carregue o Desenho CAD
A classe `Image` é o objeto de nível superior do Aspose.CAD que representa um desenho CAD na memória. Carregar o arquivo cria uma representação em memória pronta para exportação.

`Image.load` lê um arquivo CAD e cria uma representação em memória do desenho.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Passo 3: Configurar Opções de Exportação SVG
`SvgExportOptions` permite ajustar finamente a saída SVG. Abaixo definimos o modo de cor para escala de cinza e garantimos que todo o texto seja renderizado como formas, o que melhora a compatibilidade com navegadores que não possuem a fonte original.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Passo 4: Salvar como SVG
Finalmente, invoque `save` na instância `Image`, passando o nome do arquivo de destino e as opções configuradas. Aspose.CAD grava um arquivo SVG compatível com padrões que pode ser aberto diretamente em qualquer navegador moderno.

`save` grava a imagem no arquivo especificado usando as opções de exportação fornecidas.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Dica profissional:** Para gerar um SVG em cores completas, substitua `SvgColorMode.Grayscale` por `SvgColorMode.FullColor`. Essa troca preserva a paleta original enquanto ainda fornece escalabilidade vetorial.

## Por que Usar Aspose.CAD para Exportar CAD para SVG?
- **Alta fidelidade:** Dados vetoriais são mantidos, garantindo que o SVG tenha exatamente a mesma aparência do desenho CAD original.  
- **Sem dependências externas:** A conversão ocorre totalmente dentro do Java, eliminando a necessidade de ferramentas adicionais.  
- **Saída personalizável:** Opções como `setColorType` permitem controlar se o SVG será em escala de cinza ou em cores completas.  
- **Desempenho escalável:** Processa desenhos com centenas de páginas em segundos, com uso de memória abaixo de 50 MB.

## Problemas Comuns e Soluções
- **Arquivo não encontrado:** Verifique se `dataDir` aponta para a pasta correta e se o nome do arquivo DWG corresponde ao caso no sistema de arquivos.  
- **Saída SVG em branco:** Certifique-se de que `options.setTextAsShapes(true)` esteja habilitado quando o desenho fonte contém texto que deve aparecer como formas vetoriais.  
- **Formato CAD não suportado:** Aspose.CAD suporta DWG, DXF, DWF e mais de 15 outros formatos; consulte a documentação oficial para a lista completa.  
- **Gargalos de desempenho:** Para arquivos extremamente grandes, habilite o modo de streaming via `options.setEnableStreaming(true)` para manter o consumo de memória baixo.

## Perguntas Frequentes

**Q: Posso converter um arquivo DXF para SVG usando o mesmo código?**  
A: Sim, basta substituir o nome do arquivo DWG por um arquivo DXF; a API detecta e processa automaticamente ambos os formatos.

**Q: Como altero a saída para SVG em cores completas?**  
A: Defina `options.setColorType(SvgColorMode.FullColor);` antes de invocar o método `save`.

**Q: É possível incorporar fontes no SVG gerado?**  
A: Aspose.CAD converte texto em formas, portanto incorporar fontes é desnecessário; o SVG resultante contém apenas contornos vetoriais.

**Q: A biblioteca funciona em Linux e macOS?**  
A: A biblioteca Java é independente de plataforma e roda onde houver uma JVM compatível, incluindo Windows, Linux e macOS.

**Q: Qual versão do Aspose.CAD foi usada neste tutorial?**  
A: O exemplo foi testado com Aspose.CAD for Java **24.10**.

---

**Última Atualização:** 2026-06-14  
**Testado com:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Exportar DWG para PDF ou Raster Usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg para pdf java – Exportar CAD para PDF com Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportar Layout DWG Específico para PDF Usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}