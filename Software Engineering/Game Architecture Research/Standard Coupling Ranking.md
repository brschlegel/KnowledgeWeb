source 1: http://pages.cpsc.ucalgary.ca/~eberly/Courses/CPSC333/Lectures/Design/coupling.html

Page-Jones cites principles adapted from Yourdon and Constantine's work:
Connections should be:
- Narrow (rather than broad)
- Direct (rather than indirect)
- Local (rather than remote)
- Obvious (rather than obscure)
- Flexible (rather than rigid)

## Content Coupling
If one module refers to the "inside"/internals/private part of another module. Nearly impossible in many high level languages.

## High Coupling
This level is fairly undesirable, but might not be able to be avoided
#### Common Coupling
Sharing the same global data area. Also seems to be outside the scope of higher level languages
#### External Coupling
Sharing direct access to the same I/O device. Not something we deal with often

## Moderate Coupling
This level is of coupling is perfectly acceptable
#### Control Coupling
When module A passes in data to module B that is intended to control the internal logic of module B. When this coupling exists, it should be clear that module A controls module B in some way. An example would be having module A call module B directly.

## Low Coupling 
This level of coupling is the most desirable kind of coupling, if they need to be connected at all
#### Data Coupling
One module calling another directly, and communication using only parameters


