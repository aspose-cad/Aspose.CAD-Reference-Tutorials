---
date: 2025-12-21
description: Converta IFC para PNG sem esforço com Aspose.CAD para Java. Siga nosso
  tutorial passo a passo.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Converter IFC para PNG com Aspose.CAD para Java
url: /pt/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter IFC para PNG com Aspose.CAD para Java

## Introdução

Neste tutorial você aprenderá **como converter IFC para PNG** usando a poderosa biblioteca Aspose.CAD para Java. Seja você quem está construindo um visualizador BIM, gerando miniaturas para um portal de construção ou automatizando pipelines de documentação, converter arquivos IFC (Industry Foundation Classes) para imagens rasterizadas é uma necessidade comum. Vamos percorrer cada passo, explicar o raciocínio por trás das configurações e dar dicas para obter os melhores resultados visuais.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.CAD para Java (versão de avaliação gratuita disponível).  
- **Versões de IFC suportadas?** A maioria dos arquivos IFC 2x3 e IFC4 são suportados.  
- **Tempo típico de conversão?** Alguns segundos para modelos padrão; depende do tamanho do arquivo.  
- **Preciso de licença?** Uma licença temporária é necessária para uso em produção.  
- **Posso personalizar o tamanho da imagem?** Sim – use `CadRasterizationOptions` para definir largura e altura.

## O que significa “converter IFC para PNG”?
Converter IFC para PNG significa rasterizar um modelo 3‑D de construção (IFC) em uma imagem bitmap 2‑D (PNG). Esse processo achata a geometria, aplica estilos visuais padrão e produz uma imagem portátil que pode ser exibida em navegadores, relatórios ou aplicativos móveis sem a necessidade de um visualizador CAD.

## Por que usar Aspose.CAD para Java?
- **Sem software CAD externo** – API pura em Java, funciona em qualquer plataforma.  
- **Renderização de alta fidelidade** – preserva espessuras de linha, cores e camadas.  
- **Controle total** – opções de rasterização permitem definir resolução, fundo e mais.  
- **Licenciamento fácil** – licenças de avaliação e temporárias simplificam a avaliação.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

- **Biblioteca Aspose.CAD** – faça o download e instale a partir do [link de download](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – versão 8 ou superior.  
- **Uma pasta** que contenha o arquivo IFC que você deseja converter.

## Importar namespaces

No seu projeto Java, importe as classes necessárias:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Guia passo a passo

### Passo 1: Carregar o arquivo IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Aqui carregamos o arquivo IFC de origem em um objeto `IfcImage`. O Aspose.CAD analisa automaticamente a estrutura IFC e a prepara para rasterização.

### Passo 2: Definir opções vetoriais (de rasterização)

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` controla como a geometria 3‑D é achatada. Ajuste `PageWidth` e `PageHeight` para corresponder à resolução PNG desejada. Valores maiores produzem imagens com mais detalhes, mas aumentam o uso de memória.

### Passo 3: Configurar as opções de exportação PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` indica ao Aspose.CAD que o arquivo de saída será PNG e vincula as configurações de rasterização definidas no passo anterior.

### Passo 4: Salvar a imagem como PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

O método `save` grava a imagem rasterizada no disco. Após a execução desta linha, você encontrará `example.png` no mesmo diretório do seu arquivo IFC de origem.

## Problemas comuns e soluções

| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| **Saída PNG em branco** | Opções de rasterização com largura/altura definidas como 0 ou muito pequenas. | Garanta que `PageWidth` e `PageHeight` sejam inteiros positivos (por exemplo, 1500). |
| **Camadas ou cores ausentes** | A visualização padrão pode ocultar certas camadas. | Use `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` ou ajuste a visibilidade das camadas via API (se necessário). |
| **Erros de falta de memória** para arquivos IFC muito grandes | Resolução muito alta consome muita RAM. | Reduza a resolução ou processe o modelo em seções. |

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todas as versões de arquivos IFC?

A1: O Aspose.CAD suporta várias versões de arquivos IFC. Consulte a [documentação](https://reference.aspose.com/cad/java/) para detalhes de compatibilidade.

### Q2: Posso personalizar ainda mais as opções de rasterização?

A2: Absolutamente! Explore a [documentação](https://reference.aspose.com/cad/java/) para opções avançadas de personalização.

### Q3: Existe uma versão de avaliação disponível?

A3: Sim, você pode acessar a versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Como obtenho licenciamento temporário para o Aspose.CAD?

A4: Obtenha uma licença temporária neste [link](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso buscar ajuda ou discutir problemas?

A5: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade.

## Perguntas frequentes adicionais

**P: Posso converter vários arquivos IFC em lote?**  
R: Sim. Envolva a lógica de carregamento e salvamento dentro de um loop que itere sobre uma lista de caminhos de arquivo.

**P: Como altero a cor de fundo do PNG?**  
R: Defina `vectorOptions.setBackgroundColor(Color.getWhite())` (ou qualquer `java.awt.Color`) antes de criar `PngOptions`.

**P: É possível exportar para outros formatos raster, como JPEG ou BMP?**  
R: Absolutamente. Substitua `PngOptions` por `JpegOptions` ou `BmpOptions` e ajuste as configurações específicas do formato.

**P: Preciso liberar recursos após a conversão?**  
R: Chame `cadImage.dispose()` quando terminar para liberar a memória nativa.

---

**Última atualização:** 2025-12-21  
**Testado com:** Aspose.CAD para Java 24.12 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}