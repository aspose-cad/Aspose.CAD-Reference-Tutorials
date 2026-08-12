---
date: 2026-08-12
description: Extrair texto de DWG e converter DWG específico em imagem em C# usando
  Aspose.CAD for .NET. Aprenda passo a passo com trechos de código.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Convertendo DWG Particular em Imagem em C#
og_description: Extrair texto de DWG e converter DWG específico em imagem em C# com
  Aspose.CAD. Siga este guia conciso para implementação rápida.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Extrair texto de DWG e converter DWG específico em imagem em C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Extrair texto de DWG e converter DWG específico em imagem em C#
url: /pt/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertendo DWG específico em imagem em C# - Guia Aspose.CAD

## Introdução

Em aplicações de engenharia modernas, muitas vezes você precisa **extrair texto de arquivos DWG** e **converter DWG específico em formatos de imagem** para relatórios ou visualização. Aspose.CAD para .NET oferece uma API completa que lida com ambas as tarefas sem exigir nenhum software CAD externo. Neste tutorial você aprenderá como carregar um DWG, filtrar entidades de texto, rasterizar o desenho e, finalmente, salvar o resultado como uma imagem PDF — tudo em código C# limpo.

## Respostas rápidas
- **Qual é o primeiro passo?** Carregue o arquivo DWG com `new CadImage("file.dwg")`.  
- **Qual classe filtra texto?** Use `CadEntityFilter` para selecionar entidades `Text`.  
- **Como definir o tamanho da imagem?** Defina `Width` e `Height` em `CadRasterizationOptions`.  
- **Qual formato de saída é usado?** O exemplo salva em PDF, que incorpora a imagem rasterizada.  
- **Preciso de licença para produção?** Sim – uma licença comercial do Aspose.CAD remove as limitações da avaliação.

## Como extrair texto de DWG?

Carregue o DWG, aplique um filtro que selecione apenas entidades de texto e, em seguida, leia a propriedade `TextString` de cada entidade. Essa abordagem devolve cada anotação, rótulo ou texto de dimensão presente no desenho, permitindo reutilizá‑los para busca, indexação ou geração de relatórios.

## Por que converter DWG específico em imagem?

Converter um DWG em uma imagem raster permite incorporar o desenho em documentos, páginas web ou aplicativos móveis que não conseguem renderizar formatos CAD nativos. Aspose.CAD processa **mais de 50 formatos CAD** e pode rasterizar desenhos com centenas de páginas usando menos de 200 MB de memória, o que o torna adequado para cenários de servidor de alta taxa de transferência.

## Pré‑requisitos

- Visual Studio (qualquer edição recente) para compilar e executar projetos C#.  
- Aspose.CAD para .NET – certifique‑se de que a biblioteca está instalada. Você pode encontrar o link de download na **[página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/)**.  
- Um arquivo DWG que você deseja manipular; o arquivo de exemplo *visualization_-_conference_room.dwg* é usado nos trechos de código.

## Importar namespaces

Os namespaces a seguir dão acesso às classes principais de CAD, opções de rasterização e auxiliares de saída PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Etapa 1: carregar o arquivo DWG

Crie uma instância de `CadImage` passando o caminho do seu arquivo DWG. O objeto `CadImage` representa todo o desenho na memória e fornece acesso às suas camadas, entidades e metadados.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Etapa 2: filtrar entidades

`CadEntityFilter` permite selecionar apenas as entidades que você precisa. Neste guia configuramos o filtro para manter objetos **text**, descartando linhas, círculos e outras geometrias que você não deseja na imagem final.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Etapa 3: definir opções de rasterização

`CadRasterizationOptions` controla como o desenho é convertido em bitmap. Você pode definir o tamanho de saída, cor de fundo e resolução (DPI). O seguinte trecho apresenta a classe:

A classe `CadRasterizationOptions` especifica dimensões da imagem, resolução e configurações de renderização para converter desenhos CAD em formatos raster.  

Defina a largura, altura e cor de fundo desejadas antes de passar as opções para o exportador PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Etapa 4: definir opções de PDF

`PdfOptions` agrupa as configurações de rasterização com recursos específicos de PDF, como compressão. O trecho de definição desta classe aparece primeiro:

`PdfOptions` encapsula parâmetros de geração de PDF, incluindo as opções de rasterização que determinam como os dados CAD são renderizados dentro do documento PDF.  

Atribua a instância previamente criada de `CadRasterizationOptions` à propriedade `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Etapa 5: salvar como PDF

Por fim, chame o método `Save` no objeto `CadImage`, passando o nome do arquivo de destino e as `PdfOptions` configuradas. O PDF conterá uma imagem de alta qualidade do desenho filtrado.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Problemas comuns e solução de problemas

- **Texto ausente após o filtro** – Verifique se o DWG realmente contém entidades `Text`; alguns desenhos armazenam anotações como `MText`. Ajuste o filtro para incluir `MText` se necessário.  
- **Imagem de saída em branco** – Certifique‑se de que o DPI de rasterização é suficientemente alto (300 DPI é um padrão seguro) e que a cor de fundo não está definida como transparente ao visualizar o PDF.  
- **Erros de falta de memória em arquivos grandes** – Use a sobrecarga `LoadOptions` que habilita streaming, evitando que todo o arquivo seja carregado na memória de uma só vez.

## Perguntas frequentes

**Q: O Aspose.CAD é compatível com todas as versões de arquivos DWG?**  
A: Aspose.CAD suporta versões de DWG do AutoCAD 2000 até a mais recente de 2024, cobrindo mais de 90 % dos arquivos criados no campo.

**Q: Posso personalizar as opções de rasterização para diferentes saídas?**  
A: Sim – você pode alterar resolução, formato de imagem, anti‑aliasing e cor de fundo para atender a destinos PNG, JPEG ou PDF.

**Q: Onde encontrar exemplos adicionais e documentação?**  
A: Explore a abrangente [documentação do Aspose.CAD](https://reference.aspose.com/cad/net/) para mais amostras de código e detalhes da API.

**Q: Existe uma versão de avaliação gratuita do Aspose.CAD?**  
A: Absolutamente – você pode baixar uma versão de avaliação na **[página de download de avaliação da Aspose](https://releases.aspose.com/)** e avaliar todos os recursos sem restrições por 30 dias.

**Q: Como obter suporte ou conectar‑se com a comunidade?**  
A: Participe do ativo [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) onde desenvolvedores compartilham soluções e a equipe Aspose responde perguntas.

---

**Última atualização:** 2026-08-12  
**Testado com:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose

## Tutoriais Relacionados

- [Procurando texto em arquivos DWG com C# - Tutorial Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Converter desenho CAD em imagem raster no Aspose.CAD para .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Renderizando documentos DWG em C# - Guia Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}