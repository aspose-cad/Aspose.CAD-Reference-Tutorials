---
date: 2026-04-06
description: Aprenda como converter DWF para JPG em C# usando Aspose.CAD e descubra
  como extrair o tamanho do layout DWF de arquivos DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Trabalhando com arquivos DWG em C# – Obter tamanho do layout DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DWF para JPG em C# – Obter o tamanho do layout DWF a partir do DWG
url: /pt/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DWF para JPG em C# – Obter Tamanho do Layout DWF a partir de DWG

## Introdução

Se você precisa **convert DWF to JPG** e também descobrir as dimensões exatas do layout, está no lugar certo. Neste tutorial, percorreremos um exemplo completo, de ponta a ponta, que usa Aspose.CAD para .NET para abrir um arquivo DWF derivado de DWG, ler o tamanho de cada layout e salvar o layout como uma imagem JPG de alta qualidade. Ao final, você não apenas saberá como extrair informações do layout DWF, mas também terá um trecho de código reutilizável que pode ser inserido em qualquer projeto C#.

## Respostas Rápidas
- **O que significa “convert DWF to JPG”?** Significa rasterizar um layout DWF vetorial em uma imagem bitmap JPEG.  
- **Por que ler o tamanho do layout primeiro?** Conhecer as dimensões exatas permite definir as dimensões corretas da página, evitando saída esticada ou recortada.  
- **Qual biblioteca lida com isso?** Aspose.CAD para .NET fornece suporte total para DWG, DWF e conversão de imagens raster.  
- **Preciso de uma licença?** Uma licença temporária funciona para avaliação; uma licença completa é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## O que é “convert DWF to JPG” e por que isso importa?

Converter um arquivo DWF (Design Web Format) para JPG cria uma imagem portátil que pode ser exibida em navegadores, incorporada em relatórios ou compartilhada com partes interessadas que não possuem software CAD. A conversão também oferece flexibilidade para manipular a imagem (redimensionar, comprimir, marca d'água) usando ferramentas padrão de processamento de imagens.

## Por que extrair o tamanho do layout DWF?

Um arquivo DWF pode conter múltiplos layouts, cada um com seu próprio sistema de coordenadas e unidades (polegadas, milímetros, etc.). Extrair o tamanho do layout permite:

1. Preservar a proporção original ao rasterizar.  
2. Escolher o DPI correto para saída de alta resolução.  
3. Automatizar o processamento em lote de muitos layouts sem ajustes manuais.

## Pré-requisitos

Para seguir este tutorial sem interrupções, certifique‑se de que você tem os seguintes pré‑requisitos configurados:

- Aspose.CAD for .NET: Certifique‑se de que o Aspose.CAD for .NET está instalado. Você pode baixá‑lo na [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

Ter a biblioteca pronta significa que você pode focar no código em vez de procurar dependências.

## Importar Namespaces

Antes de começarmos a codificar, importe os namespaces necessários. Eles fornecem as classes que usaremos para trabalhar com arquivos CAD, opções de rasterização e I/O de arquivos.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Etapa 1: Configurar seu Ambiente

Crie um novo projeto de console ou biblioteca de classes C#, adicione uma referência ao **Aspose.CAD.dll** e garanta que o projeto tenha como alvo uma versão compatível do .NET.

## Etapa 2: Definir Caminhos de Arquivo (como extrair DWF)

Especifique onde seu arquivo DWF de origem está localizado e onde os arquivos JPG gerados devem ser gravados.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Dica profissional:** Use `Path.Combine(MyDir, "blocks_and_tables.dwf")` para um manuseio de caminho mais seguro em diferentes sistemas operacionais.

## Etapa 3: Carregar a Imagem DWF

Carregue o arquivo DWF em um objeto `Aspose.CAD.Image`. Fazemos um cast para `DwfImage` porque precisamos acessar propriedades específicas da página.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Etapa 4: Iterar pelas Páginas

Um DWF pode conter várias páginas (layouts). Percorra cada uma para processá‑las individualmente.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Etapa 5: Obter Informações do Layout

Dentro do loop, recupere o nome do layout. Esse nome será usado tanto para registro quanto para nomear o arquivo JPG de saída.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Etapa 6: Configurar Opções JPG

Crie uma instância de `JpegOptions` e configure as opções de rasterização. A propriedade `Layouts` informa ao Aspose.CAD qual layout renderizar.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Etapa 7: Determinar Tamanho da Página (convert dwg to jpg)

Calcule a largura e a altura do layout em suas unidades nativas. Essa informação é essencial para definir corretamente o tamanho da página rasterizada.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Etapa 8: Configurar Dimensões da Página

Converta as unidades nativas (polegada ou milímetro) para pixels usando os métodos auxiliares fornecidos pelo Aspose.CAD. Se o tipo de unidade não for nenhum dos dois, usamos os valores brutos.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Etapa 9: Salvar o Arquivo JPG

Por fim, vincule as opções de rasterização às opções JPEG e salve a imagem no disco.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Quando o loop terminar, você terá um arquivo JPG para cada layout, cada um dimensionado exatamente para corresponder às dimensões originais do DWF.

## Problemas Comuns e Soluções

| Sintoma | Causa Provável | Correção |
|---------|----------------|----------|
| Saída JPG vazia | `options.Layouts` não definido corretamente | Verifique se o nome do layout corresponde a `page.Name`. |
| Imagem distorcida | Conversão de DPI incorreta | Use `CommonHelper.DPI = 300` (ou o DPI desejado) antes da conversão. |
| Arquivo não encontrado | Caminho `MyDir` incorreto | Use caminhos absolutos ou `Path.Combine`. |
| Exceção de licença | Nenhuma licença aplicada | Carregue uma licença temporária ou permanente antes de chamar `Image.Load`. |

## Perguntas Frequentes

### Q1: O Aspose.CAD é compatível com os formatos de arquivo DWG mais recentes?

A1: O Aspose.CAD suporta vários formatos de arquivo DWG, incluindo as versões mais recentes. Consulte a [documentation](https://reference.aspose.com/cad/net/) para detalhes específicos de compatibilidade.

### Q2: Posso usar o Aspose.CAD em projetos comerciais e pessoais?

A2: Sim, o Aspose.CAD oferece opções de licenciamento flexíveis para uso comercial e pessoal. Visite a [purchase page](https://purchase.aspose.com/buy) para mais detalhes.

### Q3: Como posso obter uma licença temporária para o Aspose.CAD?

A3: Você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/) para fins de avaliação.

### Q4: Onde posso encontrar suporte para o Aspose.CAD?

A4: Para quaisquer dúvidas ou assistência, visite o [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Existe uma versão de teste gratuita do Aspose.CAD?

A5: Sim, você pode acessar uma versão de teste gratuita do Aspose.CAD [aqui](https://releases.aspose.com/).

### Q6: Como converter um arquivo DWG diretamente para JPG sem extrair o DWF primeiro?

A6: Você pode carregar o arquivo DWG com `Aspose.CAD.Image.Load` e usar o mesmo fluxo de rasterização; basta definir `options.Layouts` para o(s) nome(s) de layout desejado(s) do DWG.

### Q7: A conversão preserva a qualidade vetorial?

A7: Uma vez rasterizada para JPG, a imagem passa a ser bitmap, portanto a escalabilidade vetorial é perdida. Para dimensionamento sem perdas, considere exportar para PNG ou SVG.

---

**Última Atualização:** 2026-04-06  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}