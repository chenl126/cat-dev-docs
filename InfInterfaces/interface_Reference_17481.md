# Reference (Object)

**_Represents an object pointing to another object._**
This other object can be either a wireframe [GeometricElement](../SketcherInterfaces/interface_GeometricElement_54654.md) object such as a plane or a line, or a boundary representation object such as a face, a vertex or an edge. It may be, in particular, a [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. References are created using appropriate methods for parts. They are then passed to an object to enable associativity with the referenced object.

## Properties

### Property **DisplayName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the name of the referenced object. The name of the referenced object is either the name displayed in the specification tree for a [GeometricElement](../SketcherInterfaces/interface_GeometricElement_54654.md) object or a character string defining the reference for a boundary object.

**Example:**     The following example returns in `StrName` the displayable name of reference `FirstRef`:

```VBScript
StrName = FirstRef.DisplayName

```

Methods

### Func **ComposeWith**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Composes a reference with another reference thus creating a new composite reference.

**Parameters:**

` iReference`      The reference to be composed with the current reference.

**Example:**     The following example returns in `CompositeRef` the reference resulting from the composition of the `FirstRef` and `SecondRef` references.

```VBScript
Dim CompositeRef As Reference
Set CompositeRef = FirstRef.ComposeWith(SecondRef)

```