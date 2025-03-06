---
title: Exportar DGN para imagem raster em Aspose.CAD para .NET
linktitle: Exportar DGN para imagem raster
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Converta DGN em imagens raster sem esforço usando Aspose.CAD for .NET. Explore o guia passo a passo e libere o poder do .NET na manipulação de arquivos CAD.
weight: 13
url: /pt/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DGN para imagem raster em Aspose.CAD para .NET

## Introdução

No domínio dinâmico do desenvolvimento .NET, o Aspose.CAD surge como uma ferramenta poderosa para lidar com arquivos de Design Auxiliado por Computador (CAD). Este tutorial se aprofunda no processo de exportação de arquivos DGN para imagens raster usando Aspose.CAD for .NET. Se você deseja transformar seus arquivos DGN em imagens raster visualmente atraentes de maneira integrada, você está no lugar certo.

## Pré-requisitos

Antes de embarcarmos nesta jornada, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD for .NET: Certifique-se de ter a biblioteca Aspose.CAD instalada em seu projeto .NET. Você pode encontrar a biblioteca e a documentação relevante no site[local na rede Internet](https://reference.aspose.com/cad/net/).

- Exemplo de arquivo DGN: tenha um arquivo DGN pronto para conversão. Em nosso exemplo, usaremos "Nikon_D90_Camera.dgn".

Agora, vamos mergulhar no guia passo a passo.

## Importar namespaces

No seu projeto .NET, comece importando os namespaces necessários para o Aspose.CAD. Esta etapa permite acessar as classes e métodos necessários para conversão de imagem DGN em raster.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: carregar o arquivo DGN

 Comece carregando o arquivo DGN em um`CadImage` objeto. Isso fornece uma base para operações subsequentes.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Seu código para processamento posterior vai aqui
}
```

## Etapa 2: definir opções de rasterização

 Criar uma`CadRasterizationOptions` objeto e defina várias propriedades para personalizar o processo de rasterização de acordo com seus requisitos.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Etapa 3: Criar objeto JpegOptions

 Como pretendemos converter o arquivo DGN para JPEG, crie um`JpegOptions` objeto e atribuir o previamente definido`CadRasterizationOptions` para isso.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 4: salve a imagem raster

 Utilize o`Save` método do`CadImage` class para exportar o arquivo DGN para uma imagem raster no formato desejado, neste caso, um JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusão

Parabéns! Você navegou com sucesso pelas etapas para exportar um arquivo DGN para uma imagem raster usando Aspose.CAD for .NET. Este tutorial equipou você com o conhecimento essencial para integrar essa funcionalidade em seus projetos .NET sem esforço.

## Perguntas frequentes

### Q1: Posso exportar arquivos DGN para formatos diferentes de JPEG?

A1: Sim, Aspose.CAD for .NET suporta vários formatos de saída. Você pode modificar as opções de acordo na Etapa 3.

### P2 Como posso lidar com exceções durante o processo de conversão?

A2: Certifique-se de ter um tratamento de exceções adequado, conforme demonstrado no código fornecido, para resolver possíveis problemas.

### Q3: Existe uma versão de teste disponível para Aspose.CAD for .NET?

 A3: Sim, você pode explorar o produto com uma avaliação gratuita. Visita[aqui](https://releases.aspose.com/) Para maiores informações.

### Q4: Onde posso procurar assistência ou discutir questões relacionadas ao Aspose.CAD for .NET?

 A4: Vá para o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### Q5: Como obtenho uma licença temporária do Aspose.CAD for .NET?

 A5: Visita[esse link](https://purchase.aspose.com/temporary-license/)para adquirir uma licença temporária para suas necessidades de desenvolvimento.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
