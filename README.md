# Rabble Rouser docs

Herein shall be found all the documentation that pertains to the Rabble Rouser project as a whole. Documentation for Rabble Rouser apps should still be found in the relevant repos. 

Documents that should live in here include anything related to overall architecture and infrastructure, project goals or anything that isn't specific to a particular app.

## Rabble Rouser Domain Concepts

This is one attempt to document Rabble Rouser's domain language. We're using a tool called [concept maps](http://cmap.ihmc.us/docs/theory-of-concept-maps). Concept maps only document the language we use and the relationship between concepts, they are not meant to describe behaviour of a system. Concept maps can help us ensure our understandings of the fundamental concepts in our domain are the same.

![Rabble Rouser Concept Map](./concept_map.png "Rabble Rouser Concept Map")

The Rabble Rouser concept map will hopefully be useful when learning about the project, or introducing others to it.

To update the concept map, you'll need [Graphviz](http://www.graphviz.org/) installed. Graphviz is a command line tool for drawing graphs. We're using the [DOT language](http://www.graphviz.org/content/dot-language) to describe our concepts. Concepts look like:

    member -> organisation [label=" joins "]

Formatting graphs using graphviz can be bit painful, so to keep it simple, concepts are nodes linked with an arror `->`, and we name the edge that represents the relationship with a label `[label=" some label "]` (with a space on either side of the label text to ensure the output is a bit more legible).

To rebuild the graph, try running:

    dot -Tpng concept_map.gv -o concept_map.png

If you make changes to the concept map, please commit the updated graphviz document and output.

## Rabble Rouser logos

For now, logos live here too. There's a transparent `.png` which should cover most of your needs. If you need something else, there's a GIMP `.xcf` file that you can play with. 
