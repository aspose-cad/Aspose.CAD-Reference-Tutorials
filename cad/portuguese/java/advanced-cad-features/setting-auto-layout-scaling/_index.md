---
date: 2026-02-15
description: Aprenda a definir tamanho de página personalizado e criar PDF a partir
  de CAD usando Aspose.CAD para Java. Este guia passo a passo cobre a exportação de
  CAD para PDF com dimensionamento automático de layout.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Definir tamanho de página personalizado – PDF a partir de CAD com dimensionamento
  automático de layout
url: /pt/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

 to produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir Tamanho de Página Personalizado – Criar PDF a partir de CAD com Redimensionamento Automático de Layout

## Introdução

Se você precisa **definir tamanho de página personalizado** enquanto **cria PDF a partir de CAD** de forma rápida e com dimensionamento perfeito, o Aspose.CAD for Java tem a solução. O Redimensionamento Automático de Layout ajusta automaticamente as dimensões do layout para que o PDF resultante fique exatamente como desejado, independentemente do tamanho original da página CAD. Neste tutorial percorreremos todo o processo — desde o carregamento de um arquivo DXF até a exportação para PDF — destacando os recursos de **exportar CAD para PDF** da biblioteca e mostrando como você também pode **converter DWG para PDF** ou **aumentar a resolução do PDF** quando necessário.

## Respostas Rápidas
- **O que o Redimensionamento Automático de Layout faz?** Redimensiona automaticamente os layouts CAD para caber nas dimensões da página de destino ao rasterizar.
- **Quais formatos posso converter?** Qualquer formato suportado pelo Aspose.CAD (por exemplo, DXF, DWG, DWF) pode ser convertido para PDF.
- **Preciso de licença para produção?** Sim, uma licença comercial é necessária para uso que não seja avaliação.
- **Quanto tempo leva a conversão?** Normalmente menos de um segundo para arquivos padrão em hardware moderno.
- **Posso mudar o tamanho da página?** Sim, você pode definir dimensões de página personalizadas via `CadRasterizationOptions`.

## O que é “criar PDF a partir de CAD”?

Criar um PDF a partir de CAD significa pegar um desenho de engenharia baseado em vetores (DXF, DWG, etc.) e rasterizá‑lo em um documento PDF. O PDF mantém a fidelidade visual do desenho original enquanto pode ser visualizado em qualquer plataforma.

## Por que usar o Redimensionamento Automático de Layout?

- **Saída consistente:** Garante que todos os layouts preencham a página PDF sem cálculos manuais de tamanho.
- **Economia de tempo:** Elimina a necessidade de ajustar manualmente os fatores de escala para cada desenho.
- **Alta qualidade:** Mantém a espessura das linhas e a precisão da geometria durante a conversão.
- **Flexibilidade:** Funciona para **converter dxf para pdf**, **converter dwg para pdf** e até quando você precisa **aumentar a resolução do PDF** para arquivos prontos para impressão.

## Pré-requisitos

1. **Aspose.CAD for Java Library** – baixe a versão mais recente na [página de download](https://releases.aspose.com/cad/java/).  
2. **Diretório de Recursos** – crie uma pasta na sua máquina para armazenar arquivos CAD; substitua `"Your Document Directory"` no código por esse caminho.  
3. **Arquivo CAD de Exemplo** – para este guia usaremos `conic_pyramid.dxf`, que está incluído no conjunto de dados de exemplo da Aspose.

## Importar Namespaces

Primeiro, importe as classes necessárias. Isso nos dá acesso ao carregamento de imagens, rasterização e recursos de exportação para PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Como Definir Tamanho de Página Personalizado para PDF a partir de CAD

Antes de mergulharmos no código passo a passo, vamos entender por que definir um tamanho de página personalizado é importante. Quando você **define tamanho de página personalizado**, controla as dimensões físicas do PDF resultante (por exemplo, A4, Letter ou um tamanho sob medida). Isso é essencial em fluxos de trabalho de engenharia onde os desenhos devem corresponder a padrões de folha ou quando você precisa incorporar o PDF em documentos maiores.

### Etapa 1: Carregar o Arquivo CAD

Carregar o arquivo fonte é o primeiro passo em **como exportar CAD** para um documento PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Etapa 2: Criar Opções de Rasterização

Defina as dimensões da página de destino. Você também pode usar este bloco para **definir tamanho de página CAD** manualmente, se preferir um layout personalizado.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Etapa 3: Definir Redimensionamento Automático de Layout

Habilite o recurso de dimensionamento automático. Este é o núcleo de **como definir escala** para uma conversão de CAD‑para‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Etapa 4: Criar Opções de PDF

Vincule as configurações de rasterização às opções de exportação PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Etapa 5: Exportar para PDF

Por fim, salve a imagem renderizada como um arquivo PDF. Esta etapa completa o fluxo de **converter dxf para pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repita as etapas acima para quaisquer arquivos CAD adicionais que você precise processar, sejam eles **DWG**, **DWF** ou outros formatos suportados.

## Casos de Uso Comuns

| Cenário | Por que definir um tamanho de página personalizado? |
|----------|-----------------------------|
| **Submissão de desenho de construção** | Alinha o PDF aos tamanhos de folha padrão A1/A2 exigidos por órgãos reguladores. |
| **Incorporação em manuais técnicos** | Garante que o desenho se ajuste ao layout pré‑definido do manual sem necessidade de redimensionamento extra. |
| **Impressão de alta resolução** | Permite aumentar o DPI (por exemplo, `rasterizationOptions.setResolution(300)`) mantendo as dimensões da página consistentes. |

## Problemas Comuns & Solução de Problemas

| Sintoma | Causa Provável | Correção |
|---------|--------------|-----|
| Saída de PDF em branco | Opções de rasterização não definidas ou caminho do arquivo incorreto | Verifique o caminho `srcFile` e assegure que `setPageWidth/Height` não sejam zero |
| Escala distorcida | `setAutomaticLayoutsScaling` deixado como `false` | Habilite o redimensionamento automático ou calcule manualmente o fator de escala |
| Camadas ausentes | DXF de origem contém entidades não suportadas | Verifique as notas de versão do Aspose.CAD para tipos de entidade suportados |

## Perguntas Frequentes

**Q: O Aspose.CAD para Java é compatível com todos os formatos de arquivo CAD?**  
A: O Aspose.CAD para Java suporta vários formatos CAD, incluindo DWG, DXF e DWF.

**Q: Posso personalizar ainda mais as opções de escala?**  
A: Sim, a classe `CadRasterizationOptions` oferece propriedades para ajuste fino de escala, DPI e outras configurações de rasterização.

**Q: Onde posso encontrar documentação adicional para Aspose.CAD para Java?**  
A: Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações detalhadas e exemplos.

**Q: Existe um teste gratuito disponível para Aspose.CAD para Java?**  
A: Sim, você pode explorar um [teste gratuito](https://releases.aspose.com/) para experimentar os recursos do Aspose.CAD para Java.

**Q: Como posso buscar assistência ou participar de discussões sobre Aspose.CAD para Java?**  
A: Visite o [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) para conectar‑se com a comunidade e obter suporte.

### Perguntas Comuns Adicionais

**Q: Como converto um arquivo DWG para PDF em vez de DXF?**  
A: O mesmo código funciona; basta mudar a extensão do arquivo em `srcFile` para `.dwg`.

**Q: Posso definir um DPI personalizado para PDFs de alta resolução?**  
A: Sim, use `rasterizationOptions.setResolution(300);` (ou qualquer DPI que precisar).

**Q: É possível incorporar fontes no PDF gerado?**  
A: O Aspose.CAD rasteriza o desenho, portanto as fontes são renderizadas como vetores; não é necessário incorporar fontes separadamente.

## Conclusão

Seguindo este guia, você agora sabe como **definir tamanho de página personalizado** e **criar PDF a partir de CAD** usando Aspose.CAD for Java com Redimensionamento Automático de Layout. O processo simplifica o fluxo de **exportar CAD para PDF**, garante escala consistente e economiza tempo valioso de desenvolvimento. Sinta‑se à vontade para experimentar diferentes tamanhos de página, resoluções e formatos CAD para atender às necessidades do seu projeto, seja **convertendo DWG para PDF**, **aumentando a resolução do PDF** ou construindo um processador em lote **java CAD to PDF**.

---

**Última atualização:** 2026-02-15  
**Testado com:** Aspose.CAD for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}