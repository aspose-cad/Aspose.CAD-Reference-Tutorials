---
date: 2026-03-02
description: Desbloqueie o potencial do Aspose.CAD para Java. Exporte objetos OLE
  sem esforço e **salve CAD como PNG**. Baixe agora para uma gestão de dados CAD perfeita.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Salvar CAD como PNG – Exportar objetos OLE usando Aspose.CAD para Java
url: /pt/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar CAD como PNG – Exportar objetos OLE usando Aspose.CAD para Java

## Introdução

No mundo dinâmico do Computer-Aided Design (CAD), gerenciar e extrair objetos OLE (Object Linking and Embedding) de forma eficiente — e poder **salvar CAD como PNG** — é crucial para fluxos de trabalho posteriores, como relatórios, visualização na web ou arquivamento. Aspose.CAD para Java oferece uma solução poderosa, orientada a código, que permite tanto exportar objetos OLE quanto converter desenhos CAD em imagens PNG de alta qualidade em apenas algumas linhas de código.

## Respostas Rápidas
- **O que o Aspose.CAD faz?** Ele lê, manipula e converte arquivos CAD (DWG, DXF, DGN, etc.) sem a necessidade de software CAD nativo.  
- **Posso salvar CAD como PNG?** Sim — use o `PngOptions` juntamente com `CadRasterizationOptions` para rasterizar qualquer layout.  
- **Como exportar objetos OLE?** Carregue o arquivo CAD com `Image.load` e salve cada layout que contém OLE como PNG.  
- **Preciso de uma licença?** Um teste gratuito está disponível; uma licença comercial remove as limitações de avaliação.  
- **Qual versão do Java é necessária?** Java 8 ou superior é totalmente suportado.

## O que é **salvar CAD como PNG**?
Salvar CAD como PNG significa rasterizar desenhos CAD baseados em vetor em uma imagem PNG baseada em pixels. Essa conversão é útil quando você precisa de um formato leve e universalmente visualizável para páginas da web, aplicativos móveis ou documentação.

## Por que usar Aspose.CAD para Java para **converter CAD em PNG**?
- **Nenhuma instalação de CAD necessária** – a biblioteca funciona totalmente em Java.  
- **Preserva a fidelidade do layout** – você pode escolher layouts específicos, controlar DPI e manter a qualidade das linhas.  
- **Processamento em lote** – itere sobre vários arquivos com um simples loop.  
- **Exportar objetos OLE** – o conteúdo OLE incorporado em arquivos DWG/DXF é renderizado automaticamente na saída PNG.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos configurados:

- **Ambiente Java** – Certifique‑se de que você tem um ambiente de desenvolvimento Java configurado na sua máquina.  
- **Aspose.CAD para Java** – Baixe e instale a biblioteca Aspose.CAD para Java. Você pode encontrar a biblioteca no [download link](https://releases.aspose.com/cad/java/).  
- **Arquivos CAD** – Prepare os arquivos CAD contendo objetos OLE que você deseja exportar.

## Importar Namespaces

Para começar, importe os namespaces necessários ao seu projeto Java. Esses namespaces fornecem as classes e funcionalidades essenciais para trabalhar com arquivos CAD usando Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Agora, vamos dividir o processo de exportação de objetos OLE a partir de CAD em várias etapas:

## Como **salvar CAD como PNG** e exportar objetos OLE

### Etapa 1: Defina seu Diretório de Documentos

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Certifique‑se de substituir `"Your Document Directory"` pelo caminho do diretório que contém seus arquivos CAD.

### Etapa 2: Defina os Nomes dos Arquivos CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Especifique os nomes dos arquivos CAD que você deseja processar no array `files`.

### Etapa 3: Defina as Opções de Exportação PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configure as opções de exportação PNG, incluindo rasterização vetorial e configurações de layout. Essas opções permitem que você **converta CAD em PNG** com a qualidade desejada.

### Etapa 4: Iterar pelos Arquivos CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Itere por cada arquivo CAD especificado, carregue‑o usando Aspose.CAD e salve os objetos OLE como imagens PNG. Este loop demonstra uma maneira simples de **converter DWG em PNG** em massa.

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|----------|
| **Saída PNG em branco** | Incompatibilidade do nome do layout | Verifique se o nome do layout (`"Layout1"`) existe no DWG de origem. |
| **Gráficos OLE ausentes** | Objetos OLE estão armazenados em um layout diferente | Inclua todos os layouts relevantes em `rasterizationOptions.setLayouts(...)`. |
| **Erro de falta de memória em arquivos grandes** | Configurações de DPI altas | Reduza o DPI via `rasterizationOptions.setResolution(...)` ou processe os arquivos um de cada vez. |

## Perguntas Frequentes

**Q: O Aspose.CAD é compatível com todos os formatos de arquivos CAD?**  
A: O Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF e DGN. Consulte a [documentação](https://reference.aspose.com/cad/java/) para a lista completa.

**Q: Posso personalizar as configurações de exportação para objetos OLE?**  
A: Sim, o Aspose.CAD oferece opções extensas para personalizar as configurações de exportação, permitindo adaptar a saída às suas necessidades específicas.

**Q: Existe uma versão de avaliação gratuita disponível para o Aspose.CAD?**  
A: Sim, você pode explorar as capacidades do Aspose.CAD obtendo uma avaliação gratuita [aqui](https://releases.aspose.com/).

**Q: Onde posso obter suporte da comunidade para o Aspose.CAD?**  
A: Junte‑se à comunidade Aspose.CAD no [forum](https://forum.aspose.com/c/cad/19) para buscar assistência e compartilhar suas experiências.

**Q: Como posso comprar uma licença para o Aspose.CAD?**  
A: Visite a [página de compra](https://purchase.aspose.com/buy) para adquirir uma licença que atenda às suas necessidades de desenvolvimento.

## Conclusão

Com esses passos simples, porém poderosos, você pode **salvar CAD como PNG** enquanto exporta objetos OLE de arquivos CAD usando Aspose.CAD para Java. Esta ferramenta versátil capacita desenvolvedores a gerenciar dados CAD de forma eficiente, abrindo novas possibilidades no desenvolvimento de aplicações CAD e fluxos de trabalho baseados em imagens.

---

**Última atualização:** 2026-03-02  
**Testado com:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}