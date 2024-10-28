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

# Atelier Display : documenter des accrochages de collection à l’aide d’une approche ontologique

**Zoë&#0160;Renaudie, David&#0160;Valentine et Emmanuel Château-Dutier**

28 octobre 2024

<div class="logos flex">
  <div class="flex-1">
    <img id="cieco" src="./img/logo-cieco-grey.svg" style="height: 2.3em;">
  </div>
  <div class="flex-1">
    <img id="ouvroir" src="./img/logo-ouvroir.svg" style="height: 2.1em;">
  </div>
  <div class="flex-1">
    <img id="udem" src="./img/logo-udem-officiel.svg" style="height: 2.5em;">
  </div>
</div>

===vvvvvv===

![Multiple sources](./img/divers.png)

===vvvvvv===

# Accueil et introduction

===>>>>>>===

## Programme

1. Accueil et introduction
1. L’ontologie Display
1. L’application Display
1. Atelier

===>>>>>>===

# Le projet Display

===vvvvvv===

## Contexte du projet

### Nouveaux usages des collections dans les musées d’art

- Partenariat CRSH
- ~20 chercheurs, 6 musées canadiens
- Axe 1 : *La collection exposée* (Marie Fraser dir.)
- [www.cieco.co](https://www.cieco.co)

### Ouvroir d’histoire de l’art et de muséologie numériques

- Laboratoire destiné à supporter la recherche
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

===vvvvvv===

## Chronologie

2021 : définition des besoins avec les acteurs de l’axe 1
2022 : étude des outils existants
2023 : développement de l’ontologie
2024 : cahier des charges fonctionnel
2025 : développement de l’application

===vvvvvv===

## Présentation colloque

- Journée d’étude CIECO 2023, Réflexions pour un modèle de documentation des accrochages de collection (Marie + Emmanuel + Lena)
- vitrine du CRIHN : présentation des premières expérimentations : démo de visualisation et de requêtes SPARQL
- DHNB2024 Reykjavik : présentation du projet Display
- DH2024 : présentation de l’ontologie Display

===vvvvvv===

## Les modèles de documentation patrimoniaux

- [CIDOC-CRM](http://www.cidoc-crm.org)
- [CRMgeo](doi:[10.1007/s00799-016-0192-4](https://doi.org/10.1007/s00799-016-0192-4).): A Spatiotemporal Extension of CIDOC-CRM
- Art Tracks http://www.museumprovenance.org
- [OntoExhibit](https://complexhibit-project.github.io/OntoExhibit/index-en.html)
- [CRMaaa ontology](https://ontome.net/namespace/246)

**Jusqu’à présent, pas de modèle spécialisé pour la documentation des expositions ou des accrochages**

===>>>>>>===

## Tout ce que vous n’avez jamais voulu savoir sur le web sémantique sans jamais le demandé...

===vvvvvv===

## Web de documents vs web de données

![webDeDonnees](./img/webDeDonnees.png)

===vvvvvv===

![Rdf](./img/rdf01.png)

===vvvvvv===

![Rdf](./img/rdf02.png)

===vvvvvv===

![Rdf](./img/rdf03.png)

===vvvvvv===

![Rdf](./img/rdf04.png)

===vvvvvv===

![Rdf](./img/rdf04.png)

===vvvvvv===

![Rdf](./img/rdf05.png)

===vvvvvv===

![Rdf](./img/rdf06.png)

===vvvvvv===

![Rdf](./img/rdf07.png)

===vvvvvv===

![Rdf](./img/rdf08.png)

===vvvvvv===

![Rdf](./img/rdf09.png)

===vvvvvv===

![Rdf](./img/rdf10.png)

===vvvvvv===

<figure>
  <img data-src="./img/sem-web-layercake.png" alt="La pile technologique du web sémantique">
  <figcaption>
    La pile technologique du web sémantique.
  </figcaption>
</figure>

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
      <img style="margin-top: 0;" data-src="./img/example-01-directed-graph.svg" alt="Exemple de graphe orienté acyclique">
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
      <img style="margin-top: 0;" data-src="./img/class-inheritance.png" alt="">
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

## L’ontologie Display

Notre conceptualisation de la topologie de l’exposition.

Accessible en ligne : [https://w3id.org/display](#)

===vvvvvv===

## Survol de l’ontologie Display

- domaine : la topologie de l’exposition
- les classes centrales : l’espace et l’expôt
- les propriétés pour reconstituer (décrire) l’espace
- revisiter diapos DH24

===vvvvvv===

## Display : Ontological Core

A perspective on the exhibition based on:

- concept of *Exhibit*
- spatial logics (definition of abstract topological relationships)

===vvvvvv===

## Display : The Main Conceptualization

- everything takes place in exhibition spaces
- every exhibition entity (artistic or technical) is an *Exhibit*

/** Notes **/

- And that is the conceptualization we want to share with the museology community using the semantic web tools.

===vvvvvv===

## Display : The Exhibit Class

`display:Exhibit`

![The exhibit class instatiation](./img/ontology-00-display.png)

===vvvvvv===

## Display : Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-topology.png)

===>>>>>>===

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

## Fonctionnalités principales

- Importation et gestion des œuvres
- Modélisation des espaces d’exposition
- Positionnement des œuvres
- Visualisation des hypothèses

===vvvvvv===

## Exemples d’interfaces

- Base de données TMS, Mimsy...

![Axiell](./img/narratives-emu-1.jpg)

===vvvvvv===

- Sketchup, Autocad

![SketchUp](./img/lo-3000193-MacInterface.png)

===vvvvvv===

- [Scratch](https://scratch.mit.edu/)

![Scratch](./img/scratch.png)

===vvvvvv===

- [Kitchen planner](https://kitchen.planner.ikea.com/planner/#/ca/en/)

![ikea](./img/ikea.png)

===vvvvvv===

- [Visualisation abstraite](https://tafc.space/qna/the-topologists-world-map/)

![img](http://tafc.space/wp-content/uploads/qna/topologists-world-map/dark-labelled-2048x2048.png)

===vvvvvv===

## Prestataire

Tractr

![tractr](./img/tractr.png)

===>>>>>>===

# Atelier : décrire la topologie d’une exposition à l’aide de l’ontologie Display

===vvvvvv===

## But de l’atelier

Comparer la proposition conceptuelle de l’ontologie Display à une description commune de la topologie d’une expostion.

===vvvvvv===

## L’ontologie Display plus en détail

- parler

===vvvvvv===

## Rôles

- Auditoire : description d’une exposition
- Ouvroir : encodage de l’information

===vvvvvv===

## Use Case: *Feux pâles*

===vvvvvv===

<style>
  .reveal #credits {
    position: fixed;
    bottom: 0;
    color: #eee;
    left: 0;
    font-size: 14px;
  }
</style>

<!-- .slide:
data-background-image="./img/use-case-00-front.jpeg" data-background-size="auto 100%"
-->

<div id="credits">Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.</div>

===vvvvvv===

## Exhibits & Spaces Relationship

`rdf:type`: Instantiation syntax

![Instantiation syntax](./img/use-case-graph-00.png)

/** Notes **/

- We simply populate the `display:Exhibit` class to indicate the presence of an exhibit in the exhibition.

===vvvvvv===

<!-- .slide: data-visibility="hidden" -->

## Exhibits & Spaces Relationship

Combining the instantiation and the instance

![Instantiation combination visual notation](./img/use-case-graph-01.png)

/** Notes **/

- So from now we can combine the instantiation within a single entity, just to make things lighter.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:containsExhibit`: A space contains an exhibit 

![A space contains an exhibit](./img/use-case-graph-02.png)

<!-- <div class="r-stack">
  <img class="fragment fade-out"
    data-fragment-index="0"
    src="./img/tmp-3.png" />
  <img class="fragment current-visible"
    data-fragment-index="0"
    src="./img/tmp-4.png" />
</div> -->

/** Notes **/

- And we put that work in an exhibition space.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:HangingInterface`: Hanging the exhibits

![Hanging the exhibits](./img/use-case-graph-03.png)

/** Notes **/

- Using the Hanging Interface Class it can easily be stated that the CAPC work (the barcode that welcomes visitors, that we have just seen before) is hung on the entrance display wall, and is contained in the exhibition space.

===vvvvvv===

## Exhibits & Spaces Relationship

The `bot:` namespace: Describing spaces

![Describing spaces](./img/use-case-graph-04.png)

/** Notes **/

- The description of spaces uses the classes and properties of the `bot:` namespace.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:hasExhibitionSpace`: Space contains space

![Space contains space](./img/use-case-graph-05.png)

/** Notes **/

- foo

===vvvvvv===

## *Feux pâles*: Préambule

<figure class="w75">
  <img data-src="./img/use-case-01-preambule.png" alt="Salle d’entrée de l’exposition Feux pâles.">
  <figcaption>Vue de l’exposition Feux pâles (1990), “Préambule”. Photo. : Frédéric Delpech  ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.</figcaption>
</figure>

/** Notes **/

- And finally the entrance area communicates with a first room via two passages.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:PathwayInterface`: Circulating between spaces

![Circulating between spaces](./img/use-case-graph-06.png)

===vvvvvv===

## Exhibition Space Configuration

`bot:intersectsZone`: Intersecting Zones

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-intersections-couloir.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-071.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

`bot:intersectsZone`: Intersecting Zones

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-intersections-spaces.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-07.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

`display:hasExhibitionSpace`: Space contains space

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-inventaire-01.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-08.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

`display:hasExhibitionSpace`: Space contains space

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-inventaire-02.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-08-2.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

`display:adjacentExhibit:`: Spaces share element

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-inventaire-03.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-08-3.png">
  </div>
</div>

===vvvvvv===

## *Feux pâles*: De la propriété littéraire et artistique

<figure class="w75">
  <img data-src="./img/use-case-02-parcelle.png" alt="Salle d’entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 10 “De la propriété littéraire et artistique”. Photo.&#0160;: Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>

===vvvvvv===

## Intersecting Exhibits

`display:intersectingExhibit`: Exhibit spans spaces

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-parcelle.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-09.png">
  </div>
</div>

===vvvvvv===

## *Feux pâles*: Le cabinet d’amateur

<figure class="w75">
  <img data-src="./img/use-case-03-cabinets.png" alt="Salle d’entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 2 “Le Cabinet d’amateur”. Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>


===vvvvvv===

## Topological Relationship Between Exhibits

`display:faces`: vis-à-vis exhibits

<div class="flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/use-case-03-cabinets.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Vue de l’exposition Feux pâles (1990), salle 2 “Le Cabinet d’amateur”. Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-10.png">
  </div>
</div>

===vvvvvv===

## Topological Relationship Between Exhibits

<figure class="w75">
  <img data-src="./img/use-case-04-inventaire.png" alt="Salle d’entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 1 “Inventaire du mémorable”. Photo.&#0160;: Frédéric Delpech © ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>

===vvvvvv===

## Topological Relationship Between Exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](./img/use-case-graph-11-1.png)

===vvvvvv===

## Topological Relationship Between Exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](./img/use-case-graph-11-2.png)

===vvvvvv===

## Topological Relationship Between Exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](./img/use-case-graph-11-3.png)

===vvvvvv===

## Reasoning: Enhance the graph with the `OWL` semantics

![Reasoning](./img/use-case-graph-12-1.png)

===vvvvvv===

## Reasoning: Enhance the graph with the `OWL` semantics

![Reasoning](./img/use-case-graph-12.png)

===>>>>>>===

# A spatial perspective on the exhibition

<!-- @todo check take -->

===vvvvvv===

<!-- .slide: data-visibility="hidden" -->

## 3D for Historical Reconstruction

<iframe width="900" height="506.25" src="https://www.youtube.com/embed/XCqiSbplATU?si=tMcEuk9Lycfnties&amp;start=47" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<p style="font-size: 0.6em">Das Städel museum in 3D, Ihr Virtueller Besuch im Jahr 1878 <a href="http://zeitreise.staedelmuseum.de/vr-app/">http://zeitreise.staedelmuseum.de/vr-app/</a></p>

===vvvvvv===

<!-- .slide: data-visibility="hidden" -->

## From 3D to a documentation model

In our use case

- archival and visual sources are essentials
- limited constructive evidence (*vs* archeology)

**➜ a spatial documentation model independant of any visualisation techniques**

- data exchange and long-term preservation
- various applications
- 3D visualisations



===>>>>>>===

# The Display Ontology

===vvvvvv===

## Ontological Core

A perspective on the exhibition based on:

- concept of *Exhibit*
- spatial logics (definition of abstract topological relationships)

===vvvvvv===

## The Main Conceptualization

- everything takes place in exhibition spaces
- every exhibition entity (artistic or technical) is an *Exhibit*

/** Notes **/

- And that is the conceptualization we want to share with the museology community using the semantic web tools.

===vvvvvv===

## The Exhibit Class

`display:Exhibit`

![The exhibit class instatiation](./img/ontology-00-display.png)

===vvvvvv===

## Handling Description of Space

Reusing the Building Topology Ontology

> The Building Topology Ontology (BOT) is a minimal OWL DL ontology for defining relationships between the sub-components of a building.<br><br>
> (Rasmussen et al., 2021b)

Specification: https://w3c-lbd-cg.github.io/bot/
Namespace: `https://w3id.org/bot#`

===vvvvvv===

## Handling Description of Space

The Building Topology Ontology (BOT)

<figure class="w75">
  <img data-src="./img/bot-zones.png" alt="Salle d’entrée de l’exposition Feux pâles.">
  <figcaption>Classes and relationships involved in Zones (Rasmussen et al., 2021b)</figcaption>
</figure>

===vvvvvv===

## The `bot:` & `display:` Alignment Strategy

![Alignment](./img/ontology-02-alignment.png)

===vvvvvv===

## Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-1-bot-display.png)

===vvvvvv===

## Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-bot-display.png)

===vvvvvv===

## Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-topology.png)

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](./img/ontology-041-cidoc.png)

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](./img/ontology-04-cidoc.png)

===>>>>>>===

# Conclusion

The Display ontology

- can describe complex curatorial phenomena in fine detail 
- offers enough expressivity to leverage the ontological model through inferences

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/" data-background-interactive class="stack" -->

===vvvvvv===

Focusing on the expographic configuration `but` compatible with CIDOC-CRM

**Semantic web technologies provide an abstract model for effectively reasoning about incomplete and sometimes contradictory documentation.**

===vvvvvv===

## Merci !

- Display ontology <br/>[https://ouvroir.github.io/display-ontology/](https://ouvroir.github.io/display-ontology/)
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

<div class="logos" class="flex">
  <div class="flex-1">
    <img style="height: 1.7em" src="./img/logo-cfi.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="./img/logo-quebec.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="./img/logo-udem-officiel.svg">
  </div>
</div>
<div>
  <img style="height: 0.9em" src="./img/logo-crsh-en.svg">
</div>


===vvvvvv===

## Références

<div class="csl-bib-body" style="line-height: 1.35; margin-left: 2em; text-indent:-2em; font-size: 1.5rem">
  <div class="csl-entry" style="margin-bottom: 0.5em;">Guillem, A., Gros, A., Reby, K., Abergel, V. et DeLuca, L. (2023). RCC8 for CIDOC CRM: Semantic Modeling of Mereological and Topological Spatial Relations in Notre-Dame de Paris. Dans A. Bikakis, R. Ferrario, S. Jean, B. Markhoff, A. Mosca et M. Nicolosi Asmundo (dir.), <em>SWODCH’23&#0160: International Workshop on Semantic Web and Ontology Design for Cultural Heritage</em>. <a href="https://hal.science/hal-04275714">https://hal.science/hal-04275714</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=proceeding&amp;rft.atitle=RCC8%20for%20CIDOC%20CRM%3A%20Semantic%20Modeling%20of%20Mereological%20and%20Topological%20Spatial%20Relations%20in%20Notre-Dame%20de%20Paris&amp;rft.btitle=SWODCH%202023&amp;rft.place=Athens%2C%20Greece%2C%20November%207%2C%202023.&amp;rft.aufirst=Ana%C3%AFs&amp;rft.aulast=Guillem&amp;rft.au=Ana%C3%AFs%20Guillem&amp;rft.au=Antoine%20Gros&amp;rft.au=Kevin%20Reby&amp;rft.au=Violette%20Abergel&amp;rft.au=Livio%20DeLuca&amp;rft.au=Antonis%20Bikakis&amp;rft.au=Roberta%20Ferrario&amp;rft.au=St%C3%A9phane%20Jean&amp;rft.au=B%C3%A9atrice%20Markhoff&amp;rft.au=Alessandro%20Mosca&amp;rft.au=Marianna%20Nicolosi%20Asmundo&amp;rft.date=2023&amp;rft.language=en"></span>
  <div class="csl-entry" style="margin-bottom: 0.5em;">Rasmussen, M. H., Lefrançois, M., Schneider, G. F. et Pauwels, P. (2021a). BOT: The building topology ontology of the W3C linked building data group. <em>Semantic Web</em>, <em>12</em>(1), 143‑161. <a href="https://doi.org/10.3233/SW-200385">https://doi.org/10.3233/SW-200385</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_id=info%3Adoi%2F10.3233%2FSW-200385&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Ajournal&amp;rft.genre=article&amp;rft.atitle=BOT%3A%20The%20building%20topology%20ontology%20of%20the%20W3C%20linked%20building%20data%20group&amp;rft.jtitle=Semantic%20Web&amp;rft.stitle=SW&amp;rft.volume=12&amp;rft.issue=1&amp;rft.aufirst=Mads%20Holten&amp;rft.aulast=Rasmussen&amp;rft.au=Mads%20Holten%20Rasmussen&amp;rft.au=Maxime%20Lefran%C3%A7ois&amp;rft.au=Georg%20Ferdinand%20Schneider&amp;rft.au=Pieter%20Pauwels&amp;rft.au=Krzysztof%20Janowicz&amp;rft.date=2021-01-01&amp;rft.pages=143-161&amp;rft.spage=143&amp;rft.epage=161&amp;rft.issn=22104968%2C%2015700844"></span>
  <div class="csl-entry" style="margin-bottom: 0.5em;">Rasmussen, M. H., Pauwels, P., Lefrançois, M. et Schneider, G. F. (2021b, 28 juin). Building Topology Ontology [Draft Community Group Report]. <a href="https://w3c-lbd-cg.github.io/bot/">https://w3c-lbd-cg.github.io/bot/</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=standard&amp;rft.title=Building%20Topology%20Ontology&amp;rft.identifier=https%3A%2F%2Fw3c-lbd-cg.github.io%2Fbot%2F&amp;rft.aufirst=Mads%20Holten&amp;rft.aulast=Rasmussen&amp;rft.au=Mads%20Holten%20Rasmussen&amp;rft.au=Pieter%20Pauwels&amp;rft.au=Maxime%20Lefran%C3%A7ois&amp;rft.au=Georg%20Ferdinand%20Schneider&amp;rft.date=2021-06-28"></span>
  <div class="csl-entry">Renaudie, Z. (2019). <em>Le monde de <em>Feux pâles</em>, l’exposition à l’épreuve de la conservation-restauration, tome I</em> [Mémoire Master II, École supérieure d’art d’Avignon]. <a href="https://www.academia.edu/40627194/Renaudie_Zo%C3%AB_Le_monde_de_Feux_p%C3%A2les_lexposition_%C3%A0_l%C3%A9preuve_de_la_conservation_restauration_TOME_I">https://www.academia.edu/40627194/Renaudie_Zoë_Le_monde_de_Feux_pâles lexposition_à_l’épreuve_de_la_conservation_restauration_TOME_I</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adissertation&amp;rft.title=Le%20monde%20de%20%3Cem%3EFeux%20p%C3%A2les%3C%2Fem%3E%2C%20l%26%2339%3Bexposition%20%C3%A0%20l%26%2339%3B%C3%A9preuve%20de%20la%20conservation-restauration%2C%20tome%20I&amp;rft.aufirst=Zo%C3%AB&amp;rft.aulast=Renaudie&amp;rft.au=Zo%C3%AB%20Renaudie&amp;rft.date=2019&amp;rft.language=fr"></span>
  Blaney
</div>