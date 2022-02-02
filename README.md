# IMS - an Enterprise Compute Ecosystem Solution
- the IMS repository is an open source example of InMechaSol's Ecosystem Approach to Enterprise Compute Solutions.  
- an Ecosystem is comprised of many differenet human actors (users, operators, developers) 
- and mixed compute solutions (embedded products, user interfaces, web and IoT).  
### The Enterprise Architecture is designed to Maximize the Reuse of Tested Intellectual Property (IP).  
### Promote New Innovation over Recreation!
- Each compute solution within the ecosystem 
  - is created from tested reusable components purpose built for 
    - cross-platform performance guarantees
    - and intercommunication between layers of mixed Ecosystem compute solutions and human actors.

## To Clone and Checkout the Full IMS Repo with all Nested Submodules
```bash
git clone https://github.com/InMechaSol/IMS.git --recursive
cd IMS
git submodule foreach --recursive git checkout main
```
## To Update all Nested Submodules from Latest Remotes
```bash
git submodule update --progress --init --recursive --force --merge --remote
git submodule foreach --recursive git checkout main
```
## Main Submodules
- [CR](https://github.com/InMechaSol/CR) - Compute Resources are reusable cross-platform sources from which Platform Specific Compute Solutions are built.
- [CS](https://github.com/InMechaSol/CS) - Compute Solutions are Platform Specific Applications linked to Tested Production Binary Files tracked via ERP/CM.
- [P](https://github.com/InMechaSol/P) - Products contain Tested ERP/CM Controlled Compute Solutions.  Products link to top level P/Ns tracked via ERP/CM. 

## IMS Universe
IMS Universe.sln can be opened in Visual Studio to explore the entire IMS Universe.  Simulations can be run, code can be generated, repositories can be configured, and its always expanding...
### Configuration File
```JSON
{
  "Path2GitBin": "C:\\Program Files\\Git\\bin\\git.exe",
  "Path2DoxygenBin": "C:\\Program Files\\doxygen\\bin\\doxygen.exe",
  "Path2GraphVizDotBin": "C:\\Program Files\\Graphviz\\bin\\dot.exe",
  "Path2RootRepository": "C:\\IMS",
  "Repositories": [
    {
      "name": "IMS",
      "url": "https://github.com/InMechaSol/IMS.git",
      "submodnames": [ "CR", "CS", "P" ]
    },
    {
      "name": "CR",
      "url": "https://github.com/InMechaSol/CR.git",
      "submodnames": [ "ccACU", "ccACU_Tests", "ccOS", "ccOS_Tests", "ccNOos", "ccNOos_Tests" ]
    },
    {
      "name": "CS",
      "url": "https://github.com/InMechaSol/CS.git",
      "submodnames": [ "TS4900ACU" ]
    },
    {
      "name": "P",
      "url": "https://github.com/InMechaSol/P.git",
      "submodnames": [ "RECON_ACU", "TALON_ACU" ]
    },
    {
      "name": "ccACU",
      "url": "https://github.com/InMechaSol/ccACU.git",
      "submodnames": [ "ccOS" ]
    },
    {
      "name": "ccACU_Tests",
      "url": "https://github.com/InMechaSol/ccACU_Tests.git",
      "submodnames": [ "ccACU" ]
    },
    {
      "name": "ccNOos",
      "url": "https://github.com/InMechaSol/ccNOos.git",
      "submodnames": null
    },
    {
      "name": "ccNOos_Tests",
      "url": "https://github.com/InMechaSol/ccNOos_Tests.git",
      "submodnames": [ "ccNOos" ]
    },
    {
      "name": "ccOS",
      "url": "https://github.com/InMechaSol/ccOS.git",
      "submodnames": [ "ccNOos" ]
    },
    {
      "name": "ccOS_Tests",
      "url": "https://github.com/InMechaSol/ccOS_Tests.git",
      "submodnames": [ "ccOS" ]
    },
    {
      "name": "TS4900ACU",
      "url": "https://github.com/InMechaSol/TS4900ACU.git",
      "submodnames": [ "ccACU" ]
    },
    {
      "name": "RECON_ACU",
      "url": "https://github.com/InMechaSol/RECON_ACU.git",
      "submodnames": [ "TS4900ACU" ]
    },
    {
      "name": "TALON_ACU",
      "url": "https://github.com/InMechaSol/RECON_ACU.git",
      "submodnames": [ "TS4900ACU" ]
    }
  ]
}
```
