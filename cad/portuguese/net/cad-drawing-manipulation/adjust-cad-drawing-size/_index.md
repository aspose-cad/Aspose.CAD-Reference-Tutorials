---
date: 2026-03-19
description: Aprenda a redimensionar desenhos CAD em .NET com Aspose.CAD, incluindo
  como dimensionar unidades de desenho CAD e ajustar o tamanho do layout. Siga nosso
  guia passo a passo.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Como Redimensionar Desenhos CAD com Aspose.CAD para .NET
url: /pt/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Redimensionar Desenhos CAD com Aspose.CAD para .NET

## Introdução

Se você precisa **como redimensionar CAD** arquivos diretamente da sua aplicação .NET, você está no lugar certo. Neste tutorial vamos mostrar como alterar as configurações de unidade CAD, escalar as dimensões do desenho CAD e ajustar o tamanho do CAD programaticamente usando Aspose.CAD para .NET. Ao final do guia você terá uma solução sólida e pronta para produção para redimensionar qualquer formato CAD suportado.

## Respostas Rápidas
- **Qual biblioteca é necessária?** Aspose.CAD para .NET  
- **Posso mudar o tipo de unidade?** Sim – defina `UnitType` em `CadRasterizationOptions`  
- **É necessária uma licença para produção?** Uma licença válida do Aspose.CAD é necessária para uso não‑trial  
- **Para qual formato de imagem o exemplo exporta?** BMP (mas qualquer formato raster suportado funciona)  
- **Quantas linhas de código?** Menos de 30 linhas para uma operação completa de redimensionamento  

## O que é “como redimensionar CAD” na prática?
Redimensionar um desenho CAD significa converter os dados vetoriais em uma imagem raster em uma escala ou unidade específica (por exemplo, centímetros, polegadas). Isso é útil quando você precisa incorporar desenhos em relatórios, gerar miniaturas ou integrar visualizações CAD em páginas web.

## Por que ajustar o tamanho do CAD com Aspose.CAD?
- **Sem software CAD externo** – tudo roda dentro do seu código .NET.  
- **Controle granular** sobre unidades, layouts e opções de rasterização.  
- **Suporte cross‑format** – o mesmo código funciona para DWG, DXF, DWF e mais.  

## Pré-requisitos

Antes de mergulharmos, certifique‑se de que você tem:

- Biblioteca Aspose.CAD para .NET: Baixe e instale a biblioteca a partir da [página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).  
- Desenho CAD de exemplo: Um arquivo como `sample.dwg` colocado no diretório de documentos do seu projeto.  

## Importar Namespaces

Primeiro, importe os namespaces que dão acesso às classes do Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: Carregar o Desenho CAD

Carregue o arquivo fonte em um objeto `Image`. Este objeto representa o desenho CAD na memória e será a base para todas as operações subsequentes.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Etapa 2: Criar BmpOptions (ou qualquer outro formato raster)

`BmpOptions` informa ao Aspose.CAD como renderizar os dados vetoriais ao salvá‑los como bitmap. Você pode trocar por `PngOptions`, `JpegOptions`, etc., dependendo do formato de destino.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Etapa 3: Definir CadRasterizationOptions

`CadRasterizationOptions` contém as configurações principais para escala, conversão de unidade e seleção de layout. Vinculá‑lo à propriedade `VectorRasterizationOptions` de `BmpOptions` garante que o rasterizador use suas configurações personalizadas.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Etapa 4: Definir UnitType (alterar unidade CAD)

Aqui alteramos a unidade CAD do padrão para centímetros. É aqui que a palavra‑chave **change cad unit** reside, e influencia diretamente o tamanho final da imagem.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Etapa 5: Escolher Layouts (definir layouts CAD)

Se o seu desenho contém múltiplos layouts (por exemplo, Model, Sheet1), especifique quais você deseja rasterizar. Selecionar o layout correto é essencial quando você **set cad layouts** para uma saída redimensionada.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Etapa 6: Exportar para BMP (redimensionar desenho CAD)

Finalmente, salve a imagem rasterizada. O arquivo de saída reflete o novo tamanho, unidade e layout configurados—completando efetivamente a operação de **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Agora você tem um arquivo BMP que representa o desenho CAD redimensionado, pronto para processamento adicional ou exibição.

## Problemas Comuns e Soluções

| Problema | Por que acontece | Correção |
|----------|------------------|----------|
| A saída está borrada | DPI (pontos por polegada) padrão baixo | Defina `cadRasterizationOptions.Resolution = 300;` antes de salvar |
| Layout errado aparece | Erro de digitação no nome do layout | Verifique o nome exato do layout usando um visualizador CAD ou a coleção `Layouts` |
| Conversão de unidade parece errada | Mistura de unidades métricas e imperiais | Garanta que `UnitType` corresponda ao sistema de medida desejado |

## Perguntas Frequentes

### Q1: O Aspose.CAD para .NET é compatível com todos os formatos CAD?

**A1:** Aspose.CAD para .NET suporta uma ampla variedade de formatos CAD, incluindo DWG, DXF, DWF e mais. Consulte a [documentação](https://reference.aspose.com/cad/net/) para a lista completa.

### Q2: Posso redimensionar vários layouts simultaneamente?

**A2:** Sim, você pode redimensionar múltiplos layouts ajustando o array `Layouts` em `CadRasterizationOptions`.

### Q3: Onde posso obter suporte para Aspose.CAD para .NET?

**A3:** Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e assistência.

### Q4: Existe uma versão de avaliação gratuita disponível?

**A4:** Sim, você pode explorar um [free trial](https://releases.aspose.com/) para avaliar os recursos do Aspose.CAD para .NET.

### Q5: Como posso obter uma licença temporária para Aspose.CAD para .NET?

**A5:** Obtenha uma licença temporária para fins de teste [aqui](https://purchase.aspose.com/temporary-license/).

## Perguntas Frequentes

**Q: Como escalo um desenho CAD sem mudar o tipo de unidade?**  
A: Ajuste a propriedade `Zoom` de `CadRasterizationOptions` (por exemplo, `cadRasterizationOptions.Zoom = 2.0;`) para dobrar o tamanho mantendo a unidade original.

**Q: Posso exportar para formatos diferentes de BMP?**  
A: Absolutamente. Substitua `BmpOptions` por `PngOptions`, `JpegOptions` ou qualquer outra classe de formato raster suportado.

**Q: É possível processar em lote uma pasta de desenhos?**  
A: Sim. Percorra os arquivos em um diretório, aplique a mesma lógica de rasterização e salve cada saída com um nome único.

---

**Última atualização:** 2026-03-19  
**Testado com:** Aspose.CAD para .NET 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}