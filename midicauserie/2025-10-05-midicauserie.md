<!-- ’ -->
<style display="none">
.flex {
  display: flex;
}
.flex-1 {
  flex: 1;
}
.flex-1-5 {
  flex: 1.5;
}
#ouvroir {
  position: relative;
  right: 10%;
}
#cieco {
  max-width: 50%;
  position: relative;
	left: 5%;
}
#udem {
  margin-top: 0;
  postion: relative;
  bottom: 15%;
}
.reveal h3 {
  margin-top: 1em;  
  }

.reveal .logos {
  margin-top: 2em;
}
</style>

# Présentation de l’ontologie et l’outil **Display**

**Marie Fraser**, **David Valentine**, **Zoë Renaudie** et **Emmanuel Château-Dutier**

05 novembre 2025

<div class="logos flex">
  <div class="flex-1">
    <img id="cieco" src="../img/logo-cieco-grey.svg" style="height: 2.3em;">
  </div>
  <div class="flex-1">
    <img id="ouvroir" src="../img/logo-ouvroir.svg" style="height: 2.1em;">
  </div>
  <div class="flex-1">
    <img id="udem" src="../img/logo-udem-officiel.svg" style="height: 2.5em;">
  </div>
</div>
<!-- Présentation de l’Ouvroir Zoë  -->

===>>>>>>===

# <!-- Partie Marie Fraser  -->

# Le projet Display

===>>>>>>===

<!-- David fait ce que tu veux ici. Peux-tu montrer à quoi ressemble notre jeu de données Feux Pales -->

# Ontologie et jeu de données

L’ontologie Display et notre étude de cas

/** Notes **/

Plan :

- Ontologie Display
  - Outil : documentation, visuel ontologie
- Jeu de données Feux pâles
  - Visuel plan FP et fragments de graphe
  - Outils : point d’accès SPARQL et notices (si le temps le permet)
- Transition : Linked Art, métadonnées et API
  - afin de préparer les données pour l’application

===vvvvvv===

## Les ontologies : organisation des connaissances dans le web sémantique

Une ontologie est une structure abstraite utilisée pour représenter un domaine de connaissances.

Une ontologie s’organise à la manière d’une [toxonomie](https://fr.wikipedia.org/wiki/Taxonomie_(homonymie)) (une structure de classement hiérarchique : par exemple, la classification des espèces), mais avec plus de **flexibilité**.

Une ontologie est flexible car elle fonctionne comme un [graphe](https://fr.wikipedia.org/wiki/Graphe_(type_abstrait)).

([Blaney 2017](https://programminghistorian.org/en/lessons/intro-to-linked-data))

/** Notes **/

tiré de Blaney :

- modéliser l’information dans un champ d’études
- réfléchir à la façon dont on peut représenter les relations dans ce champ
- on utilise une structure de données que l’on appelle une ontologie

> An ontology is an abstraction that allows particular knowledge about the world to be represented.
> Ontologies, in this sense, are quite new and they were designed to do what a hiearchical [taxonomy](https://en.wikipedia.org/wiki/Taxonomy) does (think of the classification of species in the [Linnaean system](https://en.wikipedia.org/wiki/Linnaean_taxonomy)), but more flexibly.

===vvvvvv===

## Les ontologies

<div class="flex">
  <div class="flex-1">
    <p>De la hiérarchie au graphe :</p>

  - descriptions et représentions plus fluides
  - mises en relation plus complexes des objets
    </div>
  <div class="flex-1">
    <figure>
      <img style="margin-top: 0;" data-src="../img/example-01-directed-graph.svg" alt="Exemple de graphe orienté acyclique">
      <figcaption>
        Exemple de graphe orienté acyclique (<a href="https://commons.wikimedia.org/wiki/File:Directed_acyclic_graph.svg">image publiée</a> dans le domaine public par David W.)
      </figcaption>
    </figure>
  </div>
</div>

/** Notes **/

> An ontology is more flexible because it is non-hierarchical.
> It aims to represent the fluidity of the real world, where things can be related to each other in more complex ways than are represented by a hierarchical tree-like structure.
> Instead, an ontology is more like a spider’s web.

===vvvvvv===

## Comment s’organise une ontologie ?

- avec des **classes** qui représentent des **concepts**
- avec des **proprités** qui représentent les **relations** entre les concepts

===vvvvvv===

## La modélisation par classes

<div class="flex">
  <div class="flex-1">
<p>La classe :</p>

  - représente un concept
  - regroupe des individus aux caractéristiques communes
  - s’organise dans une structure hiérarchique
  - hérite des caractéristiques de la classe supérieure

  </div>
  <div class="flex-1">
<p>Relation « is-a » : héritage des caractéristiques</p>
    <figure>
      <img style="margin-top: 0;" data-src="../img/class-inheritance.png" alt="">
      <figcaption>
        Exemple de l’héritage dans la modélisation par classe.
      </figcaption>
    </figure>
  </div>
</div>

===vvvvvv===

## L’approche associative

- définition d’associations (relations) entre les membres des classes
- utilisation de prédicat (verbe) pour créer une relation orientée (modèle RDF)

Les relations entre les membres des classes sont **transversales** à la hiérarchie de la modélisation par classe.

===vvvvvv===

## Les ontologies : des classes et des relations

Les ontologies combinent une approche taxonomique (classement des individus dans une hiérarchie) avec une approche associative (définition des relations entre les membres des classes), nous permettant de créer des modèles complexes et flexibles.

===vvvvvv===

## Les ontologies : des conceptualisations communes

Les ontologies sont des modèles auto-descriptifs très souvent publiés en ligne qui peuvent être accédés et traités par les outils qui implémentent les standards du web sémantique.

## Raisonnement et inférence

- S’ajoute une couche logique qui permet d’inférer (ou déduire) des informations
- Contraintes appliquées aux propriétés
  - Classement automatique
- Typage des propriétés
  - Symétriques
  - Transitives
  - Inverses

===vvvvvv===

## L’ontologie Display

Notre conceptualisation de la topologie de l’exposition.

Accessible en ligne : [https://w3id.org/display](https://ntnlv.ca/display/)

### Survol

- Domaine de connaisances  la topologie de l’exposition
- Classes centrales : l’espace et l’expôt
- Propriétés topologiques pour reconstituer (décrire) l’espace

===vvvvvv===

## Affichage : Noyau ontologique

Une perspective sur l’exposition basée sur :

- le concept d’*Exposition*
- les logiques spatiales (définition de relations topologiques abstraites)

===vvvvvv===

## Affichage : La conceptualisation principale

- tout se déroule dans des espaces d’exposition
- chaque entité d’exposition (artistique ou technique) est une *Exposition*

/** Notes **/

- C’est cette conceptualisation que nous souhaitons partager avec la communauté muséologique grâce aux outils du web sémantique.

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/webvowl/index.html" data-background-interactive class="stack" -->

===vvvvvv===

![Multiple sources](../img/divers.png)

===vvvvvv===

Jeu de données Feux Pâles

===>>>>>>===

# <!-- Partie Zoë  -->

# L’application Display

===vvvvvv===

## Interface

- Une interface graphique permettant aux historiens de l’art d’alimenter l’ontologie
- recueillir des informations historiques et formuler des hypothèses
- générer un rendu de visualisation 3D et simplifié

===vvvvvv===

## Personnae

- l’auxiliaire de recherche 
- le chercheur principal
- le commissaire d’exposition

===vvvvvv===

## Analyse des besoins

- Recherche dans des archives d’exposition
- Documentation lacunaire
- Comparaison d’accrochages d’une œuvre dans plusieurs projets
- Préparation d’une exposition

===vvvvvv===

## Objectifs

- Importer des listes d’œuvres directement depuis vos archives.
- Travailler sur les espaces d’exposition, même si vous ne disposez pas toujours de plans exacts ou complets.
- Localiser les œuvres dans les espaces, et visualiser comment elles étaient disposées.
- Créer des hypothèses sur la base des informations disponibles, et explorer différentes configurations possibles.

===vvvvvv===

## [Tractr](https://www.tractr.net), notre prestataire

![tractr](../img/tractr.png)

===vvvvvv===

## Fonctionnalités principales

- Importation et gestion des œuvres
- Modélisation des espaces d’exposition
- Positionnement des œuvres
- Visualisation des hypothèses

===>>>>>>===

## Développement en cours

===vvvvvv===

## Démo

[lien](https://mk0w088ccoc088cws0og4ckw.tractr.ca/projects)
