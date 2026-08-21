---
date: 2026-05-04
description: Aprenda a converter arquivos CAD PDF exportando DGN para PDF do AutoCAD
  usando Aspose.CAD para Java. Guia passo a passo com tamanho de PDF personalizável
  e opções.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportando DGN no formato AutoCAD para PDF
second_title: Aspose.CAD Java API
title: Converter PDF CAD – Exportação fácil de DGN para PDF AutoCAD com Aspose.CAD
  para Java
url: /pt/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter PDF CAD: Exportação sem esforço de DGN para PDF AutoCAD com Aspose.CAD para Java

## Introdução

Se você precisa **converter PDF CAD** arquivos diretamente de fontes DGN, você chegou ao lugar certo. Neste tutorial vamos guiá‑lo através do uso do Aspose.CAD para Java para exportar arquivos DGN em um PDF compatível com AutoCAD. Você verá como definir dimensões de página personalizadas, escolher layouts específicos e ajustar finamente a saída PDF — tudo com código claro, passo a passo, que você pode inserir em seu próprio projeto.

## Respostas Rápidas
- **O que significa “converter PDF CAD”?** Refere‑se à transformação de arquivos fonte CAD (como DGN) em um PDF que preserva os dados vetoriais e a fidelidade do layout.  
- **Qual biblioteca realiza a conversão?** Aspose.CAD para Java fornece um teste confiável e gratuito (sem licença) para esta tarefa.  
- **Preciso de licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para uso em produção.  
- **Posso personalizar o tamanho do PDF?** Sim – o `CadRasterizationOptions` permite definir a largura, altura e escala da página.  
- **Quantas linhas de código são necessárias?** Menos de 20 linhas de código Java para carregar, configurar e salvar o PDF.

## O que é “converter PDF CAD”?
Converter PDF CAD significa pegar um desenho CAD nativo (por exemplo, DGN) e produzir um PDF que mantém os gráficos vetoriais originais, camadas e informações de layout. O PDF resultante pode ser visualizado em qualquer dispositivo sem necessidade de software CAD, tornando‑o ideal para compartilhamento, impressão ou arquivamento.

## Por que usar Aspose.CAD para Java para converter PDF CAD?
- **Suporte total a formatos** – DGN, DWG, DXF e muitos outros.  
- **Sem dependências externas** – Java puro, sem DLLs nativas.  
- **Controle granular** – você pode escolher quais layouts exportar, definir tamanhos de página personalizados e controlar a qualidade da rasterização.  
- **Escalável para trabalhos em lote** – carregue e salve dezenas de arquivos em um loop com sobrecarga mínima.

## Pré-requisitos
Antes de começarmos, certifique‑se de que você tem o seguinte:

- **Biblioteca Aspose.CAD** – faça o download [aqui](https://releases.aspose.com/cad/java/).  
- **Diretório de Documentos** – uma pasta na sua máquina onde os arquivos DGN de entrada e os PDFs de saída ficarão.

## Importar Pacotes

No seu projeto Java, importe os pacotes necessários para acessar as funcionalidades do Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Agora, vamos dividir o código de exemplo em várias etapas:

## Etapa 1: Definir Caminhos de Arquivo (como exportar dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Certifique‑se de substituir `"Your Document Directory"` pelo caminho real onde seus arquivos estão localizados.

## Etapa 2: Carregar Imagem DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Carregue o arquivo DGN usando o Aspose.CAD.

## Etapa 3: Definir Opções de Exportação PDF (personalizar tamanho do pdf, definir opções pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Aqui definimos as opções de exportação PDF, incluindo dimensões da página, dimensionamento automático e os layouts DGN específicos (visualizações) que você deseja incluir no PDF final.

## Etapa 4: Salvar Arquivo PDF

```java
objImage.save(outFile, options);
```

Salve o arquivo PDF exportado. O método `save` aplica todas as opções que você configurou na etapa anterior.

Repita estas etapas para quaisquer arquivos DGN adicionais que você queira converter. Parabéns! Você converteu com sucesso **PDF CAD** exportando arquivos DGN para o formato AutoCAD em PDF usando Aspose.CAD para Java.

## Problemas Comuns e Soluções
| Problema | Por que acontece | Correção |
|----------|------------------|----------|
| **Arquivo não encontrado** | Caminho `dataDir` incorreto | Verifique novamente o caminho da pasta e assegure‑se de que o arquivo DGN existe. |
| **Páginas em branco no PDF** | `AutomaticLayoutsScaling` definido como `false` ou IDs de layout ausentes | Mantenha `setAutomaticLayoutsScaling(true)` e verifique os nomes dos layouts (`"1","2",…`). |
| **Saída de baixa resolução** | O DPI padrão da rasterização é baixo | Use `vectorOptions.setResolution(300);` para aumentar a qualidade (adicione antes de `setVectorRasterizationOptions`). |
| **Exceção de licença** | Executando sem uma licença válida em produção | Aplique uma licença temporária ou comprada conforme descrito na documentação da Aspose. |

## Perguntas Frequentes (Adicionais)

**Q: Posso exportar apenas um layout de um arquivo DGN com múltiplos layouts?**  
A: Sim – especifique os IDs dos layouts desejados em `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: É possível incorporar fontes no PDF resultante?**  
A: Aspose.CAD incorpora as fontes necessárias automaticamente quando os dados vetoriais são rasterizados; você também pode controlar a incorporação de fontes via `PdfOptions` se necessário.

**Q: Como processar muitos arquivos DGN em lote?**  
A: Envolva as etapas dentro de um loop `for` que itere sobre uma lista de nomes de arquivos, reutilizando a mesma instância de `PdfOptions` em cada iteração.

**Q: A biblioteca suporta PDFs protegidos por senha?**  
A: Sim – você pode definir uma senha no objeto `PdfOptions` via `options.setPassword("yourPassword");`.

**Q: Onde posso encontrar mais exemplos?**  
A: A documentação oficial do Aspose.CAD e o repositório de exemplos contêm muitos cenários adicionais.

## Perguntas Frequentes (Original)

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

A1: Sim, o Aspose.CAD suporta uma ampla variedade de formatos CAD, garantindo versatilidade no manuseio de diversos tipos de arquivos.

### Q2: Posso personalizar as configurações de exportação PDF?

A2: Absolutamente. Como mostrado no tutorial, você pode ajustar opções como dimensões da página e layouts para atender aos seus requisitos.

### Q3: Onde posso encontrar suporte ou assistência adicional?

A3: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

### Q4: Existe uma versão de avaliação gratuita disponível?

A4: Sim, você pode acessar a versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q5: Como posso obter uma licença temporária?

A5: Obtenha uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

## Conclusão

Neste tutorial exploramos como **converter PDF CAD** arquivos aproveitando o Aspose.CAD para Java. Com apenas algumas linhas de código você pode carregar um desenho DGN, ajustar finamente as opções de exportação PDF e gerar PDFs de alta qualidade prontos para compartilhamento ou arquivamento. Sinta‑se à vontade para experimentar diferentes tamanhos de página, layouts ou processamento em lote para atender às necessidades do seu projeto.

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}