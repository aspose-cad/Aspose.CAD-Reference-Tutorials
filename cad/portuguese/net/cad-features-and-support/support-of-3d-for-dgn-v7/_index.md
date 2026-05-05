---
date: 2026-03-29
description: Aprenda a configurar as opções de rasterização CAD e exportar DGN para
  PDF com suporte 3D usando Aspose.CAD para .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Configurar opções de rasterização CAD para DGN V7 3D
url: /pt/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configurar Opções de Rasterização CAD para DGN V7 3D

## Introdução

Neste tutorial abrangente, você aprenderá **como configurar opções de rasterização CAD** para exportar um arquivo DGN V7 3‑D para PDF usando Aspose.CAD para .NET. Seja você quem está construindo um visualizador CAD, uma ferramenta de relatórios ou um pipeline de conversão automatizada, dominar essas configurações lhe dá controle preciso sobre tamanho da página, escala de layout, cores de fundo e as visualizações específicas que deseja renderizar. Vamos percorrer o processo passo a passo.

## Respostas Rápidas
- **O que significa “configurar opções de rasterização CAD”?**  
  Refere‑se à definição de propriedades como dimensões da página, escala, cor de fundo e seleção de layout antes de converter um arquivo CAD para um formato raster (por exemplo, PDF).
- **Como exportar DGN para PDF com suporte 3‑D?**  
  Carregue o DGN com `DgnImage`, defina `PdfOptions` + `CadRasterizationOptions`, então chame `Save`.
- **Preciso de uma licença para uso em produção?**  
  Sim – uma licença comercial é necessária para implantação; um teste gratuito está disponível.
- **Quais versões do .NET são suportadas?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Posso escolher visualizações específicas para exportar?**  
  Absolutamente – defina o array `Layouts` nas opções de rasterização.

## O que é “configurar opções de rasterização CAD”?

Configurar opções de rasterização CAD significa personalizar como um desenho CAD é rasterizado (convertido de vetor para bitmap ou PDF). Ao ajustar essas configurações, você controla a saída visual, desempenho e tamanho do arquivo do documento resultante.

## Por que usar Aspose.CAD para exportação 3‑D DGN V7?

- **Integração completa com .NET – sem necessidade de COM ou DLLs nativas.**  
- **Suporta geometria 3‑D – mantém informações de profundidade ao renderizar para PDF.**  
- **Controle granular – escolha layouts exatos, escala e cores de fundo.**  
- **Multiplataforma – funciona no Windows, Linux e macOS com .NET Core.**

## Pré-requisitos

Antes de começar, certifique‑se de que você tem:

- **Aspose.CAD for .NET** – faça o download a partir de [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** ou qualquer IDE .NET compatível.  
- **Um arquivo DGN de exemplo** – para este guia usaremos `Nikon_D90_Camera.dgn` (incluído no pacote de exemplos da Aspose).  

Agora que tudo está pronto, vamos mergulhar no código.

## Importar Namespaces

No seu projeto .NET, importe os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Etapa 1: Configurar o Diretório do Documento

Crie uma variável que aponte para a pasta onde seu DGN de origem e os arquivos de saída estarão localizados.

```csharp
string MyDir = "Your Document Directory";
```

## Etapa 2: Carregar o Arquivo DGN

Carregue o arquivo DGN como um `DgnImage`. Esse objeto fornece acesso aos dados CAD e ao pipeline de rasterização.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Etapa 3: Configurar Opções de Exportação PDF (Configurar Opções de Rasterização CAD)

Aqui **configuramos opções de rasterização CAD** que determinam como o modelo 3‑D será renderizado para PDF. Você pode ajustar o tamanho da página, habilitar a escala automática de layout, definir uma cor de fundo e escolher os layouts (visualizações) exatos que deseja exportar.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Etapa 4: Salvar a Imagem Rasterizada

Finalmente, exporte o DGN para um arquivo PDF usando as opções que você acabou de configurar.

```csharp
dgnImage.Save(outFile, options);
```

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|---------|
| **Saída PDF em branco** | Verifique se o array `Layouts` contém os identificadores de visualização corretos presentes no arquivo DGN. |
| **Cores incorretas** | Certifique‑se de que `BackgroundColor` está definido para o valor desejado; use `Color.White` para um fundo claro. |
| **Gargalo de desempenho em arquivos grandes** | Habilite `AutomaticLayoutsScaling` e considere reduzir `PageWidth/PageHeight` para uma resolução raster menor. |
| **Exceção de licença** | Instale uma licença válida do Aspose.CAD antes de carregar a imagem para evitar marcas d'água de avaliação. |

## Perguntas Frequentes

**Q: Posso usar Aspose.CAD para .NET com outros formatos de arquivo CAD?**  
A: Sim, o Aspose.CAD suporta DWG, DXF, DWF, DGN e muitos outros formatos.

**Q: Como posso tratar exceções ao trabalhar com Aspose.CAD?**  
A: Envolva seu código em um bloco `try‑catch` e inspecione `Aspose.CAD.CADException` para obter informações detalhadas sobre o erro.

**Q: O Aspose.CAD é adequado para projetos comerciais?**  
A: Absolutamente. Você pode adquirir uma licença [here](https://purchase.aspose.com/buy).

**Q: Posso experimentar o Aspose.CAD para .NET antes de comprar?**  
A: Sim, um teste gratuito está disponível [here](https://releases.aspose.com/).

**Q: Onde posso encontrar suporte da comunidade para Aspose.CAD?**  
A: Participe do fórum de discussão [here](https://forum.aspose.com/c/cad/19).

---

**Última atualização:** 2026-03-29  
**Testado com:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}