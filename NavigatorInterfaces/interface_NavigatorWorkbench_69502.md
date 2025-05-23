# NavigatorWorkbench (Object)

**_The object to manage all DMU Navigator entities._**

This version allows to manage groups and annotated views.

## Properties

### Property **AnnotatedViews**(| ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

   Returns the AnnotatedViews collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("AnnotatedViews")` on the root product, to retrieve the `AnnotatedViews` collection.

**Example:**      This example retrieves the AnnotatedViews collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheAnnotatedViewsList As AnnotatedViews
        Set TheAnnotatedViewsList = TheNavigatorWorkbench.AnnotatedViews

```

### Property **DMUDataFlow**( ) As [CATIADMUDataFlow](../NavigatorInterfaces/interface_DMUDataFlow_24296.md) (Read Only)

   Returns the DMU DataFlow object.  
### Property **Groups**( ) As [CATIAGroups](../NavigatorInterfaces/interface_Groups_8540.md) (Read Only)

   Returns the Groups collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Groups")` on the root product, to retrieve the `Groups` collection.

**Example:**      This example retrieves the Groups collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheGroupsList As Groups
        Set TheGroupsList = TheNavigatorWorkbench.Groups

```

### Property **Hyperlinks**( ) As [CATIAHyperlinks](../NavigatorInterfaces/interface_Hyperlinks_22650.md) (Read Only)

   Returns the Hyperlinks collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Hyperlinks")` on the root product, to retrieve the `Hyperlinks` collection.

**Example:**      This example retrieves the Hyperlinks collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim HyperlinksList As Hyperlinks
        Set HyperlinksList = TheNavigatorWorkbench.Hyperlinks

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

   Returns the Marker3Ds collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Marker3Ds")` on the root product, to retrieve the `Marker3Ds` collection.

**Example:**      This example retrieves the Marker3Ds collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheMarker3DsList As AnnotatedViews
        Set TheMarker3DsList = TheNavigatorWorkbench.Marker3Ds

```

Methods

### Sub **AdvancedView**( [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)  `iAnnotatedView`,  short  `iViewOption`)

   Applies the annotated view to the current viewer.

**Parameters:**

` iAnnotatedView`      The annotated view to apply.
` iViewOptions`      The option to launch the annotated view command, possible values are

  * CatAnnotatedViewCmdOption_NoToolbar : No Toolbar for annotation creation
  * CatAnnotatedViewCmdOption_NoAnimation : No Animation when applying the view

**Example:**      This example applies the view of the `NewAnnotatedView` AnnotatedView.

```VBScript
        TheNavigatorWorkbench.View,CatAnnotatedViewCmdOption_NoAnimation+CatAnnotatedViewCmdOption_NoToolbar(NewAnnotatedView)

```

### Func **GetOrder**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`) As long

   Returns the order of an object.

**Parameters:**

` iObject`      The object whose rank has to be returned.
` oCurrentRank`      The current rank of the object (from 1 to n the number of objects in the collection).

**Example:**      This example creates an annotated view `NewAnnotatedView` and returns its position.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )

        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add

        Dim iOrder As Integer
        iOrder = TheNavigatorWorkbench.GetOrder(NewAnnotatedView)

```

### Sub **SetOrder**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`,  long  `iNewRank`)

   Sets the order of an object.

**Parameters:**

` iObject`      The object whose rank has to be modified.
` iNewRank`      The new rank of the object (from 1 to n the number of objects in the collection).

**Example:**      This example creates an annotated view `NewAnnotatedView` and move it to the first position.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )

        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add
        TheNavigatorWorkbench.SetOrder NewAnnotatedView, 1

```

### Sub **View**( [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)  `iAnnotatedView`)

   Applies the annotated view to the current viewer.

**Parameters:**

` iAnnotatedView`      The annotated view to apply.

**Example:**      This example applies the view of the `NewAnnotatedView` AnnotatedView.

```VBScript
        TheNavigatorWorkbench.View(NewAnnotatedView)

```