# Level 0 Data
test generating schematics in github

```mermaid
flowchart TB
    subgraph Source["**Data Source**"]
        direction TB
        idSrcOMAO@{shape: stadium, label: "OMAO Data Lake"} --> idOMAO@{ shape: stadium, label: "Retrieve Data from OMAO: link to instructions" }
        idSrcNCEI@{shape: stadium, label: "NCEI"} --> idNCEI@{ shape: stadium, label: "Retrieve Data from NCEI: link to instructions" }
        idSrcGCP@{shape: stadium, label: "GCP Prod Storage"} --> idGCP@{ shape: stadium, label: "Retrieve Data from GCP: link to instructions" }
        idSrcOP@{shape: stadium, label: "On-Prem Storage"} --> idOP@{ shape: stadium, label: "Retrieve Data from On-prem: link to instructions" }
    end
    subgraph SurveyMD["**Survey Metadata**"]
        direction LR
        idRF@{ shape: stadium, label: "Raw File" } --> idSMD@{ shape: database, label: "link to survey metadata" }
    end
    subgraph Manufacturer["**Echosounder Manufacturer**"]
        direction LR
        idAL1@{shape: stadium, label: "AA Library Function: link to instructions"} --> idMan@{ shape: diamond, label: "Select Manufacturer" }
        idAL2@{shape: stadium, label: "EchoPype Function: link to instructions"} --> idMan
    end
    Source --> SurveyMD
    SurveyMD --> Manufacturer
    Manufacturer --> idKS@{ shape: rounded, label: "<a href='https://github.com/jmjech/schematic_test/blob/main/Kongsberg-Simrad/README.md'>Kongsberg-Simrad</a>" }
    Manufacturer --> idBS@{ shape: rounded, label: "BioSonics" }
    Manufacturer --> idASL@{ shape: rounded, label: "ASL" }
```
