---
date: 2025-12-28
description: Aprenda a criar PDF a partir de DWG, salvar DWG como PDF e adicionar
  texto a desenhos DWG com Aspose.CAD para Java — guia passo a passo.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Criar PDF a partir de DWG e adicionar texto usando Aspose.CAD para Java
url: /pt/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar PDF a partir de DWG e Adicionar Texto Usando Aspose.CAD para Java

## Introdução

Se você precisa **criar PDF a partir de DWG** arquivos enquanto também insere texto personalizado, você está no lugar certo. Neste tutorial percorreremos todo o processo — carregar um desenho DWG, adicionar uma anotação de texto e, finalmente, salvar o resultado como PDF usando Aspose.CAD para Java. Ao final, você entenderá como **salvar DWG como PDF**, personalizar a altura do texto e até adicionar anotações básicas.

## Respostas Rápidas
- **Posso converter DWG para PDF em Java?** Sim, Aspose.CAD para Java fornece uma API simples.  
- **Preciso de uma licença para uso em produção?** É necessária uma licença comercial; uma avaliação gratuita está disponível.  
- **Qual método adiciona texto a um DWG?** Use o objeto `CadText` e adicione‑o ao espaço de modelo.  
- **Posso definir a altura do texto?** Absolutamente — use `setTextHeight()` na instância `CadText`.  
- **A saída é baseada em vetor?** Quando as opções de rasterização são definidas como `UseObjectColor`, o PDF mantém dados vetoriais de alta qualidade.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré‑requisitos em vigor:

- Aspose.CAD para Java Library: Baixe e instale a biblioteca a partir da [página Aspose.CAD para Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Certifique‑se de que você tem o JDK mais recente instalado em seu sistema.

- Desenho DWG: Prepare um arquivo de desenho DWG onde você deseja adicionar texto.

## Importar Namespaces

Em seu código Java, importe os namespaces necessários para Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Agora, vamos dividir o trecho de código fornecido em várias etapas:

## Etapa 1: Configurar Diretório do Documento e Caminho do Arquivo DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Etapa 2: Carregar Imagem DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Etapa 3: Criar Objeto CadText (Adicionar Texto ao DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Etapa 4: Adicionar Texto ao CadImage (Inserir Anotação)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Etapa 5: Configurar Opções de PDF (Preparar para criar PDF a partir de DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Etapa 6: Configurar CadRasterizationOptions (Controlar renderização do PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Etapa 7: Salvar o DWG Modificado como PDF (dwg para pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Seguindo estas etapas, você será capaz de **criar PDF a partir de DWG**, adicionar texto personalizado e controlar a altura do texto — tudo com apenas algumas linhas de código Java.

## Por que Adicionar Texto ao DWG e Converter para PDF?

Adicionar texto diretamente a um arquivo DWG é útil para:

- **Marcar designs** com notas ou números de peça.
- **Criar documentação imprimível** onde o PDF serve como um formato somente leitura e amplamente suportado.
- **Automatizar processamento em lote** de grandes bibliotecas CAD sem edição manual.

## Problemas Comuns & Dicas

- **Texto não aparece?** Verifique se as coordenadas X/Y estão dentro dos limites do desenho e se a camada está visível.
- **Altura do texto incorreta?** Ajuste `setTextHeight()`; o valor está no sistema de unidades do desenho.
- **PDF parece rasterizado?** Certifique‑se de que `CadDrawTypeMode.UseObjectColor` está definido para manter informações vetoriais.
- **Desempenho em arquivos grandes?** Aumente `pageHeight`/`pageWidth` apenas conforme necessário; valores maiores consomem mais memória.

## Perguntas Frequentes

**Q: O Aspose.CAD é compatível com todas as versões de arquivos DWG?**  
A: Aspose.CAD suporta várias versões de arquivos DWG, garantindo compatibilidade com uma ampla gama de softwares CAD.

**Q: Posso personalizar a fonte e a formatação do texto adicionado?**  
A: Sim, você pode personalizar a fonte, o estilo e outras opções de formatação para o texto adicionado a arquivos DWG usando Aspose.CAD.

**Q: Existe uma avaliação gratuita disponível para Aspose.CAD para Java?**  
A: Sim, você pode explorar os recursos do Aspose.CAD obtendo uma avaliação gratuita [aqui](https://releases.aspose.com/).

**Q: Onde posso encontrar documentação detalhada para Aspose.CAD para Java?**  
A: Consulte a documentação [aqui](https://reference.aspose.com/cad/java/) para informações aprofundadas e exemplos.

**Q: Como posso obter suporte ou ajuda com Aspose.CAD?**  
A: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para obter assistência e conectar‑se com a comunidade.

---

**Última Atualização:** 2025-12-28  
**Testado com:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}