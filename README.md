# Atelier Display

Sources des diapositives de l’atelier sur Display, 28 octobre 2024, Ouvroir d’histoire de l’art et de muséologie numériques.

# Mode d'emploi (source MD)

Titre de niveau 1 (#) : pour les colonnes de diapositives.

Titre de niveau 2 (##) : pour les diapositives.

## Ajouter une diapositive

```
===vvvvvv===
```

Suivi d’un titre de niveau 2.

## Ajouter une colonne

```
===>>>>>>===
```

Suivi d’un titre de niveau 1. Il est possible de n’afficher que le titre de niveau 1 sur la diapositive d’entête de colonne.

## Cacher une diapositive

À insérer directement après le marqueur de nouvelle diapositive :

<!-- .slide: data-visibility="hidden" -->

## Speaker notes

À ajouter avant le marqueur de prochaine diapositive ou colonne. Le MD fonctione aussi dans les speaker notes.

```
/** Notes **/
```

## Modèles

### Image avec légende ou crédits

```html
<figure>
  <img data-src="./img/sem-web-layercake.png" alt="Empilement des différents blocs qui constituent le web sémantique. À l'aide d'une couleur distincte, chaque bloc représente une technologie du web sémantique. Chaque bloc est visible sur deux les faces de l'empilement : sur la face conceptuelle (x) et sur la face des implémentations (y). Etc.">
  <figcaption>
    La pile technologique du web sémantique.
  </figcaption>
</figure>
```

### Deux colonnes

```html
<div style="display: flex">
  <div class="flex-1">
    <p>Colonne 1, à gauche. Lorem ipsum dolor patente.</p>

    - descriptions et représentions plus fluides
    - mises en relation plus complexes des objets
  </div>
  <div class="flex-1">
    <p>Colonne 2. Lorem.</p>
  </div>
</div>
```

Note : à l'intérieur de l'élément `div`, il faut expliciter l'élément `p`.

### Deux colonnes avec image et légende

```html
<div class="flex">
  <div class="flex-1">
    <p>Paragraphe dans la colonne 1.</p>

  - liste dans
  - la colonne 1
  </div>
  <div class="flex-1">
    <figure>
      <img style="margin-top: 0;" data-src="./img/example-01-directed-graph.svg" alt="alt">
      <figcaption>
        Exemple de graphe orienté acyclique (<a href="https://commons.wikimedia.org/wiki/File:Directed_acyclic_graph.svg">publié dans le domaine public par David W.</a>)
      </figcaption>
    </figure>
  </div>
</div>
```

L'attribut `style` est facultatif. Le style peut être défini ailleurs selon les approches habituelles.