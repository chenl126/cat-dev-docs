# Parameter (Object)

**_Represents the parameter._**
It can be computed from a relation: formula, program, or check. It is an abstract object which is not intended to be created as such, but from which the integer, bolean, real, and string parameters derive. Here is an example to create one:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim density As RealParam
Set density = part1.Part.Parameters.CreateReal("density", 2.5)

```

**See also:**      [IntParam](../KnowledgeInterfaces/interface_IntParam_13730.md), [BoolParam](../KnowledgeInterfaces/interface_BoolParam_17217.md), [RealParam](../KnowledgeInterfaces/interface_RealParam_17053.md), [StrParam](../KnowledgeInterfaces/interface_StrParam_13874.md), [Formula](../KnowledgeInterfaces/interface_Formula_11046.md), [Rule](../KnowledgeInterfaces/interface_Rule_3720.md), [Check](../KnowledgeInterfaces/interface_Check_5408.md)

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the parameter object comment.  
### Property **Context**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

Returns the context of the parameter : a part, a product, a drafting, a process, depending where the parameter is.  
### Property **Hidden**( ) As boolean

Returns or sets wether the parameter is hidden or should be hidden. or not.  
### Property **IsTrueParameter**( ) As boolean (Read Only)

Returns a boolean saying if the parameter is a true one (real, dimension, string, etc.) or a geometrical one (isolated points, curves, surfaces).  
### Property **OptionalRelation**( ) As [CATIARelation](../KnowledgeInterfaces/interface_Relation_14366.md) (Read Only)

Returns the relation that can be used to compute the parameter. As this relation might not exist, NULL may be returned, so a test is required.

**Example:**      This example checks if there is a relation to compute the `param1` parameter, and if no relation exists, displays a message box:

```VBScript
Set param1_rel = param1.OptionalRelation
If param1_rel is Nothing Then
     MsgBox "No relation to compute param1"
End If

```

### Property **ReadOnly**( ) As boolean (Read Only)

Returns whether the parameter can be modified.

**Example:**      This example checks if the `param1` parameter can be modified, and if it cannot, displays a message box:

```VBScript
If ( param1.ReadOnly ) Then
     MsgBox "No way to change param1"
End If

```

### Property **Renamed**( ) As boolean (Read Only)

Returns a boolean saying if the parameter is a renamed parameter or not.  
### Property **UserAccessMode**( ) As long (Read Only)

Returns the user access mode of the parameter.  0    Read only parameter (cannot be destroyed). 1    Read/write parameter (cannot be destroyed). 2    User parameter (can be read, written and destroyed).  Methods

### Sub **Rename**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

Renames the parameter.

**Parameters:**

` iName`      The new name of the parameter  **Example:**      This example renames the `param1` parameter to `PartSeatbodyMinimumThickness`:

```VBScript
Call param1.Rename("PartSeatbodyMinimumThickness")

```

### Sub **ValuateFromString**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

Valuates a parameter using a string as input. The string depends on parameter nature : "True" or "False" for Boolean a numerical value for Integer or Real a numerical value with or without a unit for Dimension

**Parameters:**

` iValue`      The value to assign to the dimension parameter  **Example:**      This example sets the value of the existing `dimension` parameter to a new value:

```VBScript
dimension.ValuateFromString("300mm");

```

### Func **ValueAsString**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the value of the parameter as a string. **Example:**      This example gets the value of the existing `dimension` parameter and shows it in a message box

```VBScript
Dim str
str = dimension.ValueAsString;
MessageBox str

```