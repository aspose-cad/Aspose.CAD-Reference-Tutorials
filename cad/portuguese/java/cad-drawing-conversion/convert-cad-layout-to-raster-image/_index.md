---
date: 2025-12-18
description: Aprenda a converter DWG para PNG e outros formatos de imagem raster com
  o Aspose.CAD para Java. Exporte CAD como PNG com resultados de alta qualidade.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Converter DWG para PNG e Outros Formatos Raster Usando Aspose.CAD para Java
url: /pt/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DWG para PNG e Outros Formatos Raster usando Aspose.CAD para Java

## Introdução

Converter DWG para PNG (ou outros formatos de imagem raster) é uma necessidade comum quando você precisa compartilhar desenhos CAD com colegas que não possuem um visualizador CAD, incorporar designs em documentação ou gerar miniaturas para galerias web. Aspose.CAD para Java torna essa conversão simples, seja trabalhando com um arquivo de desenho completo ou apenas com um layout específico. Neste tutorial vamos percorrer os passos exatos para **converter um layout CAD em uma imagem raster** — a mesma técnica que você pode aplicar para gerar saídas PNG, JPEG, TIFF ou PDF.

## Respostas Rápidas
- **Qual biblioteca lida com DWG para PNG?** Aspose.CAD para Java  
- **Quais formatos podem ser exportados?** PNG, JPEG, TIFF, PDF, BMP e mais  
- **Preciso de licença para testes?** Uma avaliação gratuita funciona para desenvolvimento; uma licença é necessária para produção  
- **Posso escolher um layout específico?** Sim, use `setLayouts` para direcionar “Model”, “Layout1”, etc.  
- **É possível obter saída em alta resolução?** Absolutamente—ajuste `setPageWidth` e `setPageHeight` para controlar DPI  

## O que é “convert dwg to png”?

A expressão “convert dwg to png” descreve o processo de pegar um arquivo DWG baseado em vetor (o formato nativo de muitas aplicações CAD) e rasterizá‑lo em uma imagem PNG baseada em pixels. Imagens raster são ideais para exibição na web, compartilhamento por e‑mail e integração em softwares que não são CAD.

## Por que exportar CAD como PNG (ou outros formatos raster)?

- **Compatibilidade Universal:** PNG e JPEG são suportados por praticamente todos os visualizadores de imagem e navegadores.  
- **Carregamento Rápido:** Imagens raster carregam instantaneamente comparado a abrir um arquivo DWG pesado.  
- **Facilidade de Incorporação:** Insira PNGs diretamente no Word, PowerPoint ou HTML sem plugins adicionais.  
- **Aparência Consistente:** Você controla resolução, fundo e layout, garantindo que todos os interessados vejam o mesmo visual.  

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

1. **Ambiente de Desenvolvimento Java** – JDK 8 ou mais recente instalado e configurado.  
2. **Aspose.CAD para Java** – Baixe o JAR mais recente na [documentação do Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Importar Namespaces

Primeiro, importe as classes que você precisará. Essas importações dão acesso ao carregamento de imagens, opções de rasterização e configurações de saída TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Dica:** Se você pretende exportar para PNG em vez de TIFF, substitua `TiffOptions` por `PngOptions` (encontrado em `com.aspose.cad.imageoptions.PngOptions`).

## Guia Passo a Passo

### Etapa 1: Configurar o Diretório de Recursos

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Substitua `"Your Document Directory"` pelo caminho absoluto onde seus arquivos CAD estão armazenados.

### Etapa 2: Carregar o Arquivo CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Você pode carregar qualquer formato suportado (DWG, DXF, DGN, etc.). Esta é a **parte de como converter cad** — basta apontar para o arquivo e deixar o Aspose fazer o parsing.

### Etapa 3: Configurar Opções de Rasterização

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` controlam a resolução de saída (valores maiores = DPI mais alto).  
- `setLayouts` permite **converter cad para raster** para layouts específicos; omita para rasterizar o desenho completo.

### Etapa 4: Definir Opções de Imagem

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Se preferir PNG, instancie `PngOptions` em vez de `TiffOptions`. É aqui que você **exporta cad como png**.

### Etapa 5: Salvar a Imagem Resultante

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Altere a extensão do arquivo para `.png` (e o objeto de opções para `PngOptions`) para **salvar CAD como JPEG/PNG**.

> **Erro Comum:** Esquecer de combinar a extensão do arquivo com a classe de opções causará um `UnsupportedFormatException`. Sempre mantenha-os sincronizados.

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|---------|
| **Imagem de saída em branco** | Verifique se os nomes dos layouts em `setLayouts` correspondem exatamente aos presentes no arquivo CAD de origem. |
| **PNG de baixa resolução** | Aumente `setPageWidth` / `setPageHeight` ou defina `setResolution` nas opções de rasterização. |
| **Versão DWG não suportada** | Certifique‑se de estar usando a versão mais recente do Aspose.CAD; versões antigas podem não suportar lançamentos mais recentes do DWG. |
| **Erros de memória em arquivos grandes** | Processar páginas uma de cada vez ou aumentar o heap da JVM (`-Xmx2g`). |

## Perguntas Frequentes

**P: O Aspose.CAD é compatível com diferentes formatos de arquivo CAD?**  
R: Sim, ele suporta DWG, DXF, DGN e muitos outros.

**P: Posso personalizar a resolução da imagem raster de saída?**  
R: Absolutamente. Ajuste `setPageWidth`, `setPageHeight` ou `setResolution` em `CadRasterizationOptions`.

**P: Como posso converter vários layouts CAD em uma única execução?**  
R: Forneça um array com todos os nomes de layout para `setLayouts`, por exemplo, `new String[]{"Model","Layout1","Layout2"}`.

**P: Existem formatos de saída além do TIFF suportados?**  
R: Sim—PNG, JPEG, BMP, PDF e mais estão disponíveis através de suas respectivas classes `*Options`.

**P: Onde posso obter ajuda ou compartilhar minha experiência com o Aspose.CAD?**  
R: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e assistência oficial.

## Conclusão

Seguindo estes passos você pode **converter DWG para PNG**, **exportar CAD como PNG**, **salvar CAD como JPEG**, ou gerar qualquer outro formato raster que precisar. Aspose.CAD para Java cuida da parte pesada, permitindo que você se concentre em integrar imagens de alta qualidade em suas aplicações, documentação ou portais web.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}