---
title: Exporte objetos OLE de CAD usando Aspose.CAD para Java
linktitle: Exportar objetos OLE do CAD
second_title: API Java Aspose.CAD
description: Desbloqueie o potencial do Aspose.CAD para Java. Exporte facilmente objetos OLE de arquivos CAD. Baixe agora para gerenciamento contínuo de dados CAD.
type: docs
weight: 10
url: /pt/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## Introdução

No mundo dinâmico do Computer-Aided Design (CAD), gerenciar e extrair objetos OLE (Object Linking and Embedding) de forma eficiente é crucial. Aspose.CAD for Java fornece uma solução poderosa para exportar objetos OLE de arquivos CAD. Este guia passo a passo orientará você durante o processo, garantindo que você aproveite todo o potencial desta ferramenta.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Ambiente Java: Certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.
-  Aspose.CAD para Java: Baixe e instale a biblioteca Aspose.CAD para Java. Você pode encontrar a biblioteca no[Link para Download](https://releases.aspose.com/cad/java/).
- Arquivos CAD: Prepare os arquivos CAD contendo objetos OLE que você deseja exportar.

## Importar namespaces

Para começar, importe os namespaces necessários para o seu projeto Java. Esses namespaces fornecem as classes e funcionalidades essenciais necessárias para trabalhar com arquivos CAD usando Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Agora, vamos dividir o processo de exportação de objetos OLE do CAD em várias etapas:

## Etapa 1: defina seu diretório de documentos

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Certifique-se de substituir “Seu diretório de documentos” pelo caminho para o diretório que contém seus arquivos CAD.

## Etapa 2: definir nomes de arquivos CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Especifique os nomes dos arquivos CAD que você deseja processar no`files` variedade.

## Etapa 3: definir opções de exportação PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configure as opções de exportação de PNG, incluindo rasterização vetorial e configurações de layout.

## Etapa 4: iterar por meio de arquivos CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Itere cada arquivo CAD especificado, carregue-o usando Aspose.CAD e salve os objetos OLE como imagens PNG.

## Conclusão

Com essas etapas simples, mas poderosas, você pode exportar perfeitamente objetos OLE de arquivos CAD usando Aspose.CAD for Java. Esta ferramenta versátil permite que os desenvolvedores gerenciem dados CAD de forma eficiente, abrindo novas possibilidades no desenvolvimento de aplicações CAD.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

 A1: Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF e DGN. Consulte o[documentação](https://reference.aspose.com/cad/java/) para a lista completa.

### P2: Posso personalizar as configurações de exportação para objetos OLE?

A2: Sim, o Aspose.CAD oferece amplas opções para personalizar as configurações de exportação, permitindo que você personalize a saída de acordo com seus requisitos específicos.

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD?

 A3: Sim, você pode explorar os recursos do Aspose.CAD obtendo uma avaliação gratuita em[aqui](https://releases.aspose.com/).

### Q4: Onde posso obter suporte da comunidade para Aspose.CAD?

 A4: Junte-se à comunidade Aspose.CAD no[fórum](https://forum.aspose.com/c/cad/19) para buscar ajuda e compartilhar suas experiências.

### Q5: Como posso adquirir uma licença para Aspose.CAD?

A5: Visite o[página de compra](https://purchase.aspose.com/buy) para adquirir uma licença que atenda às suas necessidades de desenvolvimento.