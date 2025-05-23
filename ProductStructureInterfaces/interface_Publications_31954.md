# Publications (Collection)

**_The collection of the Product publications._**
A Product object can aggregate one or zero Publications collection.

## Methods

### Func **Add**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iPublicName`) As [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)

   Adds a publication object to the product and returns a pointer to the publication object.

**Parameters:**

` iPublicName`      The name of the publication
` oPub`      The publication object

**Example:** The following example adds a new publication object with the name "PubName" to the product and returns the publication object `Pub1`.

```VBScript
     Dim Prod1 As Product
     Set Pub1 = Prod1.Add(PubName)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`) As [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)

   Returns the publication object corresponding to the given publication name.

**Parameters:**

` iIdentifier`      The name of the publication
` oPub`      The publication object

**Example:** The following example returns `Pub1` publication object from the product referencing the published name `PubId`.

```VBScript
     Dim Prod1 As Product
     Set Pub1 = Prod1.Item(PubId)

```

### Sub **Remove**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIdentifier`)

   Removes a publication from the product.

**Parameters:**

` iIdentifier`      The name of the publication

**Example:** The following example removes the publication object corresponding to the name `PubId`.

```VBScript
     Dim Prod1 As Product
     Prod1.Remove(PubId)

```

### Sub **SetDirect**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPointed`)

   Valuates a publication object directly with the object it publishes.

**Parameters:**

` iIdentifier`      The name of the publication
` iPointed`      The published object The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md)

**Example:** The following example valuates the publication object of product `Prod1` having the name `PubId` with the reference object `RefObject`.

```VBScript
     Dim Prod1 As Product
     Prod1.SetDirect(PubId,RefObject)

```

### Sub **SetRelay**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`,  [CATIAPublications](../ProductStructureInterfaces/interface_Publications_31954.md)  `iRelayer`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iNameInRelay`)

   Valuates a publication object with another publication object.

**Parameters:**

` iIdentifier`      The name of the publication to be valuated
` iRelayer`      The product aggregating the valuating intermediate publication object
` iNameInRelay`      The name of the valuating publication object

**Example:** The following example valuates the publication object of product `Prod1` having the name `PubId1` with the publication object of product `Prod2` having the name `PubId2`.

```VBScript
     Dim Prod1 As Product
     Prod1.SetRelay(PubId1,Prod2,PubId2)

```