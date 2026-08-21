---
date: 2026-05-04
description: Aprenda como converter dxf para dwg e definir a fonte principal em Java
  usando Aspose.CAD. Guia passo a passo para visualizações CAD perfeitas.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Substituir fonte no DWG
second_title: Aspose.CAD Java API
title: Converter dxf para dwg e alterar fonte no DWG Aspose.CAD Java
url: /pt/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como carregar arquivo DWG em Java e substituir a fonte com Aspose.CAD

## Introdução

Se você precisar **convert dxf to dwg** em aplicações Java e dar aos seus desenhos um aspecto refinado, substituir a fonte é uma solução rápida. Com Aspose.CAD for Java você pode substituir o estilo de texto padrão por qualquer fonte instalada no sistema, garantindo que cada anotação apareça exatamente como você espera. Neste tutorial, percorreremos todo o processo — desde carregar um arquivo DWG em Java até usar o método `setPrimaryFontName` para mudar a fonte.

## Respostas Rápidas
- **Qual biblioteca eu preciso?** Aspose.CAD for Java.  
- **Posso carregar um arquivo DWG em Java?** Sim, basta chamar `Image.load()` no caminho do DWG.  
- **Qual método altera a fonte?** `setPrimaryFontName`.  
- **Preciso de licença para produção?** Sim, é necessária uma licença comercial.  
- **É possível processamento em lote?** Absolutamente – faça loop através de vários arquivos com o mesmo código.

## O que é **convert dxf to dwg**?

“Convert dxf to dwg” refere-se à transformação de um arquivo DXF (Drawing Exchange Format) para o formato nativo DWG usado por muitas aplicações CAD. A conversão permite que você pegue um desenho DXF amplamente suportado, o incorpore em um fluxo de trabalho DWG e, em seguida, aplique estilos avançados — como substituição de fonte — usando Aspose.CAD.

## Por que substituir fontes em um arquivo DWG?

- **Consistência:** Garante que todos os colaboradores vejam a mesma tipografia, independentemente da configuração de fontes local.  
- **Legibilidade:** Algumas fontes CAD padrão são difíceis de ler nas telas; trocar para uma fonte limpa como Arial melhora a clareza.  
- **Branding:** Alinha os desenhos técnicos com os guias de estilo corporativo.  

## Casos de Uso Comuns

| Cenário | Por que isso importa |
|----------|----------------|
| **Conversão em lote de desenhos DXF legados** | Você pode convertê-los para DWG e aplicar uma fonte corporativa em uma única passagem. |
| **Preparação de desenhos para apresentações ao cliente** | Fontes consistentes e legíveis fazem os documentos parecerem profissionais. |
| **Pipelines CAD automatizados** | Incorporar a substituição de fonte elimina etapas manuais de pós‑processamento. |

## Pré-requisitos

- **Java Development Kit (JDK)** – qualquer versão recente (8+ recomendada).  
- **Aspose.CAD for Java** – faça download no [website](https://releases.aspose.com/cad/java/).  
- **Arquivo DWG/DXF de exemplo** – um desenho que você deseja modificar (você pode usar qualquer arquivo DWG ou DXF para teste).

## Importar Namespaces

No seu projeto Java, importe as classes necessárias para trabalhar com Aspose.CAD. Essas importações dão acesso ao carregamento de imagens, objetos específicos de CAD e manipulação de estilos.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Guia passo a passo para substituir a fonte

### Etapa 1: Carregue seu arquivo DWG (load dwg file java)

Primeiro, aponte a API para a localização do seu arquivo DWG (ou DXF) e carregue-o em um objeto `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Dica profissional:** Se você trabalhar diretamente com arquivos DWG, substitua a extensão `.dxf` por `.dwg` na variável `srcFile`.

### Etapa 2: Iterar sobre a tabela de estilos e definir o nome da fonte principal

Cada desenho CAD contém uma coleção de objetos de estilo. Percorra-os e use o método `setPrimaryFontName` (a chamada de API que **sets primary font name**) para substituir a fonte.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Você pode mudar `"Arial"` para qualquer fonte que esteja instalada na máquina que executa o código.

### Etapa 3: Salvar o desenho modificado

Depois de atualizar a fonte, escreva as alterações de volta para um novo arquivo DWG (ou sobrescreva o original).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

O arquivo salvo agora usa a fonte que você especificou, e qualquer anotação de texto será renderizada com essa tipografia.

## Problemas Comuns e Soluções

| Problema | Solução |
|-------|----------|
| **Fonte não aplicada** | Verifique se a fonte está instalada no sistema operacional host e se a grafia corresponde exatamente. |
| **`Image.load` lança uma exceção** | Certifique-se de que o caminho do arquivo está correto e de que o arquivo é um formato DWG/DXF suportado. |
| **Desempenho reduzido em arquivos grandes** | Processar arquivos em uma thread separada ou em lote para evitar bloqueio da UI. |

## Perguntas Frequentes

**P: O método `setPrimaryFontName` afeta apenas entidades de texto?**  
R: Ele atualiza a fonte principal da tabela de estilos, o que por sua vez influencia todos os objetos de texto que referenciam esse estilo.

**P: Posso usar uma fonte personalizada que não está instalada no sistema?**  
R: Aspose.CAD depende do registro de fontes do sistema operacional. Para usar uma fonte personalizada, instale-a na máquina que executa o código.

**P: É possível mudar a fonte apenas para uma camada específica?**  
R: Sim, você pode filtrar estilos por nome da camada antes de chamar `setPrimaryFontName`.

**P: Qual versão do Aspose.CAD é necessária para arquivos DWG 2022?**  
R: A versão mais recente (até 2025) suporta totalmente DWG 2022. Sempre verifique as notas de versão para suporte a formatos específicos.

**P: Como lidar com licenciamento em um ambiente de desenvolvimento?**  
R: Use uma licença de avaliação temporária para testes. Para produção, incorpore seu arquivo de licença adquirido usando `License.setLicense("Aspose.Total.Java.lic");`.

---

**Última atualização:** 2026-05-04  
**Testado com:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}