source 1: https://www.sciencedirect.com/science/article/pii/S0164121299000783?casa_token=01tnlZ1KiqwAAAAA:1rrRpxBvDJP_j1AhVcLFEHjnkqf_YVpb7lpA6xtNByjOT5AZfkzhOH_jvirpA0hNlZaWJWyd

## Coupling Concept
---
The probability that a change in one module will impact the whole system. Commonly defined as the *interdependence between modules.* 
### Ambiguity
The between part of that definition can be misleading. It seems to imply that coupling is restricted to 2 modules. Clearly this doesn't have to be the case, as in any hierarchy based software, a module connects to both its parents and its children. In addition, interdependence implies that both modules are mutually dependent on one another, while often times that is not that case
## Definitions
---
- Impact dependence: X to Y, when Y is modified, X will recieve an impact
- Elementary coupling: Impact Dependence of modules to M through a single data
- Module coupling of M is the impact dependence of modules to m
- Module: collection of data and instructions with control mechanisms, all delimited with one entry point and one exit point
## Attributes of an Elementary Coupling
--- 
- **Complexity of Data (`C[d]`)**: How complex the data that is shared by the two modules is. Intrinsic to the data itself. Covers [[Standard Coupling Ranking#Data Coupling|DataCoupling]]
- **Program Control (`PC[d]`)**: How many different impacts the data can have on the two modules being affected. Covers [[Standard Coupling Ranking#Control Coupling|Control Coupling]]
- **Number of connections (`N[d]`)**: Number of other modules connected via *d* when *d* is used in a module.