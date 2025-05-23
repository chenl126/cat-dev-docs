# SimulationInterfaces Framework

## Object Index

  * [Replay](SimulationInterfaces/interface_Replay_8252.md)

---

# Replay (Object)

**_The interface to access a CATIAReplay

Use this interface to customize the Replay object_**

## Methods

### Func **AddProductMotion**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As long

   Adds a product to be taken into account in the Replay object.

**Parameters:**

` iProduct`      CATIAProduct. Product to add.
` oChannel`      Channel number.

### Sub **AddSample**( long  `iChannel`,  double  `iCurrentTime`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Adds a sample(set of values) for a channel at a specific time

**Parameters:**

` iChannel`      Channel number.
` iCurrentTime`      Time.
` iPosition`      Array of values to consider the the specified channel.

### Func **GetNbProductMotion**( ) As long

   Get the number of channel related to products.

**Parameters:**

` oNbChannel`      Number of channel associated to products.

### Func **GetNbSample**( long  `iChannel`) As long

   Get the number of samples for a channel number.

**Parameters:**

` iChannel`      Channel index.
` oNbSample`      Number of samples.

### Func **GetProduct**( long  `iChannel`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Get the product for a channel.

**Parameters:**

` iChannel`      Channel index.
` oProduct`      Product.

### Sub **GetSamplePosition**( long  `iChannel`,  long  `iSample`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPosition`)

   Get the sample values.

**Parameters:**

` iChannel`      Channel index.
` iSample`      Sample index.
` oPosition`      Array of values.

### Func **GetSampleTime**( long  `iChannel`,  long  `iSample`) As double

   Get the sample time.

**Parameters:**

` iChannel`      Channel index.
` iSample`      Sample index.
` oTime`      Time value.

### Sub **RemoveSample**( long  `iChannel`,  long  `iSample`)

   Remove a specific sample.

**Parameters:**

` iChannel`      Channel index.
` iSample`      Sample index.