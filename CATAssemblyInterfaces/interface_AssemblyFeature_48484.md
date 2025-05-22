# AssemblyFeature (Object)

**_Represents the AssemblyFeature object._**

## Methods

### Sub **AddAffectedComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`)

Adds a component to the affected component list. An update of the aggregating Product is necessary to apply the Assembly Feature to this component.

**Parameters:**

` iComponent`      The component to affect  **Example:**     The following example adds the component `ProdToAffect` to the affected component list of the AssemblyFeature `assemblyFeat`.

```VBScript
assemblyFeat.AddAffectedComponent( ProdToAffect )

```

### Func **AffectedComponentsCount**( ) As long

Returns the affected component list count.

**Example:**     The following example retrieves the affected component list count of the AssemblyFeature `assemblyFeat` in `affectedListSize`.

```VBScript
affectedListSize = assemblyFeat.AffectedComponentsCount

```

### Sub **ListAffectedComponents**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfComponents`)

Retrieves the affected component list.

**Parameters:**

` oListOfComponents`      The retrieved list.
The array must be previously initialized using the
AffectedComponentsCount method.  **Example:**     The following example retrieves the affected component list of the AssemblyFeature `assemblyFeat` in `affectedList`.

```VBScript
affectedListSize = assemblyFeat.AffectedComponentsCount
Dim affectedList(affectedListSize-1)
assemblyFeat.ListAffectedComponents(affectedList)

```

### Sub **RemoveAffectedComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`)

Removes a component from the affected component list. An update of the aggregating Product is necessary to remove the generated feature from this component.

**Parameters:**

` iComponent`      The affected component to remove  **Example:**     The following example removes the component `ProdToRemove` from the affected component list of the AssemblyFeature `assemblyFeat`.

```VBScript
assemblyFeat.RemoveAffectedComponent( ProdToRemove )

```