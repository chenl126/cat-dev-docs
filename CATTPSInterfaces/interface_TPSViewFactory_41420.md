# TPSViewFactory (Object)

**_Represents the TPS view factory object._**
All the created views are added to the annotation set object from which this interface is retrieved, thanks to the [AnnotationSet.TPSFactory](../CATTPSInterfaces/interface_AnnotationSet_36773.htm#TPSFactory) property.

## Methods

### Func **CreateView**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iPlane`,| | [CATVariant](../System/typedef_CATVariant_20656.md) | `iViewType`) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

   Creates a view.

**Parameters:**

` iPlane`      The plane onto which the view will be created
` iViewType`      The view type

**Legal values** :

  * 1: Front View
  * 2: Section View
  * 3: Cut View