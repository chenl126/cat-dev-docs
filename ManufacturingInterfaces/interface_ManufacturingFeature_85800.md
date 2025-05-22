# ManufacturingFeature (Object)

**_ManufacturingFeature defines a set of methods to access a Manufacturing Feature._**

## Methods

### Func **GetAGeometricAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieve a geometry attribute of a Manufacturing Feature from its name.

**Parameters:**

` iAttribute`      The identifier of the attribute to be read **Example:**     The following example retrieves the attribute 'MfgHoleExtension' of the manufacturing feature `mfgFeature`:

```VBScript
call mfgFeature.GetAGeometricAttribute('MfgHoleExtension' ,ExtentParm)

```