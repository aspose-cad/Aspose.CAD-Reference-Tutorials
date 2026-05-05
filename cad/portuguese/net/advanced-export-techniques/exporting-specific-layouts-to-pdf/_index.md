---
date: 2026-03-13
description: Aprenda a definir opções de rasterização CAD e exportar layouts DWG específicos
  para PDF usando Aspose.CAD para .NET – o guia definitivo para criar PDF a partir
  de um arquivo CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Definir opções de rasterização CAD – Exportar layouts específicos para PDF
  - Guia Aspose.CAD
url: /pt/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando Layouts Específicos para PDF - Guia Aspose.CAD

## Introdução

Neste tutorial você descobrirá **como definir opções de rasterização CAD** para que possa exportar um único layout — ou vários layouts — de um arquivo DWG diretamente para PDF. Aspose.CAD para .NET torna o processo de *dwg to pdf conversion c#* simples, dando a você controle total sobre o tamanho da página, resolução e seleção de layout. Ao final do guia, você será capaz de **criar PDF a partir de arquivo CAD** com apenas algumas linhas de código.

## Respostas Rápidas
- **O que faz “set cad rasterization options”?**  
  Ele informa ao Aspose.CAD como renderizar dados vetoriais (layouts, camadas, espessuras de linha) em páginas PDF rasterizadas.  
- **Qual método exporta um layout DWG para PDF?**  
  Use `Image.Save` com um `PdfOptions` configurado que contém seu `CadRasterizationOptions`.  
- **Posso exportar mais de um layout de uma vez?**  
  Sim – forneça um array de nomes de layout na propriedade `Layouts`.  
- **Preciso de uma licença para uso em produção?**  
  É necessária uma licença comercial; um teste gratuito está disponível para avaliação.  
- **Quais versões do .NET são suportadas?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 e posteriores.

## O que é “set cad rasterization options”?

`CadRasterizationOptions` é a classe que controla como as entidades CAD são rasterizadas ao converter para formatos baseados em raster, como PDF. Ao configurar suas propriedades — dimensões da página, seleção de layout, cor de fundo, etc. — você determina o resultado visual da operação **export dwg layout to pdf**.

## Por que definir opções de rasterização CAD?

- **Precisão** – Preserve espessuras de linha e escalas exatamente como aparecem no desenho CAD original.  
- **Desempenho** – Renderize apenas os layouts que você precisa, reduzindo o tamanho do arquivo e o tempo de processamento.  
- **Flexibilidade** – Ajuste a largura/altura da página, DPI e fundo para corresponder aos seus padrões de relatório.  

## Pré-requisitos

Antes de mergulharmos no código, certifique-se de que você tem:

- **Aspose.CAD for .NET** instalado. Você pode baixá-lo [aqui](https://releases.aspose.com/cad/net/).  
- Um ambiente de desenvolvimento .NET (Visual Studio, VS Code ou qualquer IDE de sua preferência).  
- Um arquivo DWG que contenha ao menos um layout (o arquivo de exemplo usado aqui é `visualization_-_conference_room.dwg`).

## Importar Namespaces

No seu projeto .NET, importe os namespaces necessários para Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guia Passo a Passo

### Passo 1: Carregar o arquivo DWG

Primeiro, aponte o Aspose.CAD para o arquivo DWG de origem que você deseja converter.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Passo 2: Definir **CadRasterizationOptions**

Aqui configuramos as definições de rasterização que determinam o tamanho da página PDF e a resolução.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Dica profissional:** Ajuste `PageWidth` e `PageHeight` para corresponder às dimensões do layout PDF de destino. Valores maiores aumentam o detalhe, mas também o tamanho do arquivo.

### Passo 3: Especificar o nome do layout

Informe ao Aspose.CAD quais layout(s) renderizar. Substitua `"Layout1"` pelo nome exato do layout no seu arquivo DWG.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Por que isso importa:** Ao limitar o array `Layouts` você evita exportar folhas indesejadas, tornando a operação **dwg to pdf conversion c#** mais rápida e o PDF resultante mais limpo.

### Passo 4: Criar `PdfOptions`

Vincule as configurações de rasterização às opções de exportação PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 5: Exportar para PDF

Finalmente, salve o layout renderizado como um arquivo PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Passo 6: Exibir uma mensagem de sucesso

Uma saída rápida no console confirma que a operação foi bem-sucedida.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Problemas Comuns & Soluções

| Problema | Causa | Correção |
|----------|-------|----------|
| **Nenhum PDF gerado** | O array `Layouts` não corresponde a nenhum nome de layout no DWG. | Verifique os nomes dos layouts usando um visualizador CAD e atualize a propriedade `Layouts`. |
| **Páginas em branco** | `PageWidth`/`PageHeight` definidos como 0 ou valores extremamente pequenos. | Use dimensões realistas (por exemplo, 1600 × 1600) ou deixe o Aspose calcular automaticamente omitindo essas propriedades. |
| **Escala incorreta** | DPI não definido quando é necessária saída de alta resolução. | Defina `rasterizationOptions.Resolution = 300;` (ou o DPI desejado) antes de exportar. |

## Perguntas Frequentes

**Q: Posso exportar vários layouts simultaneamente?**  
A: Sim, basta modificar o array `Layouts` no Passo 3 para incluir todos os nomes de layout desejados, por exemplo, `new string[] { "Layout1", "Layout2" }`.

**Q: O Aspose.CAD é compatível com outros formatos de arquivo CAD?**  
A: Absolutamente. Ele suporta DWG, DXF, DWF, DGN e muitos outros formatos.

**Q: Como posso ajustar as configurações de saída PDF além do tamanho da página?**  
A: Explore propriedades adicionais de `CadRasterizationOptions` como `Resolution`, `BackgroundColor` e `DrawType` para ajustar finamente o resultado.

**Q: Onde posso encontrar documentação adicional do Aspose.CAD?**  
A: Visite a [documentação](https://reference.aspose.com/cad/net/) para referências detalhadas da API e exemplos.

**Q: Existe uma versão de teste gratuita disponível?**  
A: Sim, você pode acessar o teste gratuito [aqui](https://releases.aspose.com/).

## Conclusão

Agora você aprendeu como **definir opções de rasterização CAD** e usá‑las para **exportar layouts DWG específicos para PDF** com Aspose.CAD para .NET. Essa abordagem oferece controle preciso sobre o processo de conversão, permitindo integrar a funcionalidade CAD‑para‑PDF em qualquer aplicação C# de forma rápida e confiável.

---

**Última Atualização:** 2026-03-13  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}