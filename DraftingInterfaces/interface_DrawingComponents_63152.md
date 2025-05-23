# DrawingComponents (Collection)

**_A collection of all the drawing components (ditto) currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**(| [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md) | `iDrawingComponentRef`,| | double | `iPositionX`,| | double | `iPositionY`) As [CATIADrawingComponent](../DraftingInterfaces/interface_DrawingComponent_55624.md)

   Creates a drawing component instance and adds it to the DrawingComponents collection.

**Parameters:**

` iDrawingComponentRef`      The view (i.e. the detail) that is the component reference . This view also called a detail MUST belong to a sheet of component references (i.e. details)
` iPositionX,iPositionY`      The drawing component x and y coordinates, expressed in millimeters, with respect to the drawing view coordinate system

**Returns:**      The created drawing component instance  **Example:**      The following example creates a drawing component instance with a given component reference `MyComponentRef` coming from a Sheet of component references (i.e. details) `SheetComponentRef` and retrieved in `MyComponentInst` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
     Dim MyComponentRef As DrawingView
     Set MyComponentRef = SheetComponentRef.Views.Item(1)
     Dim MyView As DrawingView
     Set MyView = MySheet.Views.ActiveView
     Dim MyComponentInst As DrawingComponent
     Set MyComponentInst = MyView.Components.Add(MyComponentRef, 100., 50.)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADrawingComponent](../DraftingInterfaces/interface_DrawingComponent_55624.md)

   Returns a drawing component instance using its index or its name from the DrawingComponents collection.

**Parameters:**

` iIndex`      The index or the name of the drawing component instance to retrieve from the collection of drawing components. As a numerics, this index is the rank of the drawing component instance in the collection. The index of the first drawing component instance in the collection is 1, and the index of the last drawing component instance is Count. As a string, it is the name you assigned to the drawing component instance using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved drawing component instance  **Example:**      This example retrieves in `ThisDrawingComponent` the second drawing component instance, `MyView` in the drawing view collection of the active sheet in the active document, supposed to be a drawing document.

```VBScript
     Dim MySheet As DrawingSheet
     Set MySheet = CATIA.ActiveDocument.Sheets.ActiveSheet
     Dim MyView  As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     Dim ThisDrawingComponent As DrawingComponent
     Set ThisDrawingComponent = MyView.Components.Item(2)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a drawing component from the DrawingComponents collection.

**Parameters:**

` iIndex`      The index of the drawing component to remove from the collection of drawing components. As a numerics, this index is the rank of the drawing component in the collection. The index of the first drawing component instance in the collection is 1, and the index of the last drawing component instance is Count. As a string, it is the name you assigned to the drawing component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the third drawing component instance in the drawing component collection of the active view of the active document, supposed to be a drawing document.

```VBScript
     Dim MyView As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     MyView.Components.Remove(3)

```