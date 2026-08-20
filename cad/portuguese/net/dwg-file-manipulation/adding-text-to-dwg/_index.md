---
date: 2026-04-06
description: Aprenda a converter DWG para PDF e adicionar texto personalizado usando
  C# e Aspose.CAD. Este guia passo a passo aborda a geração de PDF a partir de DWG,
  a inserção de uma entidade de texto e a alteração da fonte do texto no DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Adicionando Texto a Arquivos DWG em C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DWG para PDF e Adicionar Texto em C# – Tutorial Aspose.CAD
url: /pt/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DWG para PDF e Adicionar Texto em C# – Tutorial Aspose.CAD

## Introdução

No mundo acelerado de CAD e desenvolvimento .NET, **converter DWG para PDF** enquanto insere anotações personalizadas é uma necessidade frequente. Seja para gerar desenhos imprimíveis para clientes ou incorporar notas dinâmicas diretamente em um DWG, o Aspose.CAD torna a tarefa simples. Neste tutorial você aprenderá a **converter DWG para PDF**, **adicionar uma entidade de texto** e até **alterar a fonte do texto DWG** usando C#.

## Respostas Rápidas
- **Qual biblioteca é a melhor para conversão de DWG‑para‑PDF?** Aspose.CAD for .NET  
- **Posso adicionar texto personalizado durante a conversão?** Sim – crie uma entidade `CadText` e adicione-a antes de salvar.  
- **Preciso de licença para uso em produção?** É necessária uma licença comercial; uma avaliação gratuita está disponível.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **É possível alterar a fonte do texto?** Sim, ajuste as propriedades do `CadText` como `StyleType` e `TextHeight`.

## O que é “converter dwg para pdf”?

Converter um arquivo DWG para PDF transforma um desenho CAD baseado em vetores em um documento amplamente compartilhável e independente de dispositivo. O PDF mantém a geometria e as camadas originais, permitindo ainda incorporar anotações, texto ou outros metadados. O Aspose.CAD lida com a rasterização e renderização vetorial automaticamente, de modo que você não precisa de nenhum software CAD de terceiros no servidor.

## Por que adicionar texto a um DWG antes da conversão?

Incorporar texto diretamente no DWG oferece controle total sobre posicionamento, estilo e atribuição de camada. Quando o arquivo for convertido para PDF, o texto aparecerá exatamente onde foi posicionado, preservando a intenção do design e eliminando a necessidade de pós‑processamento em um editor de PDF.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

- **Biblioteca Aspose.CAD** – faça o download a partir do [download link](https://releases.aspose.com/cad/net/).  
- **Um ambiente .NET funcional** (Visual Studio 2022, .NET 6 ou qualquer versão compatível).  
- **Uma pasta para seus arquivos de teste** – nos referiremos a ela como `MyDir` ao longo do guia.

Agora, vamos percorrer o processo passo a passo.

## Importar Namespaces

Adicione as declarações `using` necessárias para acessar as classes do Aspose.CAD.

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
using Aspose.CAD.ImageOptions;
```

## Etapa 1: Carregar o Arquivo DWG

Carregue seu arquivo DWG de origem em um objeto `Image`. Esse objeto fornece acesso às entidades CAD subjacentes.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Etapa 2: Criar um Objeto CadText (Inserir Entidade de Texto)

A classe `CadText` representa uma única linha de texto em um DWG. Aqui definimos seu estilo, valor, cor, camada e posição. Ajuste `StyleType` ou `TextHeight` para **alterar a fonte do texto DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Etapa 3: Adicionar a Entidade de Texto ao Model Space

O model space do DWG contém a maioria das entidades do desenho. Ao adicionar nosso `CadText` ao bloco `*Model_Space`, o texto passa a fazer parte do desenho.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Etapa 4: Configurar Opções de PDF (Gerar PDF a partir do DWG)

Configure as opções de rasterização que controlam como o DWG é renderizado em um PDF. Você pode ajustar o tamanho da página, tipo de desenho e layout.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Etapa 5: Salvar o DWG Modificado como PDF

Finalmente, exporte o desenho modificado. O PDF resultante inclui o texto recém‑inserido.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Dica profissional:** Se precisar de um PDF de resolução mais alta, aumente `PageHeight` e `PageWidth` proporcionalmente.

## Problemas Comuns & Soluções

| Issue | Reason | Fix |
|-------|--------|-----|
| Texto não aparece no PDF | Camada ou ID de cor incorretos | Certifique‑se de que `LayerName` exista e `ColorId` esteja definido para uma cor visível (ex.: 7 para branco). |
| Texto está fora de lugar | Coordenadas de alinhamento incorretas | Verifique os valores `FirstAlignment.X/Y` em relação às unidades do desenho. |
| PDF está em branco | Opções de rasterização não definidas | Defina `DrawType` como `UseObjectColor` ou `UseObjectLineWeight`. |

## Perguntas Frequentes (Existentes)

### Q1: O Aspose.CAD é compatível com todas as versões de arquivos DWG?
A1: O Aspose.CAD suporta uma ampla gama de versões de arquivos DWG, garantindo compatibilidade com diversos softwares CAD.

### Q2: Posso adicionar múltiplas entidades de texto a um único arquivo DWG usando Aspose.CAD?
A2: Sim, você pode adicionar múltiplas entidades de texto a um arquivo DWG repetindo o processo descrito no tutorial.

### Q3: Como posso alterar a fonte e o estilo do texto no Aspose.CAD?
A3: Para modificar a fonte e o estilo do texto, ajuste as propriedades do objeto `CadText` antes de adicioná‑lo ao arquivo DWG.

### Q4: Existem considerações de licenciamento ao usar o Aspose.CAD em um projeto comercial?
A5: Sim, garanta a conformidade com os termos de licenciamento do Aspose.CAD. Consulte [Aspose.CAD Purchase](https://purchase.aspose.com/buy) para detalhes.

### Q5: Onde posso buscar ajuda ou discutir dúvidas relacionadas ao Aspose.CAD?
A5: Visite o [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) para conectar‑se com a comunidade e obter suporte.

## Perguntas Frequentes Adicionais

**Q: Como gerar PDF a partir de DWG sem adicionar texto?**  
A: Pule a etapa de criação do `CadText` e configure diretamente `PdfOptions` antes de chamar `image.Save(...)`.

**Q: Posso mudar a cor do texto programaticamente?**  
A: Sim, defina `cadText.ColorId` para um número de cor ACI específico (ex.: 1 para vermelho).

**Q: É possível inserir texto multilinha?**  
A: Use `CadMText` para blocos de texto multilinha; a abordagem é semelhante ao `CadText`.

**Q: O Aspose.CAD suporta conversão em lote de vários arquivos DWG?**  
A: Absolutamente – percorra um diretório de arquivos DWG, aplique as mesmas etapas e salve cada um como PDF.

## Conclusão

Agora você tem um fluxo de trabalho completo e pronto para produção para **converter DWG para PDF**, **adicionar texto personalizado** e **personalizar a aparência do texto** usando C# e Aspose.CAD. Esta técnica é ideal para geração automática de desenhos, pipelines de relatórios ou qualquer cenário em que seja necessário enriquecer arquivos CAD em tempo real.

---

**Última atualização:** 2026-04-06  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}