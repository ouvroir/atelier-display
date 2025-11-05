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

<!-- Partie Marie Fraser  -->

# Le projet Display



<!-- transition Zoë  -->

===>>>>>>===

<!-- David fait ce que tu veux ici. Peux-tu montrer à quoi ressemble notre jeu de données Feux Pales -->

# Display : une ontologie et des données structurées

Pour traiter l’information extraite des documents et des sources visuelles sur les expositions.

Dans le contexte de la recherche historique : incertitudes et information parcellaire ou incomplète.

- **Modèle conceptuel :** l’ontologie Display
- **Jeu de données :** une étude de cas sur *Feux pâles*
- **Modèle de données :** pour l’utilisation de l’ontologie Display dans un contexte applicatif

/** Notes **/

Plan :

- Ontologie Display
  - Outil : documentation, visuel ontologie
- Jeu de données Feux pâles
  - Visuel plan FP et fragments de graphe
  - Outils : point d’accès SPARQL et notices (si le temps le permet)
- Modèle de données (transition)
  - Linked Art, métadonnées et API
  - afin de préparer les données pour l’application

===vvvvvv===

## L’ontologie Display : perspective spatiale sur l’exposition

Une conceptualisation de la **topologie de l’exposition** mise en œuvre avec les technologies du **web sémantique** :

- `RDF` : principes des données liées
- `OWL` : structuration des connaissaces et logique formelle

/** Notes **/

Une mise en œuvre qui utilise ces technologies nous permet de...

===vvvvvv===

## L’ontologie Display : perspective spatiale sur l’exposition

Création d’un modèle de documentation indépendant de tout type de visualisation.

Basé sur les avantages de l’utilisation des standards du web :

- **interopérabilité** des données
- **pérennisation** des données
- **indépendance** des contextes applicatifs

/** Notes **/

Grâce à ces technologies **standardisées**, 

===vvvvvv===

## Le noyau ontologique

Une perspective sur l’exposition basée sur :

- le concept d’*Exhibit* : **objet situé** dans un espace d’exposition
- une logique spatiale qui définit des **relations topologiques** abstraites permettant :
  - d’exprimer la disposition spatiale des **objets entre eux**
  - d’exprimer la disposition des **objets dans l’espace**

/** Notes **/

- Comment fonctionne ce modèle conceptuel : une unité conceptuelle centrale, l’exhibit.
- Donc essentiellement on décrit sémantiquement, donc à l’aide de termes syntaxe SVO, comment sont positionnés les objets dans l’espace
- C’est cette conceptualisation que nous souhaitons partager avec la communauté muséologique grâce aux outils du web sémantique.

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/webvowl/index.html" data-background-interactive class="stack" -->

/** Notes **/

Modèle conceptuel, donc abstrait. Mais concrètement, on a testé avec Feux pâles.

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
data-background-image="../img/use-case-00-front.jpeg" data-background-size="auto 100%"
-->

<div id="credits">Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.</div>

===vvvvvv===

![Multiple sources](../img/divers.png)

/** Notes **/

In our use case

- archival and visual sources are essentials
- limited constructive evidence (*vs* archeology)

===vvvvvv===

## Définition des espaces d’exposition

`bot:intersectsZone`: Intersecting Zones

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="../img/plan-intersections-couloir.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="../img/use-case-graph-071.png">
  </div>
</div>

===vvvvvv===

## Définition des espaces d’exposition

`bot:intersectsZone`: Intersecting Zones

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="../img/plan-intersections-spaces.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="../img/use-case-graph-07.png">
  </div>
</div>

===vvvvvv===

## Définition des espaces d’exposition

`display:hasExhibitionSpace`: Space contains space

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="../img/plan-inventaire-01.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="../img/use-case-graph-08.png">
  </div>
</div>

===vvvvvv===

## Définition des espaces d’exposition

`display:hasExhibitionSpace`: Space contains space

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="../img/plan-inventaire-02.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="../img/use-case-graph-08-2.png">
  </div>
</div>

===vvvvvv===

## Définition des espaces d’exposition

`display:adjacentExhibit:`: Spaces share element

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="../img/plan-inventaire-03.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="../img/use-case-graph-08-3.png">
  </div>
</div>

===vvvvvv===

## Relations topologiques entre exhibits

<figure class="w75">
  <img data-src="../img/use-case-04-inventaire.png" alt="Salle d'entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 1 “Inventaire du mémorable”. Photo.&#0160;: Frédéric Delpech © ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>

===vvvvvv===

## Relations topologiques entre exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](../img/use-case-graph-11-1.png)

===vvvvvv===

## Relations topologiques entre exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](../img/use-case-graph-11-2.png)

===vvvvvv===

## Relations topologiques entre exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](../img/use-case-graph-11-3.png)

===vvvvvv===

## Inférence : enrichir le graphe de données

![Reasoning](../img/use-case-graph-12-1.png)

===vvvvvv===

## Inférence : enrichir le graphe de données

![Reasoning](../img/use-case-graph-12.png)

===vvvvvv===

## Modèle de données

Un modèle de données pour articuler :

- les données structurées par l’ontologie (Display)
- les métadonnées sur les **œuvres d’art** (CIDOC CRM)

Mais surtout pour :

- faciliter l’utilisation des données dans différents contextes applicatifs grâce à une formalisation idiomatique et documentée (modèle d’API Linked Art)

===>>>>>>===

<!-- Partie Zoë  -->

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

- Importation et gestion des œuvres mais aussi des sources
- Modélisation des espaces d’exposition
- Positionnement des œuvres
- Visualisation des hypothèses

===>>>>>>===

## Développement en cours

===vvvvvv===

## [Tractr](https://www.tractr.net), notre prestataire

![tractr](../img/tractr.png)

===vvvvvv===

## accueil 

![Projet](../img/interface-01.png)

===vvvvvv===

## Capture

![maps](../img/interface-02.png)

===vvvvvv===

## Capture

![maps](../img/interface-03.png)

===vvvvvv===

## Capture

![maps](../img/interface-04.png)

===vvvvvv===

## Capture

![maps](../img/interface-05.png)

===vvvvvv===

## Capture

![maps](../img/interface-06.png)

===vvvvvv===

## Capture

![maps](../img/interface-07.png)

===vvvvvv===

## Capture

![maps](../img/interface-08.png)

===vvvvvv===

## Capture

![visualisation](../img/interface-09.png)

===vvvvvv===

## Démo

[lien](https://mk0w088ccoc088cws0og4ckw.tractr.ca/projects)
