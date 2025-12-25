---
date: 2025-12-25
description: Aprenda a exportar DWG para BMP usando Aspose.CAD para Java. Este guia
  passo a passo mostra como ajustar o tamanho do desenho CAD e converter CAD para
  BMP de forma eficiente.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Exportar DWG para BMP – Ajustar o tamanho do CAD usando o tipo de unidade (Java)
url: /pt/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG para BMP – Ajustando o Tamanho do Desenho CAD Usando o Tipo de Unidade com Aspose.CAD para Java

## Introdução

Quando você precisa **exportar DWG para BMP**, controlar o tamanho de saída e a unidade de medida é essencial para o processamento subsequente ou impressão. Neste tutorial você aprenderá como ajustar o tamanho do desenho CAD e converter CAD para BMP com Aspose.CAD para Java, usando a propriedade `UnitType` para definir a unidade de medida. As etapas são explicadas em linguagem simples para que você possa acompanhar mesmo sendo novo na biblioteca.

## Respostas Rápidas
- **O que significa “exportar DWG para BMP”?** Conversão de um desenho DWG em uma imagem raster BMP.  
- **Qual propriedade controla o tamanho de saída?** `CadRasterizationOptions.setUnitType()` define a unidade (por exemplo, centímetro).  
- **Preciso de uma licença para executar o código?** Um teste gratuito funciona para avaliação; uma licença é necessária para produção.  
- **Posso escolher outros layouts?** Sim, use `setLayouts()` para especificar layouts de modelo ou espaço de papel.  
- **Quais formatos de saída são suportados?** Além de BMP, você pode exportar para PNG, JPEG, TIFF, etc., alterando a classe de opções.

## O que é **exportar DWG para BMP**?

Exportar DWG para BMP significa rasterizar um arquivo DWG baseado em vetor em uma imagem bitmap (BMP). Isso é útil quando você precisa de uma representação pixel‑perfeita para sistemas legados, pipelines de processamento de imagem ou cenários de exibição simples.

## Por que ajustar o tamanho do desenho CAD com **Tipo de Unidade**?

Definir o tipo de unidade permite controlar as dimensões físicas da imagem exportada sem calcular manualmente fatores de escala. Isso garante que o bitmap corresponda a medições do mundo real (por exemplo, centímetros), o que é crucial para desenhos de engenharia e documentação impressa.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos:

- **Ambiente de Desenvolvimento Java** – Um JDK funcional (8 ou superior) e uma IDE ou ferramenta de build (Maven/Gradle).  
- **Biblioteca Aspose.CAD para Java** – Baixe e integre a biblioteca Aspose.CAD ao seu projeto Java. Você pode obter a biblioteca [aqui](https://releases.aspose.com/cad/java/).

## Importar Namespaces

No seu código Java, inclua os namespaces necessários para acessar as funcionalidades do Aspose.CAD. Adicione as seguintes importações:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Agora, vamos dividir o processo de ajuste do tamanho do desenho CAD usando o tipo de unidade em etapas manejáveis:

## Etapa 1: Definir Diretório de Dados

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Defina o caminho para o diretório onde seus arquivos CAD estão localizados.

## Etapa 2: Carregar Desenho CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Carregue o desenho CAD usando a classe `Image` do Aspose.CAD.

## Etapa 3: Criar Opções BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instancie a classe `BmpOptions` para exportar o layout CAD para o formato BMP.

## Etapa 4: Configurar Opções de Rasterização

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Crie uma instância de `CadRasterizationOptions` e associe-a ao `BmpOptions` para rasterização vetorial.

## Etapa 5: Definir Tipo de Unidade

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Especifique o tipo de unidade desejado para o desenho CAD. Neste exemplo, definimos para **Centimeter**, o que influencia diretamente o tamanho da imagem exportada ao **ajustar o tamanho do desenho CAD**.

## Etapa 6: Definir Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Defina os layouts que serão considerados durante a exportação. Neste caso, selecionamos o layout **"Model"**, mas você pode mudar para layouts de espaço de papel, se necessário.

## Etapa 7: Exportar para BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Por fim, salve o desenho CAD modificado no formato BMP. Esta etapa completa o fluxo de **exportar DWG para BMP** enquanto preserva os ajustes de tamanho que você configurou.

## Problemas Comuns e Soluções

| Problema | Motivo | Correção |
|----------|--------|----------|
| **A imagem de saída está muito pequena** | Tipo de unidade não definido ou padrão (pixel) usado | Chame `setUnitType()` com a medida desejada (por exemplo, `UnitType.Centimeter`). |
| **Layout exportado incorreto** | Erro de digitação no nome do layout | Verifique os nomes dos layouts com um visualizador CAD; use a string exata em `setLayouts()`. |
| **Exceção de licença** | Executando sem uma licença válida em produção | Aplique uma licença temporária ou permanente conforme descrito no FAQ. |

## Perguntas Frequentes (Estendidas)

**Q: Posso usar Aspose.CAD para Java com outras linguagens de programação?**  
A: O Aspose.CAD suporta principalmente Java, mas há versões disponíveis para outras linguagens como .NET.

**Q: Existem opções de licenciamento para o Aspose.CAD?**  
A: Sim, você pode explorar as opções de licenciamento e adquirir o Aspose.CAD [aqui](https://purchase.aspose.com/buy).

**Q: Há uma versão de teste gratuita disponível para o Aspose.CAD?**  
A: Certamente, você pode acessar um teste gratuito [aqui](https://releases.aspose.com/).

**Q: Como posso obter suporte para o Aspose.CAD para Java?**  
A: Visite o fórum do Aspose.CAD [aqui](https://forum.aspose.com/c/cad/19) para suporte abrangente.

**Q: Posso obter uma licença temporária para o Aspose.CAD?**  
A: Sim, você pode adquirir uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

**Última atualização:** 2025-12-25  
**Testado com:** Aspose.CAD para Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}