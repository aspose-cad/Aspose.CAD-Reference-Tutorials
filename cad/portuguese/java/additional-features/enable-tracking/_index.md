---
date: 2025-12-01
description: Aprenda como definir o tamanho da página PDF, converter DWG para PDF
  e habilitar o rastreamento de alterações de DWG usando o Aspose.CAD para Java.
language: pt
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Definir tamanho da página PDF e rastrear DWG com Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir o Tamanho da Página PDF e Rastrear DWG com Aspose.CAD Java

## Introdução

Ao colaborar em projetos CAD, frequentemente você precisa **definir o tamanho da página PDF** para obter um layout consistente, **converter DWG para PDF** e acompanhar cada alteração feita no desenho. O Aspose.CAD para Java torna tudo isso possível em um fluxo de trabalho único e simplificado. Neste tutorial, percorreremos os passos exatos para **definir o tamanho da página PDF**, habilitar o **rastreamento de alterações DWG** e exportar o desenho como PDF — tudo usando Java.

## Respostas Rápidas
- **Como defino o tamanho da página PDF?** Use `CadRasterizationOptions.setPageWidth()` e `setPageHeight()` antes de exportar.  
- **Posso rastrear alterações durante a exportação?** Sim – implemente um `CadRenderHandler` personalizado para capturar os resultados do rastreamento.  
- **Qual método converte DWG para PDF?** Chame `image.save(stream, pdfOptions)` após configurar as opções.  
- **Quais são os principais pré‑requisitos?** JDK, Aspose.CAD para Java e uma pasta com arquivos DWG/DXF.  
- **É necessária uma licença para produção?** Sim, uma licença válida do Aspose.CAD é necessária para implantações que não sejam de avaliação.

## O que significa “definir o tamanho da página PDF” no contexto da exportação DWG?

Definir o tamanho da página PDF determina as dimensões da tela de saída do PDF (largura × altura em pixels). Isso é essencial quando você deseja que o desenho exportado se ajuste a um tamanho de papel ou layout de tela específico, garantindo que todos os elementos apareçam exatamente onde você espera.

## Por que habilitar o rastreamento ao exportar arquivos DWG?

O rastreamento (ou controle de alterações) registra quaisquer problemas de renderização, fontes ausentes ou entidades não suportadas que ocorram durante a conversão. Ao capturar essas informações, você pode:

- Identificar rapidamente questões que precisam ser corrigidas antes da entrega final.  
- Fornecer feedback claro aos membros da equipe sobre o que foi alterado ou omitido.  
- Manter um registro de auditoria para indústrias com requisitos de conformidade rigorosos.

## Pré‑requisitos

- **Java Development Kit (JDK)** – qualquer versão recente (8+).  
- **Aspose.CAD para Java** – faça o download na página oficial de [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Diretório de Documentos** – uma pasta que contém os arquivos DWG/DXF que você deseja processar.

## Importar Namespaces

Comece importando as classes necessárias do Aspose.CAD e as classes padrão de I/O do Java.

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

## Etapa 1: Carregar o Arquivo DWG (ou DXF)

Carregue seu desenho de origem em um objeto `Image`. Ajuste o caminho para apontar para o seu próprio diretório.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Etapa 2: Configurar Opções de Exportação PDF (incluindo tamanho da página)

Aqui definimos as opções PDF e **definimos explicitamente o tamanho da página PDF** para 800 × 600 pixels. É aqui que a palavra‑chave principal é aplicada.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Etapa 3: Implementar o Rastreamento

Crie um manipulador de erros personalizado que receberá as informações de rastreamento durante o processo de conversão.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Etapa 4: Exportar para PDF

Com as opções e o manipulador de rastreamento configurados, exporte o desenho. Esta etapa **converte DWG para PDF** (ou DXF para PDF no nosso exemplo).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Etapa 5: Classe CadRenderHandler – Capturando Resultados do Rastreamento

A classe `ErrorHandler` estende `CadRenderHandler` e imprime quaisquer problemas de renderização que ocorreram ao **rastrear alterações DWG**.

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

## Problemas Comuns & Como Resolucioná‑los

| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| **Fontes ausentes** | O arquivo CAD referencia fontes que não estão instaladas no servidor. | Instale as fontes necessárias ou incorpore‑as no desenho de origem. |
| **Entidades não suportadas** | Certas entidades DWG ainda não são suportadas pelo Aspose.CAD. | Use a saída de rastreamento para identificá‑las e simplifique o desenho. |
| **Tamanho de página incorreto** | `setPageWidth/Height` não foi chamado antes da exportação. | Certifique‑se de definir o tamanho da página em `CadRasterizationOptions` conforme mostrado acima. |

## Perguntas Frequentes

### Q1: Posso habilitar o rastreamento para outros formatos de arquivo CAD usando Aspose.CAD para Java?

A1: O Aspose.CAD suporta principalmente o rastreamento para arquivos DWG/DXF. Para outros formatos, consulte a documentação oficial para ver quais recursos estão disponíveis.

### Q2: Como posso lidar com opções de exportação adicionais no Aspose.CAD para Java?

A2: A biblioteca oferece muitas opções, como DPI, cor de fundo e rasterização vetorial. Explore‑as na [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3: Existe uma versão de avaliação disponível para Aspose.CAD para Java?

A3: Sim, você pode baixar uma avaliação gratuita em [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Onde posso buscar assistência ou discutir questões relacionadas ao Aspose.CAD para Java?

A4: O fórum da comunidade em [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) é um ótimo lugar para fazer perguntas e compartilhar experiências.

### Q5: Como obtenho uma licença temporária para Aspose.CAD para Java?

A5: Siga os passos descritos na página de [Temporary License](https://purchase.aspose.com/temporary-license/) para solicitar uma licença limitada no tempo para avaliação.

### Q6: Posso **converter DWG para PDF** preservando camadas?

A6: Sim. Ao configurar `CadRasterizationOptions` você pode preservar as informações de camada no PDF resultante.

### Q7: Qual é a melhor forma de **exportar DWG como PDF** com dimensões de página personalizadas?

A7: Defina a largura e a altura desejadas usando `setPageWidth` e `setPageHeight` antes de chamar `image.save()` – exatamente como demonstrado na Etapa 2.

## Conclusão

Seguindo os passos acima, você pode **definir o tamanho da página PDF**, **converter DWG para PDF** e **rastrear alterações em arquivos DWG** usando Aspose.CAD para Java. Esse fluxo de trabalho oferece controle total sobre o layout de saída enquanto fornece diagnósticos valiosos que mantêm sua colaboração CAD fluida e livre de erros. Sinta‑se à vontade para explorar opções de renderização adicionais e integrar este código em pipelines de automação maiores.

---

**Última atualização:** 2025-12-01  
**Testado com:** Aspose.CAD para Java 24.12 (mais recente na data de escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}