# Rabble Rouser docs

Here is all the documentation for the Rabble Rouser project as a whole. Documentation for individual Rabble Rouser apps should still be found in the relevant repos.

Documents that should live in here include anything related to overall architecture and infrastructure, project goals or anything that isn't specific to a particular app.

## Our vision

Rabble Rouser is for campaigning organisations who need tools to mobilise and organise their members and the community.

Rabble Rouser will be offered without licensing fees, allowing organisations to spend their time and money on the things that matter.

It will have a membership registration core and a set of plugins that perform other functions, eg. email campaigns.

## Our goals

### April 2017

* We have built the stuff our users need the most
* At least one closely allied organisation has adopted RR
* We have sponsorship to fund development

### April 2019

* The community is building plugins for RR
* Rabble Rouser is offered as a service
* Lots of sponsors fund ongoing development
* Rabble Rouser is adopted by lots of progressive campaigning organisations around the world

### April 2021

* Active and self-sustaining open source community
* Rabble Rouser conference
* Permanent Rabble Rouser team
* Rabble Rouser is the de-facto choice for campaigning organisations

## Our challenges

* Distributed team
* Competing priorities
* Decision making
* Maintaining commitment

## Rabble Rouser Domain Concepts

This is one attempt to document Rabble Rouser's domain language. We're using a tool called [concept maps](http://cmap.ihmc.us/docs/theory-of-concept-maps). Concept maps only document the language we use and the relationship between concepts, they are not meant to describe behaviour of a system. Concept maps can help us ensure we all have the same understanding of the fundamental concepts in our domain.

![Rabble Rouser Concept Map](./concept_map.png "Rabble Rouser Concept Map")

The Rabble Rouser concept map will hopefully be useful when learning about the project, or introducing others to it.

To update the concept map, you'll need [Graphviz](http://www.graphviz.org/) installed. Graphviz is a command line tool for drawing graphs. We're using the [DOT language](http://www.graphviz.org/content/dot-language) to describe our concepts. Concepts look like:

    member -> organisation [label=" joins "]

Formatting graphs using graphviz can be bit painful, so to keep it simple, concepts are nodes linked with an arrow `->`, and we name the edge that represents the relationship with a label `[label=" some label "]` (with a space on either side of the label text to ensure the output is a bit more legible).

To rebuild the graph, try running:

    dot -Tpng concept_map.gv -o concept_map.png

If you make changes to the concept map, please commit the updated graphviz document and output.

## Rabble Rouser logos

For now, logos live here too. There's a transparent `.png` which should cover most of your needs. If you need something else, there's a [GIMP](https://www.gimp.org/) `.xcf` file that you can play with.

## Rabble Rouser architectural principles:

* apps should be able to be deployed independently and function alone or in concert
* apps communicate asynchronously with each other through events (and only events). Have a look at **event driven architecture** if you're not familiar.
* apps should be written in whatever language seems right
* all data must be encrypted at rest and in transit
* the environment should be simple to deploy
* the environment should be as secure as we can make it
* the event store is the source of truth
* we value making the environment resiliant and easy to change over keeping costs down

All technical decisions should be filtered through these principles.
