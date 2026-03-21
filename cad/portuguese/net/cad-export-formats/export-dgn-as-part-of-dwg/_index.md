---
date: 2026-03-21
description: Aprenda a criar PDF a partir de DWG e exportar DGN como parte do DWG
  usando Aspose.CAD para .NET. Este guia também mostra como converter DWG para PDF
  e definir opções de PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Criar PDF a partir de DWG e Exportar DGN como Parte do DWG – Aspose.CAD para
  .NET
url: /pt/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar PDF a partir de DWG e Exportar DGN como Parte do DWG – Aspose.CAD para .NET

## Introdução

Se você precisa **criar PDF a partir de DWG** arquivos enquanto também incorpora um design DGN como parte do DWG, o Aspose.CAD para .NET torna isso simples. Neste tutorial percorreremos todo o fluxo de trabalho: carregar um DWG, localizar o underlay DGN incorporado, configurar as opções de rasterização e, finalmente, exportar o resultado para um documento PDF. Seja você quem está construindo uma ferramenta de conversão em lote, um motor de relatórios ou um serviço de integração CAD‑BIM, os passos abaixo lhe darão uma base sólida e pronta para produção.

## Respostas Rápidas
- **Qual biblioteca lida com a conversão de DWG → PDF?** Aspose.CAD for .NET  
- **Posso exportar um underlay DGN ao criar o PDF?** Sim – o underlay é acessado via `CadDgnUnderlay`.  
- **Qual método define as opções de PDF?** `PdfOptions` junto com `CadRasterizationOptions`.  
- **Preciso de uma licença para uso comercial?** Sim, é necessária uma licença válida do Aspose.CAD.  
- **Versões .NET suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## O que é “criar PDF a partir de DWG”?

Criar um PDF a partir de um arquivo DWG significa renderizar o desenho vetorial em um documento PDF raster ou vetorial. Esse processo é útil para compartilhar desenhos com partes interessadas que não possuem software CAD, arquivar ou gerar relatórios imprimíveis. O Aspose.CAD simplifica a tarefa ao lidar com o pesado parsing das entidades DWG e fornecer controle granular sobre a saída através de `PdfOptions`.

## Por que exportar DGN como parte de um DWG?

Um underlay DGN costuma representar geometria de referência de projetos MicroStation. Ao exportar o DGN junto com o DWG você preserva o contexto de design original, garantindo que os consumidores posteriores vejam o conjunto completo de desenhos. Isso é especialmente valioso em projetos multidisciplinares onde arquivos DWG e DGN coexistem.

## Pré-requisitos

- **Aspose.CAD for .NET** – faça o download [aqui](https://releases.aspose.com/cad/net/).  
- **Ambiente de Desenvolvimento** – Visual Studio (qualquer versão recente) ou sua IDE .NET preferida.  
- **Conhecimento básico de C#** – você deve estar confortável com a sintaxe C# e a estrutura de projetos .NET.

## Importar Namespaces

Adicione as diretivas `using` necessárias no topo do seu arquivo fonte C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guia Passo a Passo

### Passo 1: Definir Caminhos de Arquivo

Defina o arquivo DWG de entrada e o nome do PDF de saída.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Passo 2: Criar Instância `PdfOptions` (definir opções de pdf)

`PdfOptions` permite controlar como o PDF é gerado, como tamanho da página, compressão e metadados.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Passo 3: Carregar o Arquivo DWG

Carregue o DWG como um `CadImage` para que você possa inspecionar suas entidades.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Passo 4: Iterar Sobre as Entidades

Percorra cada entidade do desenho para localizar o underlay DGN.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Passo 5: Verificar Tipo de Entidade (como exportar dgn)

Identifique se a entidade atual é um underlay DGN.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Passo 6: Obter Caminho do Underlay

Recupere o caminho de referência externa do arquivo DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Passo 7: Definir Opções de Rasterização (converter dwg para pdf)

Configure como o DWG é rasterizado antes de ser inserido no PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Passo 8: Exportar DWG para PDF

Finalmente, salve a imagem renderizada como um arquivo PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Problemas Comuns e Soluções

| Problema | Motivo | Correção |
|----------|--------|----------|
| **`Image.Load` lança “File not found”** | Caminho incorreto ou arquivo ausente. | Use um caminho absoluto ou garanta que o DWG seja copiado para a pasta de saída. |
| **Caminho do underlay está vazio** | Underlay DGN não está incorporado ou referência quebrada. | Verifique se o DWG realmente contém um underlay DGN e se o arquivo DGN externo está acessível. |
| **Saída PDF está em branco** | Opções de rasterização definidas com tamanho zero. | Ajuste `PageWidth`/`PageHeight` ou defina `NoScaling = false`. |
| **Exceção de licença** | Executando sem uma licença válida do Aspose.CAD. | Aplique a licença antes de carregar a imagem: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD para .NET em meus projetos comerciais?
A1: Sim, você pode. Visite [aqui](https://purchase.aspose.com/buy) para explorar opções de licenciamento.

### Q2: Existem limitações no tamanho dos arquivos DWG que eu posso processar?
A2: Aspose.CAD suporta o tratamento de arquivos DWG grandes, mas limitações de hardware podem se aplicar.

### Q3: Existe uma versão de avaliação disponível?
A3: Sim, você pode obter uma avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Como posso obter licenças temporárias?
A4: Licenças temporárias podem ser obtidas [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso buscar assistência se encontrar problemas?
A5: Você pode visitar o fórum Aspose.CAD [aqui](https://forum.aspose.com/c/cad/19) para suporte.

**Q: Como definir metadados adicionais de PDF (autor, título, etc.)?**  
A: Use as propriedades `exportOptions.Metadata` antes de chamar `Save`.

**Q: Posso exportar vários layouts em páginas PDF separadas?**  
A: Sim – defina `Layouts = new string[] { "Layout1", "Layout2" }` em `CadRasterizationOptions`.

**Q: O Aspose.CAD suporta a conversão de DWG para outros formatos de imagem?**  
A: Absolutamente. Você pode exportar para PNG, JPEG, SVG e mais usando as sobrecargas correspondentes de `Image.Save`.

---

**Última atualização:** 2026-03-21  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}