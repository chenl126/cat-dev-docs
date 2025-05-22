# DefaultAnnotation (Object)

**_This interface is used to get information about default annotation._**
Ther is two kinds of default annotation : \- with a manual selection \- with a selection automatic

## Properties

### Property **LinkWiGeomType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Get the type of link between the default annotation and the geometry. Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oLinkWiGeom`      Type of link.

### Property **SearchAlgoType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Get the type of search algo to find geometry on which the annotation apply to. Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oAlgo`      Type of algo.
Methods

### Func **IsInAutomaticSearchMode**( ) As boolean

Get the type of search algo Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oIsAutoMode`      oIsAutoMode = TRUE if Automatic mode