# PspAttribute (Object)

**_Represents Attribute Interface to query Plant Ship objects' attributes._**
**Role** : To query and reset attributes.

## Methods

### Func **GetMultiStringAttributeValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Retrieves String values for the input attribute the type catPspIDLMultiString.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      List of string values  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfBSTRs

 ...
Set objArg2 = objThisIntf.GetMultiStringAttributeValues (strVar1)

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieve parameter for the input attribute name.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      Parameter of the attribute  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim ObjVar2 As Parameter

 ...
Set objArg2 = objThisIntf.GetParameter (strVar1 )

```

### Func **GetType**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CatPspIDLAttrDataType](../CATPlantShipInterfaces/enum_CatPspIDLAttrDataType_87829.md)

Retrieves type of the input attribute. If the type of the attribute is catPspIDLMultiString use GetMultiStringAttributeValues. for others, use GetParameter().

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      Type of the attribute.  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim eType As CatPspIDLAttrDataType

 ...
eType = objThisIntf.GetType (strVar1)

```

### Func **IsDerived**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As boolean

Retrieve Derived status for the input attribute.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      TRUE if the attribute is derived  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim bIsDerived As boolean

 ...
bIsDerived = objThisIntf.IsDerived (strVar1)

```

### Func **IsDiscrete**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`,  boolean  `obStatus`) As short

Query whether the input attribute is discrete or not.

**Parameters:**

` iAttributeName`      Attribute Name
` obStatus`      TRUE if attribute is discrete else FALSE
**Returns:**      Discrete Type value 1-Standard 2-Encoded discrete  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim boolVar2 As Boolean
Dim shortVar3  As Short
 ...
shortVar3 = objThisIntf.IsDiscrete (strVar1,boolVar2)

```

### Func **ListAttributes**( [CatPspIDLDomainID](../CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md)  `iDomainID`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Retrieves a list of Attributes of an object in the the input domain ID.

**Parameters:**

` iDomainID`      Domain ID. If set to catPspIDLNone, then it will return attributes in all the domains.
**Returns:**      List of attributes ( A list of CATIAPspGroupables)  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim objArg1 As CatPspIDLDomainID
Dim objArg2 As PspListOfBSTRs
 ...
Set objArg2 = objThisIntf.ListAttributes (objArg1)

```

### Func **ListDoubleDiscreteValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

Retrieves double discrete values for the input attribute.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      Discrete list of double values  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfDoubles

 ...
Set objArg2 = objThisIntf.ListDoubleDiscreteValues (strVar1 )

```

### Sub **ListEncodedDecodedDiscreteValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLDiscreteEncodedValues`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLDiscreteDecodedValue`)

Retrieves Encoded-decoded discrete values for the input attribute.

**Parameters:**

` iAttributeName`      Attribute Name
` oLDiscreteEncodedValues`      Discrete list of encoded string values
` oLDiscreteDecodedValue`      Discrete list of decoded string values
**Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfBSTRs
Dim objArg3 As PspListOfBSTRs

 ...
objThisIntf.ListEncodedDecodedDiscreteValues strVar1, objArg2, objArg3

```

### Func **ListIntegerDiscreteValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATIAPspListOfLongs](../CATPlantShipInterfaces/interface_PspListOfLongs_41364.md)

Retrieve integer (long) discrete values for the input attribute.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      Discrete list of integer values  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfLongs

 ...
Set objArg2 = objThisIntf.ListIntegerDiscreteValues (strVar1)

```

### Func **ListStringDiscreteValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

RetrievesString discrete values for the input attribute.

**Parameters:**

` iAttributeName`      Attribute Name
**Returns:**      Discrete list of string values  **Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfBSTRs

 ...
Set objArg2 = objThisIntf.ListStringDiscreteValues (strVar1)

```

### Sub **ResetDerivedAttr**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`)

Reset derived status of the attribute to not-derived.

**Parameters:**

` iAttributeName`      Attribute Name
**Example:**

```VBScript
Dim objThisIntf As PspAttribute
Dim strVar1 As CATBSTR

 ...
objThisIntf.ResetDerivedAttr strVar1

```