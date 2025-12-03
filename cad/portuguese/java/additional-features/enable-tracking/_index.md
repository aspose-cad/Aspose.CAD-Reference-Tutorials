---
date: 2025-12-03
description: Aprenda como definir o tamanho da página PDF ao converter DWG para PDF
  e habilitar o rastreamento em arquivos DWG usando Aspose.CAD para Java – um guia
  completo para exportar desenhos CAD em PDF com precisão.
language: pt
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Definir tamanho da página PDF e habilitar rastreamento em arquivos DWG usando
  Aspose.CAD em Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir o Tamanho da Página PDF e Habilitar o Rastreamento em Arquivos DWG Usando Aspose.CAD em Java

## Introdução

Se você precisa **definir o tamanho da página PDF** ao *converter DWG para PDF* e também acompanhar quaisquer problemas de renderização, o Aspose.CAD para Java oferece uma maneira limpa e programática de fazer ambos. Neste tutorial, percorreremos os passos exatos para configurar as dimensões da página, habilitar o rastreamento e exportar um PDF de desenho CAD — tudo a partir do Java. Ao final, você entenderá por que definir o tamanho correto da página é importante para desenhos CAD e como capturar informações detalhadas de rastreamento durante o processo de exportação.

## Respostas Rápidas
- **O que “definir o tamanho da página PDF” afeta?** Define a largura e a altura da tela PDF resultante, garantindo que seu desenho se ajuste perfeitamente.  
- **Preciso de uma licença para usar este recurso?** Uma versão de avaliação funciona para testes; uma licença comercial é necessária para produção.  
- **Qual versão do Aspose.CAD é necessária?** Qualquer versão recente que suporte `CadRasterizationOptions`.  
- **Posso usar isso com outros formatos CAD?** O exemplo mostra DWG/DXF, mas a mesma abordagem funciona para a maioria dos formatos suportados.  
- **Quanto tempo leva a conversão?** Normalmente menos de um segundo para arquivos modestos; desenhos maiores podem levar mais tempo.

## O que significa “definir o tamanho da página PDF” no contexto da exportação CAD?

Definir o tamanho da página PDF informa ao renderizador as dimensões exatas (em pixels ou pontos) da tela de saída. Isso é especialmente importante para desenhos técnicos onde a escala e o layout devem ser preservados. Sem configurações explícitas de tamanho de página, o PDF pode assumir um tamanho que corta ou distorce o desenho.

## Por que definir o tamanho da página PDF ao exportar desenhos CAD?
- **Preservar escala** – Engenheiros dependem de impressões em escala real.  
- **Ajustar ao papel** – Escolha A4, Letter ou um tamanho personalizado que corresponda às especificações do projeto.  
- **Melhorar a legibilidade** – Páginas maiores podem mostrar detalhes finos sem necessidade de zoom.  
- **Saída consistente** – Pipelines automatizados produzem PDFs com dimensões idênticas a cada execução.

## Como definir o tamanho da página PDF ao converter DWG para PDF?

A seguir, configuraremos `CadRasterizationOptions` com valores personalizados de largura e altura antes da exportação. Esta etapa aborda diretamente a palavra‑chave principal **definir o tamanho da página PDF**.

## Pré‑requisitos

- **Java Development Kit (JDK)** – Java 8 ou mais recente instalado em sua máquina.  
- **Aspose.CAD for Java** – Baixe da página oficial [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – Uma pasta que contém os arquivos DWG/DXF que você deseja processar.

## Importar Namespaces

Primeiro, importe as classes que você precisará. O bloco de código permanece inalterado em relação ao tutorial original.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Etapa 1: Carregar o Arquivo DWG/DXF

Carregue seu desenho fonte. Ajuste o caminho para apontar para o seu próprio arquivo.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Etapa 2: Configurar Opções de Exportação PDF (incluindo tamanho da página)

Aqui definimos a largura e a altura da página — é aqui que **definimos o tamanho da página PDF**. Os valores estão em pixels; você pode converter de polegadas ou milímetros conforme necessário.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Dica:** Se você prefere tamanhos de papel padrão, use a conversão `1 polegada = 72 pontos`. Para uma página A4 (8,27 × 11,69 pol), defina `pageWidth = 595` e `pageHeight = 842`.

## Etapa 3: Implementar o Rastreamento

O rastreamento captura quaisquer problemas de renderização. Anexamos um manipulador personalizado que será invocado após a exportação.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Etapa 4: Exportar para PDF

Agora execute a conversão. O PDF será criado com as dimensões especificadas e quaisquer informações dereamento serão impressas no console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Etapa 5: Classe CadRenderHandler

O manipulador imprime quaisquer falhas que ocorreram durante a renderização. Isso ajuda a depurar problemas ao **exportar PDF de desenho CAD**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Problemas Comuns e Soluções

| Problema | Causa | Correção |
|----------|-------|----------|
| **PDF em branco** | Tamanho da página definido como 0 ou muito pequeno | Verifique se `setPageWidth` e `setPageHeight` são valores positivos. |
| **Geometria ausente** | Erros de renderização capturados pelo manipulador | Revise a saída do console de `ErrorHandler` e trate o `RenderCode` específico. |
| **Arquivo não encontrado** | Caminho `dataDir` incorreto | Use um caminho absoluto ou garanta que o diretório exista. |
| **Exceção de licença** | Usando a versão de avaliação sem licença válida para arquivos grandes | Aplique sua licença Aspose.CAD antes de carregar a imagem. |

## Perguntas Frequentes

**Q: Posso habilitar o rastreamento para outros formatos de arquivo CAD usando Aspose.CAD para Java?**  
A: O Aspose.CAD suporta principalmente DWG/DXF para rastreamento. Para outros formatos, consulte a documentação oficial.

**Q: Como posso lidar com opções adicionais de exportação no Aspose.CAD para Java?**  
A: A biblioteca oferece muitas opções, como DPI, cor de fundo e rasterização vetorial. Consulte a [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) para detalhes.

**Q: Existe uma versão de avaliação disponível para Aspose.CAD para Java?**  
A: Sim, você pode baixar uma avaliação gratuita em [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q: Onde posso buscar assistência ou discutir problemas relacionados ao Aspose.CAD para Java?**  
A: Visite o [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para suporte da comunidade e respostas oficiais.

**Q: Como obtenho uma licença temporária para Aspose.CAD para Java?**  
A: Siga os passos descritos na página de [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Última atualização:** 2025-12-03  
**Testado com:** Aspose.CAD for Java 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}