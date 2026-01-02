---
date: 2026-01-02
description: Aprenda como exportar DWG como PDF, habilitar linhas ocultas e converter
  DWG para PDF com Aspose.CAD para Java neste tutorial passo a passo.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Exportar DWG como PDF com linhas ocultas – Aspose.CAD para Java
url: /pt/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG como PDF com Linhas Ocultas – Aspose.CAD para Java

## Introdução

Neste tutorial você aprenderá como **exportar DWG como PDF** preservando linhas ocultas usando Aspose.CAD para Java. Seja para **converter DWG para PDF**, gerar um guia no estilo **tutorial de dwg para pdf**, ou simplesmente **salvar DWG como PDF** com suporte a linhas ocultas, vamos guiá-lo passo a passo. Ao final, você terá uma solução pronta para uso que pode ser inserida em qualquer projeto Java.

## Respostas Rápidas
- **O que este tutorial cobre?** Habilitar a renderização de linhas ocultas ao exportar DWG para PDF com Aspose.CAD para Java.  
- **Qual operação principal é realizada?** `export dwg as pdf`.  
- **Preciso de uma licença?** Uma versão de avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Quais são os pré-requisitos?** Ambiente de desenvolvimento Java, biblioteca Aspose.CAD para Java e arquivos DWG.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para uma configuração básica.

## O que é “export dwg as pdf”?
Exportar um arquivo DWG para PDF converte o desenho CAD baseado em vetores para um formato de documento portátil, preservando camadas, tipos de linha e renderização opcional de linhas ocultas. Isso facilita o compartilhamento de projetos CAD com partes interessadas que podem não ter software CAD.

## Por que habilitar linhas ocultas ao exportar?
Linhas ocultas fornecem uma representação visual mais clara de modelos 3D complexos em uma página 2‑D, garantindo que apenas as arestas visíveis sejam destacadas. Isso melhora a legibilidade e costuma ser exigido em documentação de engenharia.

## Pré-requisitos

1. **Aspose.CAD para Java** – baixe a biblioteca no site oficial [aqui](https://releases.aspose.com/cad/java/).  
2. **Arquivos DWG** – mantenha os desenhos DWG de origem armazenados em um diretório conhecido.  
3. **Ambiente de desenvolvimento Java** – JDK 8+ e sua IDE preferida (Eclipse, IntelliJ, etc.).  

Agora que você está configurado, vamos mergulhar no código.

## Importar Namespaces

Comece importando as classes necessárias para trabalhar com imagens CAD e opções de PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Etapa 1: Configurar Seu Projeto

Crie um projeto Java e adicione o JAR do Aspose.CAD ao seu caminho de compilação. Em seguida, defina o diretório que contém seus arquivos DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Dica profissional:** Use um caminho absoluto ou configure um caminho relativo com base na pasta de recursos do seu projeto.

## Etapa 2: Carregar Arquivo DWG

Carregue o arquivo DWG de origem em um objeto `CadImage` para que você possa manipulá-lo.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Etapa 3: Configurar Opções de Rasterização

Selecione as camadas que deseja incluir e defina o tamanho da página para corresponder ao desenho original. É aqui que habilitamos a renderização de linhas ocultas especificando o layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Etapa 4: Definir Opções de PDF

Instrua o Aspose.CAD a rasterizar os dados vetoriais em um PDF, usando o layout “Model” para manter as linhas ocultas ocultas.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Etapa 5: Salvar o Resultado

Finalmente, exporte o DWG como um arquivo PDF. As linhas ocultas serão respeitadas de acordo com o layout que você definiu.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Erro Comum:** Esquecer de definir o layout como `"Model"` fará com que todas as linhas (incluindo as ocultas) apareçam sólidas no PDF.

## Conclusão

Agora você tem um método completo e pronto para produção para **exportar DWG como PDF** com suporte a linhas ocultas usando Aspose.CAD para Java. Essa abordagem pode ser integrada em ferramentas de processamento em lote, serviços web ou aplicativos desktop para automatizar a conversão de CAD para PDF.

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD para Java com outros formatos de arquivo CAD?
A1: Sim, o Aspose.CAD suporta vários formatos CAD como DWG, DXF, DWF e mais.

### Q2: Existe uma versão de avaliação gratuita disponível para Aspose.CAD para Java?
A2: Sim, você pode encontrar a versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q3: Como obtenho suporte para Aspose.CAD para Java?
A3: Visite o fórum Aspose.CAD [aqui](https://forum.aspose.com/c/cad/19) para suporte da comunidade.

### Q4: Onde posso encontrar documentação detalhada para Aspose.CAD para Java?
A4: Consulte a documentação [aqui](https://reference.aspose.com/cad/java/).

### Q5: Posso comprar uma licença temporária para Aspose.CAD para Java?
A5: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q6: Este método também funciona para converter DWG para PDF em um ambiente de servidor sem interface?
A6: Absolutamente. Como o código usa apenas a API Aspose.CAD, ele roda sem dependências de UI, sendo ideal para automação no lado do servidor.

---

**Última atualização:** 2026-01-02  
**Testado com:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}