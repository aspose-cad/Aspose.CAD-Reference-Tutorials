---
date: 2026-03-16
description: Aprenda a converter DWG para PDF ou imagens raster com o Aspose.CAD para
  .NET. Este tutorial passo a passo de CAD para PDF aborda a exportação de DWG para
  formatos de imagem como PNG e mostra como exportar arquivos DWG para imagens de
  forma eficiente.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Como converter DWG para PDF e imagens raster usando Aspose.CAD para .NET
url: /pt/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando DWG para PDF ou Imagens Rasterizadas - Guia Aspose.CAD

## Introdução

Se você precisa **converter DWG para PDF** (ou para formatos raster como PNG) diretamente de uma aplicação .NET, você está no lugar certo. Neste tutorial vamos percorrer os passos exatos necessários para usar Aspose.CAD for .NET para realizar a conversão, explicar por que a biblioteca é uma escolha sólida e mostrar como lidar tanto com saída PDF quanto de imagem com apenas algumas linhas de código.

## Respostas Rápidas
- **Qual biblioteca lida com a conversão de DWG?** Aspose.CAD for .NET  
- **Posso exportar DWG para PNG assim como para PDF?** Sim – as mesmas opções de rasterização funcionam para ambos os formatos.  
- **Preciso de uma licença para desenvolvimento?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **A conversão de unidades é tratada automaticamente?** Você pode definir o sistema de unidades manualmente (métrico ou imperial) como mostrado no código.

## O que é “converter DWG para PDF”?
Converter DWG para PDF significa pegar um desenho CAD (DWG) e renderizá‑lo em um documento portátil, somente para visualização (PDF). Isso é útil para compartilhar projetos com partes interessadas que não possuem software CAD, criar documentação imprimível ou arquivar desenhos em um formato universalmente legível.

## Por que usar Aspose.CAD para esta conversão?
- **Sem dependências externas** – a biblioteca funciona totalmente em código gerenciado.  
- **Alta fidelidade** – mantém camadas, espessuras de linha e informações de layout.  
- **Opções de rasterização integradas** – permite exportar para PNG, JPEG, BMP, etc., com um único objeto de configuração.  
- **Multiplataforma** – funciona no Windows, Linux e macOS com .NET Core.

## Pré‑requisitos

Antes de mergulharmos no tutorial, certifique‑se de que você tem o seguinte configurado:

- Um entendimento básico de programação .NET.  
- Biblioteca Aspose.CAD for .NET instalada. Caso não tenha, faça o download [aqui](https://releases.aspose.com/cad/net/).  
- Sua IDE favorita configurada para desenvolvimento .NET.

## Importar Namespaces

Vamos começar importando os namespaces necessários no seu projeto .NET. Isso garante que você tenha acesso à funcionalidade Aspose.CAD no seu código.

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

## Etapa 1: Carregar Arquivo DWG

Comece carregando o arquivo DWG que deseja converter. Substitua `"Your Document Directory"` pelo caminho do seu arquivo DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Etapa 2: Configurar Exportação PDF (Como exportar DWG para PDF)

Agora, vamos configurar as opções de exportação PDF. Este exemplo demonstra como definir o layout e lidar com conversões de unidades.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Etapa 3: Exportar para PDF

Execute a exportação para PDF usando as configurações definidas.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Etapa 4: Exportar para Imagens Raster (exportar dwg para imagem)

Estenda a funcionalidade para exportar imagens raster, como PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Problemas Comuns e Soluções

| Problema | Por que acontece | Como corrigir |
|----------|------------------|---------------|
| **Páginas em branco no PDF** | Layout não especificado corretamente | Certifique‑se de que `rasterizationOptions.Layouts` inclui o nome de layout correto (ex., `"Model"`). |
| **Dimensões incorretas** | DPI ou tamanho da página incompatível | Ajuste os valores de `PageHeight`, `PageWidth` e DPI em `CadRasterizationOptions`. |
| **Unidades aparecem erradas** | Conversão de unidades não definida | Use `DefineUnitSystem` para definir `currentUnitIsMetric` e `currentUnitCoefficient` com base em `cadImage.UnitType`. |
| **Exceção de licença** | Limitações da versão de avaliação | Aplique uma licença temporária ou permanente antes de chamar `Image.Load`. |

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD para .NET em meus projetos comerciais?
A1: Sim, pode. Visite [purchase.aspose.com/buy](https://purchase.aspose.com/buy) para detalhes de licenciamento.

### Q2: Existe uma avaliação gratuita disponível?
A2: Claro! Obtenha sua avaliação gratuita [aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD para .NET?
A3: Acesse o [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade.

### Q4: Posso obter uma licença temporária para fins de teste?
A4: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso encontrar a documentação detalhada?
A5: A documentação está disponível em [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Como faço para **salvar CAD como PNG** com alta qualidade?
A6: Defina `PageHeight` e `PageWidth` para as dimensões de pixel desejadas e escolha um DPI de 300 ou superior em `CadRasterizationOptions`.

### Q7: Qual é a melhor maneira de **converter dwg** quando o arquivo fonte contém vários layouts?
A7: Preencha `rasterizationOptions.Layouts` com todos os nomes de layout que deseja exportar, depois itere sobre cada layout e chame `Save` para cada formato de saída.

---

**Última Atualização:** 2026-03-16  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}