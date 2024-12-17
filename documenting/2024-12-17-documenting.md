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

# Documenting Exhibitions with the Semantic Web

**Zoë&#0160;Renaudie, David&#0160;Valentine et Emmanuel Château-Dutier**

December 17, 2024

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

===vvvvvv===

# ECD

===vvvvvv===

## Welcome

===vvvvvv===

## Programme

8:30 AM – 8:45 AM: Welcome and introduction to the event and the Ouvroir lab (15 min)  

8:45 AM – 10:00 AM: Presentations (15 min each) in this order :

- Display Ontology (presented by our team)  
- Nuria Rodríguez-Ortega  
- Anaïs Guillem  
- Nicola Carboni  
- George Bruseker  

10:00 AM – 10:15 AM: Break  

10:15 AM – 12:30 PM: Round Table

===vvvvvv===

## New uses of collections in art museums

- SSHRC Partnership
- ~20 researchers, 6 canadian museums
- First axis : *Exhibited Collections* (Marie Fraser dir.)
- [www.cieco.co](https://www.cieco.co)

### Ouvoir d’histoire de l’art et de muséologie numériques

- Digital lab to support the research
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

===vvvvvv===

## Cultural heritage documentation models

- [CIDOC-CRM](http://www.cidoc-crm.org)
- [CRMgeo](doi:[10.1007/s00799-016-0192-4](https://doi.org/10.1007/s00799-016-0192-4).): A Spatiotemporal Extension of CIDOC-CRM
- Art Tracks http://www.museumprovenance.org
- [OntoExhibit](https://complexhibit-project.github.io/OntoExhibit/index-en.html) (other presentation in this conference)
- [CRMaaa ontology](https://ontome.net/namespace/246)

**to date, there is no specialized model for the documentation of exhibition or collection diplays**

===vvvvvv===

## Why Focus on the Semantic Model?  

It drives the tool’s capabilities, ensuring:  

- **Data durability**  
- **Interoperability** across digital platforms  
- Adaptability to new technologies  

===>>>>>>===

# Documenting exhibition and collection displays

![Multiple sources](../img/divers.png)

===vvvvvv===

## A Spatial Approach to Exhibitions  

The *Display* project develops a tool to support exhibition research by:  
- Collecting and analyzing archival data  
- Documenting findings  
- Generating hypotheses  

### Key Features  

- Visualizing exhibitions spatially: **diagrams or 3D models**  
- Bridging gaps in incomplete documentation  
- Enabling **collaborative workflows** for research teams  

===vvvvvv=== 

## From Documentation to 3D Visualization  

Unlike architecture or archaeology, museology lacks "constructive logic" for modeling exhibitions.  
- Exhibition sources: archival documents and photographs  
- Require specialized approaches to reconstruction  

### How *Display* Solves This  

- Supports the full workflow: data collection → hypotheses → 3D reconstructions  
- Powered by an **OWL ontology** to handle uncertainties and gaps in documentation  

 ===vvvvvv=== 

## A tool for studying exhibitions

The *Display* tool redefines how we study exhibitions by:  

- Incorporating **spatial logic** to enhance reconstructions  
- Bridging historical gaps with innovative modeling approaches  
- Ensuring long-term usability and relevance  

**A new way to understand exhibition history through durable, interoperable, and collaborative digital tools.**  

===>>>>>>===

## The Display Ontology

An ontology for the topology of the exhibition


- Namespace: [`https://w3id.org/display#`](https://w3id.org/display/)
- Prefix: `display:`

### Approach

- Knowledge domain: the topology of the exhibition
- Structure: few classes, variety of relations
- Independent of visualization: historical uncertainties may coexist

===vvvvvv===

## Display : Ontological Core

A perspective on the exhibition based on:

- concept of *Exhibit*
- spatial logics (definition of abstract topological relationships)

===vvvvvv===

## Display : The Main Conceptualization

- everything takes place in exhibition spaces
- every exhibition entity (artistic or technical) is an *Exhibit*

===vvvvvv===

## Display : The Exhibit Class

`display:Exhibit`

![The exhibit class instatiation](../img/ontology-00-display.png)

===vvvvvv===

## Handling Description of Space

Reusing the Building Topology Ontology

> The Building Topology Ontology (BOT) is a minimal OWL DL ontology for defining relationships between the sub-components of a building.<br><br>
> (Rasmussen et al., 2021b)

- Namespace: [`https://w3id.org/bot#`](https://w3id.org/bot/)
- Prefix: `bot:`

===vvvvvv===

## Handling Description of Space

The Building Topology Ontology (BOT)

<figure class="w75">
  <img data-src="../img/bot-zones.png" alt="Salle d’entrée de l’exposition Feux pâles.">
  <figcaption>Classes and relationships involved in Zones (Rasmussen et al., 2021b)</figcaption>
</figure>

===vvvvvv===

## The `bot:` & `display:` Alignment Strategy

![Alignment](../img/ontology-02-alignment.png)

===vvvvvv===

## Handling Tolopogical Relationships

<!-- .slide: data-visibility="hidden" -->

![Tolopogical Relationships](../img/ontology-03-1-bot-display.png)

===vvvvvv===

## Handling Tolopogical Relationships

<!-- .slide: data-visibility="hidden" -->

![Tolopogical Relationships](../img/ontology-03-bot-display.png)

===vvvvvv===

## Display : Handling Tolopogical Relationships

![Tolopogical Relationships](../img/ontology-03-topology.png)

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/webvowl/index.html" data-background-interactive class="stack" -->

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](../img/ontology-041-cidoc.png)

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](../img/ontology-04-cidoc.png)

===vvvvvv===

## What’s next

- More exhibitions with the Display ontology
- Multiple instantiation with CIDOC application profiles or extensions

===>>>>>>===

# Discussions, etc.

===vvvvvv===

===>>>>>>===

## Example

```
# Fontaine
exhib:exhibit0015 rdfs:label "Fontaine (Duchamp)" .

# Display
exhib:exhibit0015 a display:Exhibit ;
  display:liesOn exhib:element0029 .

# CIDOC (LA patterns)
exhib:exhibit0015 a crm:E22_Human-Made_Object ;
  crm:P2_has_type aat:300133025 ;
  crm:P1_is_identified_by [...] , [...] ;
  crm:P67i_is_referred_to_by [...] ;
  crm:P108i_was_produced_by [
    a crm:E12_Production ;
    crm:P4_has_time-span [...] ;
    crm:P14_carried_out_by <http://www.wikidata.org/entity/Q5912>
  ] .

# In the set of Feux pâles’s exhibits (using LA generic property)
exhib:exhibit0015 la:member_of exhib:set0000 .

# Set linked with the activity
exhib:activity0000 a crm:E7_Activity ;
  crm:P16_used_specific_object exhib:set0000 .
```

===>>>>>>===

# Conclusion

The Display ontology

- can describe complex curatorial phenomena in fine detail 
- offers enough expressivity to leverage the ontological model through inferences

===vvvvvv===

Focusing on the expographic configuration `but` compatible with CIDOC-CRM

**Semantic web technologies provide an abstract model for effectively reasoning about incomplete and sometimes contradictory documentation.**

===vvvvvv===

## Merci !

- Display ontology <br/>[https://ouvroir.github.io/display-ontology/](https://ouvroir.github.io/display-ontology/)
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

<div class="logos flex">
  <div class="flex-1">
    <img style="height: 1.7em" src="../img/logo-cfi.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="../img/logo-quebec.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="../img/logo-udem-officiel.svg">
  </div>
</div>
<div>
  <img style="height: 0.9em" src="../img/logo-crsh-en.svg">
</div>