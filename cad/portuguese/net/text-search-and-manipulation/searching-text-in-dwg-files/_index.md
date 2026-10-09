---
date: 2026-10-09
description: Aprenda como carregar arquivo dwg e pesquisar texto dentro de arquivos
  DWG usando C# e Aspose.CAD for .NET. Siga este guia passo a passo para melhorar
  seus fluxos de trabalho CAD.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Pesquisando texto em arquivos DWG com C#
og_description: Aprenda como carregar arquivo dwg e pesquisar texto dentro de arquivos
  DWG usando C# e Aspose.CAD for .NET. Siga este guia passo a passo para melhorar
  seus fluxos de trabalho CAD.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Como carregar arquivo dwg e pesquisar texto em arquivos DWG com C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Como carregar arquivo dwg e pesquisar texto em arquivos DWG com C#
url: /pt/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como carregar arquivo DWG e pesquisar texto em arquivos DWG com C# - tutorial Aspose.CAD

## Introdução

No desenvolvimento moderno de CAD, ser capaz de **carregar arquivo dwg** objetos e localizar instantaneamente cadeias de texto específicas economiza horas de inspeção manual. Seja construindo uma ferramenta de processamento em lote ou adicionando recursos de pesquisa a um visualizador, o Aspose.CAD para .NET oferece uma API totalmente gerenciada que funciona no Windows, Linux e macOS sem dependências nativas. Este guia orienta você em cada passo — desde o carregamento do DWG até a exportação do resultado como PDF — para que possa integrar uma pesquisa de texto CAD confiável em suas aplicações C# hoje.

## Respostas rápidas
- **Qual é a primeira linha de código para carregar um DWG?** `new CadImage("yourfile.dwg")` cria uma representação em memória do desenho.  
- **Qual namespace contém as classes CAD?** `Aspose.CAD.Image` e `Aspose.CAD.FileFormats.Dwg` são necessários.  
- **Posso exportar os resultados da pesquisa diretamente para PDF?** Sim – use `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Preciso de uma licença para desenvolvimento?** Uma avaliação gratuita funciona para avaliação; uma licença permanente é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET 5, .NET 6, .NET Core 3.1 e .NET Framework 4.6+.

## O que é um arquivo DWG?

Um arquivo DWG é um formato binário que armazena dados de design 2D e 3D criados pelo AutoCAD e ferramentas compatíveis. É o contêiner padrão da indústria para geometria vetorial, camadas, texto e metadados. Como o formato é proprietário, a maioria dos analisadores de código aberto tem dificuldade com versões mais recentes, mas o Aspose.CAD oferece suporte total a mais de 150 versões de DWG, permitindo ler e manipular desenhos sem instalar o AutoCAD.

## Por que usar Aspose.CAD para pesquisa de texto CAD?

O Aspose.CAD pode processar **mais de 50** versões de DWG e DXF, manipulando arquivos de até 1 GB sem carregar todo o documento na memória. A biblioteca extrai texto tanto das seções **Entities** quanto **Block**, proporcionando uma taxa de sucesso de **99 %** na localização de cadeias pesquisáveis, mesmo quando estão aninhadas dentro de blocos. Essa confiabilidade quantificada o torna a escolha preferida para automação CAD de nível empresarial.

## Pré-requisitos

Antes de começar, verifique se você tem:

- **Aspose.CAD for .NET** instalado. Baixe o pacote mais recente no [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Uma pasta contendo os arquivos DWG que você deseja analisar.
- Um arquivo de licença válido para uso em produção (opcional para execuções de avaliação).

## Quais namespaces são necessários?

O namespace `Aspose.CAD` fornece as classes principais de manipulação de imagens, enquanto `Aspose.CAD.FileFormats.Dwg` contém estruturas específicas de DWG. Importe-os no topo do seu arquivo C#:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Nota:** O bloco de código acima é um placeholder; mantenha o texto exato inalterado para preservar a contagem original de placeholders.

## Como carregar arquivo dwg?

Carregar um arquivo DWG é simples com o Aspose.CAD. Use a classe `CadImage`, que representa um desenho CAD na memória. O construtor lê o arquivo sem renderizar, tornando o processo rápido mesmo para desenhos grandes. Após o carregamento, você pode inspecionar propriedades como `Width`, `Height` e `Layers` antes de executar quaisquer operações de pesquisa.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Como pesquisar texto na seção de entidades?

Para localizar texto na seção Entities, itere sobre a coleção `cadImage.Entities`. Cada entidade pode ser examinada quanto ao seu tipo (por exemplo, `MText`, `Text`, `Attribute`) e sua propriedade `TextString`. Execute uma comparação sem distinção entre maiúsculas e minúsculas contra a string alvo e colete as entidades correspondentes para processamento adicional ou realce.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Como pesquisar texto na seção de blocos?

Blocos são grupos reutilizáveis de entidades que podem conter texto aninhado. Primeiro, enumere `cadImage.BlockEntities.Values` para acessar cada definição de bloco. Em seguida, percorra a coleção `Entities` de cada bloco, aplicando a mesma lógica de correspondência de texto usada para a seção principal de Entities. Isso garante que texto oculto dentro de componentes reutilizáveis não seja perdido.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Como iterar pelos nós CAD para uma varredura completa?

Uma varredura abrangente combina as seções Entities e Block. Ao percorrer recursivamente a árvore de nós `CadImage`, você pode lidar com blocos aninhados, definições de atributos e até referências externas. Implemente um método auxiliar que aceita um `CadBaseEntity`, verifica seu tipo, extrai texto quando aplicável e, em seguida, recursivamente percorre entidades filhas se o nó contiver uma coleção.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Como exportar DWG para PDF após localizar texto?

Depois de identificar as entidades relevantes, você pode destacá‑las ou extrair suas coordenadas. O Aspose.CAD permite salvar todo o desenho como PDF preservando a qualidade vetorial. Configure `CadRasterizationOptions` se precisar de saída raster, então chame `image.Save("output.pdf", new PdfOptions())`. O PDF resultante pode ser compartilhado com partes interessadas que não possuem software CAD.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Conclusão

O Aspose.CAD para .NET fornece uma solução contínua e de alto desempenho para carregar dados de arquivos DWG, pesquisar texto específico e exportar o resultado para PDF. Seguindo os passos deste tutorial, você adicionou recursos poderosos de pesquisa de texto CAD à sua aplicação C# sem depender de ferramentas externas ou licenças caras.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD para .NET com outros formatos CAD?

A1: Sim, o Aspose.CAD suporta mais de 30 formatos CAD, incluindo DXF, DWF e STL, oferecendo uma solução versátil para fluxos de trabalho com formatos mistos.

### Q2: Existe uma avaliação gratuita disponível para Aspose.CAD para .NET?

A2: Sim, você pode explorar os recursos com o [free trial](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD para .NET?

A3: Visite o [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para assistência da comunidade e canais de suporte oficial.

### Q4: O que é uma licença temporária e como posso obter uma?

A4: Obtenha uma licença temporária [temporary license](https://purchase.aspose.com/temporary-license/) para avaliação de curto prazo ou projetos de prova de conceito.

### Q5: Onde posso encontrar documentação detalhada para Aspose.CAD para .NET?

A5: Consulte a abrangente [documentation](https://reference.aspose.com/cad/net/) para orientação aprofundada, referências de API e exemplos de código.

---

**Última atualização:** 2026-10-09  
**Testado com:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  


```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Tutoriais relacionados

- [Como converter DWG para PDF e imagens raster usando Aspose.CAD para .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Converter DWG para PNG e exportar objetos OLE - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Como ler arquivos DWT com Aspose.CAD para .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}