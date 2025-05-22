# FunctionalAction (Object)

**_The interface to access a Functional Action._**

## Properties

### Property **From**( ) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

Get the From object.  
### Property **Group**( ) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md) (Read Only)

Get the Group property.  Vary when adding/removing the action to/from a group.  
### Property **OrientationDirection**( ) As [CATFunctOrientationDirection](../CATFunctSystemItf/enum_CATFunctOrientationDirection_164048.md)

Get the OrientationDirection property.

**See also:**      [CATFunctOrientationDirection](../CATFunctSystemItf/enum_CATFunctOrientationDirection_164048.md) 
### Property **To**( ) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

Get the To object.  Methods

### Func **GetFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Returns the Facet.  
### Func **GetFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Returns the Facet.  
### Sub **InvertDirection**( )

Invert the action's Direction.  Fails if the action is included in a group.  
### Func **SearchFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Searches the Facet.  
### Func **SearchFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

Searches the Facet.