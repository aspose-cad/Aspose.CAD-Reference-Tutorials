---
date: 2026-01-07
description: Aprenda a exportar CAD para PDF e converter DGN para PDF usando Aspose.CAD
  para Java. Guia passo a passo para desenvolvedores Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Exportar CAD para PDF – Exportar DGN incorporado com Aspose.CAD para Java
url: /pt/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar CAD para PDF – Exportar DGN Incorporado com Aspose.CAD para Java

## Introdução

Neste tutorial você descobrirá **como exportar CAD para PDF** convertendo um arquivo DGN incorporado em um documento PDF de alta qualidade com Aspose.CAD para Java. Aspose.CAD é uma biblioteca robusta que oferece aos desenvolvedores Java controle total sobre a manipulação de arquivos CAD, seja para **converter DGN para PDF**, **converter DWG para PDF**, ou simplesmente renderizar desenhos CAD em outros formatos. Siga o guia passo a passo abaixo e você poderá integrar essa funcionalidade em suas aplicações em minutos.

## Respostas Rápidas
- **O que significa “exportar CAD para PDF”?** Converte desenhos CAD (DWG, DGN, etc.) em arquivos PDF preservando a qualidade vetorial.  
- **Qual biblioteca é usada?** Aspose.CAD para Java.  
- **Preciso de licença?** Uma licença é necessária para produção; há uma avaliação gratuita disponível.  
- **Quais são os pré‑requisitos principais?** Ambiente de desenvolvimento Java e o JAR do Aspose.CAD para Java.  
- **Posso personalizar a saída?** Sim – você pode selecionar layouts, definir opções de rasterização e controlar as configurações do PDF.

## O que é “exportar CAD para PDF”?
Exportar CAD para PDF significa pegar um arquivo CAD nativo (como DWG ou DGN) e gerar um documento PDF que representa fielmente a geometria original. O PDF pode ser visualizado em qualquer plataforma sem a necessidade de software CAD, tornando‑o ideal para compartilhamento, impressão ou arquivamento.

## Por que usar Aspose.CAD para Java para converter DGN para PDF?
- **Sem dependências externas** – funciona puramente em Java.  
- **Preserva dados vetoriais** – os PDFs permanecem nítidos em qualquer nível de zoom.  
- **Controle granular** – escolha layouts específicos, defina DPI de rasterização e incorpore fontes.  
- **Pronto para empresa** – suporta arquivos grandes, processamento em lote e opções de licenciamento.

## Pré‑requisitos

Antes de prosseguirmos, certifique‑se de que você possui o seguinte:

- **Ambiente de Desenvolvimento Java** – JDK 8 ou superior instalado e configurado.  
- **Aspose.CAD para Java** – faça o download do JAR mais recente em [here](https://releases.aspose.com/cad/java/).  

## Importar Pacotes

Para começar, você precisa importar as classes necessárias em seu projeto Java. Adicione as seguintes instruções de importação ao seu arquivo fonte:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Como exportar DGN para PDF usando Aspose.CAD para Java?

A seguir, um passo a passo numerado que mostra exatamente como converter um arquivo DGN incorporado (armazenado dentro de um DWG) em um PDF.

### Etapa 1: Definir Caminhos de Entrada e Saída

Defina o diretório que contém seu arquivo fonte e especifique o DWG que contém o DGN incorporado.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Etapa 2: Carregar o Arquivo DWG

Carregue o arquivo DWG em um objeto `Image`. Aspose.CAD detecta automaticamente os dados DGN incorporados.

```java
Image objImage = Image.load(fileName);
```

### Etapa 3: Configurar Opções de Rasterização

Selecione quais layout(s) você deseja incluir no PDF. Neste exemplo exportamos apenas o layout **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Etapa 4: Configurar Opções de PDF

Anexe as configurações de rasterização às opções de exportação de PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Etapa 5: Salvar o Arquivo PDF

Por fim, grave o PDF no disco usando as opções configuradas.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Converter DWG para PDF – uma dica adicional

Se o seu arquivo fonte for um DWG simples (sem DGN incorporado), você pode reutilizar o mesmo código – basta alterar o `fileName` para apontar ao DWG que deseja converter. As opções de rasterização e PDF permanecem idênticas, proporcionando um fluxo de trabalho consistente de **converter DWG para PDF**.

## Problemas Comuns e Soluções

| Problema | Motivo | Solução |
|----------|--------|----------|
| **Saída PDF em branco** | Nome do layout incompatível | Verifique se o nome do layout passado para `setLayouts` corresponde exatamente ao layout no arquivo fonte (sensível a maiúsculas/minúsculas). |
| **Exceção de licença** | Uso da avaliação sem licença | Aplique uma licença válida do Aspose.CAD antes de carregar a imagem (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Arquivo não encontrado** | Caminho `dataDir` incorreto | Use um caminho absoluto ou assegure que o caminho relativo esteja correto em relação ao diretório de trabalho do projeto. |
| **Gráficos de baixa resolução** | DPI de rasterização padrão é baixo | Defina `rasterizationOptions.setPageWidth/Height` ou `setResolution` para aumentar o DPI. |

## Perguntas Frequentes

**P: Posso usar Aspose.CAD para Java em um projeto comercial?**  
R: Sim, Aspose.CAD para Java é uma biblioteca comercial. Você pode obter uma licença em [here](https://purchase.aspose.com/buy).

**P: Existe uma avaliação gratuita disponível?**  
R: Sim, você pode acessar uma avaliação gratuita do Aspose.CAD para Java [here](https://releases.aspose.com/).

**P: Como posso obter suporte para Aspose.CAD para Java?**  
R: Você pode buscar suporte na comunidade Aspose.CAD no [forum](https://forum.aspose.com/c/cad/19).

**P: E se eu precisar de uma licença temporária?**  
R: Você pode obter uma licença temporária [here](https://purchase.aspose.com/temporary-license/).

**P: Onde encontro a documentação?**  
R: A documentação está disponível [here](https://reference.aspose.com/cad/java/).

## Conclusão

Agora você aprendeu como **exportar CAD para PDF**, especificamente como **converter DGN para PDF** e ainda **converter DWG para PDF** usando Aspose.CAD para Java. Seguindo os passos acima, você pode integrar a conversão perfeita de CAD‑para‑PDF em qualquer solução baseada em Java, entregando PDFs de alta qualidade aos seus usuários sem a necessidade de software CAD adicional.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-01-07  
**Testado com:** Aspose.CAD para Java 24.12  
**Autor:** Aspose