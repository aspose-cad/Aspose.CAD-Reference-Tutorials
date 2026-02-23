---
date: 2026-02-23
description: Apprenez à charger des fichiers DWG avec Aspose CAD DWG pour Java et
  à extraire les drapeaux de sous‑couche – un guide étape par étape pour les développeurs.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Charger le DWG et accéder aux drapeaux d'underlay (Java)
url: /fr/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

 Aspose  

Then closing shortcodes.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Charger un fichier DWG et accéder aux indicateurs de sous-couche – Aspose.CAD pour Java

Dans les flux de travail CAD modernes, **avec aspose cad dwg vous pouvez charger rapidement un fichier DWG** et extraire les détails de sous-couche souvent cachés aux utilisateurs occasionnels. Que vous construisiez un visualiseur DWG Java, automatisiez un pipeline de traitement par lots dwg, ou extrayiez des métadonnées pour l'intégration GIS, Aspose.CAD pour Java vous offre une méthode propre, orientée code, pour le faire. Dans ce tutoriel, nous parcourrons les étapes exactes pour **charger un fichier DWG**, itérer ses entités et lire les indicateurs de sous-couche que de nombreux développeurs négligent.

## Réponses rapides
- **Quelle est la classe principale pour ouvrir un DWG ?** `com.aspose.cad.Image.load()` renvoie un `CadImage`.
- **Quel objet contient les informations de sous-couche ?** `CadUnderlay` (ou ses types dérivés comme `CadDgnUnderlay`).
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.
- **Puis-je traiter plusieurs fichiers DWG dans une boucle ?** Oui – il suffit de répéter le modèle charger‑et‑itérer.
- **Cette approche est‑elle compatible avec Java 11+ ?** Absolument, Aspose.CAD prend en charge Java 8 jusqu'aux dernières versions LTS.

## aspose cad dwg – Chargement d'un fichier DWG (Java)

`Image.load()` lit le contenu binaire du DWG et crée un objet `CadImage` en mémoire. À partir de là, vous pouvez explorer les calques, blocs et entités de sous-couche sans avoir à gérer vous‑même le format de fichier DWG.

## Pourquoi extraire les indicateurs de sous-couche d'un DWG ?

Les indicateurs de sous-couche vous indiquent comment une référence externe (comme une sous-couche DGN ou PDF) est positionnée, mise à l'échelle et tournée à l'intérieur du dessin. Connaître ces valeurs vous permet de :

- Recréer la mise en page visuelle exacte dans un **visualiseur java dwg** personnalisé.
- Convertir les sous-couches en entités CAD natives pour une édition ultérieure.
- Générer des rapports incluant les métadonnées de sous-couche pour la conformité ou la documentation.
- **Traiter par lots des fichiers dwg** et stocker leurs métadonnées de sous-couche dans une base de données pour une analyse ultérieure.

## Prérequis
- **Aspose.CAD Library** – téléchargez depuis la page des [releases](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 ou plus récent.  
- **Un dossier** contenant les fichiers DWG que vous souhaitez analyser. Remplacez `"Your Document Directory"` dans le code par votre chemin réel.

## Importer les espaces de noms

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire des ressources
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Définissez l'emplacement de vos fichiers DWG. Utiliser un dossier dédié garde l'exemple propre et portable.

### Étape 2 : Charger le fichier DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Ici, nous **chargeons le fichier dwg** `BlockRefDgn.dwg` dans une instance `CadImage`, prête à être inspectée.

### Étape 3 : Itérer les entités DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
La boucle parcourt chaque entité — lignes, cercles, blocs et sous-couches — afin que nous puissions sélectionner celles dont nous avons besoin.

### Étape 4 : Identifier les entités CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Seuls les objets `CadDgnUnderlay` contiennent les indicateurs de sous-couche recherchés, nous les filtrons donc.

### Étape 5 : Accéder aux informations de sous-couche
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Une fois que nous disposons d'un `CadUnderlay`, nous pouvons lire son chemin, son nom, son point d'insertion, sa rotation, ses facteurs d'échelle, ainsi que l'énumération `UnderlayFlags` qui indique la visibilité, le rognage et d'autres options de rendu.

## Comment charger des fichiers dwg dans un processus par lots

Si vous devez **traiter par lots des fichiers dwg**, encapsulez les étapes ci‑dessus dans une simple boucle `for` qui itère sur tous les fichiers de `dataDir`. L'appel `Image.load()` fonctionne pour chaque fichier, et vous pouvez stocker les indicateurs extraits dans un CSV ou une base de données pour des rapports en aval.

## Problèmes courants et astuces
- **Chemin de sous-couche nul** – Assurez‑vous que le DWG référence réellement un fichier externe ; sinon le chemin sera vide.
- **Type de sous-couche non pris en charge** – Aspose.CAD prend actuellement en charge les sous‑couches DGN ; les sous‑couches PDF ne sont pas encore exposées via l'API.
- **Exceptions de licence** – Exécuter le code sans licence valide ajoutera un filigrane à toutes les images exportées.
- **Astuce de performance** : Réutilisez une seule instance `Image` lors du traitement de nombreux fichiers en lot pour réduire la pression du ramasse‑miettes.

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.CAD pour Java avec d'autres formats de fichiers CAD ?**  
R : Aspose.CAD se concentre principalement sur le format DWG, mais il prend également en charge DXF, DWF et d’autres formats CAD.

**Q : Existe‑t‑il une version d'essai disponible pour Aspose.CAD pour Java ?**  
R : Oui, vous pouvez explorer les fonctionnalités avec un essai gratuit depuis [ici](https://releases.aspose.com/).

**Q : Comment obtenir du support ou de l'aide avec Aspose.CAD pour Java ?**  
R : Consultez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

**Q : Des licences temporaires sont‑elles disponibles pour Aspose.CAD pour Java ?**  
R : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver la documentation complète d'Aspose.CAD pour Java ?**  
R : Consultez la [documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées.

---

**Dernière mise à jour :** 2026-02-23  
**Testé avec :** Aspose.CAD 24.12 pour Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}