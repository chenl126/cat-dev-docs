# AssemblyBoolean (Object)

**_Represents the AssemblyBoolean object._**

## Properties

### Property **Body**(| ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md) (Read Only)

   Returns the operating body.

**Example:**     The following example retrieves in `opBody` the operating body of the assembly boolean `assemblyBool`.

```VBScript
     Dim opBody As Body
     Set opBody = assemblyBool.Body

```

### Property **BodyComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the operating body.

**Example:**     The following example retrieves in `opBodyComp` the component that contains the operating body of the assembly boolean `assemblyBool`.

```VBScript
     Dim opBodyComp As Product
     Set opBodyComp = assemblyBool.BodyComponent

```