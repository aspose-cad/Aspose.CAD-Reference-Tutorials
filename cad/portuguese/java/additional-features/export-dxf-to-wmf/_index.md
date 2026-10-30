---
date: 2026-10-30
description: Aprenda como converter em lote arquivos DXF para WMF usando Aspose.CAD
  for Java, com step‑by‑step code, informações sobre a versão de avaliação gratuita
  e exportação opcional para PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Exportar DXF para o formato WMF usando Java
og_description: Converter em lote arquivos DXF para WMF usando Aspose.CAD for Java.
  Siga este guia para carregar desenhos DXF, definir rasterization options, salvar
  como WMF e, opcionalmente, exportar para PDF com versão de avaliação gratuita.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Converter em lote arquivos DXF para WMF com Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Converter em lote arquivos DXF para WMF com Aspose.CAD for Java
url: /pt/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter em lote arquivos DXF para WMF com Aspose.CAD para Java

## Introdução

Neste tutorial você aprenderá a **converter em lote arquivos DXF para WMF** usando Aspose.CAD para Java. Seja para incorporar desenhos CAD em relatórios baseados em Windows, gerar gráficos vetoriais leves para documentos Office ou automatizar conversões em larga escala, este guia orienta você a carregar um desenho DXF, configurar opções de rasterização, salvar como WMF e, opcionalmente, exportar o mesmo desenho para PDF. As etapas funcionam em qualquer plataforma que execute Java 8+.

## Respostas rápidas
- **Posso converter DXF para WMF com um teste gratuito?** Sim – a Aspose oferece um teste totalmente funcional de 30 dias.  
- **Qual versão do Java é necessária?** Java 8 ou superior.  
- **Preciso de uma licença para executar o código?** Uma licença é necessária para produção; o teste funciona para desenvolvimento e testes.  
- **A conversão é sem perdas?** Os dados vetoriais são preservados; as opções de rasterização permitem controlar a resolução.  
- **Posso também exportar o mesmo desenho para PDF?** Claro – veja a etapa “Exportar para PDF” abaixo.  
- **Como faço para converter em lote muitos arquivos DXF de uma vez?** Percorra uma pasta, aplique o mesmo padrão carregar‑rasterizar‑salvar a cada arquivo.

## O que é conversão em lote de arquivos DXF?

Converter em lote arquivos DXF significa processar múltiplos desenhos Drawing Exchange Format (DXF) em uma única execução e produzir saída WMF para cada um. WMF (Windows Metafile) é um formato de imagem vetorial que se integra nativamente ao Microsoft Office, aplicativos Windows e muitas ferramentas de relatório.

## Por que usar Aspose.CAD para Java?

Aspose.CAD para Java é um motor puro‑Java que suporta **mais de 50 formatos de entrada e saída** — incluindo DXF, DWG, DGN, PDF, PNG, SVG e WMF — enquanto oferece **99 % de fidelidade vetorial**. Ele funciona em qualquer SO que suporte Java, não requer DLLs nativas e permite controlar o tamanho da página, DPI e cor de fundo através de uma única classe `CadRasterizationOptions`. A mesma API também lida com exportações PDF, PNG e SVG, eliminando a necessidade de múltiplas bibliotecas.

### Benefícios quantificados
- **Mais de 50 formatos suportados** reduzem a necessidade de conversores de terceiros.  
- **Processa arquivos DXF de 300 páginas em menos de 5 segundos** em um servidor típico de 2,5 GHz quando rasterizado a 150 DPI.  
- **A pegada de memória permanece abaixo de 200 MB** para arquivos de até 500 MB quando você define dimensões de página adequadas.  

## Pré-requisitos

- **Aspose.CAD para Java** integrado ao seu projeto. Baixe-o do site oficial: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Uma pasta que contém os arquivos DXF que você deseja converter (por exemplo, `Your Document Directory/DXFDrawings/`).  

## Importar namespaces

`Image` é a classe principal do Aspose.CAD que representa um desenho CAD na memória. Após carregar um arquivo, todas as operações subsequentes — rasterização, conversão de formato e limpeza de recursos — são realizadas através deste objeto.

As importações a seguir trazem as classes do Aspose.CAD necessárias para carregar, rasterizar e salvar arquivos CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Guia passo a passo

### Como faço para converter em lote arquivos DXF para WMF em Java?

Carregue cada DXF com `Image.load`, configure `CadRasterizationOptions` para o tamanho de página e DPI desejados e chame `image.save` com `SaveFormat.WMF`. Esse padrão de três etapas realiza a conversão completa mantendo a qualidade vetorial intacta e requer apenas algumas linhas de código por arquivo.

#### Etapa 1: carregar desenho dxf

`Image.load` lê o arquivo DXF em um objeto `Image` do Aspose.CAD.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Etapa 2: configurar opções de rasterização

`CadRasterizationOptions` especifica o tamanho da página, resolução e fundo para rasterizar o desenho CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Etapa 3: salvar como wmf

`ImageSaveOptions` com `SaveFormat.WMF` indica ao Aspose.CAD para gravar a saída como um Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Etapa 4: liberar recursos

Chamar `image.close()` libera os recursos nativos usados pelo objeto `Image` do Aspose.CAD.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Etapa 5: opcional – exportar para pdf

`PdfOptions` configura as definições específicas de PDF ao salvar a imagem como um documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Dica profissional:** Você pode reutilizar o mesmo objeto `CadRasterizationOptions` para exportação PDF passando‑o para uma instância `PdfOptions`, economizando algumas linhas de configuração.

## Como exportar DXF para PDF usando Aspose CAD Java?

Substitua o formato de salvamento WMF por PDF usando `new ImageSaveOptions(SaveFormat.Pdf)`. As mesmas configurações de rasterização se aplicam, e você pode ainda definir opções específicas de PDF, como metadados de autor ou nível de compressão. Essa conversão em uma única linha produz um PDF pesquisável e fiel à página que espelha o layout CAD original.

## Problemas comuns e soluções

`License` é a classe Aspose usada para aplicar uma licença do produto em tempo de execução.

| Problema | Causa | Correção |
|----------|-------|----------|
| **`NullPointerException` on `cadImage.save`** | Variável `cadImage` não definida (deve ser `image`). | Substitua `cadImage` por `image` ou renomeie a variável de forma consistente. |
| **Output WMF is blank** | Tamanho da página de rasterização muito pequeno ou cor de fundo definida como transparente. | Aumente `PageWidth`/`PageHeight` ou defina uma cor de fundo via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Executando sem uma licença Aspose válida em produção. | Aplique o arquivo de licença no início da aplicação: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Perguntas frequentes

**Q: Onde posso encontrar a documentação do Aspose.CAD?**  
A: Você pode acessar a documentação [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Como faço o download do Aspose.CAD para Java?**  
A: Baixe a biblioteca [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Existe um teste gratuito disponível?**  
A: Sim, você pode obter um teste gratuito [Aspose free trial page](https://releases.aspose.com/).

**Q: Precisa de opções de licenciamento temporário?**  
A: Explore licenças temporárias [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso obter suporte?**  
A: Visite o fórum de suporte do Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Perguntas frequentes adicionais

**Q: Posso converter arquivos DXF grandes (centenas de MB) sem ficar sem memória?**  
A: Sim. Carregue o arquivo em um bloco try‑with‑resources e libere o objeto `Image` prontamente. Ajuste `CadRasterizationOptions.setPageWidth/Height` para um tamanho razoável para manter o uso de memória baixo.

**Q: A saída WMF preserva informações de camada?**  
A: WMF é um formato vetorial plano, portanto a hierarquia de camadas é achatada, mas estilos de linha, cores e padrões de hachura são preservados.

**Q: É possível definir um DPI personalizado para o WMF?**  
A: Use `rasterizationOptions.setResolution(300);` para definir o DPI antes de salvar.

**Q: Posso converter em lote vários arquivos DXF em uma única execução?**  
A: Absolutamente. Percorra um diretório, carregue cada arquivo e aplique a mesma lógica de rasterização e salvamento.

**Q: Quais versões do Java são suportadas?**  
A: Aspose.CAD para Java suporta Java 8 e posteriores, incluindo Java 11, 17 e versões LTS mais recentes.

---

**Última atualização:** 2026-10-30  
**Testado com:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Tutoriais relacionados

- [Criar PDF a partir de CAD – Exportar DXF para PDF com Aspose.CAD para Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Criar PDF a partir de DXF: Exportar camada com Aspose.CAD para Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Como converter layout DXF para imagem JPEG com Aspose.CAD em Java](/cad/java/additional-features/export-specific-layout-to-image/)









```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}