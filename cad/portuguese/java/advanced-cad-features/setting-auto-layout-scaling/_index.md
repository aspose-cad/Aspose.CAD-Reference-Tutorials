---
date: 2025-12-10
description: Aprenda como criar PDF a partir de CAD usando Aspose.CAD para Java com
  dimensionamento automático de layout. Este guia passo a passo mostra como exportar
  CAD para PDF de forma eficiente e confiável.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Criar PDF a partir de CAD – Dimensionamento automático de layout com Aspose.CAD
  Java
url: /pt/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar PDF a partir de CAD – Dimensionamento Automático de Layout com Aspose.CAD Java

## Introdução

Se você precisa **criar PDF a partir de arquivos CAD** de forma rápida e com dimensionamento perfeito, o Aspose.CAD para Java tem a solução. O Dimensionamento Automático de Layout ajusta automaticamente as dimensões do layout para que o PDF resultante fique exatamente como desejado, independentemente do tamanho original da página CAD. Neste tutorial percorreremos todo o processo — desde o carregamento de um arquivo DXF até a exportação para PDF — destacando os recursos de **exportar CAD para PDF** da biblioteca.

## Respostas Rápidas
- **O que o Dimensionamento Automático de Layout faz?** Redimensiona automaticamente os layouts CAD para caber nas dimensões da página de destino ao rasterizar.
- **Quais formatos posso converter?** Qualquer formato suportado pelo Aspose.CAD (por exemplo, DXF, DWG, DWF) pode ser convertido para PDF.
- **Preciso de licença para produção?** Sim, uma licença comercial é necessária para uso que não seja avaliação.
- **Quanto tempo leva a conversão?** Normalmente menos de um segundo para arquivos padrão em hardware moderno.
- **Posso alterar o tamanho da página?** Sim, você pode definir dimensões de página personalizadas via `CadRasterizationOptions`.

## O que significa “criar PDF a partir de CAD”?
Criar um PDF a partir de CAD significa pegar um desenho de engenharia baseado em vetor (DXF, DWG, etc.) e rasterizá‑lo em um documento PDF. O PDF mantém a fidelidade visual do desenho original, sendo amplamente visualizável em qualquer plataforma.

## Por que usar o Dimensionamento Automático de Layout?
- **Saída consistente:** Garante que todos os layouts preencham a página PDF sem cálculos manuais de tamanho.
- **Economia de tempo:** Elimina a necessidade de ajustar manualmente fatores de escala para cada desenho.
- **Alta qualidade:** Mantém a espessura das linhas e a precisão da geometria durante a conversão.

## Pré‑requisitos

1. **Biblioteca Aspose.CAD para Java** – faça o download da versão mais recente na [página de download](https://releases.aspose.com/cad/java/).  
2. **Diretório de Recursos** – crie uma pasta na sua máquina para armazenar arquivos CAD; substitua `"Your Document Directory"` no código por esse caminho.  
3. **Arquivo CAD de Exemplo** – para este guia usaremos `conic_pyramid.dxf`, que está incluído no conjunto de dados de exemplo da Aspose.

## Importar Namespaces

Primeiro, importe as classes necessárias. Isso nos dá acesso ao carregamento de imagens, rasterização e recursos de exportação para PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Etapa 1: Carregar o Arquivo CAD

Carregar o arquivo de origem é o primeiro passo em **como exportar CAD** para um documento PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Etapa 2: Criar Opções de Rasterização

Defina as dimensões da página de destino. Você também pode usar este bloco para **definir o tamanho da página CAD** manualmente, caso prefira um layout personalizado.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Etapa 3: Definir Dimensionamento Automático de Layout

Habilite o recurso de dimensionamento automático. Este é o núcleo de **como definir a escala** para uma conversão de CAD‑para‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Etapa 4: Criar Opções de PDF

Vincule as configurações de rasterização às opções de exportação para PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Etapa 5: Exportar para PDF

Por fim, salve a imagem renderizada como um arquivo PDF. Esta etapa completa o fluxo de **converter DXF para PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repita as etapas acima para quaisquer arquivos CAD adicionais que precisar processar.

## Problemas Comuns & Solução de Problemas

| Sintoma | Causa Provável | Solução |
|---------|----------------|---------|
| PDF em branco | Opções de rasterização não definidas ou caminho do arquivo incorreto | Verifique o caminho `srcFile` e assegure que `setPageWidth/Height` não sejam zero |
| Escala distorcida | `setAutomaticLayoutsScaling` deixado como `false` | Ative o dimensionamento automático ou calcule manualmente o fator de escala |
| Camadas ausentes | DXF de origem contém entidades não suportadas | Consulte as notas de versão do Aspose.CAD para tipos de entidade suportados |

## Perguntas Frequentes

### Q1: O Aspose.CAD para Java é compatível com todos os formatos de arquivo CAD?

R1: O Aspose.CAD para Java suporta vários formatos CAD, incluindo DWG, DXF e DWF.

### Q2: Posso personalizar ainda mais as opções de escala?

R2: Sim, a classe `CadRasterizationOptions` oferece diversas propriedades para ajuste fino da escala e outras configurações.

### Q3: Onde posso encontrar documentação adicional para o Aspose.CAD para Java?

R3: Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações detalhadas e exemplos.

### Q4: Existe uma versão de avaliação gratuita do Aspose.CAD para Java?

R4: Sim, você pode experimentar uma [versão de avaliação gratuita](https://releases.aspose.com/) para conhecer as capacidades do Aspose.CAD para Java.

### Q5: Como posso obter suporte ou participar de discussões sobre o Aspose.CAD para Java?

R5: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para conectar‑se com a comunidade e buscar ajuda.

**Perguntas Comuns Adicionais**

**Q: Como converto um arquivo DWG para PDF em vez de DXF?**  
R: O mesmo código funciona; basta mudar a extensão do arquivo em `srcFile` para `.dwg`.

**Q: Posso definir um DPI personalizado para PDFs de alta resolução?**  
R: Sim, use `rasterizationOptions.setResolution(300);` (ou qualquer DPI que precisar).

**Q: É possível incorporar fontes no PDF gerado?**  
R: O Aspose.CAD rasteriza o desenho, portanto as fontes são renderizadas como vetores; não é necessário incorporar fontes separadamente.

## Conclusão

Seguindo este guia, você agora sabe como **criar PDF a partir de arquivos CAD** usando Aspose.CAD para Java com Dimensionamento Automático de Layout. O processo simplifica o fluxo de **exportar CAD para PDF**, garante escala consistente e economiza tempo valioso de desenvolvimento. Sinta‑se à vontade para experimentar diferentes tamanhos de página, resoluções e formatos CAD para atender às necessidades do seu projeto.

---

**Última atualização:** 2025-12-10  
**Testado com:** Aspose.CAD para Java 24.12 (mais recente)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}