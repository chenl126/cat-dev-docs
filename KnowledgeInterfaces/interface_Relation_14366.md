# Relation (Object)

**_Represents the relation object._**
It is an abstract object which is not intended to be created as such, but from which the check, design table, formula, rule, objects derive.

**See also:**      [Check](../KnowledgeInterfaces/interface_Check_5408.md), [DesignTable](../KnowledgeInterfaces/interface_DesignTable_25284.md), [Formula](../KnowledgeInterfaces/interface_Formula_11046.md), [Rule](../KnowledgeInterfaces/interface_Rule_3720.md)

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the comment associated with the relation. The comment explains the relation's purpose. It is passed as the second input argument of the relation creation methods of the [Relations](../KnowledgeInterfaces/interface_Relations_18301.md) collection.

**Example:**      This example retrieves the `maximummass` relation comment and displays it in a message box:

```VBScript
relcomment = maximummass.Comment
MsgBox "maximummass comment : " & relcomment

```

### Property **Context**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

Returns the context of the parameter.
The context of a parameter can be a part, a product, a drafting, or a process document, depending where the parameter is.

**Returns:**      The context  **See also:**      [Part](../MecModInterfaces/interface_Part_3788.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md), CATIADrawing, CATIAProcess  
### Property **NbInParameters**( ) As long (Read Only)

Returns the number of input parameters of the relation.  
### Property **NbOutParameters**( ) As long (Read Only)

Returns the number of output parameters of the relation.
The output parameters of the relation are those constrained by the relation.  
### Property **Value**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the definition of the relation. It returns an empty string if the relation is not an expressional one (for example for a design table). The definition is the body to be executed to compute one or several parameters. It is passed as the last input argument of the relation creation methods of the [Relations](../KnowledgeInterfaces/interface_Relations_18301.md) collection.

**Example:**      This example retrieves the `maximummass` relation definition and displays it in a message box:

```VBScript
reldef = maximummass.Value
MsgBox "maximummass relation is defined as " & reldef

```

Methods

### Func **GetInParameter**( long  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

Returns an input parameter of the relation.
This method can return an object that is not a parameter, that is, you cannot handle it as a Parameter object. For example, in a relation like

```VBScript
    Area.1 = area(PartBody\Pad.1\Sketch.1)
```

the object PartBody\Pad.1\Sketch.1 is a sketch and not a parameter.
To use such an object, call the Visual Basic `TypeName` function to retrieve its real type.

```VBScript
    Dim objectType
objectType = TypeName(oParameter)
If objectType = "Parameter" Then
...
```

**Parameters:**

` iIndex`      The searched input parameter index in the relation.
**Legal values** : 1 ≤ iIndex ≤
NbInParameters 
### Func **GetOutParameter**( long  `iIndex`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Returns an output parameter of the relation. Use TypeName method on the returned parameter to get the real type of the parameter.

**Parameters:**

` iIndex`      The searched input parameter index in the relation.
**Legal values** : 1 ≤ iIndex ≤
NbOutParameters 
### Sub **Modify**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

Modifies the relation.

**Parameters:**

` iValue`      The new relation value

### Sub **Rename**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

Renames the relation.

**Parameters:**

` iName`      The new relation name