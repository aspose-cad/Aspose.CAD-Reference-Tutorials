---
date: 2026-03-02
description: Aprenda a criar um PDF único com diferentes layouts usando Aspise.CAD
  para .NET – converta CAD para PDF, exporte DWG para PDF e salve CAD como PDF de
  forma eficiente.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Como criar um único PDF com diferentes layouts - Guia Aspose.CAD
url: /pt/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como criar PDF único com diferentes layouts - Guia Aspose.CAD

## Introdução

Se você precisa **criar PDF único** arquivos que contenham vários layouts CAD, você está no lugar certo. Neste tutorial, percorreremos os passos exatos necessários para converter desenhos CAD em um documento PDF, lidando com múltiplos layouts ao longo do caminho. Você verá como o Aspose.CAD for .NET facilita **converter CAD para PDF**, **exportar DWG para PDF** e **salvar CAD como PDF** com apenas algumas linhas de código C#.

## Respostas rápidas
- **O que este tutorial cobre?** Gerar um PDF que inclua vários layouts CAD.  
- **Qual biblioteca é usada?** Aspose.CAD for .NET.  
- **Preciso de uma licença?** Um teste gratuito funciona para avaliação; uma licença é necessária para produção.  
- **Formatos CAD suportados?** DWG, DXF, DGN e muitos outros.  
- **Tempo típico de implementação?** Cerca de 10‑15 minutos para uma conversão básica.

## O que significa “criar PDF único” em um contexto CAD?

Criar um PDF único significa pegar um arquivo CAD fonte que pode conter várias definições de layout (espaços de papel) e mesclar cada layout em páginas separadas de um único documento PDF. Isso é especialmente útil para plantas arquitetônicas, esquemas de engenharia ou qualquer cenário em que o cliente espera um pacote PDF consolidado.

## Por que usar Aspose.CAD para esta tarefa?

- **Sem dependências externas** – puro .NET, sem necessidade de instalação do AutoCAD.  
- **Controle total sobre a rasterização** – você pode definir o tamanho da página, DPI e dimensões personalizadas do layout.  
- **Renderização de alta fidelidade** – os dados vetoriais são preservados quando possível, garantindo saída nítida.  
- **Pronto para lote** – o mesmo código pode ser colocado dentro de um loop para processar muitos desenhos automaticamente.

## Pré-requisitos

- Aspose.CAD for .NET: Certifique-se de que o Aspose.CAD for .NET está instalado. Você pode baixá-lo [aqui](https://releases.aspose.com/cad/net/).  
- Ambiente de desenvolvimento: Configure um ambiente de desenvolvimento .NET e tenha um entendimento básico de programação C#.

## Importar namespaces

Em seu projeto C#, inclua os namespaces necessários para aproveitar as funcionalidades do Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guia passo a passo

### Passo 1: Carregar a imagem CAD

Primeiro, carregue o arquivo CAD fonte (por exemplo, um desenho DWG). A classe `CadImage` fornece acesso a todos os layouts dentro do arquivo.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Passo 2: Personalizar opções de rasterização

Defina como cada layout deve ser rasterizado. Você pode definir um tamanho de página padrão e, em seguida, sobrescrevê-lo para layouts específicos usando `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Dica profissional:** Ajuste o DPI (`rasterizationOptions.Resolution`) se precisar de saída de alta resolução para desenhos detalhados.

### Passo 3: Definir opções de PDF

Envolva as configurações de rasterização dentro de um objeto `PdfOptions`. Isso indica ao Aspose.CAD para renderizar os dados CAD diretamente em um fluxo PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Passo 4: Salvar como PDF

Finalmente, invoque `Save` na instância `CadImage`, passando o nome do arquivo PDF de destino e as opções preparadas. A biblioteca gerará um PDF único contendo uma página para cada layout configurado.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Após esta chamada, você terá um PDF que combina os layouts “ANSI C Plot” e “8.5 x 11 Plot” em um documento coeso.

## Problemas comuns e solução de problemas

| Problema | Motivo | Correção |
|----------|--------|----------|
| Layouts ausentes no PDF | `LayoutPageSizes` não definido para um nome de layout | Verifique os nomes exatos dos layouts no arquivo CAD (sensível a maiúsculas/minúsculas). |
| Saída de baixa qualidade | DPI padrão é 96 | Defina `rasterizationOptions.Resolution = 300` (ou maior) antes de salvar. |
| Arquivo não encontrado | Caminho `MyDir` errado | Use `Path.Combine` para construir caminhos independentes de plataforma. |

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD for .NET com outros formatos CAD?

A1: Sim, o Aspose.CAD for .NET suporta vários formatos CAD como DWG, DXF, DGN e outros.

### Q2: Existe uma versão de avaliação gratuita disponível?

A2: Sim, você pode experimentar a versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q3: Como posso obter suporte para Aspose.CAD for .NET?

A3: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade.

### Q4: Onde posso encontrar documentação detalhada?

A4: Consulte a documentação [aqui](https://reference.aspose.com/cad/net/).

### Q5: Posso comprar uma licença para Aspose.CAD for .NET?

A5: Sim, você pode adquirir uma licença [aqui](https://purchase.aspose.com/buy).

**Perguntas adicionais**

**Q:** Como faço para **exportar DWG para PDF** com tamanhos de página personalizados?  
**A:** Use `CadRasterizationOptions.LayoutPageSizes` para mapear cada layout DWG para as dimensões de página PDF desejadas, como mostrado no Passo 2.

**Q:** É possível **salvar CAD como PDF** sem rasterizar dados vetoriais?  
**A:** O Aspose.CAD sempre rasteriza ao criar PDF, mas você pode aumentar o DPI para manter a fidelidade visual.

## Conclusão

Neste guia demonstramos como **criar PDF único** a partir de desenhos CAD que contêm múltiplos layouts, usando Aspose.CAD for .NET. Agora você tem os blocos de construção para **converter CAD para PDF**, **exportar DWG para PDF** e **salvar CAD como PDF** em um fluxo de trabalho único e automatizado. Experimente diferentes configurações de rasterização para atender aos requisitos de qualidade do seu projeto e integre este código em pipelines de processamento em lote maiores, conforme necessário.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-03-02  
**Testado com:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose