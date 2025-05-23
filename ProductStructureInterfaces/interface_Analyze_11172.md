# Analyze (Object)

**_Represents the analysis object associated with a product._**

## Properties

### Property **Mass**(| ) As double (Read Only)

   Returns the product mass value.

**Example:**      This example retrieves `MassValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     MassValue = myProduct.Analyze.Mass

```

### Property **Volume**( ) As double (Read Only)

   Returns the product volume value.

**Example:**      This example retrieves `VolumeValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     VolumeValue = myProduct.Analyze.Volume

```

### Property **WetArea**( ) As double (Read Only)

   Returns the product wet area (outer volume).
Note: This method uses **mm3** instead of default Catia V5 unit.

**Example:**      This example retrieves `WetAreaValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     WetAreaValue = myProduct.Analyze.WetArea

```

Methods

### Sub **GetGravityCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oGravityCenterCoordinatesArray`)

   Returns the gravity center coordinates of product.

**Parameters:**

` Coordinates`      The array storing the three gravity center coordinates. This array must be previously initialized.

**Example:**      This example retrieves the gravity center coordinates in `oGravityCenterCoordinatesArray` from the `Analyze` object associated with `myProduct`:

```VBScript
     ' Coordinates array initialization
     Dim oGravityCenterCoordinatesArray ( 2 )
     ' Get value in array
     Myproduct.Analyze.GetGravityCenter oGravityCenterCoordinatesArray

```

### Sub **GetInertia**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInertiaMatrixArray`)

   Returns the inertia matrix array of product.

**Parameters:**

` oInertiaMatrixArray`      The array storing successively the three columns of inertia matrix. This array must be previously initialized.

**Example:**      This example retrieves the inertia matrix components in `oInertiaMatrixArray` from the `Analyze` object associated with `myProduct`:

```VBScript
     ' Components array initialization
     Dim oInertiaMatrixArray ( 8 )
     ' Get value in array
     Myproduct.Analyze.GetInertia oInertiaMatrixArray
     ' oInertiaMatrixArray ( 0 ) is the Ixx component
     ' oInertiaMatrixArray ( 1 ) is the Ixy component
     ' oInertiaMatrixArray ( 2 ) is the Ixz component
     ' oInertiaMatrixArray ( 3 ) is the Iyx component
     ' oInertiaMatrixArray ( 4 ) is the Iyy component
     ' oInertiaMatrixArray ( 5 ) is the Iyz component
     ' oInertiaMatrixArray ( 6 ) is the Izx component
     ' oInertiaMatrixArray ( 7 ) is the Izy component
     ' oInertiaMatrixArray ( 8 ) is the Izz component

```