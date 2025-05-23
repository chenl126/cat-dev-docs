# StrMemberExtremity (Object)

**_Represents an extremity of a member object._**
One is called the start extremity and the other the end extremity.

## Properties

### Property **AngleCut**(| ) As double (Read Only)

   Returns the angle cut for a member extremity.  
### Property **Cutback**( ) As [CATIAStrCutback](../StructureInterfaces/interface_StrCutback_21398.md) (Read Only)

   Returns the cutback object.  
### Property **Input**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the input object defining the extremity. The input object may not belong to the support object.  
### Property **Offset**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the offset parameter defined on this extremity. This parameter can be null.  
### Property **Point**( ) As [CATIAHybridShapePoint](../GSMInterfaces/interface_Point_5884.md) (Read Only)

   Returns the point defining the extremity. This point belongs to the support object.  Methods

### Sub **AddOffset**( double  `iOffset`)

   Adds an offset on the extremity. This method has to be used when the extremity has no offset already defined, else you will get an error.  
### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the extremity.

**Parameters:**

` oCoordinates`      The coordinates of the the extremity

### Sub **ResetCutback**( )

   Resets the defined cutback object.  
### Sub **SetExtremityFromCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Modifies the coordinates of the extremity defined by a point.

**Parameters:**

` iCoordinates`      The coordinates to modify the extremity