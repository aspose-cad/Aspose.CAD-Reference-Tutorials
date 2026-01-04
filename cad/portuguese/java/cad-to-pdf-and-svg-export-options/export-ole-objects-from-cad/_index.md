---
date: 2026-01-04
description: Aprenda a **salvar CAD como PNG** e exportar objetos OLE de arquivos
  CAD sem esforço usando Aspose.CAD para Java. Configuração rápida, exemplo de código
  completo e dicas de boas práticas.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Salvar CAD como PNG e Exportar Objetos OLE com Aspose.CAD para Java
url: /pt/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar CAD como PNG e Exportar Objetos OLE com Aspose.CAD para Java

## Introdução

No mundo acelerado de Computer‑Aided Design (CAD), poder **salvar CAD como PNG** enquanto extrai objetos OLE (Object Linking and Embedding) incorporados pode simplificar drasticamente seu fluxo de trabalho. Seja construindo uma ferramenta de conversão em lote, gerando miniaturas para um portal web ou simplesmente precisando arquivar conteúdo OLE, o Aspose.CAD para Java oferece uma maneira limpa e programática de fazer isso. Neste tutorial percorreremos todo o processo, desde a configuração do projeto até a exportação de cada objeto OLE como imagem PNG.

## Respostas Rápidas
- **Posso exportar objetos OLE diretamente para PNG?** Sim – o Aspose.CAD carrega o arquivo CAD e permite rasterizar cada layout para PNG.  
- **Qual versão do Java é necessária?** Java 8 ou posterior.  
- **Preciso de licença para este recurso?** Uma avaliação gratuita funciona para testes; uma licença é necessária para produção.  
- **Os dados vetoriais serão preservados?** A rasterização PNG mantém a fidelidade visual, mas a saída é raster, não vetor.  
- **O processamento em lote é suportado?** Absolutamente – itere sobre um array de arquivos conforme mostrado no exemplo de código.

## Pré-requisitos

Antes de começar, certifique‑se de que você tem o seguinte:

- **Java Development Kit (JDK)** – Java 8+ instalado e configurado.  
- **Aspose.CAD for Java** – Baixe a biblioteca mais recente a partir do [download link](https://releases.aspose.com/cad/java/).  
- **Arquivos fonte CAD** – Qualquer arquivo DWG/DXF/DGN que contenha objetos OLE que você deseja exportar.

## Importar Namespaces

Para trabalhar com arquivos CAD você precisa importar as classes principais do Aspose.CAD. Mantenha o bloco de importação exatamente como mostrado – ele fornece as classes usadas mais adiante no tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Como Salvar CAD como PNG

A seguir está um guia conciso, passo a passo, que mostra **como exportar objetos OLE e salvar CAD como PNG**. Cada etapa inclui uma breve explicação seguida pelo código exato que você precisa copiar para o seu projeto.

### Etapa 1: Defina o Diretório do Seu Documento

Defina a pasta que contém seus desenhos CAD. Substitua o placeholder pelo caminho real na sua máquina.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Etapa 2: Defina os Nomes dos Arquivos CAD

Liste todos os arquivos CAD que você deseja processar. Você pode adicionar quantas entradas precisar.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Etapa 3: Defina as Opções de Exportação PNG

Configure as definições de rasterização. Aqui direcionamos um layout específico (`Layout1`) e usamos as opções padrão de PNG.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Etapa 4: Iterar pelos Arquivos CAD e Salvar como PNG

Carregue cada arquivo CAD, rasterize os objetos OLE e grave o arquivo PNG de saída. O sufixo `_out.png` ajuda a identificar as imagens geradas.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Problemas Comuns e Soluções

| Problema | Por que Acontece | Solução |
|----------|------------------|---------|
| **`Image.load` throws `FileNotFoundException`** | O caminho `dataDir` está incorreto ou o nome do arquivo contém um erro de digitação. | Verifique novamente a string do diretório e assegure‑se de que os nomes dos arquivos correspondam exatamente, incluindo espaços. |
| **Output PNG is blank** | O nome do layout não existe no arquivo CAD de origem. | Use `cadImage.getLayouts()` para listar os layouts disponíveis, então atualize `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasterizar imagens de alta resolução consome muita memória heap. | Aumente o heap da JVM (`-Xmx2g`) ou reduza a resolução de rasterização via `rasterizationOptions.setResolution(...)`. |

## Perguntas Frequentes

### Q1: O Aspose.CAD é compatível com todos os formatos de arquivo CAD?

A1: O Aspose.CAD suporta vários formatos CAD, incluindo DWG, DXF e DGN. Consulte a [documentação](https://reference.aspose.com/cad/java/) para a lista completa.

### Q2: Posso personalizar as configurações de exportação para objetos OLE?

A2: Sim, o Aspose.CAD oferece opções extensas para personalizar as configurações de exportação, permitindo adaptar a saída às suas necessidades específicas.

### Q3: Existe uma avaliação gratuita disponível para o Aspose.CAD?

A3: Sim, você pode explorar os recursos do Aspose.CAD obtendo uma avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Onde posso obter suporte da comunidade para o Aspose.CAD?

A4: Participe da comunidade Aspose.CAD no [forum](https://forum.aspose.com/c/cad/19) para buscar ajuda e compartilhar suas experiências.

### Q5: Como posso adquirir uma licença para o Aspose.CAD?

A5: Visite a [página de compra](https://purchase.aspose.com/buy) para adquirir uma licença que atenda às suas necessidades de desenvolvimento.

## Conclusão

Seguindo estas cinco etapas simples, você pode **salvar CAD como PNG** e extrair todos os objetos OLE incorporados com apenas algumas linhas de código Java. Essa abordagem é ideal para conversões em lote, relatórios automatizados ou qualquer cenário em que você precise de imagens rasterizadas do conteúdo CAD sem exportação manual. Sinta‑se à vontade para experimentar diferentes opções de rasterização para adequar qualidade e desempenho às suas exigências.

---

**Última atualização:** 2026-01-04  
**Testado com:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}