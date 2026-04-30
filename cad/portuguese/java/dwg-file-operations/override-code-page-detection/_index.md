---
date: 2026-01-12
description: Aprenda como exportar CAD para PDF substituindo a detecção automática
  de página de códigos em arquivos DWG usando Aspose.CAD para Java. Lida com codificação
  e CIF/MIF malformados.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Exportar CAD para PDF – Substituir a Detecção Automática de Página de Código
  em Arquivos DWG com Java
url: /pt/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD to PDF – Substituir a Detecção Automática de Página de Código em Arquivos DWG com Java

## Introdução

Neste guia abrangente você descobrirá **como exportar CAD para PDF** enquanto substitui a detecção automática de página de código que pode corromper o texto em arquivos DWG. Aspose.CAD for Java oferece controle fino sobre a codificação, permitindo recuperar dados CIF/MIF malformados e produzir saída PDF confiável. Seja construindo um conversor em lote ou integrando o processamento CAD em uma aplicação Java maior, os passos abaixo o guiarão por todo o fluxo de trabalho.

## Respostas Rápidas
- **O que significa “override code page”?** Ele força o Aspose.CAD a usar uma codificação de caracteres específica em vez de adivinhar.
- **Posso exportar DWG diretamente para PDF?** Sim – após definir a página de código correta, você pode salvar a imagem CAD como PDF.
- **Qual codificação funciona para texto japonês?** `CodePages.Japanese` e `MifCodePages.Japanese` são as escolhas corretas.
- **Preciso de licença para uso em produção?** É necessária uma licença comercial; uma licença temporária está disponível para testes.
- **Qual versão do Aspose.CAD é necessária?** Qualquer versão recente que suporte `LoadOptions` e `PdfOptions`.

## O que é “exportar CAD para PDF”?
Exportar CAD para PDF converte desenhos CAD baseados em vetor em um formato de documento de layout fixo amplamente suportado. O PDF resultante preserva linhas, camadas e texto, facilitando o compartilhamento, impressão ou incorporação do desenho em outras aplicações.

## Por que substituir a detecção automática de página de código?
Arquivos DWG frequentemente armazenam texto usando páginas de código legadas. A auto‑detecção do Aspose.CAD pode interpretar esses bytes de forma incorreta, gerando caracteres embaralhados. Ao especificar manualmente a página de código, você garante que o texto apareça exatamente como pretendido no PDF exportado, especialmente para scripts não latinos como japonês, cirílico ou árabe.

## Pré-requisitos
- **Ambiente de Desenvolvimento Java** – JDK 8+ e sua IDE favorita.
- **Aspose.CAD for Java** – Baixe a biblioteca no site oficial [here](https://releases.aspose.com/cad/java/).
- **Arquivo de Exemplo DWG** – Use o `SimpleEntities.dwg` fornecido ou qualquer DWG que precise converter.

## Importar Pacotes
No seu projeto Java, importe as classes necessárias do Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Guia Passo a Passo

### Passo 1: Configurar o Projeto Java
Crie um novo projeto Maven ou Gradle e adicione o JAR do Aspose.CAD ao classpath. Esta etapa garante que a IDE possa resolver as classes importadas.

### Passo 2: Carregar o Arquivo DWG com uma Página de Código Especificada
Informe ao Aspose.CAD qual codificação usar e se deve tentar a recuperação de dados CIF/MIF malformados.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Passo 3: Exportar a Imagem CAD para PDF
Com a página de código correta aplicada, você pode exportar o desenho com segurança. O objeto `PdfOptions` permite ajustar finamente a saída PDF (compressão, rasterização, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Passo 4: Verificar o Sucesso
Uma mensagem simples no console confirma que o processo foi concluído sem exceções.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Você pode repetir esses passos para vários arquivos DWG, ajustando o caminho de origem e o nome de saída conforme necessário.

## Problemas Comuns & Soluções
- **Caracteres estranhos ainda aparecem:** Verifique se o `specifiedEncoding` corresponde à página de código original do DWG. Use um enum `CodePages` diferente, se necessário.
- **`NullPointerException` em `cadImage.save`:** Certifique‑se de que o arquivo DWG foi carregado corretamente; verifique o caminho e as permissões do arquivo.
- **Tamanho do PDF está grande:** Ative a compressão em `PdfOptions` (por exemplo, `pdfOptions.setCompress(true)`).

## Perguntas Frequentes

**Q1: O Aspose.CAD é compatível com todas as versões de arquivos DWG?**  
A1: O Aspose.CAD suporta uma ampla gama de versões DWG, incluindo AutoCAD 2018 e versões anteriores.

**Q2: Posso usar o Aspose.CAD em projetos comerciais?**  
A2: Sim, é necessária uma licença comercial para uso em produção. Você pode obter uma licença [here](https://purchase.aspose.com/buy).

**Q3: Existem limitações na versão de avaliação gratuita?**  
A3: A avaliação impõe restrições de tamanho e recursos; consulte a documentação oficial para detalhes.

**Q4: Como posso obter suporte para o Aspose.CAD?**  
A4: Visite a comunidade [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para assistência e discussões.

**Q5: Existe uma licença temporária disponível para fins de teste?**  
A5: Sim, uma licença temporária pode ser solicitada [here](https://purchase.aspose.com/temporary-license/).

---

**Última atualização:** 2026-01-12  
**Testado com:** Aspose.CAD for Java 24.11 (mais recente na época da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}