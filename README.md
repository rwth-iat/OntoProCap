# OntoProCap – Ontology for Process Capabilities

OntoProCap is an OWL ontology for formally describing **process capabilities** in modular and conventional production systems. These descriptions are machine-interpretable, independent of specific implementations and vendors. This ontology is intended to support semantic descriptions in applications for modular automation, recipe engineering, resource matching, and digital twins.

## Motivation

Modern production systems increasingly rely on:

- Modular plants and reconfigurable assets  
- Capability-based engineering, planning, and orchestration  
- Digital twins and semantic interoperability  
- Automated feasibility checking and planning  

However, existing standards typically describe *interfaces* or *services*, while the underlying **process capabilities** remain implicit or informal.
OntoProCap addresses this gap by providing:
- Formal classification aligned with the IEC process terminology  
- Explicit semantic descriptions for process capabilities supporting capability-based engineering, planning, and orchestration

## Conceptual Foundation

OntoProCap follows the IEC process definition:

> **Process (IEC 60050 / IEV 351-42-33):**  
> *complete set of interacting operations in a system by which matter, energy or information is transformed, transported or stored* [1].

Capabilities are defined as:
> **Capability:**
> *Implementation-independent description of a function in industrial production to achieve an effect in the physical or virtual world* [2].

The ontology aligns naturally with:

- Capability–Skill–Service (CSS) model  
- Product–Process–Resource (PPR) model  
- ISA-88 / BatchML recipes  
- Module Type Package (MTP)  
- Asset Administration Shell (AAS)  


## Structure

The Ontology *OntoProCap* structures capabilities according to the **process concept of IEC 60050 / IEV 351-42-33**:
```
OntoProCap.owl
│└─ Capability 
│    ├── StorageCapability    
│    ├── TransformationCapability
|    |      ├──...
|    |      ├──EnthalpyChange
|    |      |   ├──...
|    |      |   └──TemperatureChange
|    |      |       ├──...
|    |      |       └──...
|    |      └──...
│    └── TransportCapability
└─ Process 
```

## Examples of described capabilities

- `TransformationCapability`:Capability to change the properties of a material, energy or information flow (e.g. temperature, chemical composition, position).
- `EnthalpyChange`: EnthalpyChange in terms of unit operation considers a conversion of energy which often result in a change of the state of aggregation.
- `TemperatureChange`: TemperatureChange in terms of unit operation means to transport the heat content of one material to another and it is applied for heating or cooling purposes.
- `HeatingOfLiquids`: Increasing the temperature of a liquid without changing ist state of aggregation

## License
The ontology *OntoProCap* is licensed under the Creative Commons CC BY-SA 4.0 (Attribution-ShareAlike 4.0 International) license. This means that you can freely use, distribute, edit, and build upon the ontology as long as you give proper credit to the creator of the ontology and publish your derivations under the same license.

You are free to:
- Share — copy and redistribute the material
- Adapt — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- Attribution — You must give appropriate credit.
- ShareAlike — Derivative works must be distributed under the same license.

Code artifacts (if any) are licensed separately under MIT.


Creator: Michael Winter, Indah Radityo Putri
E-Mail: {m.winter, i.putri}@iat.rwth-aachen.de

## Contact & Acknowledgements
Maintainer: [Michael Winter](mailto:m.winter@iat.rwth‑aachen.de), [Indah Putri](mailto:i.putri@iat.rwth-aachen.de)

Institution: [Chair of Information and Automation Systems (IAT) - RWTH Aachen University](https://www.iat.rwth-aachen.de/) 
Head of Institution: [Prof. Dr.-Ing. Tobias Kleinert](mailto:kleinert@iat.rwth-aachen.de)

## References

[1] International Electrotechnical Commission, “*IEV 351-42-33: process*,” International Electrotechnical Vocabulary (Electropedia), Oct. 2015. [Online]. Available: https://www.electropedia.org/iev/iev.nsf/display?openform&ievref=351-42-33. [Accessed: 27-Jan-2026].

[2] C. Diedrich et al., “*Information Model for Capabilities, Skills & Services: Definition of terminology and proposal for a technology-independent information model for capabilities and skills in flexible manufacturing*”, Berlin: Plattform Industrie 4.0, Oct. 2022. [Online]. Available: https://www.plattform-i40.de/IP/Redaktion/EN/Downloads/Publikation/CapabilitiesSkillsServices.pdf?__blob=publicationFile&v=1. [Accessed: 27-Jan-2026].