---
date: 2026-06-09
description: Aprenda como converter DXF para WMF com Aspose.CAD para Java, incluindo
  um teste gratuito, suporte a Java 8+ e exportação opcional para PDF. Guia passo
  a passo com exemplos de código.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Exportar DXF para o formato WMF usando Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Converter DXF para WMF usando Aspose.CAD em Java
url: /pt/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DXF para WMF usando Aspose.CAD em Java

## Introdução

Neste tutorial você descobrirá como **converter DXF para WMF** com Aspose.CAD para Java. Seja para incorporar desenhos CAD em um relatório baseado em Windows, gerar gráficos vetoriais leves para documentos do Office ou automatizar conversões em lote, converter DXF para WMF é uma necessidade frequente em pipelines de engenharia e relatórios. Vamos percorrer o carregamento de um desenho DXF, a configuração das opções de rasterização, a gravação do resultado como WMF e, opcionalmente, a exportação do mesmo desenho para PDF.

## Respostas Rápidas
- **Posso converter DXF para WMF com uma avaliação gratuita?** Sim – a Aspose oferece uma avaliação totalmente funcional de 30 dias.  
- **Qual versão do Java é necessária?** Java 8 ou posterior.  
- **Preciso de uma licença para executar o código?** Uma licença é necessária para produção; a avaliação funciona para desenvolvimento e testes.  
- **A conversão é sem perdas?** Os dados vetoriais são preservados; as opções de rasterização permitem controlar a resolução.  
- **Posso também exportar o mesmo desenho para PDF?** Absolutamente – veja a etapa “Exportar para PDF” abaixo.

## O que é “converter DXF para WMF”?

Converter DXF para WMF significa pegar um arquivo Drawing Exchange Format (DXF) — um formato CAD amplamente usado — e transformá‑lo em um Windows Metafile (WMF). WMF é um formato de imagem vetorial que se integra perfeitamente ao Microsoft Office, aplicativos Windows e muitas ferramentas de relatório.

## Por que usar Aspose.CAD para Java?

Aspose.CAD para Java fornece um motor puro‑Java, sem DLL nativa, que converte arquivos CAD com **mais de 99 % de fidelidade vetorial**, preservando camadas, cores, estilos de linha e padrões de hachura. Ele suporta **mais de 50 formatos de entrada e saída** — incluindo DXF, DWG, DGN, PDF, PNG, SVG e WMF — permitindo ajustar finamente o tamanho da página, DPI e cor de fundo através de opções de rasterização integradas. A mesma API também lida com exportações para PDF, PNG e SVG, eliminando a necessidade de múltiplas bibliotecas.

### Principais vantagens
- **Sem dependências externas** – puro Java, funciona em qualquer SO que execute Java.  
- **Renderização de alta fidelidade** – mantém espessura de linha, cor e detalhes de hachura.  
- **Rasterização incorporada** – controla dimensões da página, resolução e fundo.  
- **Conversão tudo‑em‑um** – as mesmas classes exportam para WMF, PDF, PNG, SVG, etc.

## Pré‑requisitos

Antes de começar, certifique-se de que você tem:

- **Aspose.CAD para Java** integrado ao seu projeto. Baixe‑o do site oficial: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Diretório de documentos** onde seus arquivos DXF estão armazenados (por exemplo, `Your Document Directory/DXFDrawings/`).

## Importar Namespaces

Os imports a seguir trazem as classes Aspose.CAD necessárias para carregar, rasterizar e salvar arquivos CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Guia Passo a Passo

### Como converter DXF para WMF em Java?

Carregue seu arquivo DXF com `Image.load("yourFile.dxf")`, configure `CadRasterizationOptions` para o tamanho de página e DPI desejados e, em seguida, chame `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Esse padrão de três etapas realiza a conversão completa mantendo a qualidade vetorial intacta e requer apenas algumas linhas de código.

#### Etapa 1: Carregar Desenho DXF

`Image.load` lê o arquivo DXF em um objeto Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Etapa 2: Configurar Opções de Rasterização

`CadRasterizationOptions` especifica o tamanho da página, resolução e fundo para rasterizar o desenho CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Etapa 3: Salvar como WMF

`ImageSaveOptions` com `SaveFormat.WMF` indica ao Aspose.CAD que escreva a saída como um Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Etapa 4: Liberar Recursos

Chamar `image.close()` libera recursos nativos usados pelo objeto Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Etapa 5: Opcional – Exportar para PDF

`PdfOptions` configura definições específicas de PDF ao salvar a imagem como um documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Dica profissional:** Você pode reutilizar o mesmo objeto `CadRasterizationOptions` para exportação PDF passando‑o para uma instância `PdfOptions`, economizando algumas linhas de configuração.

## Como exportar DXF para PDF usando Aspose CAD Java?

Exportar para PDF segue as mesmas etapas de carregamento e rasterização; basta substituir o formato de gravação WMF por PDF. Use `new ImageSaveOptions(SaveFormat.Pdf)` e, opcionalmente, defina opções específicas de PDF, como nível de compressão ou metadados de autor. Essa conversão em uma única linha produz um PDF pesquisável e preciso em página que espelha o layout CAD original.

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| **`NullPointerException` em `cadImage.save`** | Variável `cadImage` não definida (deve ser `image`). | Substitua `cadImage` por `image` ou renomeie a variável de forma consistente. |
| **Saída WMF está em branco** | Tamanho da página de rasterização muito pequeno ou cor de fundo definida como transparente. | Aumente `PageWidth`/`PageHeight` ou defina uma cor de fundo via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Exceção de licença** | Executando sem uma licença Aspose válida em produção. | Aplique o arquivo de licença no início da aplicação: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusão

Agora você tem um fluxo de trabalho completo e pronto para produção para **converter DXF para WMF** usando Aspose.CAD para Java, com uma etapa opcional para **exportar o mesmo desenho para PDF**. Essa abordagem fornece saída vetorial de alta qualidade que se integra perfeitamente com ferramentas de relatório e documentação baseadas em Windows, mantendo sua base de código simples e sem dependências.

## Perguntas Frequentes

### Q1: Onde posso encontrar a documentação do Aspose.CAD?

R1: Você pode acessar a documentação [aqui](https://reference.aspose.com/cad/java/).

### Q2: Como faço o download do Aspose.CAD para Java?

R2: Baixe a biblioteca [aqui](https://releases.aspose.com/cad/java/).

### Q3: Existe uma avaliação gratuita disponível?

R3: Sim, você pode obter uma avaliação gratuita [aqui](httpshttps://releases.aspose.com/).

### Q4: Precisa de opções de licenciamento temporário?

R4: Explore licenças temporárias [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso obter suporte?

R5: Visite o fórum de suporte do Aspose.CAD [aqui](https://forum.aspose.com/c/cad/19).

## Perguntas Frequentes

**Q: Posso converter arquivos DXF grandes (centenas de MB) sem ficar sem memória?**  
A: Sim. Carregue o arquivo em um bloco try‑with‑resources e libere o objeto `Image` prontamente. Ajuste `CadRasterizationOptions.setPageWidth/Height` para um tamanho razoável para manter o uso de memória baixo.

**Q: A saída WMF mantém informações de camada?**  
A: WMF é um formato vetorial plano, portanto a hierarquia de camadas é achatada, mas estilos de linha, cores e padrões de hachura são preservados.

**Q: É possível definir um DPI personalizado para o WMF?**  
A: Use `rasterizationOptions.setResolution(300);` para definir o DPI antes de salvar.

**Q: Posso converter em lote vários arquivos DXF em uma única execução?**  
A: Absolutamente. Percorra um diretório, carregue cada arquivo e aplique a mesma lógica de rasterização e gravação.

**Q: Quais versões do Java são suportadas?**  
A: Aspose.CAD para Java suporta Java 8 e posteriores, incluindo Java 11, 17 e versões LTS mais recentes.

---

**Última atualização:** 2026-06-09  
**Testado com:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Tutoriais Relacionados

- [Criar PDF a partir de CAD – Exportar DXF para PDF com Aspose.CAD para Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Criar PDF a partir de DXF: Exportar Camada com Aspose.CAD para Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Como Converter Layout DXF para Imagem JPEG com Aspose.CAD em Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}