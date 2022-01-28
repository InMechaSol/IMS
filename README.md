# IMS
IMS Source Controlled, index repository of all InMechaSol repositories under source control

## To clone and checkout the full IMS repo with all nested submodules
```
git clone https://github.com/InMechaSol/IMS.git --recursive
git submodule foreach --recursive checkout main
```

## Main Submodules
- CR - Compute Resources are reusable cross-platform sources from which Platform Specific Compute Solutions are built
- CS - Compute Solutions are Platform Specific Applications to be tracked via ERP/CM and from which Products are built
- P - Products are final Computing Products to be tracked via ERP/CM which are built from Compute Solutions
