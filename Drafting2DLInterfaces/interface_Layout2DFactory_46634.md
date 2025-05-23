# Layout2DFactory (Object)

**__**

## Methods

### Func **Create2DLayout**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iStandardName`) As [CATIALayout2DLayout](../Drafting2DLInterfaces/interface_Layout2DRoot_29538.md)

   Create the `2DLayout` associated to the 3D mechanical feature tha implement this interface. E.g. a Mechanical Part.

**Parameters:**

` CATBSTR`      iStandardName The standard name to apply to the new layout.
` oLayout`      The created `2DLayout`. This feature is unique for a given 3D context feature. Consequently requesting this interface on a 3D feature that is already associated to a `2DLayout` feature will fail. You must first request for any existing `2DLayout` via
[AnyObject.GetItem](../System/interface_AnyObject_17321.htm#GetItem) method using `CATLayoutRoot` key parameter to check for `2DLayout` pre-existing feature as follow :

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot")
     if MyRoot Is Nothing then
       Dim MyRootFact As Layout2DFactory
       Set MyRootFact = CATIA.ActiveDocument.Part.GetItem("CATLayoutRootFactory")
       Set MyRoot = MyRootFact.Create2DLayout("ISO_3D")
     end if

```