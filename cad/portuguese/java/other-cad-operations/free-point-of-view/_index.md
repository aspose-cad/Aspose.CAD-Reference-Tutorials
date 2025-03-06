---
title: Renderização gratuita de ponto de vista com Aspose.CAD para Java
linktitle: Ponto de vista livre
second_title: API Java Aspose.CAD
description: Explore o poder do Aspose.CAD para Java neste tutorial sobre como obter uma renderização de ponto de vista gratuita para desenhos CAD. Liberte o potencial do Aspose.CAD.
weight: 14
url: /pt/java/other-cad-operations/free-point-of-view/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderização gratuita de ponto de vista com Aspose.CAD para Java

## Introdução

Bem-vindo ao "Ponto de vista gratuito - Tutorial Aspose.CAD para Java." Neste guia abrangente, orientaremos você no processo de aproveitamento do Aspose.CAD for Java para obter uma renderização de ponto de vista gratuita para desenhos CAD. Aspose.CAD é uma biblioteca Java poderosa que oferece uma ampla gama de recursos para trabalhar com arquivos de design auxiliado por computador (CAD). O tutorial cobrirá os pré-requisitos necessários, importando pacotes essenciais e dividindo cada exemplo em guias passo a passo.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Biblioteca Aspose.CAD para Java: Baixe e instale a biblioteca Aspose.CAD para Java do[Link para Download](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Certifique-se de ter o Java instalado em sua máquina.

## Importar pacotes

Para começar, importe os pacotes necessários para o seu projeto Java. Adicione as seguintes linhas de código no início do seu arquivo Java:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

Esses pacotes são essenciais para trabalhar com arquivos CAD e personalizar as opções de renderização.

Agora, vamos dividir o exemplo fornecido em várias etapas:

## Etapa 1: configure seu diretório de documentos

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Substitua “Seu diretório de documentos” pelo caminho para o diretório de documentos real.

## Etapa 2: carregar o desenho CAD

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

Especifique o caminho para o seu desenho CAD e carregue-o usando o`Image` aula.

## Etapa 3: configurar opções de rasterização CAD

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

Personalize as opções de rasterização CAD de acordo com suas necessidades, como altura e largura da página.

## Etapa 4: configurar opções Jpeg

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Crie uma instância de`JpegOptions` e associe-o às opções de rasterização configuradas anteriormente.

## Passo 5: Definir Ângulos de Rotação

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

Especifique os ângulos de rotação ao longo dos eixos X, Y e Z para a renderização do ponto de vista livre.

## Etapa 6: salve a imagem renderizada

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

Salve a imagem renderizada com as opções especificadas no local desejado.

Repita essas etapas para seu caso de uso específico, garantindo uma renderização de ponto de vista livre para seus desenhos CAD.

## Conclusão

Parabéns! Você aprendeu com sucesso como implementar uma renderização de ponto de vista gratuita usando Aspose.CAD para Java. Este tutorial abordou etapas essenciais, desde a configuração de pré-requisitos até a personalização das opções de renderização e o salvamento da imagem de saída.

## Perguntas frequentes

### Q1: Posso usar Aspose.CAD para Java em várias plataformas?

A1: Sim, o Aspose.CAD for Java é independente de plataforma e pode ser usado em vários sistemas operacionais.

### Q2: Há alguma opção de licenciamento para Aspose.CAD para Java?

 A2: Sim, você pode explorar opções de licenciamento e fazer uma compra[aqui](https://purchase.aspose.com/buy).

### Q3: Existe um teste gratuito disponível?

 A3: Sim, você pode acessar uma versão de teste gratuita[aqui](https://releases.aspose.com/).

### Q4: Onde posso encontrar suporte para Aspose.CAD para Java?

 A4: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### P5: Como posso obter uma licença temporária?

 A5: Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
