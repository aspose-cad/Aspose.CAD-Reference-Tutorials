---
title: Converter layouts em imagem raster no Aspose.CAD para .NET
linktitle: Converter layouts em imagem raster
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Converta facilmente layouts CAD em imagens raster usando Aspose.CAD for .NET. Aprimore seu desenvolvimento com poderosos recursos de manipulação de CAD.
type: docs
weight: 12
url: /pt/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Introdução

Você deseja converter facilmente layouts em imagens raster em seus aplicativos .NET? Não procure mais! Este guia passo a passo orientará você no processo usando Aspose.CAD for .NET, uma biblioteca poderosa que simplifica tarefas de design auxiliado por computador (CAD).

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Biblioteca Aspose.CAD for .NET: Baixe e instale a biblioteca do[Página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

- Ambiente de desenvolvimento: certifique-se de ter um ambiente de desenvolvimento .NET funcional configurado em sua máquina.

- Documento para converter: Prepare um documento CAD que contenha os layouts que deseja converter em imagens raster.

- Seu diretório de documentos: substitua o espaço reservado "Seu diretório de documentos" no código pelo caminho para o diretório de documentos.

## Importar namespaces

Primeiramente, vamos importar os namespaces necessários para tornar as funcionalidades do Aspose.CAD acessíveis em seu código.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passo 1: Carregue o Documento CAD

Comece carregando o documento CAD usando a biblioteca Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Seu código para etapas adicionais irá aqui
}
```

## Etapa 2: configurar opções de rasterização

 Crie uma instância de`CadRasterizationOptions` para definir a largura e altura da página e especificar os layouts que deseja converter.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Etapa 3: configurar TiffOptions para a imagem resultante

 Crie uma instância de`TiffOptions`para definir o formato da imagem resultante.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 4: salve a imagem resultante

Especifique o caminho de saída e salve a imagem convertida.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusão

Parabéns! Você converteu com sucesso layouts CAD em um formato de imagem raster usando Aspose.CAD for .NET. As possibilidades são vastas e este guia serve como ponto de partida para seus empreendimentos relacionados a CAD.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos CAD?

 A1: Aspose.CAD suporta uma ampla variedade de formatos CAD, incluindo DWG, DXF, DWF, STL e muito mais. Verifica a[documentação](https://reference.aspose.com/cad/net/) para uma lista abrangente.

### Q2: Como posso obter uma licença temporária para Aspose.CAD?

 A2: Visite o[página de licença temporária](https://purchase.aspose.com/temporary-license/) adquirir uma licença temporária para fins de teste e avaliação.

### Q3: Onde posso encontrar suporte para Aspose.CAD?

 A3: Os fóruns são um ótimo lugar para buscar assistência. Visite a[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para se conectar com a comunidade e obter ajuda.

### Q4: Posso experimentar o Aspose.CAD gratuitamente?

 A4: Com certeza! Pegue o seu[teste grátis](https://releases.aspose.com/) para explorar os recursos e capacidades do Aspose.CAD.

### Q5: Onde posso comprar uma licença para Aspose.CAD?

 A5: Navegue até o[página de compra](https://purchase.aspose.com/buy) para comprar uma licença e desbloquear todo o potencial do Aspose.CAD.