---
title: Tempo limite ao salvar para CAD com Aspose.CAD
linktitle: Colocar tempo limite para salvar
second_title: API Java Aspose.CAD
description: Aprenda como aumentar o desempenho do seu aplicativo Java com Aspose.CAD. Defina um tempo limite para salvar desenhos CAD. Siga nosso guia passo a passo.
weight: 15
url: /pt/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tempo limite ao salvar para CAD com Aspose.CAD

## Introdução

Bem-vindo ao tutorial sobre como definir um tempo limite para salvar usando Aspose.CAD para Java. Neste guia, orientaremos você no processo de configuração de um tempo limite para salvar desenhos CAD para melhorar o desempenho do seu aplicativo. Aspose.CAD for Java é uma biblioteca poderosa que permite trabalhar perfeitamente com arquivos CAD em seus aplicativos Java.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Biblioteca Aspose.CAD for Java: Certifique-se de ter a biblioteca Aspose.CAD for Java integrada ao seu projeto. Você pode baixar a biblioteca do[local na rede Internet](https://releases.aspose.com/cad/java/).
- Ambiente de Desenvolvimento: Configure seu ambiente de desenvolvimento Java com todas as ferramentas e dependências necessárias.

## Importar pacotes

Para começar, importe os pacotes necessários para o seu projeto Java. Adicione as seguintes linhas no início do seu arquivo Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Agora, vamos dividir o código de exemplo em instruções passo a passo:

## Etapa 1: definir diretórios de origem e saída

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Certifique-se de ter os diretórios de origem e saída corretos para seus desenhos CAD.

## Etapa 2: Criar fonte de token de interrupção

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicialize uma fonte de token de interrupção para gerenciar interrupções durante a operação de salvamento.

## Etapa 3: carregar o desenho CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Carregue o desenho CAD em um`CadImage` objeto.

## Etapa 4: configurar opções de rasterização

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure opções de rasterização para o desenho CAD.

## Passo 5: Configurar Opções de PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configure opções de PDF com opções de rasterização vetorial e token de interrupção.

## Etapa 6: Salvar desenho com tempo limite

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Salve o desenho CAD em um arquivo PDF com o tempo limite especificado.

## Etapa 7: lidar com a interrupção

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Crie um thread para lidar com a operação de salvamento e interrompa-a após um tempo limite especificado.

## Conclusão

Parabéns! Você aprendeu com sucesso como definir um tempo limite para salvar usando Aspose.CAD para Java. Esse recurso pode aumentar bastante a eficiência de seus aplicativos relacionados a CAD.

## Perguntas frequentes

### Q1: Como posso baixar Aspose.CAD para Java?

 A1: Você pode baixá-lo do[página de lançamentos](https://releases.aspose.com/cad/java/).

### P2: Onde posso encontrar a documentação do Aspose.CAD para Java?

 A2: Consulte o[documentação](https://reference.aspose.com/cad/java/) para obter informações abrangentes.

### Q3: Existe um teste gratuito disponível?

A3: Sim, você pode obter uma avaliação gratuita em[esse link](https://releases.aspose.com/).

### P4: Como obtenho uma licença temporária?

 A4: Visita[aqui](https://purchase.aspose.com/temporary-license/) para obter detalhes da licença temporária.

### Q5: Precisa de ajuda ou tem dúvidas?

 A5: Vá para o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio comunitário.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
