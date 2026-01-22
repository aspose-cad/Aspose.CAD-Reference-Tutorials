---
date: 2026-01-22
description: Aprenda como definir o tempo limite ao salvar CAD em PDF usando Aspose.CAD
  para Java. Aumente o desempenho com este guia passo a passo.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Como definir o tempo limite ao salvar CAD com Aspose.CAD
url: /pt/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tempo limite ao salvar CAD com Aspose.CAD

## Introdução

Bem-vindo ao tutorial sobre **como definir um tempo limite** ao salvar desenhos CAD usando Aspose.CAD para Java. Neste guia, vamos orientá-lo o de ` um tempo respons.

### Por que definir um tempo limite ao salvar CAD para PDF?
Salvar desenhos CAD grandes ou complexos pode consumir CPU e memória significativas. Adicionar um tempo limite:
- Impede que a aplicação congele.  
- Permite lidar com tarefas de longa duração de forma elegante.  
- Melhora a experiência geral do usuário, especialmente em ambientes web ou com interface gráfica.

## Pré-requisitos

- **Biblioteca Aspose.CAD para Java** – Certifique-se de que a biblioteca está integrada ao seu projeto. Você pode baixar a biblioteca no [site](https://releases.aspose.com/cad/java/).  
- **Ambiente de desenvolvimento** – Uma IDE Java (IntelliJ, Eclipse, etc.) com JDK 8+ instalado.

## Importar Pacotes

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Agora, vamos dividir o código de exemplo em instruções passo a passo:

## Etapa 1: Definir diretórios de origem e saída

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Certifique-se de que os diretórios de origem e saída estejam corretos para seus desenhos CAD.

## Etapa 2: Criar Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicialize um `InterruptionTokenSource` para gerenciar interrupções durante a operação de salvamento.

## Etapa 3: Carregar desenho CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Carregue o desenho CAD em um objeto `CadImage`.

## Etapa 4: Configurar opções de rasterização

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure as opções de rasterização para o desenho CAD.

## Etapa 5: Configurar opções de PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configure as opções de PDF com opções de rasterização vetorial e o token de interrupção.

## Etapa 6: Salvar desenho com tempo limite

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Salve o desenho CAD em um arquivo PDF com o tempo limite especificado.

## Etapa 7: Manipular interrupção

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

Crie uma thread para gerenciar a operação de salvamento e interrompê-la após um tempo limite especificado.

## Armadilhas comuns e solução de problemas
- **Tempo limite muito curto** – Se o desenho for grande, um tempo limite muito curto pode abortar a operação antes que ela termine. Aumente a duração do `sleep` ou ajuste as configurações de rasterização.  
- **Licença ausente** – Executar sem uma licença válida lançará uma exceção. Aplique uma licença temporária ou permanente antes de executar o código.  
- **Caminhos incorretos** – Certifique-se de que `SourceDir` e `OutputDir` apontem para pastas existentes; caso contrário, `Image.load` ou `save` falharão.

## Perguntas frequentes

**P: Como posso baixar o Aspose.CAD para Java?**  
R: Você pode baixá-lo na [página de lançamentos](https://releases.aspose.com/cad/java/).

**P: Onde posso encontrar a documentação do Aspose.CAD para Java?**  
R: Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações completas.

**P: Existe uma avaliação gratuita disponível?**  
R: Sim, você pode obter uma avaliação gratuita neste [link](https://releases.aspose.com/).

**P: Como obtenho uma licença temporária?**  
R: Visite [aqui](https://purchase.aspose.com/temporary-license/) para detalhes da licença temporária.

**P: Precisa de ajuda ou tem perguntas?**  
R: Acesse o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade.

## Conclusão

Parabéns! Agora você sabe **como definir um tempo limite** nas operações de salvamento ao converter desenhos CAD para PDF usando Aspose.CAD para Java. Implementar esse tempo limite melhora a confiabilidade e a responsividade de suas aplicações relacionadas a CAD.

---

**Última atualização:** 2026-01-22  
**Testado com:** Aspose.CAD for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}