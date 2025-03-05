---
title: Exportando imagens 3D para PDF - Tutorial Aspose.CAD
linktitle: Exportando imagens 3D para PDF
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Converta facilmente imagens CAD 3D em PDF com Aspose.CAD for .NET. Siga nosso tutorial passo a passo para exportar PDF sem problemas.
type: docs
weight: 10
url: /pt/net/3d-image-export/exporting-3d-images-to-pdf/
---
## Introdução

Você deseja exportar facilmente imagens 3D para PDF usando Aspose.CAD for .NET? Este tutorial passo a passo irá guiá-lo através do processo, garantindo que você aproveite o poder do Aspose.CAD para converter facilmente suas imagens 3D para o formato PDF.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.CAD para .NET: Certifique-se de ter a biblioteca Aspose.CAD para .NET instalada. Caso contrário, você pode baixá-lo no[Página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

- Diretório de documentos: Configure um diretório onde seus arquivos CAD são armazenados e anote o caminho.

## Importar namespaces

Em seu projeto .NET, importe os namespaces necessários para trabalhar com Aspose.CAD. Adicione as seguintes linhas ao topo do seu arquivo de código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Etapa 1: carregar a imagem CAD

 Comece carregando a imagem CAD que deseja exportar para PDF. Use o`Load` método da biblioteca Aspose.CAD. Substituir`"conic_pyramid.dxf"` com o caminho para o seu arquivo CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Seu código para carregar a imagem CAD vai aqui
}
```

## Etapa 2: configurar opções de rasterização

 Configure as opções de rasterização para a imagem CAD. Defina parâmetros como largura da página, altura da página e layouts. Remova o comentário da linha relacionada a`TypeOfEntities` se suas entidades forem 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Passo 3: Definir opções de PDF

Crie opções de PDF e associe-as às opções de rasterização.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 4: Salvar como PDF

Salve a imagem CAD como um arquivo PDF usando as opções configuradas. Especifique o caminho de saída do arquivo PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Conclusão

Parabéns! Você exportou com sucesso imagens 3D para PDF usando Aspose.CAD for .NET. Este tutorial simples garante que você converta facilmente seus arquivos CAD em um formato mais acessível.

## Perguntas frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

A1: Sim, o Aspose.CAD suporta uma ampla variedade de formatos CAD, garantindo flexibilidade no manuseio de vários tipos de arquivos.

### P2: Posso personalizar as dimensões da página ao exportar para PDF?

A2: Absolutamente. O tutorial demonstra como configurar a largura e a altura da página de acordo com suas necessidades.

### Q3: As licenças temporárias estão disponíveis para Aspose.CAD?

 A3: Sim, você pode obter licenças temporárias para Aspose.CAD visitando[Licença Temporária](https://purchase.aspose.com/temporary-license/).

### P4: Onde posso encontrar suporte adicional ou discussões na comunidade?

 A4: Vá para o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e envolvimento com a comunidade.

### Q5: Existe uma versão de teste gratuita do Aspose.CAD disponível?

 A5: Sim, você pode explorar os recursos do Aspose.CAD acessando o[teste grátis](https://releases.aspose.com/).