# IMS
IMS Source Controlled, index repository of all InMechaSol repositories under source control

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
- CR - Compute Resources are reusable cross-platform sources from which Platform Specific Compute Solutions are built
- CS - Compute Solutions are Platform Specific Applications to be tracked via ERP/CM and from which Products are built
- P - Products are final Computing Products to be tracked via ERP/CM which are built from Compute Solutions

## IMS Universe
IMS Universe.sln should be opened in Visual Studio to Explore the Entire IMS Universe.  Simulations can be run, code can be generated, repositories can be conigured, and its always expanding...
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
      "submodnames": [ RECON_ACU, TALON_ACU ]
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
