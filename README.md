# (DRAFT) Standards supporting cartographic best practices 
Contributors: Amy Griffin, Serena Coetzee, Silvana Camboim, Dalia Varanka, Francis Harvey, Petr Kubicek, Zdenek Stachon, Iain Burnell, Keith Ryden

## 1. Introduction
Contemporary cartographic practice uses a range of computing technologies to build print and electronic medium maps. Some technologies allow the creation only of simple maps, through manipulation of a constrained set of design parameters (e.g., Mapline or Google’s MyMaps). Others allow the manipulation of an expansive range of design elements (e.g., ArcGIS Pro, QGIS, Mapbox). Many software tools for making maps are not built by cartographers, but rather by software engineers, some of whom have limited cartographic training or mapmaking experience. Among the tools developers may use to help them design and implement mapmaking software are standards, such as those developed by groups like the Open Geospatial Consortium (OGC). 

Bocher & Ertz (2018) pointed to the low quality of maps using open standards (OGC included). They suggested a stronger focus on cartographic theory in the core OGC Symbology encoding standards and developed a proposed conceptual basis for defining geographical data symbology (Bocher & Ertz, 2020). This standard, now called the OGC Cartographic Symbology Standard, defines conceptual and logical models for symbols and offers encodings for transmitting and interoperating symbols between map production technologies. The standard includes examples that demonstrate that the standard can be applied to produce maps. What the standard doesn't currently do is support software designers to build in best practices in composing maps from these symbols. In other words, it doesn't provide guidance on which symbols could be successfully used together. 

Periodically, researchers have tried to capture cartographic knowledge to help non-experts make good maps using varied approaches, including expert systems, cartographic workflows, and cartographic ontologies (Forrest, 1993; Brus et al., 2010; Tsorlini et al., 2017).  Software engineers are usually not attempting to design software to entirely replace mapmakers but rather to support the cartographic design process. Their task is to apply a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software (Bourque & Fairly, 2014) for which they need an understanding of the fundamentals of computer science, namely the systematic study of algorithms (i.e., workflows) and data structures (i.e., ontologies) (Gibbs & Tucker, 1986). We consider how we might connect software engineers’ knowledge of algorithms and data structures to cartographic expertise via cartographic workflows or cartographic ontologies, respectively. 

Software engineers are familiar with workflows and often think in such terms (Wing, 2014). A workflow is the series of activities necessary to complete a task (ISO 12967-1:2020) and can be distinguished from an expert system in that it is not able to learn from experience and is therefore more constrained in its operations and outcomes (Aniba et al., 2009). As an unstructured problem, the cartographic design process is contingent in nature; design decisions are influenced by a multiplicity of contextual factors (Griffin et al., 2017).  This characteristic suggests potentially it might help to combine workflows with design patterns (Coetzee & Rautenbach, 2017), when seeking to communicate cartographic knowledge to software engineers.

Software engineers are also familiar with schema representation of data and information. Ontology design patterns (ODP) are general templates that describe entities and relations for topical information schemas. Their development often begins as concept maps or a set of natural language propositions stating the core constraints to be represented by the schema. They guide the design of applied ontologies by suggesting a formal logic semantic structure among sets of objects and literal annotation (Fig. 1). Concurrently, Knowledge Representation and Reasoning expertise has developed to make concept models dynamic through executable logic. Such general schemas are refined by communities in application to take local practices and approaches into account (D’Ignazio & Klein, 2019).
 
Figure 1. ODP example ‘Place.’ (Aldo Gangemi, Submissions:Place - Odp (ontologydesignpatterns.org))

In this technical paper, we explore some different opportunities for how the future development and use of standards can support developers in embedding cartographic best practice into software design. Cartographic workflows and ontologies can support the approach of building expert systems, or systems based on artificial intelligence, to construct solutions that can help users build knowledge and helpful maps within the current panorama of an abundance of available spatial data.


## 2. Geospatial semantics, cartographic terminology, and applied ontology
### Background 
The complexity and rapidity of data and changes to data in very large databases, sometimes called ‘Big Data,’ present challenges for effective processing with widely used software that rely primarily on human interpretation. Research has shown that graph-based models employing basic node-edge-node structures promote semi-automated interpretation of information systems as knowledge representation and reasoning through the application of machine-readable logic axioms.  Formal map semantics federated as a graph are an applied ontology, a digital representation of a world-view.  Efficient ontology schemas require a balance of informal linguistic annotation and formal logic properties relating object sets and their members. Cartographic representations involve visual vocabulary in addition to linguistic annotation for human interpretations, but like Big Data, have semantic processing challenges.  A body of literature has examined map semantics as a type of ‘map language’ from an analogue perspective. Map semantics have also been analyzed using formal logic to identify and clarify consistencies and differences between cartography and linguistics. However, such individual studies have not been integrated to create principles of formal map semantics. 

### Capabilities Vision 
Reasonable expectations for formal map semantic principles extend similar findings for database handling. Among these are the flexibility of graph data organization; the separation of the logical schema from instance data; targeted complex query support; and reasoning rules. Flexibility of the node-edge-node directly link any number of related data with a subject to more clearly and directly represent information concepts. In this way, data portrayal are directly associated with the entities they represent at scales of semantic resolution from primitive features to semantic subgraphs of complex classes, instead of more rigid table layers or indexes. To do so reduces the distinction between ‘data’ and ‘portrayal’ layers often found in GIS.  Entity semantics as associated attributes and properties are developed as a separate schema from data storage, allowing the modification of the target concepts without the need to change the data instance ‘shapes’ in terms of length or structure. Query languages target each resource of a triple separately, allowing for greater semantic specification through more efficient processing. Query designs rely on graph theory approaches to discover database concepts such as neighborhood, inclusion/exclusion, indirectly related information, or erroneous information.  Instance data are set-based as object classes, so groups of individuals are handled all at once through reasoning rules rather than processing each instance individually as they would be in a table.

Graphs are compatible with a wide range of relational data and can be embedded with statistical techniques such as graph neural network (GNN) and natural language processing to extend maps for Geographic Artificial Intelligence (GeoAI). Qualitatively, ontologies extend semantic representation for human expression and intuitive understanding relating to the representation of a worldview as is normally done in natural language. The logical properties within and between concepts help explain an understanding of context that is key to semantically sensitive interpretation. At different levels of generalization, a carto-ontology formalizes common knowledge relationships, yet supports specific user vocabularies across communities. 

### Use case
In a multinational geoinformation system project, a team of designers, managers, end users, developers, and other experts from different regions are working together to develop a comprehensive mapping system. The team encounters communication issues due to inconsistencies in the understanding and usage of key cartographic terms such as "Map Projection" and "Toponym" (Table 1). This leads to confusion, misinterpretation, and delays in project execution. Importantly, these communication issues can stem not only from differences in the languages that project participants speak, but also their level of experience with geospatial tools and disciplinary background.

Standardization of definitions and workflows is required to streamline communication and ensure a shared understanding of important cartographic terms. The goal is to develop a Unified Cartographic Definitions and Workflows Alignment (UCDWA) that can be accessed and understood by all stakeholders involved in the project, irrespective of their geographic location or professional background. Notably, this ontology should deal not only with language differences, but also locale (language + country) differences in terminology.

The UCDWA is a centralized, web-accessible resource that provides unified, scientifically-based definitions for key cartographic terms and processes. The database leverages the work of the ICA, the OGC, and other renowned bodies in cartography. It includes terms from the Multilingual Dictionary of Technical Terms in Cartography, CartoBOK, OGC Definitions Server, OSGeo Lexicon, and other authoritative sources. Recognizing the global nature of geoinformation system projects, the UCDWA provides translations of definitions in multiple languages and locales, making it accessible to a wide range of users. It is also designed to be easily parsed by automated systems, ensuring seamless integration into automated workflows. Finally, it should also have a user-friendly interface and be continuously updated to ensure it remains current with the latest developments in cartographic science.

| Source | URL | Definition |
| ------ | --- | ---------- | 
| Map Projection (ICA Body of Knowledge) | https://ltb.itc.utwente.nl/page/659/concept/131500 | Map projection is the mapping from the curved surface into a plane. |
| Map Projection (ISO TC211) | https://isotc211.geolexica.org/concepts/618/ | Coordinate conversion from an ellipsoidal coordinate system to a plane. | 
| Map Projection (OGC Definitions Server) | https://defs.opengis.net/vocprez/object?uri=http%3A//www.opengis.net/def/glossary/term/MapProjection | A coordinate conversion from a geodetic coordinate system to a planar surface, converting geodetic latitude and longitude to plane (map) coordinates. The result is a two-dimensional coordinate system called a projected coordinate reference system. |

Table 1: Example of differences in terminology definitions among sources.


### Proposed outputs
-	Proposed standardization of terminology through an ontology (i.e., the UCDWA)
-	Explore the linkage of similar (but not equivalent) concepts
-	Case study thematic map design workflows that connect multiple definition servers to develop a proof of concept for UCDWA
  
## 3. Good cartographic practices in different contexts
### Background
Maps have transitioned from being specialist tools that were designed and produced by experts to ubiquitous tools that support daily business operations and everyday life activities. Many people now have many maps in their pockets, thanks to internet-enabled delivery of spatial information and the computational power of mobile phones. Yet, the power of maps still lies in the way they simplify and generalize the complexity of the world. This means that not all of the world’s information should be included on every map, and maps may need to look different for different map use situations. In a simple example from a map used commonly in everyday life, maps supporting navigation at night need a dark base map to reduce strain on the user’s eyes when switching their gaze between the map and the road. Overall performance, however, tends to generally be better with devices in light mode compared with dark mode (Piepenbrock et al., 2014; Dobres et al., 2017), meaning that dark base maps may be best reserved for map use situations where they provide a distinct benefit. 

Software tools and APIs have also changed the process of making maps, enabling more people to build their own maps for their own purposes. However, making a clear, functional map that is fit for its purpose and audience is not a process that can easily be reduced to a small number of simple rules that will work for all design situations. One design decision can have flow-on consequences for what other design decisions might work well for a given map. Moreover, mobile devices give us the possibility to build maps whose design adapts as the use context changes.  

### Capabilities Vision
The multifactorial, iterative nature of map design and the way that cartographic design decisions interact with each other makes the design of maps a difficult thing to standardize in toto.  A noticable exception to this are certain authoritative map series, most notably national topographic maps, that do have pre-determined feature catalogs and strict generalization, styling and symbolisation rules.

There have been some efforts to develop basic portrayal standards that describe key features of particular symbol types and layout configurations (see, for example, an effort in this regard from the US Census Bureau). De facto standards also exist. For example, the ColorBrewer color palettes (Harrower and Brewer, 2003; Brewer, 2003) have been implemented in many mapping software packages and maps made with these palettes are seen in common use. Such standards, however, operate on individual elements in isolation and do not consider their interactions, meaning that one might follow all of the standards and still not produce a good result. Design templates incorporated into software can be considered a form of standardization, but these also only work well, for example, when the mapped geography fits neatly into the map frame component of the template. 

Despite the success of narrowly focused de facto standards like the ColorBrewer colors, and past attempts to capture the implicit knowledge of expert cartographers in expert systems (e.g., Forrest 2003; Brus et al., 2010; Tsorlini et al., 2017) to build a whole-of-process design standard, none have been successful enough to achieve wide use, perhaps because these standards do not respond to variations in map use context. A considerable challenge is that this context is a wide and multi-faceted notion. It includes physical aspects of the map-reading (such as lighting conditions, device resolution, etc.), but also cognitive and user issues such as map literacy, familiarity with the topic mapped, accessibility, and inclusivity (e.g., of different social and cultural groups). 

To build towards a holistic solution that considers how design elements work together and are shaped by context, a useful approach might be the development of design patterns that could be implemented by software developers (Coetzee and Rautenbach, 2017). Design patterns have been described as “a solution to a problem in context” (Alexander (1979) quoted in Shalloway and Trott, 2004, p. 75). Automatically derived (or user-specified) elements of context could be used to determine which design pattern is most helpful for the map use situation.

Recent developments in AI may present an opportunity to learn successful design patterns from existing high-quality maps in different contexts, and their analysis may discover implicit design rules that cross different contexts and could be built into future software.

### Use case
Legibility is an important attribute of a successful map. Legibility is determined by whether there is sufficient contrast between map elements and whether the size of elements is large enough for them to be clearly seen, among other factors. Different mobile devices have different capabilities in terms of screen size and display brightness, meaning there are different constraints on the contrast and size of map elements. A design standard could define minimum element sizes and levels of contrast that are needed for elements to be legible and APIs that adhere to the standard could provide methods for automatically sensing these context elements on the device and adjusting their design within the map. Design patterns could describe good choices for particular types of devices (e.g., mobile phone, tablet, laptop, external monitor).

### Proposed outputs
-	Standard that describes context elements in a way that allows for their measurement / automatic sensing by sensors on devices that deliver maps.
-	Production of a set of design patterns that can produce reasonably good design starting points for the production of a map.


## 4. Emerging context: 3D and immersive cartography (VR/AR)
### Background and challenges 
Bocher and Ertz (2018) pointed to the low quality of maps using open standards (OGC included). They suggested taking cartographic theory more into account in the core OGC Symbology encoding standards. Using the visual variables proposed by Bertin (shape, size, hue/colour, value, texture, and orientation; 1967, 1983) as the underlying cartographic instruction, they proposed the symbology code which constitutes a style that describes how a map is authored.

This was later elaborated into the conceptual basis for the geographical data symbology definition as the OGC Symbology Conceptual Model: Core Part using the Bertin's variables for interoperable encoding of cartographic principles (Bocher and Ertz, 2020). The core concept is extensible for different data models (raster, vector, 2D, 3D, VR) and uses alternative encoding methods (JSON, CSS).
However, Bertin’s variables original visual variables have been extended in various ways.  Several authors added new static visual variables (saturation/intensity, arrangement, focus/crispness, resolution, transparency, spacing) for specific visualisation contexts (e.g., uncertainty). See fig. xx for examples of static visual variables and the source references. Visual variables have also been extended for interactive displays, with six new visual variables: movement, duration, frequency, order, rate of change, and synchronisation. 

The use of the third dimension, however, has opened a new perspective in cartographic visualization. The question is whether we can effectively use the advantages of 3D visualization and eliminate its disadvantages (Table 2).

| Advantages of 3D                            | Disadvantages of 3D               |
| ------------------------------------------- | --------------------------------- |
| More usable space                           | Perspective distortion            | 
| More natural way of representing the world  | Overlapping objects               |
| Additional visual variables                 | Visual clutter                    |
| Extensions to existing visual variables     | Insufficient use of screen space  |

Table 2. Opportunities and Constraints in 3D Visualization.

## Capabilities Vision
For three-dimensional or dynamic media (virtual reality displays, smartphones), the potential for using multidimensional visualization is higher than for static media, e.g.:
- Global view (i.e., bird's eye view) can enable rotation of the navigation plan according to the user's movement and dynamic visualization of markings, escape routes, or user movement in the plan.
- Local view (i.e., first-person view) enables the creation of interactive escape visualizations or simulations or non-interactive escape video animations. These can be used as a complement to the traditional global view of evacuation (an egocentric frame of reference).

New possibilities have been proposed for interactive 3D models: e.g. camera settings, lighting and illumination, shading, shadows, and atmospheric and environmental effects (Haeberling 2002). For example, illumination on colour hue can be an interactive method for supporting for wayfinding. But due to the artificial illumination in the three-dimensional virtual world model, the variation in colour hue also suffers a variation in saturation because of natural brightness. The variable lighting and illumination can cause different perceptions and influence the task results (Figure 2). Likewise, it's unclear which level of detail and realism might be most appropriate. More research is needed to strengthen our understanding of what is best practice in this regard.

![image](https://github.com/user-attachments/assets/17189f80-18ec-4b47-b762-2edb8dbaf6c5)

Figure 2. Example of different appearances of 3D buildings under different lighting conditions.

![image](https://github.com/user-attachments/assets/a5cd0a54-dfc0-4635-be81-38d578aaa74c)

Figure 3. Example of different levels of detail and realism in a 3D visualization.


## Use case
Currently, a massive amount of 3D spatial data is created in connection with the development of Building Information Model (BIM) approaches. This data can be used for the purpose of creating immersive environments that can serve, for example, as a virtual asset for crisis management purposes. An example might be an emergency evacuation that can be carried out in a non-existent building (Figure 4) if it can be practiced in a digital twin of an existing building, where this approach is significantly cheaper and eliminates the risk of injury to the participants of the emergency evacuation. This approach can be used in the case of a wide range of publicly accessible buildings.

![image](https://github.com/user-attachments/assets/69c2c1e9-44b6-4e73-8dc1-cb3a6cb19e90)

Figure 4. Example of a BIM transformed with the use of lighting and camera settings to simulate a building for the purpose of practicing building evacuation in an emergency.


## Proposed outputs
-	Best practice guidelines for the use of immersive 3D visual cues – position of the light source, level of realism, etc. 
-	Terminological anchoring of cartographic concepts within immersive geographic environments (see also section 2)


## 5. Emerging context: Big geospatial data
### Background
Big geospatial data have the potential to provide important insights but are challenging to map effectively. Because of their volume and velocity, we need quick methods for making sense of the data.

### Capabilities Vision
More data only helps if you can make sense of it. Big geospatial data seriously test cartographic generalization methods and computational approaches. Useful standards would capture best practice for how to use visualizations to clarify large amounts of heterogeneous data that change quickly.

### Use Case
The billions of financial transactions that occur each day can be challenging to make sense of. Yet, fraud is an increasing problem and detecting fraud can draw on the locational information in a stream of data to identify anomalous patterns of financial transactions that may suggest fraud. These data streams may include fixed locations (e.g., particular credit card payment points), with the streaming constituting many transactions performed by different users at that location, or dynamic locations as when a person making a transaction is moving across space. Taking too long to identify fraudulent transactions can lead to more losses, and visualization is still faster than computational methods at identifying outliers (Lokanen 2023).

An interaction design standard could describe what kinds of interactions with big data or AI models fed with big data are likely to produce reasoning processes that lead to new insights.
Design patterns could describe best practices for reducing the visual complexity of a visualization without affecting the quality or integrity of the underlying data.


### Proposed Outputs
- Standard describing the map interaction capabilities that are required for deriving meaning from big data.
- Reduce the distinction between data and portrayal by finding ways to simplify visualizations of big data without altering the data model by removing data.
- Find methods that account for systemic change when comparing historical data with real-time data.


## 6. Summary of standardization requirements
Summary of aspects of cartographic practice that could be standardized to support broader application of cartographic best practices

## 7. Conclusions

## 8. Acknowledgements 
This technical paper draws on and extends research first reported in Griffin et al. (2021). We would like to acknowledge the constructive suggestions from attendees of the OGC Portrayal Domain Working Group Workshop at Member Meetings #126 and #127, who provided feedback on early iterations of these ideas.

## 9. References
Abhayaratna, J., van den Brink, L., Car, N., Atkinson, R., Homburg, T., Knibbe, F., McGlinn, K., Wagner, A., Bonduel, M., Rasmussen, M. H., Thiery, F. Eds. 2020. OGC Benefits of Representing Spatial Data Using Semantic and Graph Technologies. Open Geospatial Consortium. http://www.opengis.net/doc/wp/using-semantic-graph

Bertin, J. (1983). Semiology of Graphics: Diagrams, Networks, Maps (1st ed). ESRI Press, California, USA.
 
Bocher, E. and Ertz, O. (2018). A redesign of OGC Symbology Encoding standard for sharing cartography. PeerJ Computer Science, 4, e143; DOI 10.7717/peerj-cs.143

Bocher, E., and Ertz, O.(2020). OGC Symbology Conceptual Model: CorePart. Available online: http://www.opengis.net/doc/IS/SymCore/1.0.

Bourque, P. & Fairly, R. E. (eds.), (2014). Guide to the Software Engineering Body of Knowledge (SWEBOK) V3.0. IEEE Computer Society. Available online at: https://www.computer.org/education/bodies-of-knowledge/software-engineering/v3.

Brewer, C. A. (2003). A transition in improving maps: The ColorBrewer example. Cartography and Geographic Information Science, 30(2), 159-162.

Brus, J., Zdena, D., Kanok, J., & Pechanec, V. (2010). Design of intelligent system in cartography. In 9th Roedunet IEEE International Conference, (pp. 112-117). IEEE.

Coetzee, S., and Rautenbach, V. (2017). A design pattern approach to cartography with big geospatial data. The Cartographic Journal, 54(4), 301-312. 

DiBiase, D., MacEachren, A. M., Krygier, J. B. and Reeves C. (1992). Animation and the Role of Map Design in Scientific Visualization. Cartography and Geographic
Information Systems, 19(4), 201-214.

D’Ignazio, C. & Klein, L. (2019). Data Feminism. Cambridge, MA, MIT Press.

Dobres, J., Chahine, N., and Reimer, B. (2017). Effects of ambient illumination, contrast polarity, and letter size on text legibility under glance-like reading. Applied Ergonomics, 60, 68-73.

Evans, E. (2003). Domain-driven design: Tackling complexity in the heart of software. Upper Saddle River, NJ, Addison-Wesley.

Forrest, D. (1993). Expert systems and cartographic design. The Cartographic Journal, 30(2), 143-148.

Gibbs N. E. and Tucker A. B. (1986). A model curriculum for a liberal arts degree in computer science. Communications of the ACM, 29(3), 202-210.

Griffin, A. L., Coetzee, S., Kubicek, P., Camboim, S. P., Harvey, F., Behr, F. J., & Brus, J. (2021). Perspectives on making cartographic knowledge accessible to software developers. Abstracts of the ICA, 3, 96.

Griffin, A. L., White, T., Fish, C., Tomio, B., Huang, H., Sluter, C. R., Bravo, J. V. M., Fabrikant, S. I., Bleisch, S., Yamada, M. & Picanço, P. (2017). Designing across map use contexts: A research agenda. International Journal of Cartography, 3(sup1), 90-114.

Haeberling, C. (2005). Cartographic Design Principles For 3D Maps – A Contribution To Cartographic Theory. Proceedings of 22nd ICA Congress Mapping Approaches into a Changing World, A Coruna, Spain, Jul 9-16.

Harrower, M., & Brewer, C. A. (2003). ColorBrewer. org: an online tool for selecting colour schemes for maps. The Cartographic Journal, 40(1), 27-37.

ISO. (2020). ISO 12967-1:2020, Health informatics — Service architecture (HISA) — Part 1: Enterprise viewpoint.

Lokanen, M. (2023). Financial fraud detection: the use of visualization techniques in credit card fraud and money laundering domains. Journal of Money Laundering Control, 26(3), 436-444.

Percivall, G, Reed, C. Simonis, I, Lieberman, J, and Ramage, S, 2012. Big Geospatial Data – an OGC White Paper. Available online at: https://www.google.com/url?q=https://docs.ogc.org/wp/16-131r2/16-131r2.html&sa=D&source=docs&ust=1683478379205872&usg=AOvVaw3vYPD6-VLCsKwEuGfnWcTv

Piepenbrock, C., Mayr, S., & Buchner, A. (2014). Positive Display Polarity Is Particularly Advantageous for Small Character Sizes: Implications for Display Design. Human Factors, 56(5), 942–951. 

Rautenbach, V., Coetzee, S., Schiewe, J., and Çöltekin, A. (2015). An Assessment of Visual Variables for the Cartographic Design of 3D Informal Settlement Models. Proceedings of the ICC 2015, Rio de Janeiro, Brazil.

Shalloway, A., and Trott, J. (2004). Design Patterns Explained: A New Perspective on Object-Oriented Design, Second Edition. Upper Saddle River, NJ: Addison Wesley. 

Tsorlini, A., Sieber, R., Hurni, L., Klauser, H., & Gloor, T. (2017). Designing a Rule-based Wizard for Visualizing Statistical Data on Thematic Maps. Cartographic Perspectives, 86, 5-23.

Wing J. M., (2014). Computational thinking benefits society. 40th Anniversary Blog on Social Issues in Computing. Available online at: http://socialissues.cs.toronto.edu/index.html%3Fp=279.html. 
