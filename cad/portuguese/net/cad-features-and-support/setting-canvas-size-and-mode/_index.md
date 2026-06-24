---
date: 2026-03-29
description: Aprenda como criar PDF a partir de CAD, definir o tamanho da tela e exportar
  CAD para PDF ou TIFF usando Aspose.CAD para .NET neste guia passo a passo.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Como criar PDF a partir de CAD: definir tamanho da tela e modo no Aspose.CAD
  para .NET'
url: /pt/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definindo o Tamanho da Tela e o Modo no Aspose.CAD para .NET

## Introdução

Pronto para **criar PDF a partir de CAD** arquivos enquanto controla as dimensões de saída? Neste tutorial, vamos percorrer a configuração do tamanho da tela e do modo, carregar um arquivo CAD e exportá‑lo para PDF ou TIFF com Aspose.CAD para .NET. Seja para **converter DXF para PDF**, gerar desenhos em alta resolução ou simplesmente ajustar a área de rasterização, os passos abaixo fornecerão uma solução robusta e pronta para produção.

## Respostas Rápidas
- **O que significa “criar PDF a partir de CAD”?** Converter um desenho CAD (por exemplo, DXF, DWG) em um documento PDF que preserva detalhes vetoriais e raster.  
- **Qual opção controla o tamanho da saída?** `CadRasterizationOptions.PageWidth` e `PageHeight` (tamanho da tela).  
- **Posso exportar para TIFF também?** Sim – use `TiffOptions` com as mesmas configurações de rasterização.  
- **Preciso de licença para produção?** É necessária uma licença comercial; uma versão de avaliação gratuita está disponível.  
- **Versões .NET suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## O que é “criar PDF a partir de CAD”?
Criar um PDF a partir de CAD significa renderizar o desenho CAD em um formato orientado a página (PDF) que pode ser visualizado, impresso ou compartilhado sem a necessidade de software CAD. Aspose.CAD realiza o trabalho pesado, permitindo que você defina o tamanho da tela, a escala e o formato de saída.

## Por que definir o tamanho da tela ao criar PDF a partir de CAD?
Definir o tamanho da tela dá controle preciso sobre a resolução e as dimensões do PDF ou TIFF resultante. Isso é especialmente útil quando:
- Preparar desenhos para impressão em tamanhos de papel específicos.  
- Gerar miniaturas ou imagens em alta resolução para visualização na web.  
- Garantir layout consistente em vários documentos.

## Pré-requisitos

- Biblioteca Aspose.CAD: Baixe e instale a biblioteca Aspose.CAD a partir do [site Aspose.CAD](https://releases.aspose.com/cad/net/).
- Ambiente de Desenvolvimento: Certifique-se de que você tem um ambiente de desenvolvimento .NET configurado em sua máquina.
- Arquivo CAD de Exemplo: Para este tutorial, usaremos um arquivo DXF de exemplo. Você pode encontrar um na [documentação Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importar Namespaces

Primeiro, importe os namespaces necessários para o processamento de CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Como Criar PDF a partir de CAD com Tamanho de Tela Personalizado

### Etapa 1: Carregar Arquivo CAD

Começamos **carregando o arquivo CAD** (por exemplo, um DXF) em um objeto `Image`. Este é o ponto onde você **carrega o arquivo CAD** na memória.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Etapa 2: Criar CadRasterizationOptions

Crie uma instância `CadRasterizationOptions` e defina o tamanho da tela. As propriedades `PageWidth` e `PageHeight` permitem que você **defina o tamanho da tela** nas dimensões exatas necessárias.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Etapa 3: Criar PdfOptions (Exportar CAD para PDF)

Vincule as configurações de rasterização a um objeto `PdfOptions`. Esta configuração permite que você **exporte CAD para PDF** com a tela personalizada que definiu.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Etapa 4: Exportar para PDF (Converter DXF para PDF)

Agora salve a imagem como PDF. Esta etapa **cria PDF a partir de CAD** usando as opções que configuramos.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Etapa 5: Criar TiffOptions (Exportar CAD para TIFF)

Se também precisar de uma imagem raster, configure `TiffOptions`. As mesmas opções de rasterização são reutilizadas, de modo que a **exportação de CAD para TIFF** respeita o tamanho da tela.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Etapa 6: Exportar para TIFF

Finalmente, salve o desenho como um arquivo TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Problemas Comuns e Soluções

- **A tela aparece recortada** – Verifique se `AutomaticLayoutsScaling` está definido como `true` e `NoScaling` como `false` para que o desenho escale para caber na tela.  
- **PDF de baixa resolução** – Aumente `PageWidth`/`PageHeight` ou defina `Resolution` em `CadRasterizationOptions`.  
- **Erro de arquivo não encontrado** – Certifique‑se de que `MyDir` aponta para um diretório válido e que o nome do arquivo DXF corresponde exatamente.

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD com outras bibliotecas .NET?
A1: Sim, Aspose.CAD integra‑se perfeitamente com outras bibliotecas .NET, proporcionando recursos avançados para manipulação de CAD.

### Q2: Existe uma versão de avaliação gratuita para Aspose.CAD?
A2: Sim, você pode explorar os recursos do Aspose.CAD com uma avaliação gratuita. Visite [aqui](https://releases.aspose.com/) para começar.

### Q3: Como posso obter suporte para Aspose.CAD?
A3: Para suporte e discussões, visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Onde posso encontrar documentação completa para Aspose.CAD?
A4: Consulte a [documentação Aspose.CAD](https://reference.aspose.com/cad/net/) para informações detalhadas e exemplos.

### Q5: Como comprar Aspose.CAD para .NET?
A5: Para adquirir o Aspose.CAD, visite a [página de compra](https://purchase.aspose.com/buy).

**Perguntas Adicionais**

**Q: Posso exportar um desenho CAD de várias páginas para um único PDF?**  
**A:** Sim. Defina `PageCount` em `CadRasterizationOptions` e a biblioteca concatenará as páginas em um único PDF.

**Q: O tamanho da tela afeta a qualidade dos dados vetoriais?**  
**A:** Os dados vetoriais permanecem independentes da resolução; o tamanho da tela influencia apenas os elementos rasterizados e a resolução da imagem.

---

**Última Atualização:** 2026-03-29  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}