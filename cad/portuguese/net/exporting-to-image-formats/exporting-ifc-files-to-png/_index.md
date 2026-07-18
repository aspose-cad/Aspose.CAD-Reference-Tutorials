---
date: 2026-07-18
description: Como exportar CAD para PNG usando Aspose.CAD para .NET. Converta arquivos
  IFC em imagens PNG de alta qualidade de forma rápida e confiável.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Exportando Arquivos IFC para PNG
og_description: Como exportar CAD para PNG usando Aspose.CAD para .NET. Aprenda a
  conversão passo a passo de arquivos IFC em imagens PNG sem necessidade de código.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Como Exportar CAD para PNG – Guia Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Como Exportar CAD para PNG – Exportando Arquivos IFC com Aspose.CAD
url: /pt/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Exportar CAD para PNG – Exportando Arquivos IFC com Aspose.CAD

## Introdução

Se você precisa de **how to export cad to png**, o Aspose.CAD para .NET oferece uma maneira confiável e sem código de transformar modelos IFC (Industry Foundation Classes) em imagens raster PNG nítidas. Neste tutorial, percorreremos todo o fluxo de trabalho — desde a instalação da biblioteca até a gravação do PNG final — para que você possa integrar a conversão em qualquer aplicação .NET com confiança.

## Respostas Rápidas
- **Qual biblioteca realiza a conversão?** Aspose.CAD for .NET.
- **Formato de origem suportado?** IFC (Industry Foundation Classes) files.
- **Formato de imagem de destino?** PNG, com controle total sobre tamanho e resolução.
- **Versão mínima do .NET?** .NET Framework 4.5+ ou .NET Core 3.1+.
- **Requisito de licença?** Uma licença válida do Aspose.CAD para uso em produção.

## O que é “how to export cad to png”?

A frase refere‑se ao processo de conversão de formatos de arquivo baseados em CAD, como IFC, em imagens raster Portable Network Graphics (PNG). Essa conversão permite visualização, compartilhamento e incorporação fáceis de visualizações CAD em páginas da web, documentação ou relatórios, oferecendo um formato leve e amplamente suportado que preserva a fidelidade visual sem exigir visualizadores CAD especializados.

## Por que usar Aspose.CAD para esta conversão?

O Aspose.CAD suporta **mais de 50 formatos CAD e BIM** e pode processar modelos IFC com várias centenas de páginas sem carregar o arquivo inteiro na memória. Ele oferece conversões rápidas e eficientes em memória em hardware de servidor padrão, lidando automaticamente com camadas, espessuras de linha e mapeamento de cores, ao mesmo tempo que oferece amplas opções de configuração para qualidade e tamanho da saída.

## Pré-requisitos

### 1. Instalação do Aspose.CAD
Certifique-se de que o Aspose.CAD para .NET está instalado. Você pode baixá‑lo na página de lançamentos [aqui](https://releases.aspose.com/cad/net/).

### 2. Diretório de Documentos
Crie um diretório designado para seus documentos. No exemplo fornecido, a variável `MyDir` representa o diretório de documentos.

## Importar Namespaces
Agora que os pré-requisitos estão prontos, importe os namespaces necessários para trabalhar com Aspose.CAD em seu projeto .NET.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Como Exportar CAD para PNG?

`IfcImage` representa uma imagem CAD IFC que pode ser rasterizada em formatos raster como PNG. Carregue seu arquivo IFC com `new IfcImage("source.ifc")`, configure a rasterização via `RasterizationOptions`, defina as configurações específicas de PNG com `PngOptions` e, finalmente, chame `Save(outputPath, pngOptions)`. Esse fluxo de ponta a ponta converte o modelo CAD em um PNG de alta resolução em apenas algumas linhas de código, lidando automaticamente com camadas, cores e espessuras de linha.

## Etapa 1: Carregar Arquivo IFC
A classe `IfcImage` carrega um modelo IFC e o prepara para rasterização.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

## Etapa 2: Definir Opções de Rasterização
A classe `RasterizationOptions` define como os dados vetoriais são convertidos em imagens raster, incluindo largura da página, altura e cor de fundo.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Defina as opções de rasterização para configurar a largura e a altura da página para a saída PNG.

## Etapa 3: Definir Opções PNG
A classe `PngOptions` contém configurações específicas para a saída PNG, como nível de compressão e profundidade de cor.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Crie opções PNG e associe as opções de rasterização definidas anteriormente.

## Etapa 4: Especificar Caminho de Saída
O caminho de saída determina onde o arquivo PNG gerado será salvo.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Defina o caminho de saída para o arquivo PNG, garantindo que ele tenha o mesmo nome do arquivo de origem com a extensão ".png". Finalmente, salve a imagem convertida.

## Problemas Comuns e Soluções
- **Fontes ou estilos de linha ausentes:** Certifique-se de que o IFC de origem referencia todos os recursos necessários; o Aspose.CAD incorpora ativos ausentes quando possível.
- **Arquivos grandes causam picos de memória:** Use a propriedade `MemoryLimit` em `RasterizationOptions` para limitar o uso de memória.
- **Cores incorretas:** Verifique se as definições de cor do IFC de origem estão em conformidade com o esquema IFC; o Aspose.CAD respeita o mapeamento padrão de cores.

## Perguntas Frequentes

**Q: Posso usar Aspose.CAD para .NET no macOS ou Linux?**  
A: Não, o Aspose.CAD para .NET foi projetado especificamente para ambientes Windows.

**Q: Existe uma licença temporária disponível para fins de teste?**  
A: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/) para avaliação.

**Q: Como posso obter suporte para Aspose.CAD?**  
A: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**Q: Onde posso encontrar documentação abrangente?**  
A: Consulte a [documentação Aspose.CAD](https://reference.aspose.com/cad/net/) para informações detalhadas e exemplos.

**Q: E se eu encontrar problemas durante a instalação?**  
A: Verifique a documentação ou procure ajuda no [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Última Atualização:** 2026-07-18  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriais Relacionados

- [Converter Desenho CAD para Imagem Raster no Aspose.CAD para .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Conversão de STL para PNG Facilitada com Aspose.CAD para .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Exportar Layouts CAD para Formatos de Imagem Raster no Aspose.CAD para .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}