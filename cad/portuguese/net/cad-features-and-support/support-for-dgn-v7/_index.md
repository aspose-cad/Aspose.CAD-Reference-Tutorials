---
title: Suporte para DGN V7 em Aspose.CAD para .NET
linktitle: Suporte para DGN V7
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore o suporte perfeito do Aspose.CAD for .NET para DGN V7. Converta arquivos DGN em imagens rasterizadas sem esforço com orientação passo a passo.
weight: 19
url: /pt/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Suporte para DGN V7 em Aspose.CAD para .NET

## Introdução

No domínio do desenvolvimento .NET, Aspose.CAD se destaca como uma biblioteca poderosa para lidar com arquivos de Design Auxiliado por Computador (CAD). Este tutorial se aprofunda em um recurso específico do Aspose.CAD for .NET – suporte para arquivos DGN V7. DGN, abreviação de Design, é um formato de arquivo amplamente utilizado no domínio CAD. Aspose.CAD simplifica o processo de trabalho com arquivos DGN V7, oferecendo aos desenvolvedores uma experiência perfeita.

## Pré-requisitos

Antes de mergulharmos na implementação, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD para .NET: Certifique-se de ter a biblioteca Aspose.CAD instalada. Você pode baixá-lo no[local na rede Internet](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: configure um ambiente de desenvolvimento .NET funcional, incluindo Visual Studio ou qualquer outro IDE preferido.

Agora que classificamos os pré-requisitos, vamos explorar como aproveitar o suporte para DGN V7 no Aspose.CAD for .NET.

## Importar namespaces

Comece importando os namespaces necessários para acessar a funcionalidade do Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o arquivo DGN

 Comece carregando um arquivo DGN existente como um`CadImage` Substituir`"Your Document Directory"` e`"Nikon_D90_Camera.dgn"` com o caminho do diretório e o nome do arquivo apropriados.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // O código para outras etapas está aqui ...
}
```

## Etapa 2: configurar opções de rasterização

 Criar uma`CadRasterizationOptions` objeto para definir e definir várias propriedades relacionadas à rasterização.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Etapa 3: definir opções de rasterização vetorial

 Criar uma`JpegOptions` objeto, pois pretendemos converter o arquivo DGN para JPEG. Atribuir o criado anteriormente`CadRasterizationOptions` objetar a isso.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Etapa 4: salve a imagem rasterizada

 Ligar para`Save` método do`CadImage` objeto de classe para exportar o arquivo DGN para uma imagem raster, neste caso, um JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Com essas etapas concluídas, o arquivo DGN é exportado com sucesso para uma imagem raster.

## Conclusão

Neste tutorial, exploramos o suporte contínuo para DGN V7 no Aspose.CAD for .NET. Seguindo o guia passo a passo, os desenvolvedores podem converter facilmente arquivos DGN em imagens raster, expandindo os recursos de seus aplicativos .NET.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com as especificações DGN V7 mais recentes?

A1: Sim, o Aspose.CAD foi projetado para lidar perfeitamente com arquivos DGN V7, garantindo compatibilidade com as especificações mais recentes.

### P2: Posso personalizar as opções de rasterização para conversão de arquivos DGN?

 A2: Absolutamente. O tutorial demonstra como criar e configurar`CadRasterizationOptions` para personalizar o processo de conversão.

### P3: Existem outros formatos de saída suportados além de JPEG?

A3: Sim, Aspose.CAD suporta vários formatos de saída. Você pode explorar a documentação para obter uma lista abrangente.

### Q4: Como posso obter suporte para consultas relacionadas ao Aspose.CAD?

 A4: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### Q5: Existe uma avaliação gratuita disponível para Aspose.CAD for .NET?

 A5: Sim, você pode acessar uma avaliação gratuita[aqui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
