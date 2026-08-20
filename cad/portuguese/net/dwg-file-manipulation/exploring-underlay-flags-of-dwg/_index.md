---
date: 2026-04-09
description: Aprenda como converter DWG para imagem e como ler as flags de subfundo
  usando Aspose.CAD para .NET neste guia passo a passo.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Explorando as bandeiras de underlay de arquivos DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DWG para Imagem – Explorando as Flags de Underlay de Arquivos DWG
  – Tutorial Aspose.CAD
url: /pt/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Explorando Bandeiras de Underlay de Arquivos DWG - Tutorial Aspose.CAD

## Introdução

Se você está mergulhando no complexo mundo dos arquivos CAD, especificamente arquivos DWG, e deseja **converter DWG em imagem** enquanto também descobre **como ler as bandeiras de underlay**, você está no lugar certo. Este tutorial orienta você passo a passo usando a poderosa biblioteca Aspose.CAD para .NET, para que possa extrair informações de underlay e renderizar o desenho como uma imagem com confiança.

## Respostas Rápidas
- **O que significa “converter DWG em imagem”?**  
  Significa renderizar um desenho DWG em um formato raster (PNG, JPEG, etc.) usando Aspose.CAD.
- **Qual método revela as bandeiras de underlay?**  
  Acesse a propriedade `Flags` do objeto `CadUnderlay` após carregar o DWG.
- **Preciso de uma licença para Aspose.CAD?**  
  Uma licença temporária está disponível para avaliação; uma licença completa é necessária para produção.
- **Quais versões do .NET são suportadas?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 e posteriores.
- **Posso extrair a geometria do underlay?**  
  Sim – o caminho do underlay, ponto de inserção, escala, rotação e estados das bandeiras são todos acessíveis.

## O que é “converter DWG em imagem” e por que isso importa?

Converter um arquivo DWG em uma imagem permite exibir desenhos CAD em navegadores, incorporá-los em relatórios ou compartilhá-los com partes interessadas que não possuem um visualizador CAD. Durante a renderização, muitas vezes é necessário inspecionar objetos **underlay** (por exemplo, referências DGN) para garantir que apareçam corretamente. Compreender as bandeiras de underlay ajuda a solucionar problemas de recorte, renderização em monocromático e de visibilidade antes de gerar a imagem final.

## Pré-requisitos

- Um entendimento básico de programação em C# e .NET.  
- Biblioteca **Aspose.CAD for .NET** instalada. Se ainda não a possui, faça o download **[aqui](https://releases.aspose.com/cad/net/)**.  
- Um arquivo DWG para teste – o arquivo de exemplo **“BlockRefDgn.dwg”** é usado ao longo deste guia.

## Importar Namespaces

Para começar, importe os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: Carregar o Arquivo DWG e Converter para `CadImage`

Primeiro, carregue o arquivo DWG e faça o cast para `CadImage`. Este objeto fornece acesso a todas as entidades do desenho, incluindo underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Etapa 2: Iterar pelas Entidades

Em seguida, percorra cada entidade no desenho. É aqui que você localizará os objetos underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Etapa 3: Verificar o Tipo `CadDgnUnderlay`

Identifique as entidades underlay verificando seu tipo em tempo de execução. A classe `CadDgnUnderlay` representa underlays DGN incorporados em um DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Etapa 4: Acessar as Bandeiras de Underlay

Depois de obter um `CadDgnUnderlay`, faça o cast para `CadUnderlay` para ler suas propriedades e estados das bandeiras. As bandeiras indicam se o underlay está visível, recortado ou renderizado em monocromático.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### O que a saída indica

- **UnderlayPath / UnderlayName** – onde o arquivo DGN externo está localizado.  
- **InsertionPoint (X, Y)** – coordenadas onde o underlay é colocado no espaço DWG.  
- **RotationAngle** – rotação aplicada ao underlay.  
- **ScaleX / ScaleY / ScaleZ** – fatores de escala para cada eixo.  
- **Flags** – valores booleanos que indicam visibilidade (`UnderlayIsOn`), recorte (`ClippingIsOn`) e renderização em monocromático (`Monochrome`).

## Problemas Comuns & Soluções

| Problema | Razão | Solução |
|----------|-------|---------|
| Nenhuma saída para verificações de bandeira | As bandeiras de underlay são definidas como 0 quando o underlay está desativado. | Certifique-se de que o DWG realmente contém um underlay ativo ou altere a visibilidade no arquivo CAD de origem. |
| Exceção `Invalid cast` | A entidade não é um `CadDgnUnderlay`. | Verifique a condição `if (entity is CadDgnUnderlay)` antes de fazer o cast. |
| Falha na renderização da imagem após extração de bandeira | O underlay pode estar recortado ou desativado, resultando em uma área em branco. | Ajuste as bandeiras (`UnderlayIsOn = true`, `ClippingIsOn = false`) antes de renderizar a imagem final. |

## Perguntas Frequentes

### Q1: Posso usar Aspose.CAD para .NET com outros formatos de arquivo CAD?

A1: Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF, DGN e outros. Consulte a documentação para a lista completa.

### Q2: Existe uma licença temporária disponível para Aspose.CAD para .NET?

A2: Sim, você pode obter uma licença temporária **[aqui](https://purchase.aspose.com/temporary-license/)**.

### Q3: Onde posso encontrar suporte para Aspose.CAD para .NET?

A3: Visite o fórum de suporte **[aqui](https://forum.aspose.com/c/cad/19)** para obter assistência.

### Q4: Como comprar Aspose.CAD para .NET?

A4: Adquira a biblioteca **[aqui](https://purchase.aspose.com/buy)**.

### Q5: Existe uma versão de avaliação gratuita?

A5: Sim, você pode acessar a versão de avaliação gratuita **[aqui](https://releases.aspose.com/)**.

## Conclusão

Parabéns! Você aprendeu com sucesso **como converter DWG em imagem** enquanto domina **como ler as bandeiras de underlay** usando Aspose.CAD para .NET. Com esse conhecimento você pode:

- Renderizar desenhos DWG como imagens raster para cenários web ou de relatórios.  
- Inspecionar e manipular propriedades de underlay para garantir a exibição correta.  
- Depurar problemas de visibilidade, recorte e monocromático antes da geração da imagem final.

Sinta-se à vontade para explorar outros recursos do Aspose.CAD, como gerenciamento de camadas, extração de texto e conversão em lote, para ampliar ainda mais seus fluxos de trabalho de automação CAD.

---

**Última Atualização:** 2026-04-09  
**Testado com:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}