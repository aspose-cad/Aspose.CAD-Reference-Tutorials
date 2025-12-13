---
date: 2025-12-13
description: Aprenda como salvar CAD como JPEG em Java usando Aspose.CAD, adicionar
  múltiplas camadas e ajustar as dimensões do CAD para uma conversão de imagem precisa.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Salvar CAD como JPEG com suporte a camadas em Java
url: /pt/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar CAD como JPEG com Suporte a Camadas em Java

## Introdução

Neste tutorial você descobrirá como **salvar CAD como JPEG** aproveitando ao máximo o suporte a camadas no Aspose.CAD para Java. As camadas permitem isolar partes específicas de um desenho, facilitando a exportação apenas do que você precisa. Vamos percorrer cada etapa, desde a configuração do ambiente até a exportação de um JPEG que inclui apenas as camadas que você escolher.

## Respostas Rápidas
- **O que significa “salvar CAD como JPEG”?** Converte um desenho CAD em uma imagem raster JPEG.
- **Posso incluir apenas camadas selecionadas?** Sim – use o método `setLayers` para especificar quais camadas renderizar.
- **Como altero o tamanho da imagem?** Ajuste `setPageWidth` e `setPageHeight` em `CadRasterizationOptions`.
- **Esta é uma solução apenas para Java?** O exemplo usa Aspose.CAD para Java, mas os mesmos conceitos se aplicam a outras linguagens.
- **Preciso de licença?** Um teste gratuito funciona para experimentação; uma licença comercial é necessária para produção.

## Pré‑requisitos

Antes de começar, certifique‑se de que você possui o seguinte:

1. **Biblioteca Aspose.CAD para Java** – faça o download no [site](https://releases.aspose.com/cad/java/). Siga o guia de instalação para adicionar os arquivos JAR ao classpath do seu projeto.  
2. **Ambiente de Desenvolvimento Java** – um JDK recente (8 ou superior) instalado na sua máquina.

Agora que tudo está configurado, vamos explorar o código necessário para **salvar CAD como JPEG** com renderização seletiva de camadas.

## Importar Namespaces

Comece importando as classes necessárias do Aspose.CAD e as utilidades padrão do Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Guia Passo a Passo

### Etapa 1: Definir Caminhos de Arquivo

Defina onde o arquivo DWF de origem está localizado e onde o JPEG de saída será gravado.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Etapa 2: Carregar a Imagem DWF

Use o método `Image.load` do Aspose.CAD para ler o desenho CAD.

```java
Image image = Image.load(srcFile);
```

### Etapa 3: Configurar Opções de Rasterização (Ajustar Dimensões do CAD)

Crie uma instância de `CadRasterizationOptions` e defina o tamanho de saída desejado. Alterar esses valores permite **ajustar as dimensões do CAD** para o JPEG final.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Etapa 4: Especificar Camadas (Adicionar Múltiplas Camadas)

Se quiser renderizar mais de uma camada, basta adicionar seus nomes à lista. Aqui começamos com uma única camada chamada “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Dica profissional:* Para **adicionar várias camadas**, expanda a chamada `Arrays.asList`, por exemplo, `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Etapa 5: Configurar Opções JPEG (Converter Imagem CAD em Java)

Associe as configurações de rasterização ao formato de saída JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Etapa 6: Exportar para JPG (Salvar CAD como JPEG)

Por fim, grave a imagem no disco. Esta etapa **salva o desenho CAD como um arquivo JPEG** que contém apenas as camadas selecionadas.

```java
image.save(outFile, jpegOptions);
```

Seguindo estas etapas, você salvou com sucesso **CAD como JPEG** controlando quais camadas aparecem e personalizando as dimensões da imagem.

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|---------|
| **Camadas não aparecem** | Verifique se os nomes das camadas correspondem exatamente ao que está armazenado no arquivo DWF (sensível a maiúsculas/minúsculas). |
| **Imagem de saída está em branco** | Certifique‑se de que `setPageWidth` e `setPageHeight` são suficientemente grandes para as extensões do desenho. |
| **Exceção de licença** | Use uma licença de teste para experimentação; obtenha uma licença completa para ambientes de produção. |

## Perguntas Frequentes

**P: Posso adicionar várias camadas às opções de rasterização?**  
R: Absolutamente. Expanda a `stringList` com nomes de camadas adicionais, por exemplo, `Arrays.asList("LayerA", "LayerB")`.

**P: O Aspose.CAD é compatível com outros formatos CAD?**  
R: Sim, ele suporta DWG, DXF, DWF e muitos outros formatos.

**P: Como posso alterar as dimensões da imagem de saída?**  
R: Modifique `setPageWidth` e `setPageHeight` na instância `CadRasterizationOptions`.

**P: Onde posso comprar uma licença para o Aspose.CAD?**  
R: Você pode explorar as opções de licenciamento [aqui](https://purchase.aspose.com/buy).

**P: Onde encontro suporte da comunidade?**  
R: Participe da comunidade Aspose.CAD no [fórum](https://forum.aspose.com/c/cad/19) para obter ajuda e discussões.

---

**Última atualização:** 2025-12-13  
**Testado com:** Aspose.CAD para Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}