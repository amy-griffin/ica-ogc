# Standards supporting cartographic best practices

## 1. Technical Paper Objective

## 2. Introduction

## 3. Geospatial semantics, cartographic terminology, and applied ontology
### Background 
The complexity and rapidity of very large databases, sometimes called ‘Big Data,’ present challenges for effective processing with widely used software that rely primarily on human interpretation. Research has shown that graph-based models employing basic node-edge-node structures promote semi-automated interpretation of information systems as knowledge representation and reasoning through the application of machine-readable logic axioms.  Formal map semantics federated as a graph are an applied ontology, a digital representation of a world-view.  Efficient ontology schemas require a balance of informal linguistic annotation and formal logic properties relating object sets and their members. Cartographic representations involve visual vocabulary in addition to linguistic annotation for human interpretations, but like Big Data, have semantic processing challenges.  A body of literature has examined map semantics as a type of ‘map language’ from an analogue perspective. Map semantics have also been analyzed using formal logic to identify and clarify consistencies and differences between cartography and linguistics. However, such individual studies have not been integrated to create principles of formal map semantics. 
### Capabilities Vision 
Reasonable expectations for formal map semantic principles extend similar findings for database handling. Among these are the flexibility of graph data organization; the separation of the logical schema from instance data; targeted complex query support; and reasoning rules. Flexibility of the node-edge-node directly link any number of related data with a subject to more clearly and directly represent information concepts. In this way, data portrayal are directly associated with the entities they represent at scales of semantic resolution from primitive features to semantic subgraphs of complex classes, instead of more rigid table layers or indexes. To do so reduces the distinction between ‘data’ and ‘portrayal’ layers often found in GIS.  Entity semantics as associated attributes and properties are developed as a separate schema from data storage, allowing the modification of the target concepts without the need to change the data instance ‘shapes’ in terms of length or structure. Query languages target each resource of a triple separately, allowing for greater semantic specification through more efficient processing. Query designs rely on graph theory approaches to discover database concepts such as neighborhood, inclusion/exclusion, indirectly related information, or erroneous information.  Instance data are set-based as object classes, so groups of individuals are handled all at once through reasoning rules rather than processing each instance individually as they would be in a table.
Significance
Graphs are compatible with a wide range of relational data and can be embedded with statistical techniques such as graph neural network (GNN) and natural language processing to extend maps for Geographic Artificial Intelligence (GeoAI). Qualitatively, ontologies extend semantic representation for human expression and intuitive understanding relating to the representation of a worldview as is normally done in natural language. The logical properties within and between concepts help explain an understanding of context that is key to semantically sensitive interpretation. At different levels of generalization, a carto-ontology formalizes common knowledge relationships, yet supports specific user vocabularies across communities. 
### Use case
The objective of the use case is to build and evaluate visualization for graph-based map semantics within different contexts that draw on capabilities listed below.

-	The semantic specification and differentiation of multi-lingual cartographic terms 
-	The balance of linguistic annotation and logic formalisms in cartography
-	The close physical relation of cartographic representation to data
-	The development of cartographic schema that allows for flexible instantiation
-	Queries that reveal map semantics
-	Portrayal for knowledge discovery through reasoning

The procedure involves the following actions 
-	Map feature definitions of different languages parsed as semantic subgraphs with annotation
-	Aligning portrayal/style/symbology conventions or intuitions to discover and align feature type and spatial relation representation patterns 
-	Exploring extensions of symbology to formal semantic aspects of features
-	Map queries based on semantic specifications 
-	Generalization and summary of results

### Proposed standard / product / output 
-	Key aspects, implications, application context, and recommendation
-	Proposed standardized terminology through an ontology 


## 4. Good cartographic practices in different contexts
### Background
Maps have transitioned from being specialist tools that were designed and produced by experts to ubiquitous tools that support daily business operations and everyday life activities. Many people now have many maps in their pockets, thanks to internet-enabled delivery of spatial information and the computational power of mobile phones. Yet, the power of maps still lies in the way they simplify and generalize the complexity of the world. This means that not all of the world’s information should be included on every map, and maps may need to look different for different map use situations. In a simple example from a map used commonly in everyday life, maps supporting navigation at night need a dark base map to reduce strain on the user’s eyes when switching their gaze between the map and the road. Overall performance, however, tends to generally be better with devices in light mode compared with dark mode (Piepenbrock et al., 2014; Dobres et al., 2017), meaning that dark base maps may be best reserved for map use situations where they provide a distinct benefit. 

Software tools and APIs have also changed the process of making maps, enabling more people to build their own maps for their own purposes. However, making a clear, functional map that is fit for its purpose and audience is not a process that can easily be reduced to a small number of simple rules that will work for all design situations. One design decision can have flow-on consequences for what other design decisions might work well for a given map. Moreover, mobile devices give us the possibility to build maps whose design adapts as the use context changes.  

### Capabilities Vision
The multifactorial, iterative nature of map design and the way that cartographic design decisions interact with each other makes the design of maps a difficult thing to standardize in toto.  A noticable exception to this are certain authoritative map(serie)s, most notably national topographic maps, that do have pre-determined feature catalogs and strict generalization, styling and symbolisation rules.

There have been some efforts to develop basic portrayal standards that describe key features of particular symbol types and layout configurations (see, for example, an effort in this regard from the US Census Bureau). De facto standards also exist. For example, the ColorBrewer color palettes (Harrower and Brewer, 2003; Brewer, 2003) have been implemented in many mapping software packages and maps made with these palettes are seen in common use. 
Such standards, however, operate on individual elements in isolation and do not consider their interactions, meaning that one might follow all of the standards and still not produce a good result. Design templates incorporated into software can be considered a form of standardization, but these also only work well, for example, when the mapped geography fits neatly into the map frame component of the template. 

Despite the success of narrowly focused de facto standards like the ColorBrewer colors, and past attempts to capture the implicit knowledge of expert cartographers in expert systems (e.g., Forrest 2003; Brus et al., 2010; Tsorlini et al., 2017) to build a whole-of-process design standard, none have been successful enough to achieve wide use, perhaps because these standards do not respond to variations in map use context. A considerable challenge is that this context is a wide and multi-facetted notion. It includes physical aspects of the map-reading (such as lighting conditions, device resolution, etc.), but also cognitive and user issues such as map literacy, familiarity with the topic mapped, accessibility, and inclusivity (e.g., of different social and cultural groups). 

To build towards a holistic standard that considers how design elements work together and are shaped by context, a useful approach might be the development of design patterns that could be implemented by software developers (Coetzee and Rautenbach 2017). Design patterns have been described as “a solution to a problem in context” (Alexander (1979) quoted in Shalloway and Trott, 2004, p. 75). Automatically derived (or user-specified) elements of context could be used to determine which design pattern is most helpful for the map use situation.

Recent developments in AI may present an opportunity to learn successful design patterns from existing high-quality maps in different contexts, and their analysis may discover implicit design rules that cross different contexts and could be built into future software.

### Significance

### Use case
Legibility is an important attribute of a successful map. Legibility is determined by whether there is sufficient contrast between map elements and whether the size of elements is large enough for them to be clearly seen, among other factors. Different mobile devices have different capabilities in terms of screen size and display brightness, meaning there are different constraints on the contrast and size of map elements. A design standard could define minimum element sizes and levels of contrast that are needed for elements to be legible and APIs that adhere to the standard could provide methods for automatically sensing these context elements on the device and adjusting their design within the map. Design patterns could describe good choices for particular types of devices (e.g., mobile phone, tablet, laptop, external monitor).

### Proposed standard
-	Standard that describes context elements in a way that allows for their measurement / automatic sensing by sensors on devices that deliver maps.
-	Production of a set of design patterns that can produce reasonably good design starting points.


## 5. Emerging context: 3D and immersive cartography (VR/AR)

## 6. Emerging context: Big geospatial data

## 7. Summary of standardization requirements

## 8. Conclusions
