# DrawingViewGenerativeLinks (Object)

**_Represents the generative links of a drawing view._**

The generative links of a drawing view is an object that manages the way the generative view points at the 3D document.

## Methods

### Sub **AddLink**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iLink`)

   Adds a link to the drawing view.

**Example:**      This example adds a link to the Part document `MyPartDocument` to the `MyView` drawing view.

```VBScript
     Dim viewLinks As DrawingViewGenerativeLinks
     Set viewLinks = MyView.GenerativeLinks
     viewLinks.AddLink(MyPartDocument)

```

### Sub **CopyLinksTo**( [CATIAGenerativeViewLinks](../DraftingInterfaces/interface_DrawingViewGenerativeLinks_142664.md)  `iLinks`)

   Copies the links of the drawing view.

**Example:**      This example copies the links of the `MyView` drawing view to the `MyLinks` object.

```VBScript
     Dim viewLinks As DrawingViewGenerativeLinks
     Set viewLinks = MyView.GenerativeLinks
     Dim MyLinks As DrawingViewGenerativeLinks
     viewLinks.CopyLinksTo(MyLinks)

```

### Func **FirstLink**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns the first link of the drawing view.

**Example:**      This example retrieves the first link of the `MyView` drawing view.

```VBScript
     Dim viewLinks As DrawingViewGenerativeLinks
     Set viewLinks = MyView.GenerativeLinks
     Dim firstLink As AnyObject
     Set firstLink = MyView.FirstLink()

```

### Func **NextLink**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns the next link of the drawing view.

**Example:**      This example retrieves the next link of the `MyView` drawing view.

```VBScript
     Dim viewLinks As DrawingViewGenerativeLinks
     Set viewLinks = MyView.GenerativeLinks
     Dim nextLink As AnyObject
     nextLink = viewLinks.NextLink()

```

### Sub **RemoveAllLinks**( )

   Removes all links of the drawing view.

**Example:**      This example retrieves all links of the `MyView` drawing view.

```VBScript
     Dim viewLinks As DrawingViewGenerativeLinks
     Set viewLinks = MyView.GenerativeLinks
     viewLinks.RemoveAllLinks()

```