---
date: 2025-12-28
description: Aprenda como carregar arquivos DWG em projetos Java e definir o nome
  da fonte principal usando Aspose.CAD para Java. Guia passo a passo para visualizações
  CAD perfeitas.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Como carregar um arquivo DWG em Java e substituir a fonte usando Aspose.CAD
url: /pt/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como carregar arquivo DWG em Java e substituir a fonte com Aspose.CAD

## Introdução

Se você precisa **carregar arquivos DWG em aplicações Java** e dar aos seus desenhos um aspecto mais refinado, substituir a fonte é uma solução rápida. Com o Aspose.CAD para Java você pode trocar o estilo de texto padrão por qualquer fonte instalada no sistema, garantindo que cada anotação apareça exatamente como esperado. Neste tutorial vamos percorrer todo o processo — desde o carregamento de um arquivo DWG em Java até o uso do método `setPrimaryFontName` para alterar a fonte.

## Respostas rápidas
- **Qual biblioteca eu preciso?** Aspose.CAD para Java.  
- **Posso carregar um arquivo DWG em Java?** Sim, basta chamar `Image.load()` passando o caminho do DWG.  
- **Qual método altera a fonte?** `setPrimaryFontName`.  
- **Preciso de licença para produção?** Sim, é necessária uma licença comercial.  
- **É possível processamento em lote?** Absolutamente – basta percorrer vários arquivos com o mesmo código.

## O que é “load dwg file java”?

Carregar um arquivo DWG em um ambiente Java significa ler os dados binários CAD para um objeto `Image` que o Aspose.CAD pode manipular. Depois que o arquivo é carregado, você tem acesso programático total a camadas, estilos e entidades de texto.

## Por que substituir fontes em um arquivo DWG?

- **Consistência:** Garante que todos os colaboradores vejam a mesma tipografia, independentemente da configuração de fontes local.  
- **Legibilidade:** Algumas fontes padrão do CAD são difíceis de ler em telas; trocar para uma fonte limpa como Arial melhora a clareza.  
- **Branding:** Alinha os desenhos técnicos com as diretrizes de estilo corporativas.

## Pré‑requisitos

- **Java Development Kit (JDK)** – qualquer versão recente (8+ recomendado).  
- **Aspose.CAD para Java** – faça o download no [site](https://releases.aspose.com/cad/java/).  
- **Arquivo DWG de exemplo** – um desenho que você deseja modificar (qualquer arquivo DWG ou DXF serve para teste).

## Importar namespaces

No seu projeto Java, importe as classes necessárias para trabalhar com Aspose.CAD. Essas importações dão acesso ao carregamento de imagens, objetos específicos de CAD e manipulação de estilos.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Guia passo a passo para substituir a fonte

### Etapa 1: Carregar seu arquivo DWG (load dwg file java)

Primeiro, aponte a API para a localização do seu arquivo DWG (ou DXF) e carregue‑o em um objeto `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Dica:** Se você trabalha diretamente com arquivos DWG, substitua a extensão `.dxf` por `.dwg` na variável `srcFile`.

### Etapa 2: Percorrer a tabela de estilos e definir o nome da fonte principal

Cada desenho CAD contém uma coleção de objetos de estilo. Percorra‑a e use o método `setPrimaryFontName` (a chamada de API que **define o nome da fonte principal**) para substituir a fonte.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Você pode mudar `"Arial"` para qualquer fonte que esteja instalada na máquina onde o código está sendo executado.

### Etapa 3: Salvar o desenho modificado

Após atualizar a fonte, grave as alterações em um novo arquivo DWG (ou sobrescreva o original).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

O arquivo salvo agora usa a fonte especificada, e qualquer anotação de texto será renderizada com essa tipografia.

## Problemas comuns e soluções

| Problema | Solução |
|----------|---------|
| **Fonte não aplicada** | Verifique se a fonte está instalada no SO host e se o nome está escrito exatamente igual. |
| **`Image.load` lança exceção** | Certifique‑se de que o caminho do arquivo está correto e que o arquivo é um formato DWG/DXF suportado. |
| **Desempenho lento em arquivos grandes** | Processar os arquivos em uma thread separada ou em lote para evitar bloqueio da UI. |

## Perguntas frequentes adicionais

**P: O método `setPrimaryFontName` afeta apenas entidades de texto?**  
R: Ele atualiza a fonte principal da tabela de estilos, o que, por sua vez, influencia todos os objetos de texto que referenciam esse estilo.

**P: Posso usar uma fonte personalizada que não está instalada no sistema?**  
R: O Aspose.CAD depende do registro de fontes do sistema operacional. Para usar uma fonte personalizada, instale‑a na máquina onde o código será executado.

**P: É possível mudar a fonte apenas para uma camada específica?**  
R: Sim, você pode filtrar estilos por nome de camada antes de chamar `setPrimaryFontName`.

**P: Qual versão do Aspose.CAD é necessária para arquivos DWG 2022?**  
R: A versão mais recente (até 2025) oferece suporte total ao DWG 2022. Consulte as notas de versão para detalhes sobre suporte a formatos específicos.

**P: Como lidar com licenciamento em ambiente de desenvolvimento?**  
R: Use uma licença de avaliação temporária para testes. Para produção, incorpore seu arquivo de licença adquirido usando `License.setLicense("Aspose.Total.Java.lic");`.

---

**Última atualização:** 2025-12-28  
**Testado com:** Aspose.CAD para Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}