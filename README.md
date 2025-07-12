# schematic_test
test generating schematics in github

```mermaid
flowchart TD;
    idRF@{ shape: stadium, label: "Raw File" }-->idMan@{ shape: diamond, label: "Manufacturer" };
    idMan-->idKS@{ shape: rounded, label: "<a href='https://github.com/jmjech/schematic_test/blob/main/Kongsberg-Simrad/README.md'>Kongsberg-Simrad</a>" };
    idMan-->idBS@{ shape: rounded, label: "BioSonics" };
    idMan-->idASL@{ shape: rounded, label: "ASL" };
B[an <b>important</b> <a href='http://google.com'>link</a>]
```
