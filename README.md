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
### Background and challenges 2D vs 2D cartography 
Bocher and Ertz (2018) pointed to the low quality of maps using open standards (OGC included). They suggested taking cartographic theory more into account in the core OGC Symbology encoding standards. Using the visual variables proposed by Bertin (shape, size, hue/colour, value, texture, and orientation; 1967, 1983) as the underlying cartographic instruction, they proposed the symbology code which constitutes a style that describes how a map is authored.
Their activities later (Bocher and Ertz, 2020) grew out in proposing the conceptual basis for the geographical data symbology definition as the OGC Symbology Conceptual Model: Core Part using the Bertins variables for interoperable encoding of cartographic principles. The core concept is extensible for different data models (raster, vector, 2D, 3D, VR) and uses alternative encoding methods (JSON, XML, CSS).
However, the original Bertin’s variables have been extended in various ways.  Several authors added new static visual variables (saturation/intensity, arrangement, focus/crispness, resolution, transparency, spacing) for a specific visualisation context (uncertainty). See fig. xx for examples of static visual variables and the source references. With the advent of computer cartography, visual variables were extended for interactive displays, with six new visual variables: movement, duration, frequency, order, rate of change, and synchronisation. 
The use of the third dimension, however, opened a new perspective in cartographic visualization.
The question is whether we can effectively use the advantages of 3D visualization and eliminate its disadvantages.
Advantages of 3D visualization:
+ more usable space
+ a more natural way of representing the real world
+ additional graphical variables and extensions to existing ones
Disadvantages (weaknesses) of 3D visualisation:
- unequal scale in different parts of the 3D scene (perspective distortion) - overlapping objects
- overlapping objects
- visual clusters
- insufficient use of screen size
New possibilities have been proposed for interactive 3D models: e.g. camera settings, Lighting and illumination, shading, shadows, and atmospheric and environmental effects (Haeberling 2002).
 Use case:
The role of Illumination on colour hue in an interactive display for way finding. Due to the artificial illumination in the three-dimensional virtual world model, the variation in colour hue also suffers a variation in saturation because of natural brightness. The variable lighting and illumination cause different perception and influences the task results. 


Use case 2 (possible)
Does the level of realism affect the participant in the wayfinding task in 3D environment/XR?
Immersive cartography (XR - AR/VR/MR)
Background and challenges
Immersive environments (Çöltekin et al. 2020) are widely used in many fields of human activity – e.g., architecture, culture, crisis management, education, landscape planning, military, tourism, etc. Even in the metaverse, a geospatial aspect appears (Geoconnection, winter 2021).
 Challenges are connected with the displayed content, display devices, control devices, and user aspects. Emerging applications use traditional approaches that need to be modified and standardized for immersive virtual geographic environments.
We can start with the variability of available display devices for 3D environments, from traditional monitors to smartphones to HMDs, and the associated variability of input devices enabling interaction with the given environment. Furthermore, there is unclear use of graphic variables for visualizing the content of a 3D environment when some traditional variables are used only to a limited extent. And last but not least, there are user aspects, including, among other things, ethics, social inequality, the possibility of exclusion, etc.


Use case - Emergency evacuation

The field of emergency management is connected with existing standards dealing with interoperability, interfaces, applications, or data. Currently, a massive amount of 3D spatial data is created in connection with the development of BIM approaches. This data can be used for the purpose of creating immersive environments that can serve, for example, as a virtual asset for crisis management purposes. An example might be an emergency evacuation that can be carried out in a non-existent building if it can be practiced in a digital twin of an existing building, where this approach is significantly cheaper and without the risk of injury to the participants of the emergency evacuation. This approach can be used in the case of a wide range of publicly accessible buildings.
 
For three-dimensional or dynamic media (virtual reality displays, smartphones), the potential for using multidimensional visualization is higher than for static media, e.g.:
- Global view (i.e., bird's eye view) can enable rotation of the navigation plan according to the user's movement and dynamic visualization of markings, escape routes, or user movement in the plan.
- Local view (i.e., first-person view) enables the creation of interactive escape visualizations or simulations or non-interactive escape video animations. These can be used as a complement to the traditional global view of evacuation (an egocentric frame of reference).

Proposed standard / product / output
1.	The transformation from BIM to a Digital twin environment.
 
2.	Visual cues – position of the light source, level of realism, etc. 
3.	Interactions with the environment.
4.	Terminological anchoring of cartographic concepts within immersive geographic environments (connected with the previous chapter)


## 6. Emerging context: Big geospatial data

## 7. Summary of standardization requirements
Summary of aspects of cartographic practice that could be standardized to support broader application of cartographic best practices

## 8. Conclusions

## 9. References
Abhayaratna, J., van den Brink, L., Car, N., Atkinson, R., Homburg, T., Knibbe, F., McGlinn, K., Wagner, A., Bonduel, M., Rasmussen, M. H., Thiery, F. Eds. 2020. OGC Benefits of Representing Spatial Data Using Semantic and Graph Technologies. Open Geospatial Consortium. http://www.opengis.net/doc/wp/using-semantic-graph

Bertin J (1983) Semiology of Graphics: Diagrams, Networks, Maps (1st ed). ESRI Press, California, USA.
 
Bocher, E., and ERTZ, O.(2020): OGC Symbology Conceptual Model: CorePart. Online: http://www.opengis.net/doc/IS/SymCore/1.0

BOCHER and ERTZ (2018), A redesign of OGC Symbology Encoding standard for sharing cartography. PeerJ Comput. Sci. 4:e143; DOI 10.7717/peerj-cs.143

Brewer, C. A. (2003). A transition in improving maps: The ColorBrewer example. Cartography and Geographic Information Science, 30(2), 159-162.

Coetzee, S., and Rautenbach, V. (2017). A design pattern approach to cartography with big geospatial data. The Cartographic Journal, 54(4), 301-312. 

DiBIASE, D., MacEACHREN, A. M., KRYGIER, J. B. a REEVES C. (1992). Animation and the Role of Map Design in Scientific Visualization. Cartography and Geographic
Information Systems, r. 19, č. 4, s. 201-214

Dobres, J., Chahine, N., and Reimer, B. (2017). Effects of ambient illumination, contrast polarity, and letter size on text legibility under glance-like reading. Applied Ergonomics, 60, 68-73.

HAEBERLING, CH. (2005). Cartographic Design Principles For 3D Maps – A Contribution To Cartographic Theory. Proceedings of 22nd ICA Congress Mapping Approaches into a Changing World, A Coruna, Spain, Jul 9-16

Harrower, M., & Brewer, C. A. (2003). ColorBrewer. org: an online tool for selecting colour schemes for maps. The Cartographic Journal, 40(1), 27-37.

Percivall, G, Reed, C. Simonis, I, Lieberman, J, and Ramage, S, 2012. Big Geospatial Data – an OGC White Paper. Available online at https://www.google.com/url?q=https://docs.ogc.org/wp/16-131r2/16-131r2.html&sa=D&source=docs&ust=1683478379205872&usg=AOvVaw3vYPD6-VLCsKwEuGfnWcTv

Piepenbrock, C., Mayr, S., & Buchner, A. (2014). Positive Display Polarity Is Particularly Advantageous for Small Character Sizes: Implications for Display Design. Human Factors, 56(5), 942–951. 

RAUTENBACH, V., COETZEE, S., SCHIEWE, J., and ÇÖLTEKIN, A. (2015). An Assessment of Visual Variables for the Cartographic Design of 3D Informal Settlement Models. Proceedings of the ICC 2015, Rio de Janeiro, Brazil

