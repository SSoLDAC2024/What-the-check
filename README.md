# Challenge: Data Validation & Rule Checking

## Champions
- Ruben Verstraeten
- Jeroen Werbrouck

## Number of people per team: 
4

## Challenge Description
Two major trends in the architecture, engineering, and construction industry are the increasing complexity of regulations, which focus on a building's performance, and the digital evolution, which is boosting efficiency and productivity. One potential of the latter could be to (semi)automate the compliance check of digital architectural models against building regulations or even requirements in general. This asks for a fresh look at digital building models and formalisation strategies for requirements that are usually written in natural language.

A first step is to acquire the data, which consists of both building information and contextual datasets, and be stored locally on a computer or on the Web. In this challenge, we focus on datasets based on Semantic Web technologies. Secondly, the logic of the regulation, implicitly described in natural language, has to be transformed into a machine-manageable notation. For this, we focus on the DMN standard, a graphical notation designed to model decisions based on logical constraints. Thirdly, a dictionary is needed to indicate how the concepts used in the DMN diagram can be found in the actual datasets, and allow a generic compliance checking engine to match the DMN with multiple data schema’s (IFC, RVT, LBD, …).

## Challenger Research Questions (choose at least 1)
- Can you automate the checking of a specific regulation? To what extent can this checking be generic? I.e., can you exclude both rule-specific concepts and building-specific concepts from your code, so that your code can be re-used for different regulations or building projects?
- Can you find a way to translate DMN diagrams into automated Linked Data checking mechanisms? (e.g. SHACL, SPARQL, ...) 
- Can you build a GUI that integrates a DMN editor with a BIM viewer?
- **EXTRA:** What are the requirements for a “dictionary” that matches RDF-based datasets with DMN concepts? I.e., if the DMN mentions “Door”, how do we reach the “door” elements in the dataset? The same holds for properties.
- **EXTRA:** For the building data, can you allow different types of data sources at once? E.g., the building model is IFC, the contextual data is RDF?

## Datasets
### Building Datasets
- [Building datasets in Revit](datasets/heartbreak_hotel.rvt)
- [Building datasets in IFC](datasets/heartbreak_hotel.ifc)
- Building datasets in TTL: duplex, Schependomlaan, …
- Generate your own dataset (convert with the IFCtoLBD converter)

### DMN
- [Specifications](https://www.omg.org/dmn/)
- [KIE DMN editor](https://sandbox.kie.org/) or [DMN-BPMN.io](https://demo.bpmn.io/dmn)
- [Local DMN Engine: KIE incubator] (https://github.com/apache/incubator-kie-tools/releases/tag/0.32.0) (other: [cDMN](https://cdmn.readthedocs.io/en/latest/), [Camunda](https://camunda.com/dmn/), [Redhat](https://access.redhat.com/documentation/en-us/red_hat_decision_manager/7.3/html/designing_a_decision_service_using_dmn_models/dmn-execution-con), ...)
- [dmn-js](https://bpmn.io/toolkit/dmn-js/)

### Python Libraries
- [cDMN Reasoning Engine (Katholic University Leuven, Belgium)](https://cdmn.readthedocs.io/en/latest/)
- [IFC OpenShell](https://ifcopenshell.org/)

### Regulatory Texts
- [Example Regulation: Flemish Access Norm](datasets/flemish_access_example_rules.pdf)

## Tools Needed
- Code editor
- Python 3.11
