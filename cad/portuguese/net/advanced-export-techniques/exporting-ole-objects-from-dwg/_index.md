---
description: Aprenda a converter DWG para PNG e extrair objetos OLE de arquivos DWG
  usando Aspose.CAD para .NET – um guia rápido e focado em código.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converter DWG para PNG e Exportar Objetos OLE - Tutorial Aspose.CAD
url: /pt/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

 final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando Objetos OLE de Arquivos DWG - Tutorial Aspose.CAD

## Introdução

Se você precisa **converter DWG para PNG** enquanto extrai objetos OLE incorporados, você está no lugar certo. Aspose.CAD para .NET torna esse processo de duas etapas simples, permitindo automatizar a extração e rasterização em apenas algumas linhas de C#. Nos próximos minutos, vamos percorrer todo o fluxo de trabalho, desde a configuração do ambiente até salvar cada DWG como PNG que contém os dados OLE extraídos.

## Respostas Rápidas
- **O que este tutorial cobre?** Conversão de DWG para PNG e extração de objetos OLE usando Aspose.CAD para .NET.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Posso processar vários arquivos DWG ao mesmo tempo?** Sim – o exemplo percorre um array de nomes de arquivos.  
- **Onde posso encontrar mais exemplos?** Consulte a documentação oficial do Aspose.CAD e os links do fórum abaixo.

## O que é **convert DWG to PNG**?
Converter um DWG (desenho AutoCAD) para uma imagem PNG rasteriza os dados vetoriais, facilitando a visualização ou incorporação em páginas web, relatórios ou outras aplicações que não suportam DWG nativamente. Quando objetos OLE estão presentes, eles podem ser extraídos e salvos como ativos separados durante a conversão.

## Por que extrair objetos OLE de arquivos CAD?
Muitos desenhos DWG incorporam planilhas, gráficos ou outros documentos do Office como objetos OLE. Extraí‑los permite reutilizar os dados originais, automatizar relatórios ou migrar conteúdo para formatos mais recentes sem perder informações incorporadas.

## Pré‑requisitos

- Biblioteca Aspose.CAD para .NET: Certifique‑se de que a biblioteca está instalada. Você pode baixá‑la na [página de download do Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Diretório de Documentos: Configure um diretório onde seus arquivos DWG estão armazenados. Substitua `"Your Document Directory"` no trecho de código fornecido pelo caminho real.

## Importar Namespaces

No seu projeto .NET, importe os namespaces necessários:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guia Passo a Passo

### Etapa 1: Definir o Diretório de Documentos

```csharp
string MyDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` pelo caminho onde seus arquivos DWG estão localizados.

### Etapa 2: Listar os arquivos DWG que você deseja processar

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Etapa 3: Configurar opções de exportação para conversão PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Você pode ajustar `CadRasterizationOptions` (por exemplo, `PageWidth`, `PageHeight`, `BackgroundColor`) para corresponder à resolução de saída desejada.

### Etapa 4: Iterar por cada DWG e realizar a conversão

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Durante este loop, a biblioteca extrai automaticamente **objetos OLE** incorporados em cada desenho e os inclui no PNG gerado. Se precisar dos fluxos OLE brutos, pode acessar a coleção `cadImage.OleObjects` – uma maneira prática de **como extrair ole** programaticamente.

## Problemas Comuns & Solução de Problemas

- **Nome de layout ausente** – Certifique‑se de que o layout especificado (`"Layout1"` no exemplo) exista no DWG de origem; caso contrário, o rasterizador retornará ao espaço de modelo padrão.
- **Arquivos grandes causam pressão de memória** – Processar arquivos um de cada vez (conforme demonstrado) e descartar objetos `CadImage` rapidamente com `using`.
- **Cores inesperadas** – Defina `rasterizationOptions.BackgroundColor` para corresponder ao fundo do desenho se a transparência for necessária.

## Perguntas Frequentes

### Q1: O Aspose.CAD para .NET é adequado tanto para arquivos CAD junior quanto senior?
R1: Sim, Aspose.CAD para .NET é versátil e pode lidar com uma ampla variedade de arquivos CAD, incluindo variantes junior e senior.

### Q2: Posso personalizar opções de exportação para diferentes layouts?
R2: Absolutamente! Conforme mostrado no tutorial, você pode personalizar as opções de exportação, incluindo layouts, para atender às suas necessidades específicas.

### Q3: Onde posso encontrar documentação detalhada para Aspose.CAD para .NET?
R3: Explore a [documentação do Aspose.CAD para .NET](https://reference.aspose.com/cad/net/) para informações detalhadas e exemplos.

### Q4: Existe uma avaliação gratuita disponível?
R4: Sim, você pode experimentar os recursos do Aspose.CAD para .NET com uma avaliação gratuita. Visite [este link](https://releases.aspose.com/) para começar.

### Q5: Como posso obter suporte ou conectar-me com a comunidade?
R5: Para suporte e engajamento com a comunidade, visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q6: Como **extrair OLE de CAD** sem converter para PNG?
R6: Use a coleção `CadImage.OleObjects` após carregar o DWG; você pode percorrer cada `OleObject` e salvar seus dados brutos em um arquivo.

## Conclusão

Agora você viu como **converter DWG para PNG** enquanto extrai **objetos OLE** de forma contínua usando Aspose.CAD para .NET. Essa abordagem economiza tempo, elimina etapas manuais de copiar‑colar e integra‑se perfeitamente a pipelines automatizados. Sinta‑se à vontade para experimentar outros formatos raster (JPEG, BMP) ou explorar o rico conjunto de recursos de manipulação CAD que a Aspose oferece.

---

**Última atualização:** 2026-03-13  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}