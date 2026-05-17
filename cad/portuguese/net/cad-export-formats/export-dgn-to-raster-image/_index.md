---
date: 2026-03-24
description: Aprenda como converter DGN para PNG e salvar CAD como JPEG usando Aspose.CAD
  para .NET – um guia rápido para conversão de CAD em imagem.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Como Converter DGN para PNG no Aspose.CAD para .NET
url: /pt/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter DGN para PNG no Aspose.CAD para .NET

No desenvolvimento .NET moderno, **convert dgn to png** é uma necessidade comum quando você precisa exibir desenhos CAD na web ou incorporá‑los em relatórios. Aspose.CAD para .NET torna essa conversão simples, permitindo transformar um arquivo DGN em uma imagem raster de alta qualidade com apenas algumas linhas de código. Neste guia, percorreremos todo o processo, desde a configuração do projeto até a gravação do arquivo PNG (ou JPEG) final.

## Respostas Rápidas
- **Posso converter DGN para PNG com Aspose.CAD?** Sim – basta configurar as opções de rasterização e escolher a saída PNG ou JPEG.  
- **Preciso de uma licença para uso em produção?** Uma licença válida do Aspose.CAD é necessária para implantações que não sejam de avaliação.  
- **Quais versões do .NET são suportadas?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Quais formatos de imagem estão disponíveis?** PNG, JPEG, BMP, GIF, TIFF e mais.  
- **É necessário tratamento de exceções?** Absolutamente – envolva a conversão em try/catch para lidar com problemas de acesso a arquivos.

## O que é “convert dgn to png”?
Converter um arquivo DGN (MicroStation) para PNG significa rasterizar dados CAD vetoriais em uma imagem baseada em pixels. Isso é útil para geração de pré‑visualizações, incorporação de desenhos em e‑mails HTML ou criação de miniaturas para sistemas de gerenciamento de documentos.

## Por que usar Aspose.CAD para conversão de CAD para imagem?
- **Sem dependências externas** – funciona puramente em código gerenciado.  
- **Alta fidelidade** – preserva espessuras de linhas, camadas e cores.  
- **Saída flexível** – altere entre PNG, JPEG, BMP, etc., mudando uma única opção.  
- **Desempenho otimizado** – a rasterização é rápida mesmo para desenhos grandes.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

- **Aspose.CAD para .NET** instalado em seu projeto. Você pode baixá‑lo no [website](https://reference.aspose.com/cad/net/).  
- Um arquivo DGN de exemplo (por exemplo, `Nikon_D90_Camera.dgn`) colocado em um diretório conhecido.

## Importar Namespaces

Comece adicionando as declarações `using` necessárias para que você possa acessar as classes do Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Etapa 1: Carregar o Arquivo DGN

Carregue o DGN de origem em um objeto `CadImage`. Esse objeto representa o desenho CAD na memória e será a fonte para a rasterização.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Etapa 2: Definir Opções de Rasterização

Configure como o desenho CAD deve ser rasterizado. Você pode controlar o tamanho da imagem, escala e cor de fundo aqui.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Etapa 3: Escolher o Formato de Saída (PNG ou JPEG)

Embora o tutorial se concentre em PNG, você também pode querer **salvar cad como jpeg**. Crie o objeto de opções de imagem apropriado e anexe as configurações de rasterização.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Dica profissional:** Para gerar um arquivo PNG, substitua `new JpegOptions()` por `new PngOptions()`.

## Etapa 4: Salvar a Imagem Raster

Por fim, chame `Save` na instância `CadImage`, fornecendo o nome de arquivo desejado e o objeto de opções que você configurou.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Se você mudou para `PngOptions`, o arquivo será salvo como `ExportDGNToRasterImage_out.png`.

## Problemas Comuns e Soluções

| Problema | Causa | Correção |
|----------|-------|----------|
| **Imagem de saída em branco** | `NoScaling` configurado incorretamente ou layout não selecionado | Defina `AutomaticLayoutsScaling = true` ou especifique o layout desejado. |
| **Falta de memória para arquivos grandes** | Carregando DGN enorme sem streaming | Use `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Versão DGN não suportada** | Versões antigas do MicroStation | Certifique‑se de que você tem a versão mais recente do Aspose.CAD que suporta formatos legados. |

## Perguntas Frequentes

**Q: Posso exportar arquivos DGN para formatos além de JPEG?**  
A: Sim, o Aspose.CAD para .NET suporta PNG, BMP, GIF, TIFF e mais – basta trocar a classe de opções (por exemplo, `new PngOptions()`).

**Q: Como devo tratar exceções durante a conversão?**  
A: Envolva o código de conversão em um bloco `try/catch` e registre `Aspose.CAD.CadException` para obter informações detalhadas sobre o erro.

**Q: Existe uma versão de avaliação disponível para Aspose.CAD para .NET?**  
A: Sim, você pode explorar o produto com uma avaliação gratuita. Visite [aqui](https://releases.aspose.com/) para mais informações.

**Q: Onde posso buscar assistência ou discutir problemas relacionados ao Aspose.CAD para .NET?**  
A: Acesse o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**Q: Como obtenho uma licença temporária para Aspose.CAD para .NET?**  
A: Visite [este link](https://purchase.aspose.com/temporary-license/) para adquirir uma licença temporária para suas necessidades de desenvolvimento.

## Conclusão

Agora você aprendeu como **convert dgn to png** (ou JPEG) usando Aspose.CAD para .NET. Ajustando as opções de rasterização e trocando a classe de opções de imagem, você pode personalizar a saída para atender a qualquer requisito de projeto. Sinta‑se à vontade para experimentar diferentes tamanhos de página, configurações de DPI e formatos de arquivo para obter a imagem raster perfeita para sua aplicação.

---

**Última atualização:** 2026-03-24  
**Testado com:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}