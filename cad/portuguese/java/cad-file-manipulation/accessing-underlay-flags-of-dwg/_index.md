---
date: 2026-02-23
description: Aprenda a carregar arquivos DWG usando Aspose CAD DWG para Java e extrair
  flags de underlay – um guia passo a passo para desenvolvedores.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Carregar DWG e Acessar Flags de Underlay (Java)
url: /pt/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Carregar Arquivo DWG e Acessar Flags de Substituição – Aspose.CAD for Java

Em fluxos de trabalho CAD modernos, **com aspose cad dwg você pode carregar rapidamente um arquivo DWG** e extrair detalhes de sub-referência que frequentemente ficam ocultos para visualizadores casuais. Seja construindo um visualizador DWG em Java, automatizando um pipeline de processamento em lote de DWG, ou extraindo metadados para integração GIS, Aspose.CAD for Java oferece uma maneira limpa, orientada a código, de fazer isso. Neste tutorial, percorreremos os passos exatos para **carregar um arquivo DWG**, iterar suas entidades e ler as flags de sub-referência que muitos desenvolvedores ignoram.

## Quick Answers
- **Qual é a classe principal para abrir um DWG?** `com.aspose.cad.Image.load()` retorna um `CadImage`.
- **Qual objeto contém as informações de sub-referência?** `CadUnderlay` (ou seus tipos derivados como `CadDgnUnderlay`).
- **Preciso de uma licença para desenvolvimento?** Uma versão de avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.
- **Posso processar vários arquivos DWG em um loop?** Sim – basta repetir o padrão de carregar‑e‑iterar.
- **Esta abordagem é compatível com Java 11+?** Absolutamente, Aspose.CAD suporta Java 8 até as versões LTS mais recentes.

## aspose cad dwg – Loading a DWG File (Java)

`Image.load()` lê o conteúdo binário do DWG e cria um objeto `CadImage` em memória. A partir daí, você pode explorar camadas, blocos e entidades de sub-referência sem precisar lidar com o formato de arquivo DWG diretamente.

## Why extract underlay flags from a DWG?

Underlay flags informam como uma referência externa (como um sub-referência DGN ou PDF) está posicionada, dimensionada e rotacionada dentro do desenho. Conhecer esses valores permite que você:

- Recriar o layout visual exato em um **visualizador java dwg** personalizado.
- Converter sub-referências em entidades CAD nativas para edição adicional.
- Gerar relatórios que incluam metadados de sub-referência para conformidade ou documentação.
- **Processar arquivos dwg em lote** e armazenar seus metadados de sub-referência em um banco de dados para análise posterior.

## Prerequisites
- **Aspose.CAD Library** – download da página de [releases](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 ou superior.  
- **Uma pasta** contendo os arquivos DWG que você deseja analisar. Substitua `"Your Document Directory"` no código pelo caminho real.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Defina onde seus arquivos DWG estão localizados. Usar uma pasta dedicada mantém o exemplo limpo e portátil.

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Aqui nós **carregamos o arquivo dwg** `BlockRefDgn.dwg` em uma instância `CadImage`, pronta para inspeção.

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
O loop percorre cada entidade — linhas, círculos, blocos e sub-referências — para que possamos selecionar as que precisamos.

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Apenas objetos `CadDgnUnderlay` contêm as flags de sub-referência que buscamos, portanto filtramos por eles.

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Uma vez que temos um `CadUnderlay`, podemos ler seu caminho, nome, ponto de inserção, rotação, fatores de escala e o enum `UnderlayFlags` que indica visibilidade, recorte e outras opções de renderização.

## How to load dwg files in a batch process

Se precisar **processar arquivos dwg em lote**, envolva as etapas acima em um simples loop `for` que itere sobre todos os arquivos em `dataDir`. A mesma chamada `Image.load()` funciona para cada arquivo, e você pode armazenar as flags extraídas em um CSV ou em um banco de dados para relatórios posteriores.

## Common Issues & Tips
- **Caminho de sub-referência nulo** – Certifique-se de que o DWG realmente referencia um arquivo externo; caso contrário, o caminho ficará vazio.
- **Tipo de sub-referência não suportado** – O Aspose.CAD atualmente suporta sub-referências DGN; sub-referências PDF ainda não estão expostas via API.
- **Exceções de licença** – Executar o código sem uma licença válida adicionará uma marca d'água a quaisquer imagens exportadas.
- **Dica de desempenho:** Reutilize uma única instância `Image` ao processar muitos arquivos em lote para reduzir a pressão do GC.

## Frequently Asked Questions

**Q: Posso usar Aspose.CAD for Java com outros formatos de arquivo CAD?**  
A: O Aspose.CAD foca principalmente no formato DWG, mas também suporta DXF, DWF e outros formatos CAD.

**Q: Existe uma versão de avaliação disponível para Aspose.CAD for Java?**  
A: Sim, você pode explorar os recursos com uma avaliação gratuita a partir de [aqui](https://releases.aspose.com/).

**Q: Como posso obter suporte ou assistência com Aspose.CAD for Java?**  
A: Visite o [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) para suporte da comunidade e discussões.

**Q: Licenças temporárias estão disponíveis para Aspose.CAD for Java?**  
A: Sim, você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso encontrar a documentação completa para Aspose.CAD for Java?**  
A: Consulte a [documentação](https://reference.aspose.com/cad/java/) para informações detalhadas.

---

**Última atualização:** 2026-02-23  
**Testado com:** Aspose.CAD 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}