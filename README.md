# The Idea of ATAG (Applied Text as Graph)

## Introduction

"Applied Text as Graph" is a structured way to handle and analyze text by turning it into an interconnected graph. In this approach, every individual character in a block of text is represented by a "character node" (orange in the next figure). These nodes are connected in sequence, highlighting the linear arrangement of the text. Each block of text, whether it's a word or a paragraph, begins with a  "text node" (blue) that serves as a starting point or a root element. These blocks of text can be linked to one another to suggest a reading sequence. The framework is highly detailed, focusing on the granular level of individual characters. To make referencing specific characters easier, each one is assigned a unique code, known as a UUID.

But the framework isn't just about individual characters; it also allows for the addition of annotations by "annotation nodes" (green). These annotations can provide context or explanations. The annotation node is connected to the specific characters it belongs to. Furthermore, annotations can be linked to a text nodes offering a way to add additional information about the annotation.

So, think of "Applied Text as Graph" as a dynamic, interactive map for text. It not only helps you navigate the content but also enables in-depth analysis and layered annotations.

![ATAG example](https://git.thm.de/aksz15/download/-/raw/master/ATAG/ATAG-example.png)

https://excalidraw.com/#json=3kpVIZ3IIA2Axenielq19,_Br52Sz_N0WnfIvj3taDTg

- There are pieces of linear text
- Every character in this linear text is in a character node (orange) which is connected to the previous or following character node
- Every piece of text can be connected to previous and following pieces of text (in the sense of a proposed reading order)
- Every piece of text starts with a text node
- The granularity is on the character level 
- Every character is adressable by a UUID
- These pieces of text can be annotated by annotations nodes (green)
- These annotation nodes can have a connection to another text node with a characterchain (which can be annotated ...)

## The idea in the Hildegard letter [R2](https://liberepistolarum.mni.thm.de/id/300dcfe1-9f1a-4e21-914d-4730fd85f1d2) in a graph

![Eugenio](https://git.thm.de/aksz15/download/-/raw/master/xml2spo/Eugenio.png)

In the ATAG framework used in the Hildegard project, the main body of text serves as the normalized version, meaning it contains the standard or expanded form of the content. Annotations, on the other hand, are where abbreviations or other variants are stored. This arrangement allows for a clean and readable base text, while still providing a way to include additional forms or information via annotations.

One of the most flexible features of ATAG is its ability to change the base text dynamically, even after annotations have been added. This makes it easy to update or modify the text as needed, without losing any of the associated annotations. This dynamic nature of the base text is especially beneficial for evolving projects or collaborative environments where the text might need to be adjusted frequently.

## The idea in a Socinian [letter](https://sozinianer.de/id/ed_m3l_ldy_vkb)

![Praecellentissime](https://git.thm.de/aksz15/download/-/raw/master/xml2spo/Praecellentissime.png)

In the ATAG framework used in the [Socinian Letter Project](https://sozinianer.mni.thm.de/home), the text you see is considered the original version, capturing the content in its initial form. Any expansions, elaborations, or additional details are stored in the annotations. This setup allows for a clean and unaltered base text, while still offering the capability to add more information or context through annotations. In this way, readers can engage with the original text while also having the option to explore the expanded material, all without cluttering the main body of the text.

## Summary

ATAG, or Applied Text as Graph, is a methodology designed for modeling both text and annotations in a structured manner. At its core, ATAG operates on three main elements: a text node that signifies the beginning of a text block, a chain of individual character nodes that make up the text, and annotations that can be interlinked with another text node. One of the flexible aspects of ATAG is that while it requires a foundational character chain, often referred to as a text stream, it doesn't impose any restrictions on what this chain should contain.

Notably, the base character chain in ATAG is dynamic, meaning you can edit or modify it even after it has been annotated. This is especially useful in collaborative settings or when information is updated. Furthermore, ATAG is designed to handle an almost unlimited number of parallel and overlapping annotations, much like existing Standoff Systems used in text analysis. This makes it highly versatile for complex projects that require layered insights.

Looking ahead, there are several directions for future work in ATAG. The framework is exploring the integration of Text Encoding Initiative (TEI) standards to further enrich its capabilities. Additionally, development is underway for a web-based editor that would make interacting with ATAG more user-friendly. There's also a focus on creating a generic publication system to streamline the process of sharing and disseminating the text and annotations modeled in ATAG.

## Links

### Graphbased publication environment
https://github.com/digicademy/graph-dse

#### used on 
https://sozinianer.mni.thm.de

https://liberepistolarum.mni.thm.de/home

### TEI2json-Converter
https://gitlab.rlp.net/adwmainz/digicademy/sbw/tei2json





