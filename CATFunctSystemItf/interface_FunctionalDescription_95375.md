# FunctionalDescription (Object)

**_The interface to access a Functional Description._**

## Properties

### Property **Actions**( ) As [CATIAFunctionalActions](../CATFunctSystemItf/interface_FunctionalActions_62210.md) (Read Only)

Get the Actions collection.  
### Property **ActionsGroups**( ) As [CATIAFunctActionsGroups](../CATFunctSystemItf/interface_FunctActionsGroups_70306.md) (Read Only)

Get the ActionsGroups collection.  
### Property **Objects**( ) As [CATIAFunctionalObjects](../CATFunctSystemItf/interface_FunctionalObjects_61835.md) (Read Only)

Get the Objects collection.  
### Property **Variants**( ) As [CATIAFunctionalVariants](../CATFunctSystemItf/interface_FunctionalVariants_70232.md) (Read Only)

Get the Variants collection.  (gives a NULL pointer if the description is a itself variant)  Methods

### Func **CreatePosition**( double  `iX`,  double  `iY`) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

Create a Position.  To create actions pointing to NULL  
### Func **GetFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Returns the Facet.  
### Func **GetFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Returns the Facet.  
### Func **SearchFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Searches the Facet.  
### Func **SearchFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Searches the Facet.  
### Sub **Unlock**( )

Unlock.  To remove the protection against modifications.