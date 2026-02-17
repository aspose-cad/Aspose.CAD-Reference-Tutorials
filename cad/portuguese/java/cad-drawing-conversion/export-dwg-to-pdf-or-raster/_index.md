---
date: 2026-02-17
description: Aprenda como a biblioteca Java CAD Aspose.CAD for Java pode exportar
  DWG para PDF ou imagens raster rapidamente e com precisão.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Exportar DWG para PDF ou Raster usando a biblioteca Java CAD Aspose.CAD para
  Java
url: /pt/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG para PDF ou Raster Usando a biblioteca java cad Aspose.CAD for Java

## Introdução

No mundo dinâmico do design assistido por computador (CAD), o manuseio eficiente de desenhos é crucial. Com a **java cad library** **Aspose.CAD for Java** você pode **export dwg to pdf** — ou imagens raster — em apenas algumas linhas de código. Este tutorial orienta você por todo o processo, desde o carregamento de um arquivo DWG até a geração de um PDF de alta qualidade, destacando por que o Aspose.CAD Java é a biblioteca ideal para tarefas de conversão CAD.

## Respostas Rápidas
- **O que este tutorial cobre?** Exportação de arquivos DWG para PDF ou imagens raster usando Aspose.CAD for Java.  
- **Preciso de uma licença?** Uma licença temporária gratuita está disponível para avaliação; uma licença completa é necessária para produção.  
- **Qual versão do Java é suportada?** Qualquer runtime Java 8+ funciona com a última API Aspose.CAD Java.  
- **Posso converter DWG para outros formatos de imagem?** Sim – as mesmas opções de rasterização permitem gerar PNG, JPEG, BMP, etc.  
- **Quanto tempo leva a conversão?** Normalmente menos de um segundo para desenhos padrão; arquivos maiores podem levar alguns segundos.

## Por que a java cad library é a melhor escolha para conversão de DWG?

- **Implementação pura em Java** – sem DLLs nativas ou ferramentas externas.  
- **Manipulação precisa de unidades** – unidades métricas e imperiais são detectadas automaticamente.  
- **Saída raster de alta qualidade** – controle refinado de DPI e tamanho de página.  
- **Suporte total a PDF** – geração de PDF preservando vetores sem dependências adicionais.  
- **Licenciamento flexível** – comece com uma **temporary license aspose** para testes, depois faça upgrade quando entrar em produção.

## O que é “export dwg to pdf”?

Exportar DWG para PDF significa converter um desenho nativo do AutoCAD em um documento PDF portátil e independente de dispositivo. O PDF resultante preserva dados vetoriais, camadas e escala, tornando‑o ideal para compartilhamento, impressão ou arquivamento.

## Por que usar Aspose.CAD Java para essa conversão?

Porque a **java cad library** cuida de tudo, desde a conversão de unidades até a rasterização internamente, evitando a complexidade de ferramentas de terceiros e proporcionando resultados consistentes em todas as plataformas.

## Pré‑requisitos

Antes de mergulhar no código, certifique‑se de que você tem:

- Conhecimento básico de programação Java.  
- Biblioteca Aspose.CAD for Java instalada. Se ainda não a baixou, obtenha‑a **[aqui](https://releases.aspose.com/cad/java/)**.  
- Um arquivo DWG para teste – o exemplo **Bottom_plate.dwg** é usado neste guia.

## Importar Namespaces

No seu projeto Java, importe as classes necessárias para iniciar a conversão:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guia Passo a Passo

### Passo 1: Carregar o Arquivo DWG

Primeiro, carregue seu desenho DWG usando a classe `Image`. Isso cria uma representação em memória que o Aspose.CAD pode manipular.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Passo 2: Determinar o Tipo de Unidade

Entender se o desenho usa unidades métricas ou imperiais é essencial para a escala correta. O método auxiliar `IsMetric` (implementação omitida para brevidade) retorna um valor booleano.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Passo 3: Definir Opções de Rasterização

Com base no sistema de unidades, configure o tamanho da página, escala e o tipo de unidade de destino. Essas opções determinam como o DWG será rasterizado antes de ser incorporado a um PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Passo 4: Configurar Opções de PDF (pdf options cad)

Crie uma instância de `PdfOptions` e anexe as configurações de rasterização. Isso informa ao Aspose.CAD como incorporar o conteúdo rasterizado ao PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Passo 5: Salvar como PDF

Finalmente, exporte o desenho para um arquivo PDF. O método `save` recebe o caminho de saída e as `PdfOptions` configuradas.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Quando o código terminar, você encontrará **Saved.pdf** na sua pasta `DWGDrawings`, pronto para distribuição ou arquivamento.

## Como converter imagens raster dwg com java cad library

Se precisar de imagens raster em vez de um PDF, basta substituir o `PdfOptions` pelas opções de imagem raster apropriadas (por exemplo, `PngOptions`, `JpegOptions`). A mesma instância de `CadRasterizationOptions` pode ser reutilizada, permitindo que você **convert dwg raster** com alterações mínimas no código.

## Como gerar pdf dwg usando pdf options cad

O exemplo acima já **generates pdf dwg**. Ajustando `pdfOptions`—por exemplo, definindo `pdfOptions.setCompress(true)`—você pode controlar o tamanho e a qualidade do PDF. Isso demonstra a flexibilidade da API **pdf options cad**.

## Problemas Comuns & Dicas

- **Tamanho de página incorreto** – Verifique novamente a lógica de conversão de unidades; coeficientes incompatíveis podem gerar páginas excessivamente grandes.  
- **Fontes ou espessuras de linha ausentes** – Garanta que o DWG referencie todos os recursos externos antes da conversão.  
- **Desempenho em desenhos grandes** – Aumente a configuração `DPI` em `CadRasterizationOptions` somente quando for necessária qualidade superior; DPI menor acelera o processamento.  
- **Questões de licença** – Para avaliação você pode usar uma **temporary license aspose**; uma licença completa é necessária para implantações em produção.

## Perguntas Frequentes

**P: Posso usar Aspose.CAD for Java com outros frameworks Java?**  
R: Sim, o Aspose.CAD for Java integra‑se perfeitamente com frameworks populares como Spring, Jakarta EE e Android.

**P: Existe uma licença temporária disponível para Aspose.CAD for Java?**  
R: Sim, você pode obter uma licença temporária **[aqui](https://purchase.aspose.com/temporary-license/)**.

**P: Onde encontro suporte para Aspose.CAD for Java?**  
R: Visite o **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** para obter ajuda da comunidade e dos engenheiros da Aspose.

**P: Como posso comprar uma licença para Aspose.CAD for Java?**  
R: Você pode comprar uma licença **[aqui](https://purchase.aspose.com/buy)**.

**P: Quais unidades o Aspose.CAD for Java suporta?**  
R: O Aspose.CAD for Java suporta unidades métricas e imperiais, detectando automaticamente o sistema de unidades do desenho.

**P: Posso converter DWG para outros formatos de imagem (por exemplo, PNG, JPEG) usando a mesma API?**  
R: Absolutamente. Substitua `PdfOptions` pelas opções de imagem raster adequadas (por exemplo, `PngOptions`) e reutilize o mesmo `CadRasterizationOptions`.

## Conclusão

Este tutorial demonstrou como **export dwg to pdf** e imagens raster usando a **java cad library** Aspose.CAD for Java. Seguindo o guia passo a passo, você pode integrar conversões CAD confiáveis em qualquer aplicação Java, seja para PDFs de documentação ou imagens raster para exibição na web.

---

**Última atualização:** 2026-02-17  
**Testado com:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}