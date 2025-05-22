# ManufacturingInsert (Object)

**_The interface to access a CATIAManufacturingInsert._**

## Properties

### Property **InsertType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Return the technological type of a the insert. Example: The following example return the insert type theType of to the insert CurrentInsert theType=CurrentInsert.InsertType.  
### Property **NumberOfAttributes**( ) As short (Read Only)

Give the Number of attributes of an insert object. Example: The following example returns the Number of attributes of the insert object CurrentInsert. Number = CurrentInsert.NumberOfAttributes.  Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieve by is name the attribute of an insert object. Each attribute is a CKE object. Example: The following example retreives in MachiningQuality the attribute MfgMachiningQuality of the insert CurrentInsert

```VBScript
Set MachiningQuality = CurrentInsert.GetAttribute(MfgMachiningQuality).

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iAttributName) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Gives the NLS value of an insert object
Example:
The following example gives in NLSresult the NLS value of the "MFG_COMMENT" attributes
of the insert CurrentInsert
NLSresult = CurrentInsert.GetAttributeNLSName("MFG_COMMENT").

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  oListOfAttributeUnits)

Retrieve the list of attribute units of an insert object.
The number of items in the output array is equal to the number of attributes of the insert.
When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.
Example:
The following example retrieves in TabAttributeUnits the list of attribute units
of the insert object CurrentInsert
call CurrentInsert.GetListOfAttributeUnits(TabAttributeUnits).

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  oListOfAttributes)

Retrieve the list of attributes of an insert object.
Each attribute is returned as the name of a CKE object.
Example:
The following example retrieves in TabAttributes the list of attributes
of the insert object CurrentInsert
call CurrentInsert.GetListOfAttributes(TabAttributes).