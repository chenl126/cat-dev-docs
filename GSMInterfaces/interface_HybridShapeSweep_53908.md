# HybridShapeSweep (Object)

**_Represents the hybrid shape Sweep feature object._**
**Role** : Declare hybrid shape Sweep root feature object. All interfaces for different type of sweep derivates HybridShapeSweep.

Use the CATIAHybridShapeFactory to create a HybridShapeSweep objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FillTwistedAreas**( ) As long

Returns or sets the fill twisted areas mode.  
### Property **SetbackValue**( ) As double

Returns or sets the setback value.  Methods

### Sub **AddCutPoints**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`)

Sets two cut points on the master guide. These points define a zone to be kept on the final swept surface.

**Parameters:**

` iElement1`      First / start cut point.
` iElement2`      Second / end cut point.

### Sub **AddFillPoints**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`)

Sets two fill points on the master guide. These points define a zone to be filled on the final swept surface.

**Parameters:**

` iElement1`      First / start fill point.
` iElement2`      Second / end fill point.

### Func **GetCutPoint**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

### Func **GetFillPoint**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

### Sub **RemoveAllCutPoints**( )

Removes all cut points.  
### Sub **RemoveAllFillPoints**( )

Removes all fill points.