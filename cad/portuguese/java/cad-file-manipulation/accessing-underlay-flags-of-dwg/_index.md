---
date: 2025-12-22
description: Aprenda a carregar arquivos DWG e extrair informações de underlay com
  Aspose.CAD para Java – um guia passo a passo que cobre as flags de underlay.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Carregar arquivo DWG e acessar sinalizadores de underlay – Aspose.CAD para
  Java
url: /pt/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Carregar Arquivo DWG & Acessar Flags de Underlay – Aspose.CAD para Java

Nos fluxos de trabalho modernos de CAD, **carregar um arquivo DWG** rapidamente e extrair detalhes de underlay é uma necessidade comum. Seja você quem está construindo um visualizador, automatizando o processamento em lote ou extraindo metadados para integração GIS, o Aspose.CAD para Java oferece uma maneira limpa, orientada a código, de fazer isso. Neste tutorial, percorreremos os passos exatos para **carregar o arquivo DWG**, iterar suas entidades e ler os flags de underlay que muitos desenvolvedores ignoram.

## Respostas Rápidas
- **Qual é a classe principal para abrir um DWG?** `com.aspose.cad.Image.load()` retorna um `CadImage`.
- **Qual objeto contém as informações de underlay?** `CadUnderlay` (ou seus tipos derivados como `CadDgnUnderlay`).
- **Preciso de licença para desenvolvimento?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.
- **Posso processar vários arquivos DWG em um loop?** Sim – basta repetir o padrão de carregar‑e‑iterar.
- **Esta abordagem é compatível com Java 11+?** Absolutamente, o Aspose.CAD suporta Java 8 até as versões LTS mais recentes.

## O que é “load dwg file” no Aspose.CAD?
`Image.load()` lê o conteúdo binário do DWG e cria um objeto `CadImage` em memória. A partir daí, você pode explorar camadas, blocos e entidades de underlay sem lidar diretamente com o formato do arquivo DWG.

## Por que extrair flags de underlay de um DWG?
Os flags de underlay indicam como uma referência externa (como um underlay DGN ou PDF) está posicionada, dimensionada e rotacionada dentro do desenho. Conhecer esses valores permite que você:

- Recrie o layout visual exato em um visualizador personalizado.
- Converta underlays em entidades CAD nativas para edição adicional.
- Gere relatórios que incluam metadados de underlay para conformidade ou documentação.

## Pré‑requisitos
- **Biblioteca Aspose.CAD** – faça o download na página de [releases](https://releases.aspose.com/cad/java/).
- **Java Development Kit** – JDK 8 ou superior.
- **Uma pasta** contendo os arquivos DWG que você deseja analisar. Substitua `"Your Document Directory"` no código pelo caminho real.

## Importar Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Guia Passo a Passo

### Etapa 1: Definir o Diretório de Recursos
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Defina onde seus arquivos DWG estão armazenados. Usar uma pasta dedicada mantém o exemplo limpo e portátil.

### Etapa 2: Carregar o Arquivo DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Aqui **carregamos o arquivo dwg** `BlockRefDgn.dwg` em uma instância `CadImage`, pronta para inspeção.

### Etapa 3: Iterar pelas Entidades do DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
O loop percorre cada entidade—linhas, círculos, blocos e underlays—para que possamos selecionar as que precisamos.

### Etapa 4: Identificar Entidades CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Somente objetos `CadDgnUnderlay` contêm os flags de underlay que buscamos, então filtramos por eles.

### Etapa 5: Acessar Informações do Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Depois de obter um `CadUnderlay`, podemos ler seu caminho, nome, ponto de inserção, rotação, fatores de escala e o enum `UnderlayFlags` que indica visibilidade, recorte e outras opções de renderização.

## Problemas Comuns & Dicas
- **Caminho de underlay nulo** – Certifique‑se de que o DWG realmente referencia um arquivo externo; caso contrário, o caminho ficará vazio.
- **Tipo de underlay não suportado** – O Aspose.CAD atualmente suporta underlays DGN; underlays PDF ainda não estão expostos via API.
- **Exceções de licença** – Executar o código sem uma licença válida adicionará uma marca d'água a quaisquer imagens exportadas.

## Perguntas Frequentes

**P: Posso usar o Aspose.CAD para Java com outros formatos de arquivo CAD?**  
R: O Aspose.CAD foca principalmente no formato DWG, mas também suporta DXF, DWF e outros formatos CAD.

**P: Existe uma versão de avaliação disponível para o Aspose.CAD para Java?**  
R: Sim, você pode explorar os recursos com uma avaliação gratuita [aqui](https://releases.aspose.com/).

**P: Como posso obter suporte ou assistência com o Aspose.CAD para Java?**  
R: Visite o [fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**P: Licenças temporárias estão disponíveis para o Aspose.CAD para Java?**  
R: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

**P: Onde encontro a documentação completa do Aspose.CAD para Java?**  
R: Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações detalhadas.

---

**Última atualização:** 2025-12-22  
**Testado com:** Aspose.CAD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}