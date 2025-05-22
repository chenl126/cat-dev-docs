# DrawingThread (Object)

**_Represents a drawing thread in a drawing view._**

## Properties

### Property **Type**( ) As [CatThreadType](../DraftingInterfaces/enum_CatThreadType_35594.md)

Returns or sets a CatThreadType (threaded or taped) on a thread. Be careful, this method is only available on threads which are linked to 2D circle geometry  **Example:**      The following example sets the type Taped in `MyThread`

```VBScript
 If MyThread.IsLinkedTo()=cat2DCircle Then
    MyThread.Type = catTaped
  End If

```

Methods

### Func **IsLinkedTo**( ) As [CatThreadLinkedTo](../DraftingInterfaces/enum_CatThreadLinkedTo_59064.md)

Specifies which kind of objects the thread is linked to.

**Returns:**      oLinkedType The type of thread link  **Example:**      The following example retrieves the CatThreadLinkedTo in `MyThread` This view belongs to the drawing view collection of the drawing sheet

```VBScript
ThreadLinkType = MyThread.IsLinkedTo

```