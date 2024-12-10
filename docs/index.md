# About

## Introduction 
_UN/CEFACT Verifiable Trade Documents_  is a specification of how the most commonly used documents in global trade and logistics must be implemented with modern web technologies, promoting an interoperable, scalable, and cryptographically signed global trade documentation infrastructure. 

The specification aims to make it easy and unambiguous for trade actors to digitally issue, verify and operationalize documents involved in global trade and transportation. The provided schemas can be directly implemented with commodity or open source software, requiring a minimum of technical effort. 

UN-VTD continues UN/CEFACT's decades-old leadership as global supply chains transition into the next generation of scalable, secure, digital infrastructure, as emergent verifiable credentials and surrounding technologies are adopted by global trade and logistics actors.

## Background
UN-VTD is a physical, technology-specific implementation of the KTDDE business requirements which were generated during the [2024 ICC DSI Key Trade Document Data Elements](https://www.digitalizetrade.org/ktdde/) project. The main output of KTDDE was a list of logical data models, based on applicable standards and defined by business domain experts. 

![The KTDDE phase one trade documents](./images/ktdde.jpg)
The first set of trace document requirements defined by KTDDE.

The project will primarily aim to implement the documents which were targeted by the ICC-DSI KTDDE, and roughly targeted in the same batched order. Note that complete coverage of the full set of the 36 KTDDE documents is not necessarily a success criteria, nor is strict alignment to the KTDDE specification. Similarly, other document types may be included on the premise that they are a generally applicable document commonly exchanged in international trade and transport use cases.

The underlying semantics of the UN-VTD documents are primarily based upon the [UN/CEFACT Buy-Ship-Pay](https://vocabulary.uncefact.org/) data model, ensuring linkage back to legacy implementations. 

The way in which the specification is technically defined is adapted from the [W3C Traceability Vocabulary](https://w3id.org/traceability) specification. 

## Benefits
- *Data verification*, linking the issuer's signature cryptographically to the data.
- *Interoperability*, the only realiastic globally scalable architecture. 
- *Standardized semantics* in a global, heterogeneous sector. 
- *Digitization*, all of the above are ultimately enablers of true digitization which depends upon structured, reliable data which can be operationalized both on the producer and consumer side.  

## Output
The primary resource of each UN-VTD document is a schema which defines the core data structure of each document. The driving principles at this layer is to a) promote modular data modeling for optimal reuse of components, b) strive for simplicity in the recognition that the targeted user base is heterogeneous and thus the developer and user experience are essential measures of success, and c) adhere to a defined list of design conventions to prevent inconsistent user experiences.

Technically, the schemas are expressed as JSON Schemas which has the benefit of baing supported by a vast choice of libraries which support it. For example, API specifications are typically expressing request and repsonse payloads using JSON Schema. The trade document schemas will be presented and made available online leveraging such tools. By consuming the project’s own JSON Schema output, we ensure feasibility, usability and show a practical way for implementers to adopt these UN/CEFACT outputs.

### Semantics
The trade document schemas will be produced with a corresponding Linked Data context which ensures strong semantics of exchanged documents. This semantic layer will automatically underpin any implementation of the UN/CEFACT schemas; data providers and consumers may freely choose to ignore or leverage it.

The project will take a pragmatic approach to implementing the Linked Data layer; the aim is to annotate meaningful term definitions to document instances, not constructing an elaborate ontology. Similarly, the project does not aim to create any new term definitions, but will leverage existing web vocabularies. The primary vocabulary will be the UN/CEFACT Web Vocabulary, but terms will be pulled in from elsewhere for example if not defined by UN/CEFACT, if another definition is specific, or if it is recognized to be broader adopted.

### Digital Signatures
All documents will be modeled following the Verifiable Credentials data model. This ensures that documents can be digitally signed by issuers in a standardized way. The ability to sign data in a vendor-neutral manner is the key to unlock supply chain and trade digitization at global scale.

Beyond adhering to the prevalent Verifiable Credential data model, the project will make recommendations on for example on versioning, signing method, cryptographic suites, and revocation methods with the goal to promote interoperability; on the principle that less ambiguity leads to easier adoption and better interoperability.

## Contribution 
https://github.com/uncefact/spec-unvtd