# NBility model design guidelines

NBility model adheres to generic design rules. Every adjustment and/or expansion should conform to these rules. These guidelines consist of:

* NBility metamodel
* Naming conventions
* Model explenation / design choices
* Consistency rules

## NBility metamodel

NBility uses a metamodel:

![NBility_metamodel](images/NBility%20metamodel.png)

The definitions of the elements and relationships in the metamodel are as follows:

* elements
    * business function: collection of business behavior based on a chosen set of criteria such as required business resources and/or competencies, and is managed or performed as a whole
    * business object: concept used within a particular business domain.
        * A business object is an abstraction of a collection of things in the real world (material or immaterial) important for a grid operator (and therefore to be managed)
        * A business object is countable 
    * value stream: sequence of activities that create an overall result for a customer, stakeholder, or end user
* relations
    * controls: changes and prevents changes to the state of a concept
    * modifies: changes the state of a concept
    * composed of: consists of one or more other concepts
    * contextualizes: influences the definition of a concept
    * serves: provides functionality to another concept
    * triggers: temporal or causal relationship between concepts
    * associated to: unspecified relationship

The metamodel defines multiplicities using crow’s foot notation, in which a ring represents ’zero’, a dash represents ’one’ and a crow’s foot represents ’many’ or ’infinite’. In pairs, they represent the minimum and maximum multiplicities.

* For example, the figure shows that each business function is composed of zero to many business functions and that each business object is controlled by one business function.
* The metamodel has a contextualizes relationship. Contextualization is an abstraction mechanism, like generalization, aggregation, and composition. A context is a relation between things and names. The business object energy grid may be instantiated to actual grids, such as the one in the city of Rotterdam or Amsterdam, but it can also serve as a context for a collection of lower-level business objects, such as grid component and grid design. An example of an object instance that can change context is the transformer. When installed in an energy grid, it ceases to be a material in the context of work and starts to be a grid component in the context of the energy grid. In enterprise data models, the elements at the highest level of abstraction are typically called subject areas, which refers to their role as the context for lower-level elements. In our metamodel, we choose to be agnostic to the level of abstraction and, therefore, do not use subject areas.

## Naming convention

Naming conventions (every element on a certain level of abstraction has a unique name that can be understood by outsiders.

* The naming convention for a capabiliy is: < noun + verb >.
    * Every capability can be preceded by: 'a grid operator can' < noun + verb >.
    * The noun in the name of the capability is mostly the business object managed by that capability.
    * The description of a capability starts with: 'the ability to …
* The naming convention of a business object is: < noun >
    * The name is defined in singular.
    * In defining business objects the concepts and definitions of laws and regulations are leading.
    * Search terms are not synonyms or approved aliases but only a tool for people to find the right business object.
* The naming convention for a value stream is: < verb + noun >


## Model explanation / design choices

The model is created with some design choices which are explained below. Every adjustment and/or expansion should conform to these choices or explain why these weren't applicable (with a valuecase). 

* Granularity: The model has three abstraction layers and maximal 7 objects per layer.
    * Three abstraction layers are defined to support strategic, tactical and operational management of a grid operator.
    * A capability on levels 3, 2 or 1 is only defined if the lifecycle of such a capability differs.
        * So if the business capability can separately be managed and the activities of the capability can separately be changed.
        * An indication might be if there is a separate business owner within most grid operators, although this is just an indication.
* No registration capabilities - The registration of a business object is always part of the capability managing the business object. No capabilities are defined just for registration of a business object.
* Two Capability groupings: NBility consists of two Capability groupings: the core capability group (identification starts with 'C'); and the enterprise capability group  (identification starts with 'E')
    * Core capabilities are capabilities specific for a grid operator
    * Enterprise capabilities are capabilities directing and supporting the business including capabilities developing and maintaining the production factors of a grid operator (such as employees, digital products, office buildings).
* Two value stream groupings: Capabilities (core and enterprise) deliver value working together in a value stream context. NBility consists of two value stream groups: externally focused primary value streams realising the grid operator business (identification starts with 'P') and internally focused supporting value streams (identification starts with 'I').
* Identification: Every capability and value stream has an identification. 
    * Capability identification starts with the grouping identification ('C', 'E') and contains a number within a level and a dot '.' for every level. E.g. C.1; E.1.2.1.
    * Value stream identification starts with the grouping identification ('P', 'I') and contains a letter for every valuestream, e.g. P.A, E.B
* Service decoupling: Core value streams do not contain enterprise domain capabilities because these are decoupled via internal services realised by internal value streams.

* Business capabilities/functions and business objects are part of the enterprise architecture capability (E.1.3.1). The translation to enterprise design (e.g. data, processes, supporting digital products, employees with knowledge and experience, office building) is part of the domains managing these production factors (E.2-E.7).  
* Process definitions (E.2.1.1 Define and improve processes) are separated from process sessions/cases (E2.1.2 Orchestrate processes).
* Materials and working equipment is purchased in the enterprise domain (E.5.2) and managed in the core domain (5.4).
* Main capability ‘E.1.2 Align stakeholders’ contains (generic) communication to external and internal stakeholders to influence these stakeholders towards the strategic objectives of the grid operator. The operational specific communication is being done in the core capability domains ‘Service customers’ and ‘Facilitate the energy market’ and the enterprise domain ‘Recruit and manage human capital’.
* Enterprise capability domains ‘Develop and maintain digital technology’ and ‘Manage office real estate’ exist apart from ‘Obtain goods and services’ because of the ‘lifecycle/maintenance’ component.
* The capability domain ‘Develop and maintain digital technology’ is based on the IT4IT model of the open group.
* The main capability E.2.2 ‘Manage data’ is aimed at business data. This is data created and maintained by the core and enterprise capabilities that can be combined.  


## Consistency rules

NBility model adheres to Consistency rules and guidelines. 
The metamodel is the basis for formulating consistency rules and guidelines. The metamodel already contains a set of rules in the form of multiplicities that are not zero to many. These rules can be uses as a checklist. The rules (R) are rigid, and the guidelines (G) are recommendations. Rules refer to an element that is composed of or contextualizes other elements as their abstraction. The number of times an element is (recursively) composed or contextualized by another element determines its level of abstraction. 

* Rules
    * R1 Each business function is composed in at most one business function
    * R2 Each business object is contextualized by at most one business object
    * R3 Each composition and contextualization relationship is not part of a cycle
    * R4 At each level of abstraction, the business functions are mutually exclusive
    * R5 At each level of abstraction, the business functions are collectively exhaustive
    * R6 At each level of abstraction, the business objects are mutually exclusive
    * R7 At each level of abstraction, the business objects are collectively exhaustive
    * R8 Each business function relates to a business object only if their abstractions are related or when they have no abstractions
    * R9 Each business object is associated to a business object only if it is at the same level of abstraction
    * R10 Each business function controls and/or modifies at least one business object
    * R11 Each business object is controlled by exactly one business function
* Guidelines
    * G1 Each business function controls and/or modifies exactly one business object
    * G2 Each business object is controlled and/or modified by exactly one business Function
 
The rationales for these rules and guidelines are as follows.

* R1-3 Business architecture models may contain more elements than humans can process easily. Abstraction mechanisms such as composition and contextualization allow the elements to be grouped into bite-sized chunks. These rules ensure the formation of a nested hierarchy, required by rules 4 to 7.
* R4-7 The MECE principle applies at each level of abstraction. This principle states that items in a group must be mutually exclusive (ME) and collectively exhaustive (CE), meaning that they may not have gaps or overlaps. The collection of business functions at a particular level of abstraction conforms to this principle if each atomic business activity in an organization is associated with exactly one business function. For business objects, this implies that each thing in an organization is associated with exactly one business object. For example, business objects Customer and Corporate Customer are not mutually exclusive, because a particular corporate customer is associated with both business objects. If these are the only business objects used to describe an energy system operator, they also have gaps, because the energy grid is not associated with either.
* R8 If a business function is related to a business object, then the abstraction of the function is by definition related to the abstraction of the object. This rule implicitly restricts the relationships between business functions and business objects to matching levels of abstraction. This increases consistency, allowing stakeholders to easily switch perspectives.
* R9 Restricting association relationships within each level of abstraction allows levels to be used independently.
* R10 A business function that does not control and/or modify a business object cannot create value and must be eliminated.
* R11 The controls relationship enables a business function to prevent state changes to business objects. This implies access control, that is, any business function that modifies a business object can do so only because the controlling business function allows it. Assigning each business function the exclusive control over a business object creates low coupling. A business object not controlled by a business function is not of interest to the business and is therefore not a business object.
* G1&2 At each level of abstraction, these guidelines create a similar number of business functions and business objects, and thus, a matching level of granularity. These guidelines are not rules, because managing a business object may require multiple functions. A typical example is where different functions manage the same business object but at different life stages. In such cases, the definition of multiple functions is allowed if managing each life stage requires its own set of resources or competencies. Multiple functions can modify a business object, but only one can control it (rule 11).
