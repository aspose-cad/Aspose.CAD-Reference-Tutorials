---
date: 2026-02-15
description: Aprenda a definir o tamanho da página PDF e converter CAD para PDF usando
  Aspose.CAD para Java, com dimensionamento automático de layout e exportação para
  TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Definir tamanho da página PDF – Converter CAD para PDF (Java)
url: /pt/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir Tamanho da Tela e Modo

## Introdução

Se você precisa **definir o tamanho da página PDF** ao converter desenhos CAD para PDF, está no lugar certo. Neste tutorial mostraremos como usar o Aspose.CAD for Java para definir dimensões exatas da tela, habilitar o dimensionamento automático de layout e, em seguida, exportar o resultado tanto para PDF quanto para TIFF. Seja preparando esquemas de engenharia para impressão ou gerando miniaturas para uma galeria web, controlar o tamanho da página e a resolução de saída é essencial.

## Respostas Rápidas
- **O que significa “converter CAD para PDF”?** Transformar um desenho CAD (por exemplo, DXF, DWG) em um documento PDF que pode ser visualizado em qualquer plataforma.  
- **Posso também exportar para TIFF?** Sim—use `TiffOptions` para criar imagens raster de alta resolução.  
- **Qual opção controla o tamanho da tela em Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **O que é dimensionamento automático de layout?** Uma flag (`setAutomaticLayoutsScaling(true)`) que preserva as proporções originais do layout quando o tamanho da tela é alterado.  
- **Preciso de licença para Aspose.CAD?** É necessária uma licença temporária ou permanente para uso em produção.

## Como Definir o Tamanho da Página PDF ao Converter CAD para PDF (Java)

Definir o tamanho da página PDF (ou tamanho da tela) permite que você determine as dimensões finais do documento, o que é especialmente útil quando você precisa **alterar as dimensões do PDF** para atender a padrões de impressão ou requisitos de UI. A seguir, percorremos cada passo, explicando o *porquê* de cada linha de código.

## O que é **convert CAD to PDF**?

Converter CAD para PDF significa pegar desenhos de engenharia baseados em vetor e renderizá‑los como páginas PDF, preservando linhas, camadas e geometria enquanto torna o arquivo universalmente acessível.

## Por que definir o tamanho da tela **java**?

Definir o tamanho da tela em Java permite que você especifique a resolução de saída e as dimensões da página, garantindo que o PDF ou TIFF resultante atenda aos seus requisitos de impressão ou exibição. Também oferece controle sobre o comportamento de dimensionamento, essencial para desenhos de grande formato.

## Pré‑requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos configurados:

- Aspose.CAD for Java: Garanta que a biblioteca Aspose.CAD esteja instalada no seu ambiente Java. Você pode baixá‑la [aqui](https://releases.aspose.com/cad/java/).
- Diretório de Documentos: Configure um diretório de documentos para armazenar seus arquivos CAD. Este diretório será referenciado nas etapas do tutorial.

Agora, vamos começar com o guia passo a passo.

## Importar Namespaces

Nesta etapa, importaremos os namespaces necessários para iniciar seu projeto Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Etapa 1: Importar Classes Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Neste trecho, configuramos o caminho para o diretório de recursos e carregamos um arquivo DXF usando a classe `Image` do Aspose.CAD.

## Etapa 2: Definir Propriedades **CadRasterizationOptions** (definir tamanho da tela java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Aqui, criamos uma instância de `CadRasterizationOptions` e configuramos propriedades como largura da página, altura da página e **dimensionamento automático de layout**. Este é o núcleo da **configuração do modo de tela** para sua conversão.

## Etapa 3: Criar PdfOptions e Definir VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Agora, criamos uma instância de `PdfOptions` e definimos sua propriedade `VectorRasterizationOptions` para as `CadRasterizationOptions` configuradas anteriormente.

## Etapa 4: Exportar para PDF (converter cad para pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Por fim, salvamos a imagem CAD em um arquivo PDF usando as opções especificadas, completando o processo de **converter CAD para PDF**.

## Etapa 5: Criar TiffOptions e Definir VectorRasterizationOptions (exportar cad para tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nesta etapa, configuramos uma instância de `TiffOptions` e definimos sua propriedade `VectorRasterizationOptions`.

## Etapa 6: Exportar para TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Por fim, salvamos a imagem CAD em um arquivo TIFF usando as opções especificadas, demonstrando como **exportar CAD para TIFF** após configurar o tamanho da tela.

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| PDF de saída está em branco | `setNoScaling(true)` desabilita a renderização para alguns desenhos | Remova `setNoScaling(true)` ou defina como `false`. |
| Resolução do TIFF parece baixa | Largura/altura da página muito pequena | Aumente os valores de `setPageWidth` / `setPageHeight`. |
| Layout parece distorcido | Dimensionamento automático de layout desativado | Certifique‑se de que `setAutomaticLayoutsScaling(true)` esteja habilitado. |

## Por que Ajustar o Tamanho da Tela e DPI?

Alterar o tamanho da tela influencia diretamente a resolução de rasterização da saída. Se precisar **aumentar a resolução do TIFF**, basta elevar os valores de `setPageWidth` / `setPageHeight` ou chamar `rasterizationOptions.setResolution(300)` antes de criar o `TiffOptions`. Isso fornece imagens raster de alta qualidade adequadas para impressão ou inspeção detalhada.

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD for Java com outros frameworks Java?

A1: Sim, o Aspose.CAD foi projetado para integrar‑se perfeitamente com diversos frameworks Java.

### Q2: Existe uma licença temporária disponível para Aspose.CAD?

A2: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q3: Onde posso obter suporte da comunidade para Aspose.CAD?

A3: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

### Q4: Posso experimentar o Aspose.CAD gratuitamente?

A4: Absolutamente! Obtenha uma avaliação gratuita [aqui](https://releases.aspose.com/).

### Q5: Como compro Aspose.CAD for Java?

A5: Compre o produto [aqui](https://purchase.aspose.com/buy).

**Perguntas e Respostas Adicionais**

**P: O tamanho da tela afeta a qualidade vetorial no PDF?**  
R: Não. O tamanho da tela controla as dimensões da página; os dados vetoriais permanecem independentes de resolução, garantindo renderização nítida em qualquer nível de zoom.

**P: Posso definir um DPI diferente para a saída TIFF?**  
R: Sim. Ajuste `rasterizationOptions.setResolution(dpiValue)` antes de criar `TiffOptions`.

**P: Como posso **alterar as dimensões do PDF** para um PDF existente sem re‑renderizar o CAD?**  
R: Use o Aspose.PDF para carregar o PDF gerado e chame `pdf.getPages().setPageSize(PageSize.A4)` ou um tamanho personalizado.

**P: Qual a melhor forma de **converter dxf para pdf** preservando camadas?**  
R: Mantenha `setAutomaticLayoutsScaling(true)` e evite `setNoScaling(true)`; isso preserva a visibilidade das camadas e a fidelidade do layout.

## Conclusão

Parabéns! Você concluiu com sucesso a **conversão de CAD para PDF** e a **exportação de CAD para TIFF** enquanto **definia o tamanho da tela java**, habilitando **dimensionamento automático de layout**, e aprendeu a **configurar o modo de tela** para saídas de alta qualidade. Este tutorial fornece uma base sólida para seus projetos de conversão CAD. Explore mais recursos e possibilidades na [documentação do Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Última atualização:** 2026-02-15  
**Testado com:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}