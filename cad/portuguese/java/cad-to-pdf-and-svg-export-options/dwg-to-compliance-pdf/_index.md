---
title: DWG para PDF de conformidade usando Aspose.CAD para Java
linktitle: DWG para PDF de conformidade
second_title: API Java Aspose.CAD
description: Converta facilmente desenhos DWG em arquivos compatíveis com PDF/A1a e PDF/A1b usando Aspose.CAD para Java. Simplifique seu fluxo de trabalho com precisão e facilidade.
weight: 11
url: /pt/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG para PDF de conformidade usando Aspose.CAD para Java

## Introdução

No mundo em constante evolução do design digital, a necessidade de converter desenhos DWG em formatos PDF compatíveis é crucial para uma colaboração perfeita e documentação padronizada. O Aspose.CAD for Java surge como uma ferramenta poderosa, oferecendo eficiência e precisão neste processo. Neste tutorial, exploraremos como utilizar Aspose.CAD for Java para converter facilmente arquivos DWG em PDFs compatíveis, garantindo a adesão aos padrões PDF/A1a e PDF/A1b.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java funcional configurado em seu sistema.
-  Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD para Java do[Link para Download](https://releases.aspose.com/cad/java/).
- Diretório de documentos: Crie um diretório para armazenar seus desenhos DWG.

## Importar namespaces

Em seu projeto Java, importe os namespaces necessários para acessar as funcionalidades do Aspose.CAD. Adicione as seguintes linhas no início do seu arquivo Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Etapa 1: definir o diretório de recursos

Defina o caminho para o diretório de recursos onde os desenhos DWG estão armazenados.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Etapa 2: carregar o arquivo DWG

Carregue o arquivo DWG usando a biblioteca Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Passo 3: Criar Opções de PDF

Crie uma instância de PdfOptions e defina as opções de rasterização vetorial.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Etapa 4: definir as opções principais do PDF

Defina as opções principais do PDF, especificando o padrão de conformidade (PDF/A1a ou PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Passo 5: Salvar PDF com Conformidade A1a

Salve o arquivo PDF com conformidade A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Etapa 6: Alterar conformidade para A1b

Altere a conformidade para PDF/A1b e salve o PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Repita essas etapas para cada arquivo DWG que deseja converter.

## Conclusão

Concluindo, Aspose.CAD for Java fornece uma solução robusta para converter arquivos DWG em PDFs compatíveis. Seguindo este guia passo a passo, você pode agilizar o processo de conversão e garantir que seus documentos estejam de acordo com os padrões do setor.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todas as versões de arquivos DWG?

 A1: Aspose.CAD suporta várias versões de arquivos DWG, incluindo os mais recentes. Consulte o[documentação](https://reference.aspose.com/cad/java/) para obter informações detalhadas de compatibilidade.

### Q2: Posso personalizar as configurações de saída de PDF usando Aspose.CAD?

A2: Com certeza! Aspose.CAD oferece uma gama de opções de personalização, permitindo adaptar a saída do PDF às suas necessidades específicas.

### Q3: Há uma licença temporária disponível para Aspose.CAD?

 A3: Sim, você pode obter uma licença temporária para fins de teste em[esse link](https://purchase.aspose.com/temporary-license/).

### Q4: Onde posso buscar suporte ou interagir com a comunidade do Aspose.CAD?

 A4: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### Q5: Posso experimentar o Aspose.CAD gratuitamente antes de fazer uma compra?

 A5: Certamente! Baixe a versão de teste gratuita em[aqui](https://releases.aspose.com/) explorar as capacidades antes de tomar uma decisão.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
