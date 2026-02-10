---
date: 2025-12-28
description: Apprenez à personnaliser les polices dans les dessins DWG avec Aspose.CAD
  pour Java. Guide étape par étape pour ajouter du texte, remplacer les polices et
  perfectionner les annotations CAD.
linktitle: CAD Text and Annotation
second_title: Aspose.CAD Java API
title: Comment personnaliser les polices dans le texte et les annotations CAD
url: /fr/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment personnaliser les polices dans le texte CAD et les annotations

## Introduction 

Si vous cherchez à **personnaliser les polices** dans vos dessins DWG, vous êtes au bon endroit. Dans ce tutoriel, nous vous guiderons à travers l’ajout de texte, le remplacement des polices et l’ajustement des styles de police à l’aide d’Aspose.CAD for Java. Que vous raffiniez un schéma, prépariez des documents de construction ou souhaitiez simplement une **annotation de texte dwg** plus claire, ces étapes vous aideront à obtenir une finition professionnelle rapidement et de manière fiable.

## Réponses rapides
- **Quel est le principal objectif de la personnalisation des polices dans DWG ?** Améliorer la lisibilité et correspondre à la marque ou aux normes du projet.  
- **Quelle bibliothèque gère les modifications ?** Aspose.CAD for Java.  
- **Ai-je besoin d’une licence ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour la production.  
- **Puis-je traiter de gros fichiers DWG ?** Oui – l’API diffuse les données efficacement, adaptée aux grands dessins.  
- **Un logiciel supplémentaire est‑il requis ?** Seul un runtime Java (JDK 8 ou plus récent) et le JAR Aspose.CAD.

## Qu’est‑ce que la « personnalisation des polices » dans le CAD ?
Personnaliser les polices signifie remplacer le style de texte par défaut dans un fichier DWG par une police de votre choix, ajuster sa taille, son épaisseur ou appliquer un style différent à des calques ou objets spécifiques. Cela garantit que le dessin apparaît exactement comme vous le souhaitez sur tous les visionneurs.

## Pourquoi utiliser Aspose.CAD for Java pour personnaliser les polices ?
- **Contrôle total** sur les objets texte sans ouvrir le dessin dans un éditeur GUI.  
- **Traitement par lots** – traiter des dizaines de fichiers dans un seul script.  
- **Multi‑plateforme** – fonctionne sous Windows, Linux et macOS.  
- **Aucune dépendance externe** – l’API gère l’analyse DWG en interne.

## Prérequis
- Java Development Kit 8 ou plus récent installé.  
- JAR Aspose.CAD for Java ajouté au classpath de votre projet.  
- Un fichier DWG que vous souhaitez modifier.

## Comment ajouter du texte dans un DWG
Ajouter de nouvelles informations textuelles est un besoin fréquent lorsque vous souhaitez étiqueter des pièces, ajouter des notes ou créer une **annotation de texte dwg**. Suivez ces étapes :

1. **Charger le fichier DWG** en utilisant `CadImage`.  
2. **Créer une entité `CadText`** avec la chaîne souhaitée, l’emplacement et la police.  
3. **Ajouter l’entité** à la collection d’entités du dessin.  
4. **Enregistrer** le fichier modifié.

> *Note : Le fragment de code réel n’est pas modifié par rapport au tutoriel original et est inclus dans le sous‑tutoriel lié.*  

## Comment remplacer la police dans un DWG
Remplacer une police existante dans tout le dessin aide à maintenir la cohérence, surtout lorsque la police d’origine n’est pas disponible sur le système cible.

1. **Ouvrir le DWG** avec `CadImage`.  
2. **Itérer** sur tous les objets `CadText`.  
3. **Définir la propriété `FontName`** à la police de votre choix (par ex., « Arial »).  
4. **Enregistrer** le dessin mis à jour.

Cette méthode est détaillée dans le sous‑tutoriel « Substitute Font in DWG ».

## Comment changer le style de police DWG pour un style particulier
Parfois, seul un style de texte spécifique (par ex., « Title ») nécessite une nouvelle police tandis que les autres restent inchangés.

1. **Identifier le nom du style** que vous souhaitez modifier.  
2. **Localiser l’objet `CadTextStyle` correspondant**.  
3. **Mettre à jour son `FontName`** ainsi que tout attribut de style supplémentaire.  
4. **Conserver les modifications** en enregistrant le fichier.

Le guide étape par étape est disponible dans le sous‑tutoriel « Substitute Font of a Particular Style in DWG ».

## Cas d’utilisation courants
- **Dessins de construction** où les polices standard de l’entreprise sont obligatoires.  
- **Plans architecturaux** qui nécessitent des annotations lisibles pour les clients.  
- **Conversion par lots** de fichiers DWG anciens vers un nouveau jeu de polices d’entreprise.

## Tutoriels sur le texte CAD et les annotations
### [Ajouter du texte dans un DWG avec Aspose.CAD for Java](./add-text-in-dwg/)
Améliorez vos dessins DWG sans effort avec Aspose.CAD for Java. Ajoutez du texte de manière fluide grâce à notre guide étape par étape.

### [Remplacer la police dans un DWG avec Aspose.CAD for Java](./substitute-font-in-dwg/)
Améliorez vos conceptions CAD sans effort. Apprenez à remplacer les polices dans les fichiers DWG en utilisant Aspose.CAD for Java. Guide étape par étape pour une perfection visuelle.

### [Remplacer la police d’un style particulier dans un DWG avec Aspose.CAD for Java](./substitute-font-of-particular-style-in-dwg/)
Apprenez comment remplacer les polices dans les fichiers DWG en utilisant Aspose.CAD for Java. Guide étape par étape pour personnaliser les styles avec précision.

## Questions fréquentes

**Q : Puis‑je utiliser ces méthodes avec des fichiers DWG créés dans d’anciennes versions d’AutoCAD ?**  
A : Oui. Aspose.CAD prend en charge les versions DWG de R12 jusqu’aux dernières versions.

**Q : Que se passe‑t‑il si la police cible n’est pas installée sur la machine du visualiseur ?**  
A : Le dessin reviendra à une police par défaut, ce qui peut affecter la mise en page. Il est recommandé d’incorporer la police ou de s’assurer qu’elle est installée sur toutes les machines.

**Q : Est‑il possible de remplacer les polices uniquement sur un calque spécifique ?**  
A : Absolument. Filtrez les objets `CadText` par leur `LayerName` avant de modifier le `FontName`.

**Q : Dois‑je reconstruire le dessin après les changements de police ?**  
A : Aucune reconstruction manuelle n’est requise ; l’enregistrement du `CadImage` écrit toutes les mises à jour dans le fichier.

**Q : Comment puis‑je vérifier que le changement de police a été appliqué correctement ?**  
A : Ouvrez le DWG dans n’importe quel visualiseur qui prend en charge la police choisie, ou énumérez programmatique les objets `CadText` pour lire à nouveau le `FontName`.

---

**Dernière mise à jour :** 2025-12-28  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
