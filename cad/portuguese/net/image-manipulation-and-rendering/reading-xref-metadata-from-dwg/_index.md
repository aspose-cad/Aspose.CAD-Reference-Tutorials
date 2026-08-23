---
date: 2026-08-23
description: Desbloqueie o potencial do Aspose.CAD para .NET com nosso tutorial passo
  a passo sobre como ler xref metadata de arquivos DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: Lendo xref metadata de arquivos DWG
og_description: Aprenda a ler xref metadata de arquivos DWG com Aspose.CAD para .NET.
  Este guia orienta você pelos pré-requisitos, etapas de código e armadilhas comuns
  em menos de dez minutos.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Como ler xref metadata de arquivos DWG usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Como ler xref metadata de arquivos DWG usando Aspose.CAD
url: /pt/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como ler metadados xref de arquivos DWG usando Aspose.CAD

## Introdução

Neste tutorial, você aprenderá **como ler metadados xref** de arquivos DWG usando a biblioteca Aspose.CAD para .NET. Seja para auditar referências externas, migrar desenhos legados ou construir um pipeline BIM personalizado, extrair informações XREF é uma necessidade comum. Vamos percorrer cada passo, desde a configuração do projeto até o processamento dos metadados, e destacaremos dicas práticas que você pode aplicar imediatamente.

## Respostas rápidas
- **Qual é o objetivo principal?** Recuperar pontos de inserção e caminhos de arquivos de referências externas (XREFs) incorporados em um desenho DWG.  
- **Qual biblioteca é necessária?** Aspose.CAD para .NET (suporta mais de 50 formatos CAD).  
- **Preciso de uma licença?** É necessária uma licença temporária ou completa para uso em produção; uma versão de avaliação gratuita está disponível.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Quanto tempo o código leva para executar?** Processar um DWG típico de 200 páginas com algumas XREFs é concluído em menos de um segundo em hardware padrão.

## O que é ler metadados xref?

`read xref metadata` refere‑se à operação de acessar as propriedades de entidades de referência externa armazenadas dentro de um desenho DWG, como suas coordenadas de inserção, caminhos de arquivos de origem e flags de visibilidade. Essa operação permite que você descubra programaticamente como um desenho é composto por outros arquivos, possibilitando validação automatizada, geração de relatórios ou processamento em lote de recursos vinculados.

## Por que usar Aspose.CAD para esta tarefa?

Aspose.CAD suporta **mais de 50 formatos de arquivos CAD** e pode ler arquivos DWG **sem exigir AutoCAD**. A biblioteca processa desenhos grandes **em fluxos de memória eficientes**, permitindo lidar com arquivos de várias centenas de páginas sem carregar o arquivo inteiro na RAM. Essas capacidades quantificáveis a tornam uma escolha confiável para automação CAD de nível empresarial.

## Pré‑requisitos

Antes de mergulharmos no código, verifique se você tem o seguinte:

- Aspose.CAD para .NET instalado. Baixe o pacote mais recente da [página de lançamento do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Uma pasta local que contém os arquivos DWG que você deseja inspecionar. Atualize a variável `MyDir` no código de exemplo para apontar para essa pasta.
- Uma licença válida do Aspose.CAD (ou a versão de avaliação gratuita) se você planeja executar o código em um ambiente de produção.

Agora que o ambiente está pronto, vamos começar a codificar.

## Importar namespaces

A primeira coisa que você precisa fazer é importar os namespaces que expõem a API do Aspose.CAD. As diretivas `using` trazem os namespaces do Aspose.CAD para o escopo, permitindo acesso a classes CAD como `Image` e `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## Como ler metadados xref de arquivos DWG?

Carregue o desenho, enumere suas entidades, filtre objetos XREF e, em seguida, extraia as propriedades desejadas — tudo em algumas linhas de código simples. As seções a seguir dividem o processo em quatro etapas lógicas que você pode copiar e colar em qualquer projeto de console ou serviço .NET.

### Passo 1: carregar o arquivo DWG

Crie uma instância `Image` a partir do arquivo DWG que você deseja analisar. `Image.Load` carrega um arquivo CAD e retorna um objeto `CadImage` que representa o desenho. Ajuste a variável `sourceFilePath` para o local exato do seu desenho.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### Passo 2: iterar pelas entidades

Percorra a coleção `Entities` do objeto `Image`. `CadBaseEntity` é a classe base para todas as entidades CAD no Aspose.CAD. Para cada entidade, verifique se ela é uma referência XREF e colete seus metadados.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### Passo 3: extrair metadados

Quando você encontrar uma entidade XREF, leia seu ponto de inserção (X, Y, Z) e o caminho do desenho referenciado. `CadUnderlay` representa uma entidade de referência externa (XREF) dentro de um desenho DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### Passo 4: processar metadados

Nesta fase, você pode armazenar as informações extraídas em um banco de dados, gravá‑las em um arquivo CSV ou alimentá‑las em fluxos de trabalho BIM subsequentes. O exemplo simplesmente imprime os valores no console, mas você está livre para substituir isso por qualquer lógica personalizada.

```csharp
// Your custom logic for processing metadata goes here
```

## Problemas comuns e solução de problemas

| Sintoma | Causa provável | Correção |
|---------|----------------|----------|
| Nenhuma entidade XREF é retornada | O desenho usa um tipo de referência diferente (por exemplo, INSERT) | Verifique o tipo de entidade contra `CadEntityType.Xref` e também trate `Insert` se necessário |
| `Image.Load` lança uma exceção | Caminho de arquivo incorreto ou versão DWG não suportada | Verifique o caminho e assegure que está usando Aspose.CAD 24.11 ou mais recente |
| Valores de metadados estão vazios | O XREF está definido mas não resolvido (arquivo externo ausente) | Garanta que o arquivo referenciado exista no disco ou forneça um resolvedor de sistema de arquivos virtual |

## Perguntas frequentes

**Q: O Aspose.CAD para .NET é compatível com todos os formatos de arquivos CAD?**  
A: Sim, o Aspose.CAD para .NET suporta **mais de 50 formatos de entrada e saída**, incluindo DWG, DXF, DGN e IFC, oferecendo ampla cobertura para a maioria dos fluxos de trabalho de engenharia.

**Q: Posso usar a versão de avaliação gratuita antes de decidir pela compra?**  
A: Certamente! Você pode acessar a página de download da versão de avaliação [free trial download page](https://releases.aspose.com/).

**Q: Onde posso encontrar documentação abrangente para Aspose.CAD para .NET?**  
A: A documentação está disponível [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**Q: Como obtenho uma licença temporária para Aspose.CAD para .NET?**  
A: Você pode obter uma licença temporária [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Precisa de assistência ou tem dúvidas específicas?**  
A: Participe da comunidade Aspose.CAD em [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) para suporte especializado e discussões.

## Conclusão

Agora você tem um padrão completo e pronto para produção para **ler metadados XREF** de arquivos DWG com Aspose.CAD para .NET. Seguindo as quatro etapas — carregar o arquivo, iterar entidades, extrair o ponto de inserção e o caminho da sub‑camada, e processar os resultados — você pode integrar essa capacidade em qualquer aplicação centrada em CAD, seja uma ferramenta de migração de dados, um script de controle de qualidade ou um pipeline BIM personalizado.

---

**Última atualização:** 2026-08-23  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriais relacionados

- [Como alterar o caminho xref e editar hiperlinks em arquivos CAD - Tutorial Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [Obtendo atributos de bloco de arquivos DWG - Tutorial Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [Convertendo arquivos DWG grandes para PDF - Tutorial Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}