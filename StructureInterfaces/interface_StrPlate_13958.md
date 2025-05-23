# StrPlate (Object)

**_Represents a structure plate object._**
A plate is defined by a thickness and aggregates a support object and a sketch defining its contour.

## Properties

### Property **Offset**(| ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the offset between the given support and the support of the plate.  
### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the sketch object of the plate.  
### Property **StandardThickness**( ) As double

   Returns the standard thickness following the support orientation.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support of the plate.  Methods

### Sub **ReverseDirection**( )

   Reverses the material orientation of the plate.

```VBScript
     Plate_1.ReverseDirection

```