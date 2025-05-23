# HybridShapeOffset (Object)

**_Represents the hybrid shape offset feature object._**

**Role** : To access the data of the hybrid shape offset feature object. This data includes:

  * The element to offset
  * The offset direction
  * The offset value

Use the CATIAHybridShapeFactory to create a HybridShapeOffset object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **OffsetDirection**(| ) As boolean

   Returns or sets whether the offset direction is to be inverted.

**True** to invert the offset direction.  
### Property **OffsetValue**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

   Returns or sets the offset value.  
### Property **OffsetedObject**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the face to offset.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Property **SuppressMode**( ) As boolean

   Returns or sets suppress mode.

**True** to activate suppress mode  Methods

### Sub **AddTrickyFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTrickyFace`)

   Adds a tricky face object on the object.  
### Func **GetTrickyFace**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the invalid face object on the object.
param : iRank =position of faces ionvalid for offset  
### Sub **RemoveTrickyFace**( long  `iRank`)

   Remove the tricky face object on the object.
param : iRank =position of the face in the list of TrickyFaces  
### Sub **SetOffsetValue**( double  `iOffset`)

   Set Offset value with input as double.
To be replace in further release by integration in the pragma put_xxx