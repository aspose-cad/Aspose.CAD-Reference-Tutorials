---
date: 2026-05-20
description: Aprenda como converter DWG para PDF enquanto substitui a detecção automática
  de página de código usando Aspose.CAD for Java. Inclui etapas de exportação de dwg
  para pdf, dicas de codificação e solução de problemas.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Substituir a Detecção Automática de Página de Código em Arquivos DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Converter DWG para PDF – Substituir a Detecção de Página de Código em Java
url: /pt/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DWG para PDF – Substituir a Detecção de Página de Código em Java

Neste tutorial abrangente, você aprenderá **como converter DWG para PDF** enquanto substitui a detecção automática de página de código que pode corromper o texto. Aspose.CAD for Java oferece controle preciso sobre a codificação de caracteres, permitindo recuperar dados CIF/MIF malformados e gerar saída PDF confiável. Seja construindo um conversor em lote ou adicionando processamento CAD a um serviço Java maior, as etapas abaixo orientam todo o fluxo de trabalho — da configuração do projeto à verificação.

## Respostas Rápidas
- **O que significa “substituir a página de código”?** Força o Aspose.CAD a usar uma codificação de caracteres específica em vez de adivinhar.
- **Posso exportar DWG diretamente para PDF?** Sim — após definir a página de código correta, você pode salvar a imagem CAD como PDF.
- **Qual codificação funciona para texto em japonês?** `CodePages.Japanese` e `MifCodePages.Japanese` são as escolhas corretas.
- **Preciso de licença para uso em produção?** É necessária uma licença comercial; uma licença temporária está disponível para testes.
- **Qual versão do Aspose.CAD é necessária?** Qualquer versão recente que suporte `LoadOptions` e `PdfOptions`.

## O que é “exportar CAD para PDF”?
Exportar CAD para PDF transforma um desenho DWG baseado em vetores em um documento PDF de layout fixo, visualizável universalmente. A conversão mantém todas as entidades geométricas, linhas, camadas e texto incorporado, ao mesmo tempo que achata o desenho em um formato que pode ser facilmente compartilhado, impresso, arquivado ou embutido em outras aplicações sem exigir software CAD.

## Por que sobrescrever a detecção automática de página de código?
Especificar manualmente a página de código garante que os bytes de texto sejam interpretados corretamente, eliminando os caracteres estranhos que frequentemente aparecem quando a auto‑detecção do Aspose.CAD adivinha a codificação legada errada. Isso é essencial para scripts não latinos, como japonês, cirílico ou árabe, e assegura que o PDF exportado corresponda ao design original.

## Pré-requisitos
- **Ambiente de Desenvolvimento Java** – JDK 8+ e sua IDE preferida.  
- **Aspose.CAD for Java** – Baixe a biblioteca no site oficial [here](https://releases.aspose.com/cad/java/).  
- **Arquivo de Exemplo DWG** – Use o `SimpleEntities.dwg` fornecido ou qualquer DWG que precise converter.

## Importar Pacotes
As classes `Document`, `LoadOptions` e `PdfOptions` são o núcleo do processo de conversão.

A classe `Document` representa um desenho CAD na memória, oferecendo métodos para carregar, manipular e salvar o arquivo em vários formatos.  
A classe `LoadOptions` permite especificar a página de código e opções de recuperação ao carregar um arquivo DWG.  
A classe `PdfOptions` controla configurações específicas de PDF, como compressão, rasterização e metadados.

No seu projeto Java, importe as classes necessárias do Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Como converter DWG para PDF com sobrescrita da página de código?
Carregue o arquivo DWG usando `LoadOptions` para especificar a página de código exata, então invoque o método `save` no `CadImage` resultante com uma instância configurada de `PdfOptions`. Essa abordagem em duas etapas garante que o texto seja interpretado corretamente e que o PDF gerado preserve a fidelidade, camadas e qualidade vetorial do desenho original.

### Etapa 1: Configurar o Projeto Java
Crie um projeto Maven ou Gradle e adicione o JAR do Aspose.CAD ao classpath. Isso garante que a IDE possa resolver as classes importadas e que o tempo de execução localize a biblioteca.

### Etapa 2: Carregar o Arquivo DWG com uma Página de Código Especificada
Informe ao Aspose.CAD qual codificação usar e se deve tentar a recuperação de dados CIF/MIF malformados.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Etapa 3: Exportar a Imagem CAD para PDF
Com a página de código correta aplicada, você pode exportar o desenho com segurança. O objeto `PdfOptions` permite ajustar finamente a saída PDF (compressão, rasterização, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Etapa 4: Verificar o Sucesso
Uma mensagem simples no console confirma que o processo foi concluído sem exceções.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Você pode repetir essas etapas para vários arquivos DWG, ajustando o caminho de origem e o nome de saída conforme necessário.

## Problemas Comuns & Soluções
- **Caracteres estranhos ainda aparecem:** Verifique se o `specifiedEncoding` corresponde à página de código original do DWG. Use um enum `CodePages` diferente, se necessário.  
- **`NullPointerException` em `cadImage.save`:** Certifique-se de que o arquivo DWG foi carregado corretamente; verifique o caminho e as permissões do arquivo.  
- **Tamanho do PDF está grande:** Ative a compressão em `PdfOptions` (por exemplo, `pdfOptions.setCompress(true)`) para reduzir o tamanho do arquivo sem perder qualidade.

## Perguntas Frequentes

**Q1: O Aspose.CAD é compatível com todas as versões de arquivos DWG?**  
A1: O Aspose.CAD suporta mais de 30 versões de DWG, incluindo AutoCAD 2018 e versões anteriores.

**Q2: Posso usar o Aspose.CAD em projetos comerciais?**  
A2: Sim, uma licença comercial é necessária para uso em produção. Você pode obter uma licença [here](https://purchase.aspose.com/buy).

**Q3: Existem limitações na versão de avaliação gratuita?**  
A1: O teste impõe restrições de tamanho e recursos; consulte a documentação oficial para detalhes.

**Q4: Como posso obter suporte para o Aspose.CAD?**  
A4: Visite a comunidade [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para assistência e discussões.

**Q5: Existe uma licença temporária disponível para fins de teste?**  
A5: Sim, uma licença temporária pode ser solicitada [here](https://purchase.aspose.com/temporary-license/).

---

**Última Atualização:** 2026-05-20  
**Testado Com:** Aspose.CAD for Java 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose

## Tutoriais Relacionados

- [Exportar DWG para PDF e Converter Desenhos CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Exportar Layout DWG Específico para PDF Usando Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG para PDF ou Raster Usando Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}