---
date: 2026-01-10
description: Aprenda a ler arquivos DWG e criar entidades multileader DWG usando Aspose.CAD
  para Java neste tutorial passo a passo.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Como ler DWG e suportar MLeader com Aspose.CAD para Java
url: /pt/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como ler DWG e dar suporte a MLeader com Aspose.CAD para Java

## Introdução

Se você precisa **ler arquivos DWG** e trabalhar com entidades **multileader DWG** em uma aplicação Java, chegou ao lugar certo. Aspose.CAD para Java oferece uma maneira limpa e programática de abrir desenhos DWG, inspecionar objetos MLeader e validar suas propriedades — tudo isso sem a necessidade de uma estação de trabalho CAD completa. Neste tutorial, percorreremos cada passo, desde o carregamento de um arquivo DWG até a confirmação de que os dados do multileader correspondem ao estilo esperado.

## Respostas rápidas
- **O que envolve “como ler dwg”?** Carregar o DWG com `Image.load()` e fazer cast para `CadImage`.
- **Posso criar entidades multileader dwg?** Sim – você pode adicionar, editar e validar objetos MLeader usando a API CadMLeader.
- **Qual versão da biblioteca é necessária?** Qualquer versão recente do Aspose.CAD para Java (a API mostrada funciona com builds 2024+).
- **Preciso de licença para desenvolvimento?** Uma licença temporária funciona para testes; uma licença completa é necessária para produção.
- **O código é multiplataforma?** Absolutamente – Java roda no Windows, Linux e macOS.

## O que é “como ler dwg” com Aspose.CAD?

Ler um arquivo DWG significa converter o desenho binário em um objeto `CadImage` em memória. Uma vez que você tem esse objeto, pode enumerar suas entidades (linhas, círculos, texto, objetos **MLeader**, etc.) e inspecionar suas propriedades.

## Por que dar suporte a entidades MLeader?

Objetos MLeader (multileader) combinam linhas de chamada com texto ou blocos anexados, tornando‑os essenciais para anotações em desenhos de engenharia. Suportá‑los permite:

- Verificar se as anotações estão em conformidade com os padrões da empresa.
- Extrair texto para processamento posterior (por exemplo, geração de lista de materiais).
- Modificar programaticamente estilos de líder ou substituir conteúdo de blocos.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

1. **Ambiente de desenvolvimento Java** – JDK 11+ e sua IDE favorita (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD para Java** – Baixe o JAR mais recente a partir do [link de download](https://releases.aspose.com/cad/java/).  

## Importar namespaces

Adicione as seguintes importações à sua classe Java para trabalhar com entidades DWG e opções de rasterização:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Como ler arquivos DWG usando Aspose.CAD para Java

### Etapa 1: Carregar o arquivo DWG e obter um `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Etapa 2: Validar que o desenho contém entidades MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Etapa 3: Verificar o estilo do MLeader e atributos básicos

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Etapa 4: Acessar os dados de contexto do MLeader (o coração do multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Etapa 5: Validar atributos ao nível de contexto

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Etapa 6: Trabalhar com o nó MLeader e sua linha de líder

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Etapa 7: Validar atributos adicionais do nó MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Etapa 8: Verificar propriedades relacionadas ao texto

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Etapa 9: Revisar outros atributos do MLeader para completude

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Problemas comuns e soluções

| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| `ClassCastException` ao fazer cast da entidade | O índice selecionado não é um objeto MLeader. | Verifique `cadImage.getEntities()[i] instanceof CadMLeader` antes de fazer o cast. |
| Valores `null` para pontos da linha de líder | O desenho usa um estilo de líder personalizado que não é totalmente suportado. | Use a versão mais recente do Aspose.CAD ou recorra ao estilo padrão para testes. |
| Falhas de asserção em valores numéricos | Pequenas diferenças de arredondamento entre versões de CAD. | Ajuste a tolerância em `Assert.areEqual(..., delta)` conforme mostrado nos exemplos. |

## Perguntas frequentes

**P: Posso usar Aspose.CAD para Java com outros formatos CAD?**  
R: Sim, Aspose.CAD suporta DXF, DWF, DGN e vários formatos raster além do DWG.

**P: Onde encontro documentação detalhada do Aspose.CAD para Java?**  
R: Consulte a [documentação oficial](https://reference.aspose.com/cad/java/) para detalhes da API e exemplos de código.

**P: Existe uma versão de avaliação gratuita?**  
R: Absolutamente – você pode baixar uma avaliação na página de [teste gratuito](https://releases.aspose.com/).

**P: Como obtenho uma licença temporária para testes?**  
R: Obtenha uma licença temporária através do [link de licença temporária](https://purchase.aspose.com/temporary-license/).

**P: Onde posso pedir ajuda à comunidade?**  
R: O [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) é o melhor lugar para compartilhar dúvidas e soluções.

## Conclusão

Agora você tem um guia completo, de ponta a ponta, para **como ler arquivos DWG** e **criar entidades multileader DWG** usando Aspose.CAD para Java. Seguindo os passos acima, você pode validar estilos de MLeader, extrair dados de anotação e integrar o processamento de DWG em qualquer fluxo de trabalho baseado em Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-01-10  
**Testado com:** Aspose.CAD 24.11 para Java  
**Autor:** Aspose