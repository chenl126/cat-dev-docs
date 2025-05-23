# ManufacturingOutputGenerator (Object)

**_Father object to generate output machining code._**

## Methods

### Sub **AddMeToBuffer**(| long | `oAddMe`)

   Management of specific buffer for aligned points elimination.  
### Sub **GenerateOutputCode**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`)

   Return the Output Code for an object in the right CNC Machine.  
### Sub **GetAPTCode**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oCode`)

   Retrieve generated APT code.  
### Sub **GetCurrentObject**( long  `oCurrentObject`)

   Get current object from buffer.  
### Sub **HasToResetModalValues**( long  `oIsModal`)

   Return the characteristic of an object : Reset or not Modal Values.  
### Sub **InitFileGenerator**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFormat`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `oData`)

   Init the Output Generator on the current Object and initialise all datas. Generation of NC code can start from the Process, Setup, Program or an Activity.

**Parameters:**

` iFormat`      Format of the output file : "APT", ...
` iFileName`      Output file name
` oData`      iData contains all the information about the generated NC code

### Sub **IsModal**( long  `oIsModal`)

   Return the characteristic of an object : Modal or Not Modal.  
### Func **IsSimilarTo**( [CATIAManufacturingOutputGenerator](../ManufacturingInterfaces/interface_ManufacturingOutputGenerator_169508.md)  `iObject`) As long

   Implement a method to specify if two objects are same (when Modal Mode). The result depends on the tolerance on the values (to points)  
### Sub **RunFileGenerator**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`)

   Runs the Output Generator on the datas used for generation. Generation of NC code can start from the Process, Setup, Program or an Activity.

**Parameters:**

` iData`      iData contains all the information about the generated NC code

### Sub **SetCurrentObject**( long  `iCurrentObject`)

   Set current object to buffer.