# SelectedElement (Object)

**_Represents an element contained by a Selection object._**
This object is an object contained by a [Selection](../InfInterfaces/interface_Selection_18040.md) object. The [Selection](../InfInterfaces/interface_Selection_18040.md) object contains [SelectedElement](../InfInterfaces/interface_SelectedElement_47693.md) objects, which are accessed through the [Selection.Count2](../InfInterfaces/interface_Selection_18040.htm#Count2) and [Selection.Item2](../InfInterfaces/interface_Selection_18040.htm#Item2) methods.

## Properties

### Property **Document**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md) (Read Only)

Returns the document to which the selected element belongs.  
### Property **LeafProduct**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

Returns the leaf product corresponding to the selection in the specification tree.
**Role** : Returns the leaf [Product](../ProductStructureInterfaces/interface_Product_11223.md) (component, corresponding for example to "Product1.1" in the specification tree). The [AnyObject](../System/interface_AnyObject_17321.md) returned is a [Product](../ProductStructureInterfaces/interface_Product_11223.md) if a product appears in the specification tree, in the path corresponding to the current selection, and a fake [AnyObject](../System/interface_AnyObject_17321.md) whose [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property equals to "InvalidLeafProduct" otherwise. Cumulated with the use of the [AnyObject.Parent](../System/interface_AnyObject_17321.htm#Parent) property (which enables to navigate into the object structure), the current property enables the scripter to obtain the path, in the specification tree, corresponding to the selection.

**Example:**      The following example supposes a [Part](../MecModInterfaces/interface_Part_3788.md) or a [Product](../ProductStructureInterfaces/interface_Product_11223.md) is opened. It asks the end user to select a [Shape](../MecModInterfaces/interface_Shape_5555.md) in the current window. It then sends message boxes containing the names of the automation objects contained in the specification tree path corresponding to the shape selected, and, regarding the automation objects which are products (only products which are components), a message box containing the abcissa of the translation of the product compared to its reference product.

```VBScript
Dim Status,Feature,LeafProduct,LeafProductProcessed,InputObjectType(0)
Dim Document,Selection,AutomationTreeNodeOrProduct,Position,AxisComponentsArray(11)
Set Document = CATIA.ActiveDocument : Set Selection = Document.Selection
    'We propose to the user that he select a feature
InputObjectType(0)="AnyObject"
Status=Selection.SelectElement2(InputObjectType,"Select a feature",true)
if (Status = "Cancel") then Exit Sub
Set Feature = Selection.Item(1).Value
Set LeafProduct = Selection.Item(1).LeafProduct
LeafProductProcessed = true
if (LeafProduct.Name<>"InvalidLeafProduct") then LeafProductProcessed = false
Set AutomationTreeNodeOrProduct = Feature
do while (TypeName(AutomationTreeNodeOrProduct)<>"Application")
    '  We send a message box, if AutomationTreeNodeOrProduct is not nor a Shapes object neither a PartDocument object
    if ((TypeName(AutomationTreeNodeOrProduct)<>"Shapes") And _
        (TypeName(AutomationTreeNodeOrProduct)<>"Bodies") And _
        (TypeName(AutomationTreeNodeOrProduct)<>"PartDocument") And _
        (TypeName(AutomationTreeNodeOrProduct)<>"Products") And _
        (TypeName(AutomationTreeNodeOrProduct)<>"ProductDocument")) then
        msgbox AutomationTreeNodeOrProduct.Name
        if (TypeName(AutomationTreeNodeOrProduct)="Product") then
    '          We display a message box containing the abcissa of the translation, except in the case of the
    '          root product
            if (TypeName(AutomationTreeNodeOrProduct.Parent.Parent)<>"Application") then
                Set Position = AutomationTreeNodeOrProduct.Position
                Call Position.GetComponents(AxisComponentsArray)
                msgbox AxisComponentsArray(9)
            end if
        end if
    end if
    '  We determine the next automation tree node or product
    Set AutomationTreeNodeOrProduct = AutomationTreeNodeOrProduct.Parent
    if ((TypeName(AutomationTreeNodeOrProduct)="Application") And (Not LeafProductProcessed)) then
    '      The specification tree path corresponding to the selection contains at least one product, which the current
    '      loop as not yet processed. It means that the parent in the specification tree of the feature corresponding
    '      to the last message box sent is LeafProduct
        Set AutomationTreeNodeOrProduct = LeafProduct
        LeafProductProcessed = true
    end if
loop
```

If you run the preceeding piece of script, the current document beeing a product with the following specification tree:

```VBScript
    +--------+
    !Product3!
    +----+---+
         !
         +- Product2 (Product2.1)             'translation value: 10
         !     !
         !     +- Product1 (Product1.1)       'translation value: 20
         !           !
         !           +- Part1 (Part1.1)
         !                !
         !                +- Part1
         !                     !
         !                     +- PartBody
         !                           !
         !                           +- Pad.1
         +- Part2 (Part2.1)
```

and you select Pad.1, the message boxes displayed will be:

```VBScript
    Pad.1
    PartBody
    Part1
    Part1.1
    Product1.1
    20
    Product2.1
    10
    Product3

```

### Property **Reference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

Returns a Reference version of the Value property.
**Role** : Returns a [Reference](../InfInterfaces/interface_Reference_17481.md) version of Value .  
### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the string constant which describes the selected element Automation type.
This type is returned by the Value property, and may be, for instance `"Pad"` or `"Line2D"`.
**Caution** : This property gives the leaf automation type of the object, in the inheritance hierarchy. Nevertheless, after a call to [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) , [Selection.SelectElement3](../InfInterfaces/interface_Selection_18040.htm#SelectElement3) , [Selection.SelectElement4](../InfInterfaces/interface_Selection_18040.htm#SelectElement4) , [Selection.IndicateOrSelectElement2D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement2D) or [Selection.IndicateOrSelectElement3D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement3D) , this property gives the input filter string constant relative to the effective selection (more precisely the first filter string constant delivered through the iFilterType parameter, for which the current automation object fullfills the string constant). This string constant may be an automation object name corresponding to the iFilterType parameter with which [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) has previously been called, or even a [CATSelectionFilter](../InfInterfaces/enum_CATSelectionFilter_67138.md) value name.

**Example:**      Suppose you run the following piece of script:

```VBScript
Set Selection = CATIA.ActiveDocument.Selection
    '  We propose to the user that he select a Prism or a Hole
ReDim InputObjectType(1) : InputObjectType(0)="Prism" : InputObjectType(1)="Hole"
Status=Selection.SelectElement2(InputObjectType,"Select a prism or a hole",true)
if (Status = "Cancel") then Exit Sub
AutomationType = Selection.Item(1).Type
```

If the user selects a Pad, the script `AutomationType` variable will contain `"Prism"` and not `"Pad"`.
Consequently, in most cases, use the VBScript TypeName function instead of this property.  
### Property **Value**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) (Read Only)

Returns the actual selected automation object.  Methods

### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioPoint`)

Returns the coordinates of the pick point.

**Parameters:**

` oPoint`      The coordinates of the pick point, i.e. the hit between the geometric object and the cursor. The length of this parameter will be 3, except if the document is a
[DrawingDocument](../DraftingInterfaces/interface_DrawingDocument_48585.md)
**Example:**      This example retrieves the coordinates of the pick point in the array myArray:

```VBScript
Dim oSelElem As SelectedElement
Set oSelElem = CATIA.ActiveDocument.Selection.Item(1)
ReDim myArray(2)
oSelElem.GetCoordinates myArray

```