# FunctScripts (Collection)

**_The interface to access a set of Functional Scripts._**

It is managed on a Functional Element, thru the GenerativeKnowledge Facet Manager (GKW).

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)

Create a FunctScript.  
### Sub **Delete**( [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)  `iScript`)

Delete a FunctScript.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)

Returns an association using its index or its name from the Scripts collection.

**Parameters:**

` iIndex`      The index or the name of the Script to retrieve from the collection of Scripts. As a numerics, this index is the rank of the Script in the collection. The index of the first Script in the collection is 1, and the index of the last Script is Count. As a string, it is the name you assigned to the Script using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Script **Example:**      This example retrieves in `Act1` the fifth Script in the collection and in `Act2` the Script named `Moves`.

```VBScript
Dim FunctElem As FunctionalObject
Set FunctElem = FunctDoc.CurrentDescription.Objects.Elem("Valve")
Dim FacetGKW As FunctionalGenScriptMgr
Set FacetGKW = FunctElem.GetFacetByName("GKW")
Dim Assoc1 As FunctScript
Set Assoc1 = FacetGKW.Scripts.Elem(5)
Dim Assoc2 As FunctScript
Set Assoc2 = FacetGKW.Scripts.Elem("Producing the Skeleton 2D")

```