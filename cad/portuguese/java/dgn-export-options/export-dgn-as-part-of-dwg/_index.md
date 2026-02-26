---
date: 2026-01-10
description: Aprenda como exportar DGN para DWG e converter MicroStation DGN para
  AutoCAD DWG usando Aspose.CAD para Java. Guia passo a passo.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exportar DGN para DWG com Aspose.CAD para Java
url: /pt/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DGN para DWG com Aspose.CAD para Java

## Introdução

Neste tutorial, você aprenderá como **exportar dgn para dwg** e incorporar um design MicroStation DGN dentro de um arquivo AutoCAD DWG usando a biblioteca Aspose.CAD para Java. Seja migrando desenhos legados do MicroStation ou precisando combinar subcamadas DGN com layouts DWG, este guia o conduzirá por cada passo — desde a configuração do ambiente até a geração de uma visualização em PDF do DWG final.

## Respostas Rápidas
- **O que a “export dgn to dwg” realiza?** Ela incorpora uma subcamada DGN em um DWG, permitindo visualização contínua no AutoCAD.
- **Qual formato posso exportar o resultado para visualização rápida?** Você pode **export cad file to pdf** usando `PdfOptions`.
- **Preciso de uma licença para executar o código?** Uma licença temporária ou paga da Aspose.CAD é necessária para uso em produção.
- **Qual versão do Java é suportada?** Java 8 ou posterior funciona com a versão mais recente do Aspose.CAD para Java.
- **Existe uma avaliação gratuita disponível?** Sim – faça o download de uma avaliação no site da Aspose.

## O que é “export dgn to dwg”?

Exportar DGN para DWG significa converter ou incorporar um design MicroStation DGN como uma subcamada dentro de um desenho AutoCAD DWG. Isso permite que profissionais de CAD aproveitem ativos DGN existentes sem recriar a geometria do zero.

## Por que converter MicroStation DGN para AutoCAD DWG?

- **Colaboração:** Equipes que utilizam AutoCAD podem visualizar e editar conteúdo DGN diretamente.
- **Padronização:** DWG é o formato de fato para muitos fluxos de trabalho subsequentes (por exemplo, geração de PDF, renderização 3D).
- **Preservação:** Mantém as referências DGN originais intactas, reduzindo a perda de dados.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de que você tem os seguintes pré-requisitos configurados:

1. **Aspose.CAD Library:** Baixe e instale a biblioteca Aspose.CAD para Java. Você pode encontrar a biblioteca [aqui](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Certifique-se de que o Java está instalado em seu sistema.
3. **Integrated Development Environment (IDE):** Escolha uma IDE Java como Eclipse ou IntelliJ para uma experiência de desenvolvimento mais fluida.

## Importar Pacotes

No seu projeto Java, importe os pacotes Aspose.CAD necessários para habilitar a manipulação de arquivos CAD. Aqui está um exemplo:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Etapa 1: Definir Caminhos de Arquivo

Defina os caminhos de arquivo de entrada e saída para o arquivo DWG. Atualize as variáveis `dataDir`, `fileName` e `outPath` conforme necessário.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Etapa 2: Criar Instância de PdfOptions

Crie uma instância da classe `PdfOptions`, pois estamos **exportando o arquivo CAD para PDF** para verificação rápida.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Etapa 3: Carregar Arquivo DWG

Carregue o arquivo DWG existente como uma imagem e converta-o para o tipo `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Etapa 4: Iterar Sobre Entidades

Percorra cada entidade dentro do arquivo DWG e verifique se é uma definição de imagem. Se for, recupere a referência externa ao objeto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Etapa 5: Definir Opções de Rasterização

Defina as configurações para o objeto `CadRasterizationOptions`, incluindo largura da página, altura, layouts e cor de fundo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Etapa 6: Definir Opções de Rasterização Vetorial

Defina as opções de rasterização vetorial para a exportação.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Etapa 7: Exportar DWG para PDF

Finalmente, exporte o DWG para PDF chamando o método `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|----------|
| **Nenhuma subcamada DGN aparece** | O DWG não contém uma entidade `DGNUNDERLAY`. | Verifique se o DWG de origem inclui uma referência DGN. |
| **PDF está em branco** | Opções de rasterização definidas com tamanho zero ou layout errado. | Certifique-se de que `setPageWidth`/`setPageHeight` são positivos e `setLayouts` corresponde ao nome do layout do DWG. |
| **Exceção de licença** | Executando sem uma licença válida da Aspose.CAD. | Aplique uma licença temporária ou comprada antes de chamar quaisquer métodos da API. |

## Perguntas Frequentes

### Q1: Onde posso encontrar a documentação do Aspose.CAD para Java?

A1: A documentação pode ser encontrada [aqui](https://reference.aspose.com/cad/java/).

### Q2: Como posso baixar a biblioteca Aspose.CAD para Java?

A2: Você pode baixar a biblioteca neste [link](https://releases.aspose.com/cad/java/).

### Q3: Existe uma avaliação gratuita disponível para Aspose.CAD para Java?

A3: Sim, você pode encontrar a avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Onde posso obter uma licença temporária para Aspose.CAD para Java?

A4: Obtenha uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Precisa de ajuda ou tem perguntas?

A5: Visite o fórum de suporte da comunidade Aspose.CAD [aqui](https://forum.aspose.com/c/cad/19).

### Q6: Posso converter o PDF resultante de volta para DWG?

A6: O PDF é uma visualização raster; a conversão de volta para DWG requer uma ferramenta de engenharia reversa separada.

### Q7: Essa abordagem funciona com outros formatos CAD como DWF ou DXF?

A7: Sim, o Aspose.CAD suporta muitos formatos; você só precisa ajustar as extensões de arquivo e as configurações de rasterização conforme necessário.

---

**Última atualização:** 2026-01-10  
**Testado com:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}