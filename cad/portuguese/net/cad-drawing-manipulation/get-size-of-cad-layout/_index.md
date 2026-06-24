---
date: 2026-03-21
description: Aprenda como obter o tamanho do layout CAD no .NET usando Aspose.CAD.
  Siga nosso guia passo a passo para manipulação eficiente de arquivos CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Obter o tamanho do layout CAD no Aspose.CAD para .NET
url: /pt/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obter o Tamanho do Layout CAD no Aspose.CAD para .NET

## Introdução

Neste tutorial abrangente, você descobrirá **como obter o tamanho do layout CAD** usando a biblioteca Aspose.CAD para .NET. Seja construindo um visualizador CAD, gerando miniaturas ou precisando de dimensões precisas do layout para processamento posterior, conhecer o tamanho exato de cada layout é essencial. Percorreremos todo o fluxo de trabalho — desde o carregamento de um desenho até a extração das dimensões do layout e, opcionalmente, a gravação deles como imagens — para que você possa integrar essa funcionalidade em suas próprias aplicações com confiança.

## Respostas rápidas
- **O que significa “obter tamanho do layout CAD”?** Significa recuperar a largura e a altura (nas unidades do desenho) de cada layout não‑vazio em um arquivo CAD.  
- **Qual biblioteca oferece isso?** Aspose.CAD para .NET fornece uma API simples para acessar informações de layout.  
- **Preciso de licença?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para uso em produção.  
- **Formatos suportados?** DWG, DXF e muitos outros formatos CAD/BIM são totalmente suportados.  
- **Tempo típico de implementação?** Cerca de 10‑15 minutos para uma rotina básica de recuperação de tamanho.

## O que é “obter tamanho do layout CAD”?
Obter o tamanho do layout CAD significa extrair as extensões geométricas de cada layout (espaço papel) definido em um desenho CAD. Essas extensões são expressas nas unidades nativas do desenho (geralmente milímetros ou polegadas) e são úteis para tarefas como dimensionamento, impressão ou geração de imagens de pré‑visualização.

## Por que recuperar o tamanho do layout CAD com Aspose.CAD?
- **Nenhum software CAD necessário** – Funciona completamente no lado do servidor.  
- **Multiplataforma** – Compatível com .NET Framework, .NET Core e .NET 5/6+.  
- **Medições precisas** – Retorna as extensões exatas armazenadas no arquivo, evitando análises manuais.  
- **Integração fácil** – Chamadas de API simples se encaixam naturalmente em projetos C# existentes.

## Pré‑requisitos

Antes de mergulharmos no código, certifique‑se de que você tem o seguinte:

- Aspose.CAD para .NET instalado. Você pode baixá‑lo na [página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Um ou mais arquivos CAD (DWG, DXF, etc.) que você deseja analisar. Este guia usa `conic_pyramid.dxf` e `Bottom_plate.dwg` como arquivos de exemplo.

## Importar namespaces

No seu projeto .NET, comece importando os namespaces necessários:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Etapa 1: Configurar o diretório do documento

Defina a pasta que contém seus arquivos CAD. Substitua o placeholder pelo caminho real na sua máquina.

```csharp
string MyDir = "Your Document Directory";
```

## Etapa 2: Especificar caminhos dos arquivos CAD

Crie um array que aponta para cada arquivo CAD que você deseja processar.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Etapa 3: Iterar pelos arquivos CAD

Carregue cada arquivo, detecte seu formato e prepare‑se para extrair as informações de layout.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Etapa 4: Obter layouts não‑vazios

Precisamos de um método auxiliar que retorne apenas os layouts que realmente contêm entidades de desenho. Layouts vazios são ignorados porque não têm tamanho a relatar.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Etapa 5: Obter layouts para arquivos DWG

Arquivos DWG armazenam informações de layout na tabela `HeaderVariables`. O método a seguir extrai os nomes de todos os layouts não‑vazios de um desenho DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Etapa 6: Obter layouts para arquivos DXF

Arquivos DXF usam uma estrutura diferente. Este método analisa a coleção `Tables` para encontrar layouts de espaço papel que contêm entidades.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Etapa 7: Recuperar o tamanho do layout e salvar como imagem

Por fim, percorra cada layout descoberto, leia suas extensões e, opcionalmente, renderize o layout em um arquivo de imagem para verificação visual.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Problemas comuns e dicas

- **Nomes de layout ausentes:** Certifique‑se de que o arquivo CAD realmente contém layouts de espaço papel; alguns arquivos possuem apenas espaço modelo.  
- **Unidades incorretas:** O tamanho é retornado nas unidades nativas do desenho. Converta para milímetros ou polegadas, se necessário.  
- **Desempenho:** Carregar arquivos DWG/DXF muito grandes pode consumir muita memória; considere processar os arquivos de forma assíncrona ou em lotes.

## Perguntas frequentes

**P: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?**  
R: Sim, o Aspose.CAD suporta uma ampla gama de formatos, incluindo DWG, DXF, DGN e muitos tipos de arquivos BIM.

**P: Posso personalizar as opções de gravação da imagem?**  
R: Absolutamente! Você pode ajustar o `CadRasterizationOptions` (formato, resolução, cor de fundo, etc.) para atender às suas necessidades específicas.

**P: Onde posso encontrar documentação adicional?**  
R: Consulte a [documentação do Aspose.CAD](https://reference.aspose.com/cad/net/) para referências detalhadas da API e mais exemplos.

**P: Existe uma avaliação gratuita disponível?**  
R: Sim, você pode explorar o Aspose.CAD com uma [avaliação gratuita](https://releases.aspose.com/).

**P: Como posso obter suporte técnico?**  
R: Para suporte técnico, visite o [fórum do Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Última atualização:** 2026-03-21  
**Testado com:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}