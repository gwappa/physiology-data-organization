

## Schema or Ontology?

### Ontology: a bottom-up, "open-world" description

- A concept originated from the semantic-web initiatives:
  - Describes relationships between entities in the internet, by means of a predicate logic and combinations of URIs.
  - Normally, for any relationship, the subject, the object, and (even) the meaning of the relationship is uniquely defined in terms of URI.
  - Common format: RDF (written in XML, Turtle, JSON-RD etc.)
- Descriptive:
  - typically, there is no assumption on the form of the graph that represents a set of linked data: an ontology sets the lower bound of all the possible relationships 
  - "open-world assumption": we can be only sure to the extent any description is made, while we must remain ignorant about what is not stated

Ontology is the concept normally used to describe linked data.

One notable feature related to this concept is its descriptive nature. Typically, there is no assumption on the form of the graph that represents a set of linked data.

If nothing is stated for relationships between entities A and B, we don't know whether there are any relationships there or not. As an extreme, it is even possible that A and B represent the same single object in the end.



### Schema: a top-down, "closed-world" description

- Has been used to validate the structure of a document e.g. web pages:
  - Describes how a document should be structured.
  - Keywords must be defined in terms of URIs, but the content of the data does not have to be "unique" in the world of internet (i.e. does not have to have a URI).
  - Common format: language-specific schema format (XML Schema, JSON Schema etc.)
- Prescriptive and deterministic:
  - The form that a graph can take is fixed or limited: a schema sets the upper bound of how a document may be structured
  - If your object does not conform to the schema definition, it simply means that your description is wrong

This nature of a schema definition has some deterministic consequences. If the values of a property differ between objects A and B, then A and B is different by definition. As a corollary, if you want to claim that A and B represent the same single object, and still they differ in the values of a property, the only implication is that the information of either A or B is wrong, or at least ill-formed.

You can infer various things in a deterministic way if an object conforms to a schema, but you cannot possibly apply the logic at all to an object that doesn't (or, for example, if the object conforms to another incompatible schema).



### Which one should we use?

Finally it comes to the initial question: which approach should we take, ontological or schematic? Considering my assumptions below, we must use both: the question is rather about which one is suitable for describing what.

- My assumptions:
  - Some general structures are common to all the physiology experiments: descriptions must be schematic rather than ontological.
  - We remain descriptive when we define what entities are, and their relationships between each other.

- Corollary:
  - Any expression that is prescriptive must be a description.
  - An aspect that stays descriptive in any sense must be a definition.
- Strategy to be taken:
  - We use structures based on a certain schema for describing how to organize data and metadata, and for validating specific datasets to be published.
  - We use terms defined ontologically for characterizing entities and their relationships.

After all, it seems that these different concepts reflect the two sides of the same thing.

