---
title: Exportando DWG para PDF ou imagens raster - Guia Aspose.CAD
linktitle: Exportando DWG para PDF ou imagens raster
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore um guia completo sobre como exportar DWG para PDF ou imagens raster usando Aspose.CAD for .NET. Aprenda as etapas, os pré-requisitos e experimente esta poderosa biblioteca.
type: docs
weight: 11
url: /pt/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Introdução

Você deseja converter facilmente arquivos DWG em PDF ou imagens raster em seu aplicativo .NET? Não procure mais! Este guia passo a passo orientará você no processo usando a poderosa biblioteca Aspose.CAD for .NET. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este tutorial atende a todos os níveis de habilidade.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter o seguinte em vigor:

- Uma compreensão básica da programação .NET.
-  Biblioteca Aspose.CAD para .NET instalada. Se não, baixe-o[aqui](https://releases.aspose.com/cad/net/).
- Seu ambiente de desenvolvimento integrado (IDE) favorito configurado para desenvolvimento .NET.

## Importar namespaces

Vamos começar importando os namespaces necessários em seu projeto .NET. Isso garante que você tenha acesso à funcionalidade Aspose.CAD em seu código.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Etapa 1: carregar o arquivo DWG

Comece carregando o arquivo DWG que deseja converter. Substitua “Seu diretório de documentos” pelo caminho do arquivo DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Seu código para carregar DWG vai aqui
}
```

## Passo 2: Configurar a exportação de PDF

Agora, vamos definir as configurações de exportação de PDF. Este exemplo demonstra como definir o layout e lidar com conversões de unidades.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Verifique e defina o sistema de unidades
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Seu código para configurar a exportação de PDF vai aqui
```

## Passo 3: Exportar para PDF

Execute a exportação para PDF usando as configurações definidas.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Etapa 4: exportar para imagens raster

Amplie a funcionalidade para exportar para imagens rasterizadas, como PNG.

```csharp
// Tamanho A4 a 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como usar o Aspose.CAD for .NET para exportar arquivos DWG para imagens PDF e raster. Esta poderosa biblioteca agiliza o processo, tornando-o eficiente e fácil de usar para o desenvolvedor.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD for .NET em meus projetos comerciais?

 A1: Sim, você pode. Visita[buy.aspose.com/buy](https://purchase.aspose.com/buy) para detalhes de licenciamento.

### P2: Existe um teste gratuito disponível?

 A2: Certamente! Faça seu teste gratuito[aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD for .NET?

 A3: Vá para o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.

### P4: Posso obter uma licença temporária para fins de teste?

 A4: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso encontrar a documentação detalhada?

 R5: A documentação está disponível em[Aspose.CAD](https://reference.aspose.com/cad/net/).