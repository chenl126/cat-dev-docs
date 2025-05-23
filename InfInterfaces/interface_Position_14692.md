# Position (Object)

**_Represents the position object._**
The position object is the 3D-axis system associated with an object.

## Methods

### Sub **GetComponents**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oAxisComponentsArray`)

   Returns the components of an object's position. This returns the 3D-axis system associated with the object.

**Parameters:**

` oAxisComponentsArray`      The array used to store the twelve components retrieved from the objet's position. The first nine represent succcessively the components of the x-axis, y-axis, and z-axis. The last three represent the coordinates of the origin point.

**Example:**      This example retrieves in `oAxisComponentsArray` the 3D-axis system components from the `Position` object associated with `MyObject`:

```VBScript
     Dim oAxisComponentsArray ( 11 )
     MyObject.Position.GetComponents oAxisComponentsArray

```

### Sub **SetComponents**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAxisComponentsArray`)

   Sets the components of an object's position. This sets the 3D-axis system associated with the object.

**Parameters:**

` iAxisComponentsArray`      The array initialized with the components to set to the object's position. The first nine represent succcessively the components of the x-axis, y-axis, and z-axis. The last three represent the coordinates of the origin point.

**Example:**      This example sets the 3D-axis system components stored in `iAxisComponentsArray` to the `Position` object associated with `MyObject`:

```VBScript
     Dim iAxisComponentsArray( 11 )
     ' x axis components
     iAxisComponentsArray( 0 )  = 1.000
     iAxisComponentsArray( 1 )  = 0
     iAxisComponentsArray( 2 )  = 0.707
     ' y axis components
     iAxisComponentsArray( 3 )  = 0
     iAxisComponentsArray( 4 )  = 0
     iAxisComponentsArray( 5 )  = 0.707
     ' z axis components
     iAxisComponentsArray( 6 )  = 0
     iAxisComponentsArray( 7 )  = -0.707
     iAxisComponentsArray( 8 )  = 0.707
     ' origin point coordinates
     iAxisComponentsArray( 9 )  = 1.000
     iAxisComponentsArray( 10 ) = 2.000
     iAxisComponentsArray( 11 ) = 3.000
     MyObject.Position.SetComponents iAxisComponentsArray

```