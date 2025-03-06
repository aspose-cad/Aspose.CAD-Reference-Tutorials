---
title: Exporte layouts CAD para formatos de imagem raster no Aspose.CAD for .NET
linktitle: Exporte layouts CAD para formatos de imagem raster
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Aprenda como exportar layouts CAD para imagens raster usando Aspose.CAD for .NET. Siga nosso guia passo a passo para uma conversão perfeita.
weight: 10
url: /pt/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporte layouts CAD para formatos de imagem raster no Aspose.CAD for .NET

## Introdução

Você está procurando converter layouts CAD em formatos de imagem raster com eficiência usando Aspose.CAD for .NET? Este guia passo a passo orientará você durante o processo, fornecendo instruções detalhadas e trechos de código para tornar a tarefa perfeita. Quer você seja um desenvolvedor experiente ou um novato no Aspose.CAD, este tutorial atende a todos os níveis de conhecimento.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter o seguinte:

- Biblioteca Aspose.CAD for .NET: Certifique-se de ter a biblioteca Aspose.CAD instalada. Caso contrário, você pode baixá-lo no[Site Aspose.CAD](https://releases.aspose.com/cad/net/).

- Arquivo de desenho CAD: Prepare um arquivo de desenho CAD (por exemplo, conic_pyramid.dxf) que deseja converter em formatos de imagem raster.

## Importar namespaces

Em seu projeto .NET, importe os namespaces necessários para aproveitar as funcionalidades do Aspose.CAD. Inclua os seguintes namespaces no início do seu código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o desenho CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Carregar um desenho CAD em uma instância de imagem
using (var image = Image.Load(sourceFilePath))
{
    // Seu código para carregar o desenho CAD vai aqui
}
```

## Etapa 2: Criar CadRasterizationOptions

```csharp
// Crie uma instância de CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Etapa 3: especificar camadas

```csharp
// Adicione o nome da camada à lista de camadas do CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Etapa 4: criar opções Jpeg

```csharp
// Crie uma instância de JpegOptions (ou qualquer ImageOptions para formatos raster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 5: exportar para formato JPEG

```csharp
// Exporte cada camada para o formato Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Etapa Adicional: Converter Todas as Camadas

Se você deseja converter todas as camadas, use o seguinte método:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Este método itera sobre todas as camadas do desenho CAD, exportando cada camada para um arquivo JPEG separado.

## Conclusão

Parabéns! Você aprendeu com sucesso como exportar layouts CAD para formatos de imagem raster usando Aspose.CAD for .NET. Este tutorial fornece um guia completo para desenvolvedores que buscam soluções eficientes e confiáveis para conversão de CAD.

## Perguntas frequentes

### Q1: Posso usar outros formatos de imagem para exportação?

 A1: Sim, você pode. Simplesmente substitua`JpegOptions` com as opções do formato desejado, como`PngOptions` ou`BmpOptions`.

### Q2: Existe uma versão de teste disponível?

 A2: Sim, você pode explorar a funcionalidade do Aspose.CAD baixando a versão de teste[aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD?

 A3: Visite o Aspose.CAD[fórum](https://forum.aspose.com/c/cad/19) para suporte da comunidade ou considere adquirir uma licença para suporte dedicado.

### P4: As licenças temporárias estão disponíveis?

 A4: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Onde posso encontrar a documentação?

 A5: Consulte a documentação detalhada[aqui](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
