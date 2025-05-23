# CATPlantShipInterfaces Framework

## Object Index

  * [PspAppFactory](CATPlantShipInterfaces/interface_PspAppFactory_36446.md)
  * [PspApplication](CATPlantShipInterfaces/interface_PspApplication_42486.md)
  * [PspAttribute](CATPlantShipInterfaces/interface_PspAttribute_31780.md)
  * [PspAttributeReport](CATPlantShipInterfaces/interface_PspAttributeReport_70682.md)
  * [PspBuildPart](CATPlantShipInterfaces/interface_PspBuildPart_30554.md)
  * [PspClass](CATPlantShipInterfaces/interface_PspClass_13994.md)
  * [PspCntrFlow](CATPlantShipInterfaces/interface_PspCntrFlow_26160.md)
  * [PspConnectable](CATPlantShipInterfaces/interface_PspConnectable_41588.md)
  * [PspConnector](CATPlantShipInterfaces/interface_PspConnector_31646.md)
  * [PspFunctional](CATPlantShipInterfaces/interface_PspFunctional_36800.md)
  * [PspGroup](CATPlantShipInterfaces/interface_PspGroup_14418.md)
  * [PspGroupable](CATPlantShipInterfaces/interface_PspGroupable_31100.md)
  * [PspID](CATPlantShipInterfaces/interface_PspID_4796.md)
  * [PspLightBend](CATPlantShipInterfaces/interface_PspLightBend_29782.md)
  * [PspLightConnector](CATPlantShipInterfaces/interface_PspLightConnector_62040.md)
  * [PspLightPart](CATPlantShipInterfaces/interface_PspLightPart_30786.md)
  * [PspListOfBSTRs](CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)
  * [PspListOfDoubles](CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)
  * [PspListOfLongs](CATPlantShipInterfaces/interface_PspListOfLongs_41364.md)
  * [PspListOfObjects](CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)
  * [PspLogicalLine](CATPlantShipInterfaces/interface_PspLogicalLine_40658.md)
  * [PspObject](CATPlantShipInterfaces/interface_PspObject_17416.md)
  * [PspPartConnector](CATPlantShipInterfaces/interface_PspPartConnector_55256.md)
  * [PspPhsyicalProduct](CATPlantShipInterfaces/interface_PspPhsyicalProduct_69816.md)
  * [PspPhysical](CATPlantShipInterfaces/interface_PspPhysical_26308.md)
  * [PspPlacePart](CATPlantShipInterfaces/interface_PspPlacePart_30238.md)
  * [PspResource](CATPlantShipInterfaces/interface_PspResource_26635.md)
  * [PspSpatial](CATPlantShipInterfaces/interface_PspSpatial_21700.md)
  * [PspStretchableData](CATPlantShipInterfaces/interface_PspStretchableData_67114.md)
  * [PspTempListFactory](CATPlantShipInterfaces/interface_PspTempListFactory_69400.md)
  * [PspWorkbench](CATPlantShipInterfaces/interface_PspWorkbench_31080.md)

## Enumerated Types Index

  * [CatPspIDLApplicationID](CATPlantShipInterfaces/enum_CatPspIDLApplicationID_94374.md)
  * [CatPspIDLAttrDataType](CATPlantShipInterfaces/enum_CatPspIDLAttrDataType_87829.md)
  * [CatPspIDLDomainID](CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md)
  * [CatPspIDLFlowCapability](CATPlantShipInterfaces/enum_CatPspIDLFlowCapability_107424.md)
  * [CatPspIDLFlowReality](CATPlantShipInterfaces/enum_CatPspIDLFlowReality_81334.md)
  * [CatPspIDLFunctionStatus](CATPlantShipInterfaces/enum_CatPspIDLFunctionStatus_109872.md)
  * [CatPspIDLPartConnectorType](CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)

---

# CatPspIDLApplicationID (Enumeration)

**_Application IDs._**

**Role** : Application identification.

**Values:**

` catPspIDLCATPiping`      Piping Design Application
` catPspIDLCATHVAC`      HVAC Design Application
` catPspIDLCATEquipment`      Equipment Arrangement application
` catPspIDLCATWaveguide`      Waveguide Design application
` catPspIDLCATTubing`      Tubing Design application
` catPspIDLCATHanger`      Hanger Design application
` catPspIDLCATRaceway`      Raceway Design application
` catPspIDLCATConduit`      Conduit Design application
` catPspIDLCATCompAccess`      Compartment and Access appication
` catPspIDLCATElectrical`      Electrical Design application
` catPspIDLCATPID`      Piping and Instrumentation Diagrams
` catPspIDLCATHVACDiagram`      HVAC Diagrams
` catPspIDLCATTubingDiagram`      Tubing Diagrams
` catPspIDLCATWaveguideDiagram`      Waveguide Diagrams
` catPspIDLCATElectricalDiagram`      Electrical Diagrams

---

# CatPspIDLAttrDataType (Enumeration)

**_Attribute type._**

**Role** : Attribute type

**Values:**

` catPspIDLInteger`      integer type
` catPspIDLDouble`      Double type
` catPspIDLString`      String type
` catPspIDLMultiString`      Special attribute of type List of string
` catPspIDLBoolean`      Boolean type

---

# CatPspIDLDomainID (Enumeration)

**_Doamin IDs._**

**Role** : Represents Domain identification

**Values:**

` catPspIDLNone,`      No domain
` catPspIDLCATPIP,`      CATPIP Domain
` catPspIDLCATINS,`      CATINS Domain
` catPspIDLCATHVA`      CATHVA Domain
` catPspIDLCATEQT`      CATEQT Domain
` catPspIDLCATTUB`      CATTUB Domain
` catPspIDLCATMLD`      CATMLD Domain
` catPspIDLCATWVG`      CATWVG Domain
` catPspIDLCATRWY`      CATRWY Domain
` catPspIDLCATCND`      CATCND Domain
` catPspIDLCATHGR`      CATHGR Domain
` catPspIDLCATCAM`      CATCAM Domain
` catPspIDLCATELE`      CATELE Domain

---

# CatPspIDLFlowCapability (Enumeration)

**_Flow capability directions._**

**Role** : Represents flow direction capability of a connector.

**Values:**

` CatPspIDLFlowCapability_Undefined`      Undefined.
` CatPspIDLFlowCapability_InDirection`      In.
` CatPspIDLFlowCapability_OutDirection`      Out.
` CatPspIDLFlowCapability_InOutDirection`      In-Out.

---

# CatPspIDLFlowReality (Enumeration)

**_Actual Flow directions._**

**Role** : Represents Actual flow directions of a connector.

**Values:**

` CatPspIDLFlowReality_Undefined`      Undefined.
` CatPspIDLFlowReality_InDirection`      In.
` CatPspIDLFlowReality_OutDirection`      Out.
` CatPspIDLFlowReality_InOutDirection`      In-Out.

---

# CatPspIDLFunctionStatus (Enumeration)

**_Indicates if function has network data and if it is linked to a physical part._**

**Role** : Function object status.

**Values:**

` catPspIDLFuncUndefined`      Function data is undefined.
` catPspIDLInFuncNet`      Function with network data and is not linked to any physical part
` catPspIDLFuncNetPhysType`      Function with network data and has only physical type information.
` catPspIDLFuncNetPhysNoPos`      Function with network data and has physical information but no 3D position.
` catPspIDLFuncNoNetPhys`      Function with no network data and is linked to a resolved physical part with 3D position.
` catPspIDLFuncNetPhys`      Function with network data and is linked to a resolved physical part with 3D position.

---

# CatPspIDLPartConnectorType (Enumeration)

**_Part Connector types._**

**Role** : Types of part connector.

**Values:**

` CatPspIDLPartCtrTypeNotRecognized`      Undefined.
` CatPspIDLPartCtrTypeFace`      Face connector
` CatPspIDLPartCtrTypeSupport`      Support type connect
` CatPspIDLPartCtrTypeCenter`      Center
` CatPspIDLPartCtrTypeTop`      Top
` CatPspIDLPartCtrTypeBottom`      Buttom
` CatPspIDLPartCtrTypeLeft`      Left
` CatPspIDLPartCtrTypeRight`      Right
` CatPspIDLPartCtrTypeTopLeft`      Top-Left
` CatPspIDLPartCtrTypeTopRight`      Top-Right
` CatPspIDLPartCtrTypeBottomLeft`      Bottom-Left
` CatPspIDLPartCtrTypeBottomRight`      Bottom-Right
` CatPspIDLPartCtrTypeCircular`      Circular
` CatPspIDLPartCtrTypeRectangular`      Rectangular
` CatPspIDLPartCtrTypeUpOnly`      Up only

---

# PspAppFactory (Object)

**_Represents the application factory._**

**Role** : To create, instanciate, delete and query groups, logical lines, compartments and parts.

## Methods

### Func **CreateGroup**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGroupType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGroupID`) As [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)

   Creates a group in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query.
` iGroupType`      Group Startup type.
` iGroupID`      Group ID. A default ID will be generated if input is NULL.

**Returns:**      Created Group instance.  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim iStrVar2 As String
     Dim iStrVar3 As String
     Dim iObj4 As PspGroup
      ...
     Set iObj4=objThisIntf.CreateGroup (iobj1,iStrVar2,iStrVar3 )

```

### Sub **DeleteCompartment**( [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)  `iCompartment`)

   Delete a compartment instance.

**Parameters:**

` iCompartment`      Compartment to be deleted

**Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As PspGroup

      ...
     objThisIntf.DeleteCompartment iobj1

```

### Sub **DeleteGroup**( [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)  `iGroup`)

   Delete a group.

**Parameters:**

` iGroup`      Group to be deleted.

**Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As PspGroup

      ...
     objThisIntf.DeleteGroup iobj1

```

### Sub **DeleteLogicalLine**( [CATIAPspLogicalLine](../CATPlantShipInterfaces/interface_PspLogicalLine_40658.md)  `iLogicalLine`)

   Delete a logical line instance.

**Parameters:**

` iLogicalLine`      Logical Line to be deleted

**Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As PspLogicalLine

      ...
     objThisIntf.DeleteLogicalLine iobj1

```

### Sub **DeletePart**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iPart`)

   Delete a part.

**Parameters:**

` iProduct`      Part to be deleted.

**Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product

      ...
     objThisIntf.DeletePart iobj1

```

### Func **GetCompartment**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCompartmentID`) As [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)

   Instanciate a compartment from the catalog into the current Product.

**Parameters:**

` iCurrentProduct`      The current Product into which a compartment will be instanciated.
` iCompartmentID`      Compartment ID to get from the compartment catalog.

**Returns:**      Compartment instance.  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim iStrVar2 As String
     Dim iObj3 As PspGroup
      ...
     Set iObj3=objThisIntf.GetCompartment (iobj1,iStrVar2 )

```

### Func **GetLogicalLine**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogicalLineID`) As [CATIAPspLogicalLine](../CATPlantShipInterfaces/interface_PspLogicalLine_40658.md)

   Returns a PspLogicalLine Logical line Instance.

**Parameters:**

` iCurrentProduct`      The current Product into which a logical line will be instanciated.
` iLogicalLineID`      Logical line ID to get from the logical line catalog.

**Returns:**      Logical line instance.  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim iStrVar2 As String
      ...
     objThisIntf.GetLogicalLine (iobj1,iStrVar2 )

```

### Func **ListCompartments**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

   Retrieves a list of Compartments in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query.

**Returns:**      A list of Compartmemts ( A list of CATIAPspGroup)  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim objArg2 As PspListOfObjects

      ...
     Set ObjArg2 = objThisIntf.ListCompartments (iobj1 )

```

### Func **ListGroups**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

   Retrieve a list of Groups in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query..

**Returns:**      A list of Groups ( A list of CATIAPspGroup)  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim objArg2 As ListOfObjects

      ...
     Set ObjArg2 = objThisIntf.ListGroups (iobj1)

```

### Func **ListLogicalLines**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

   Returns a list of logical lines in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query..

**Returns:**      A list of logical Lines (A list of PspLogicalLine)  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim objArg2 As PspListOfObjects

      ...
     Set ObjArg2 = objThisIntf.ListLogicalLines (iobj1 )

```

### Func **ListPhysicals**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CatPspIDLDomainID](../CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md)  `iDomainID`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

   Returns a list of Physical objects in the node.

**Parameters:**

` iCurrentProduct`      The current Product to query.
` iDomainID`      Physical objects that have this domain ID. To get list of all in all domains set iDomainID= catPspIDLNone.

**Returns:**      A list of physical objects (A list of PspPhysical objects)  **Example:**

```VBScript
     Dim objThisIntf As PspAppFactory
     Dim iobj1 As Product
     Dim iobjArg2 As CatPspIDLDomainID
     Dim objArg3 As PspListOfObjects

      ...
     Set ObjArg3 = objThisIntf.ListPhysicals (iobj1, iobjArg2 )

```

---

# PspApplication (Object)

**_Represents an application._**

**Role** : To activate and query a Distributive System application.

## Methods

### Sub **Initialization**( )

   Initializes the application environment (load feature start up objects, activate the application..).

**Example:**

```VBScript
     Dim objPrdRoot        As Product
     Dim objPspWorkbench   As PspWorkbench
     Dim objPspApplnPip       As PspApplication
     Dim objPspApplnTub    As PspApplication

     Set objPrdRoot = CATIA.ActiveDocument.Product
     Set objPspWorkbench = objPrdRoot.GetTechnologicalObject ("PspWorkbench")

     Set objPspApplnPip = objPspWorkbench.GetApplication(catPspIDLCATPiping)
     ...

     objPspApplnPip.Initialization
     ....
     Set objPspApplnTub = objPspWorkbench.GetApplication(catPspIDLCATTubing)

```

---

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

---

# PspAttributeReport (Object)

**_Represents the Attribute Report._**

**Role** : To generate attributes report.

## Methods

### Func **GenerateReport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInputFormatFile`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOutputfile`) As long

   Generate report (output format in html or CSV) and returns the status. It reports attribute data for all the selected objects in the document.

**Parameters:**

` iInputFormatFile`      Attribute report format filename. It should contain the directory path.

```VBScript
     Note:
       The format file is a text (.txt) file containing data in following
       order.
       Title=Title of the report
       TextFormat=HTML  or  TextFormat=CSV (Comma separated )
       Attrib=AttributeName likes Nominal size,EndStyle, Rating etc.
       Len=Integer value indicating length of attribute value
       and so on...
       Report format sample: Sample.txt
       Title=Piping parts report
       TextFormat=HTML
       Attrib=ID
       Len=15
       Attrib=Nominal size
       Len=10
       Attrib=Rating
       Len=10
       .... and so on

```

` iOutputfile`      Output filename. Full file name of the report output.

**Returns:**      0 or 1. **Legal values** :
`1 :` Report generation failed.
`0 :` Report generation succeeded.  **Example:**

```VBScript
     Dim objThisIntf As PspAttributeReport
     Dim strVar1 As CATBSTR
     Dim StrVar2 As CATBSTR
     Dim longRet    As Long
      ...
     olongRet = objThisIntf.GenerateReport (strVar1,strVar2 )

```

---

# PspBuildPart (Object)

**_Represents Interface to create and modify a part._**

**Role** : To build and define a part.

## Methods

### Func **ChangePartType**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `uPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns the part after changing the part type of an existing part.

**Parameters:**

` iReferencePart`      Reference Product in CATPart document to modify.
` iPartType`      New part class type.
` iPartNumber`      New Part number.

**Returns:**      New reference Product in CATPart document  **Example:**

```VBScript
     Dim objThisIntf As PspBuildPart
     Dim iRefPart As   Product
     Dim iuPartType As CATBSTR
     Dim uPartNumber As CATBSTR
     Dim oNewRefPart As Product
      ...
     Set oNewRefPart= objThisIntf.ChagePartType (iRefPart, iuPartType, uPartNumber )

```

### Func **ListPartParametricAttributes**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Returns the part parametric attribute names.

**Parameters:**

` iRefPart`      Reference Product in new CATPart document.

**Returns:**      List of parametric attribute names.  **Example:**

```VBScript
     Dim objThisIntf As PspBuildPart
     Dim iRefPart As Product
     Dim oLAttributeNames As PspListOfBSTRs

      ...
     Set oLAttributeNames = objThisIntf.ListPartParametricAttributes (iRefPart)

```

### Func **NewPart**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `uPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Create a new part.

**Parameters:**

` iPartType`      Part class type.
` iPartNumber`      Part number.

**Returns:**      Retruns Reference Product pointer in new CATPart document.  **Example:**

```VBScript
     Dim objThisIntf As PspBuildPart
     Dim iuPartType As CATBSTR
     Dim uPartNumber As CATBSTR
     Dim oNewRefPart As Product
      ...
     Set oNewRefPart = objThisIntf.NewPart (iuPartType, uPartNumber)

```

### Sub **SetPartParametricAttributes**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `iLAttributeNames`)

   Sets the part parametric attribute names.

**Parameters:**

` iRefPart`      Reference Product in new CATPart document.
` iLAttributeNames`      List of parametric attribute names.

**Example:**

```VBScript
     Dim objThisIntf As PspBuildPart
     Dim iRefPart As Product
     Dim iLAttributeNames As PspListOfBSTRs

      ...
     objThisIntf.SetPartParametricAttributes iRefPart, iLAttributeNames

```

---

# PspClass (Object)

**_Represent Interface to list the start up object classes of an application._**

**Role** : Application object classes.

## Properties

### Property **StartUpConnectors**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

   Returns a List of start-up Connector object classes.

**Example:**

```VBScript
     Dim objThisIntf As PspClass
     Dim objArg1 As PspListOfBSTRs
      ...
     Set objArg1 = objThisIntf.StartUpConnectors

```

### Property **StartUpFunctions**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

   Returns a List of start-up Function object classes.

**Example:**

```VBScript
     Dim objThisIntf As PspClass
     Dim objArg1 As PspListOfBSTRs
      ...
     Set objArg1 = objThisIntf.StartupFunctions

```

### Property **StartUpPhysicals**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

   Returns a List of start-up physical object classes.

**Example:**

```VBScript
     Dim objThisIntf As PspClass
     Dim objArg1 As PspListOfBSTRs
      ...
     Set objArg1 = objThisIntf.StartupPhysicals

```

---

# PspCntrFlow (Object)

**_Represents Interface to manage Connector Flow property._**

**Role** : To query and modify Plant-Ship Connector Flow property.

## Properties

### Property **FlowCapability**( ) As [CatPspIDLFlowCapability](../CATPlantShipInterfaces/enum_CatPspIDLFlowCapability_107424.md)

   Returns or sets Flow capability of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspCntrFlow
     Dim ojArg1 As CatPspIDLFlowCapability
      ...
     Set ojArg1 = objThisIntf.FlowCapability

```

### Property **FlowReality**( ) As [CatPspIDLFlowReality](../CATPlantShipInterfaces/enum_CatPspIDLFlowReality_81334.md)

   Returns or sets Flow reality of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspCntrFlow
     Dim ojArg1 As CatPspIDLFlowReality
      ...
     Set ojArg1 = objThisIntf.FlowReality

```

---

# PspConnectable (Object)

**_Represents an Interface to manage object behaviors in making connections._**

**Role** : To specify object behaviors such as adding a connector and removing a connector.

## Properties

### Property **Connectors**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of connectors of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspConnectable
     Dim objArg1 As CatPspIDLDomainID
     Dim objArg2 As PspListOfBSTRs
      ...
     Set objArg2 = objThisIntf.Connectors

```

### Property **ValidConnectorTypes**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

   Returns a list of Valid connector types on this object.

**Example:**

```VBScript
     Dim objThisIntf As PspConnectable
     Dim objArg1 As PspListOfBSTRs
      ...
     Set objArg1 = objThisIntf.ValidConnectorTypes

```

Methods

### Func **GetConnectorByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuConnectorName`) As [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)

   Retrieves a connector with the given name.

**Parameters:**

` iConnectorName`      Connector name to look for.

**Returns:**      Connector with given name.  **Example:**

```VBScript
     Dim objThisIntf As PspConnectable
     Dim strVar1 As PspListOfBSTRs
     Dim objArg2 As PspConnector
      ...
     Set objArg2 = objThisIntf.GetConnectorByName (strVar1)

```

### Sub **ListConnectables**( [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `iuClassFilter`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntbles`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntrsOnThisObj`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntrsOnConnected`)

   Retrieve a list of connectors of the object.

**Parameters:**

` iuClassFilter`      Class filter list. If iuClassFilter is an empty list then it will get connectors for all the application connector types.
` oLCntbles`      a list of CATIAPspConnectable objects that connect this object
` oLCntrsOnThisObj`      a list of connectors on "this" object in the connections ( A list of CATIAPspConnector)
` oLCntrsOnConnected`      a list of connectors on the other objects that the member of the former list is connected to (positions in oLCntrsOnThisObj and oLCntrsOnConnected corresponds to each other) ( A list of CATIAPspConnector)

**Example:**

```VBScript
     Dim objThisIntf As PspConnectable
     Dim objArg1 As PspListOfBSTRs
     Dim objArg2 As PspListofObjects
     Dim objArg3 As PspListofObjects
     Dim objArg4 As PspListofObjects
      ...
     objThisIntf.ListConnectables objArg1,objArg2,objArg3,objArg4

```

---

# PspConnector (Object)

**_Represents connector object._**

**Role** : To specify connector behaviors such as connect and disconnect.

## Properties

### Property **AttrNames**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Returns or Sets Attribute names of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim ojArg1 As CATIAPspListOfBSTRs
      ...
     Set ojArg1 = objThisIntf.AttrNames

```

### Property **ConnectorName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets name of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim strVar1 As CATBSTR
      ...
     Set strVar1 = objThisIntf.Name
     Dim strVar1 As CATBSTR
      ...
     objThisIntf.ConnectorName = strVar2

```

Methods

### Sub **Connect**( [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)  `iCntrToConnect`)

   Connect the connector to another connector.

**Parameters:**

` iCntrToConnect`      the connector to be connected to

**Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim objArg1 As PspConnector
      ...
     objThisIntf.Connect objArg1

```

### Sub **Disconnect**( [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)  `iCntrToDisconnect`)

   DisConnect the connector from another connector.

**Parameters:**

` iCntrToDisconnect`      The connector to be disconnected from

**Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim objArg1 As PspConnector
      ...
     objThisIntf.Disconnect objArg1

```

### Func **GetAssociatedConnectable**( ) As [CATIAPspConnectable](../CATPlantShipInterfaces/interface_PspConnectable_41588.md)

   Get the connectable-owner of this connector.

**Parameters:**

` oConnectable`      Connectable owner of this connector

**Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim objArg1 As CATIAPspConnectable
      ...
     Set objArg1 = objThisIntf.GetAssociatedConnectable

```

### Func **IsCntrConnected**( ) As boolean

   Query whether the connector has been connected.

**Returns:**      TRUE if this connector is connected.  **Example:**

```VBScript
     Dim objThisIntf As PspConnector
     Dim bArg1 As boolean
      ...
     bArg1 = objThisIntf.IsCntrConnected

```

---

# PspFunctional (Object)

**_Represents Plant Ship functional object._**

**Role** : To access Plant Ship Functional object information.

## Properties

### Property **CatalogPartName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns catalog part name of physical object that realizes this function.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
      ...
     Set strVar1 = objThisIntf.CatalogPartName

```

### Property **FunctionStatus**( ) As [CatPspIDLFunctionStatus](../CATPlantShipInterfaces/enum_CatPspIDLFunctionStatus_109872.md) (Read Only)

   Returns function object status.

**Example:**

```VBScript
     Dim objThisIntf As PspPhysical
     Dim objArg1 As CatPspIDLFunctionStatus
      ...
     objArg1 = objThisIntf.FunctionStatus

```

### Property **PartCatalogName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns Part catalog name of physical object that realizes this function.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
      ...
     strVar1 = objThisIntf.PartCatalogName

```

### Property **PartNumber**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns part number of physical object that realizes this function.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
      ...
     strVar1 = objThisIntf.PartNumber

```

### Property **PartType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the part type of physical object that realizes this function.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
      ...
     strVar1 = objThisIntf.PartType

```

### Property **Physicals**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of all associated physical objects.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim objArg1 As PspListOfObjects
      ...
     Set objArg1 = objThisIntf.Physicals

```

### Property **Standard**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return Standard.

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
      ...
     strVar1 = objThisIntf.Standard

```

Methods

### Func **GetCompatiblePartTypes**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Retrieves a list of all physical part types that are compatible with this function.

**Parameters:**

` iuStandard`      Standard name

**Returns:**      List of Compatible Part Types.  **Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
     Dim objArg2 As PspListOfBSTRs

      ...
     Set objArg1 = objThisIntf.GetCompatiblePartTypes   (strVar1)

```

### Func **IsOKToIntegrate**( ) As boolean

   Check it is OK to integrate (realize) this function with a physical part.

**Returns:**      TRUE if ok to be integrated  **Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim objArg1 As boolean
      ...
     objArg1 = objThisIntf.IsOKToIntegrate

```

### Func **IsRealized**( ) As boolean

   Checks if the Function object is realized or not.

**Returns:**      TRUE if the object is Realized  **Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim objArg1 As boolean
      ...
     objArg1 = objThisIntf.IsRealized

```

### Func **IsSpecDriven**( ) As boolean

   Checks if the functional object is specification driven or not.

**Returns:**      TRUE if this object is specification driven.  **Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim objArg1 As boolean
      ...
     objArg1 = objThisIntf.IsSpecDriven

```

### Sub **ListCompatiblePartNumbers**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuCatalogName`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLPartTypes`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLCatalogPartNames`)

   Retrieves a list of compatible Part numbers and part types.

**Parameters:**

` iuPartType`      part type
` iuStandard`      Standard name
` iuCatalogName`      catalog name
` oLPartTypes`      a list of part types
` oLCatalogPartNames`      List of catalog part names

**Example:**

```VBScript
     Dim objThisIntf As PspFunctional
     Dim strVar1 As CATBSTR
     Dim strVar2 As CATBSTR
     Dim strVar3 As CATBSTR
     Dim objArg4 As PspListOfBSTRs
     Dim objArg5 As PspListOfBSTRs

     ..
     ..
     objThisIntf.ListCompatiblePartNumbers strVar1,strVar2,strVar3,objArg4,objArg5

```

---

# PspGroup (Object)

**_Represent the Group._**

**Role** : It manages group members in making logical relationship.

## Properties

### Property **Members**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Members of the Group.

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspListOfObjects

      ...
     Set ObjArg1 = objThisIntf.Members

```

Methods

### Sub **AddMember**( [CATIAPspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md)  `iGroupable`)

   Adds a member to the group.

**Parameters:**

` iGroupable`      Member to add

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspGroupable

      ...
      objThisIntf.AddMember objArg1

```

### Sub **RemoveMember**( [CATIAPspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md)  `iGroupable`)

   Removes a member from the group.

**Parameters:**

` iGroupable`      a member to be removed

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspGroupable

      ...
      objThisIntf.RemoveMember objArg1

```

---

# PspGroupable (Object)

**_Represent the Groupable object that can be grouped by Group object._**

**Role** : It is used to query the group object link to this object.

## Properties

### Property **Groups**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Groups to which this object is a member.

**Example:**

```VBScript
     Dim objThisIntf As PspGroupable
     Dim objArg1 As PspListOfObjects

      ...
     Set ObjArg1 = objThisIntf.Groups

```

---

# PspID (Object)

**_Represents the interface to generate and set IDs for the Distributive System Objects._**

**Role** : This is the interface for Plant Ship object ID generation.

## Methods

### Func **GenAndPutID**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the Generated ID with the sequence number and is stored on the object.

**Returns:**      ID generated  **Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     iStrVar1 =objThisIntf.GenAndPutID

```

### Func **GenAndPutIDNoGenSeqNum**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Generates ID without the sequence number and is stored on the object.

**Returns:**      ID generated  **Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     iStrVar1 =objThisIntf.GenAndPutIDNoGenSeqNum

```

### Func **GenIDNoGenSeqNum**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Generates ID without the sequence number( if not set previously) and is not stored on the object.

**Parameters:**

` oGeneratedID`      ID generated

**Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     iStrVar1 =objThisIntf.GenIDNoGenSeqNum

```

### Func **GetID**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets ID for the object.

**Returns:**      ID of the object.  **Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     iStrVar1 =objThisIntf.GetID

```

### Func **GetLocalID**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves local ID of the object.

**Returns:**      Local ID generated  **Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     iStrVar1 =objThisIntf.GetLocalID

```

### Func **IsIDGenerated**( ) As boolean

   Checks if the ID on the object is generated( based on the ID Schema).

**Parameters:**

` oBIsGenerated`      TRUE if ID is generated from the ID schema

**Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim bVar1 As boolean
      ...
     bVar1 =objThisIntf.IsIDGenerated

```

### Sub **SetID**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iID`)

   Sets ID for the object.

**Parameters:**

` oID`      ID to be set.

**Example:**

```VBScript
     Dim objThisIntf As PspID

     Dim iStrVar1 As String
      ...
     objThisIntf.SetID iStrVar1

```

---

# PspLightBend (Object)

**_Represents the Light bendable object._**

**Role** : It is used access light bendable data.

## Methods

### Func **GetBendData**( ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the list of bend radii.

**Returns:**      List of bend radius (PspListOfDoubles).  **Example:**

```VBScript
     Dim objThisIntf As PspLightBend

     Dim objArg1 As PspListOfDoubles
      ...
     Set objArg1 = objThisIntf.GetBendData

```

### Sub **SetBendData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListOfBendRadius`)

   Sets a list of bend radii.

**Parameters:**

` iListOfBendRadius`      List of bend radius.

**Example:**

```VBScript
     Dim objThisIntf As PspLightBend

     Dim objArg1 As CATSafeArrayVariant
      ...
     objThisIntf.SetBendData objArg1

```

---

# PspLightConnector (Object)

**_Represents the light connector._**

**Role** : To access light connector data.

## Methods

### Func **GetAlignmentVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetAlignmentVector (objArg1)

```

### Func **GetOrientationVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the Orientation Direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetOrientationVector (objArg1)

```

### Func **GetOrigin**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oOrigin`      Origin point position-three double values stand for x,y,z

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetOrigin (objArg1)

```

### Sub **SetAlignmentVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAlignmentDirection`)

   Sets the alignment direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iAlignmentDirection`      Three double values stand for X,Y,Z component of the Alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetAlignmentVector objArg1, dbVar2

```

### Sub **SetOrientationVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrientationDirection`)

   Sets the Orientation Direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iAlignmentDirection`      Three double values stand for X,Y,Z component of the Alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetAlignmentVector objArg1, dbVar2

```

### Sub **SetOrigin**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb3Position`)

   Sets the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iDb3Position`      absolute X-Y-Z coordinates of the current position of the connector to be set

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(3) As CATSafeArrayVariant
      ...
     objThisIntf.SetOrigin objArg1, dbVar2

```

---

# PspLightPart (Object)

**_Represents the light part._**

**Role** : To access light object data.

## Methods

### Func **GetDefinition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Retrieves the points defining the object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).

**Returns:**      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.  **Example:**

```VBScript
     Dim objThisIntf As PspLightPart
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
     Set objArg1 = Nothing
      ...
     Set objArg2 = objThisIntf.GetDefinition (objArg1)

```

### Sub **SetDefinition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListPoints`)

   Set the points defining the light object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).
` oListPoints`      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.

**Example:**

```VBScript
     Dim objThisIntf As PspLightPart
     Dim objArg1 As CATSafeArrayVariant
     Dim dbVar2(3) As CATSafeArrayVariant
      ...
     objThisIntf.SetDefinition objArg1, dbVar2

```

---

# PspListOfBSTRs (Object)

**_Represents a collection of CATBSTR type of strings._**

**Role** : Collection of CATBSTR type of strings.

## Properties

### Property **Count**( ) As long (Read Only)

   Returns the number of character strings in the list.

**Example:**      This example retrieves in `NumberOfStrings` the number of character strings currently gathered in `MyList`.

```VBScript
     Dim NumberOfStrings As long
     NumberOfStrings = MyList.Count

```

Methods

### Sub **Append**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iBSTR`)

   Adds a character string to the end of the list.

**Parameters:**

` iBSTR`      The character string to be added to the list.

**Example:**      The following example appends a string to the list.

```VBScript
     Dim MyList As PspListOfBSTRs
     MyList.Append("MyString")

```

### Func **Item**( long  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns a character string from its index in the list.

**Parameters:**

` iIndex`      The index of the first character string in the collection is 1, and the index of the last character string is Count.

**Returns:**      the retrieved string.  **Example:**      The following example returns the third character string in the list.

```VBScript
     Dim MyStr As String
     Dim MyList As PspListOfBSTRs
     MyStr = PspListOfBSTRs.Item(3)

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Remove a character string from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the character string to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As PspListOfBSTRs
     MyList.Remove(2)

```

---

# PspListOfDoubles (Object)

**_Represents a collection of double values._**

**Role** : Collection of double.

## Properties

### Property **Count**( ) As long (Read Only)

   Returns the number of doubles in the list.

**Example:**      This example retrieves in `NumberOfdoubles` the number of doubles currently gathered in `MyList`.

```VBScript
     NumberOfdoubles = MyList.Count

```

Methods

### Sub **Append**( double  `iDouble`)

   Adds a double to the end of the list.

**Parameters:**

` iDouble`      The double to be added to the list.

**Example:**      The following example appends an object to the list.

```VBScript
     Dim MyDouble As Double
     MyDouble = 0.6789
     Dim MyList As PspListOfDoubles
     MyList.Append(MyDouble)

```

### Func **Item**( long  `iIndex`) As double

   Returns a double from its index in the list.

**Parameters:**

` iIndex`      The index of the first double in the collection is 1, and the index of the last double is Count.

**Returns:**      the retrieved double.  **Example:**      The following example returns in the third double in the list.

```VBScript
     Dim MyDouble As double
     Dim MyList As PspListOfDoubles
     MyDouble = PspListOfDoubles.Item(3)

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Removes a double from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the double to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As PspListOfDoubles
     MyList.RemoveByIndex(2)

```

---

# PspListOfLongs (Object)

**_Represents a collection of Long values._**

**Role** : Collection of Long.

## Properties

### Property **Count**( ) As long (Read Only)

   Returns the number of long integers in the list.

**Example:**      This example retrieves in `NumberOfLongs` the number of long integers currently gathered in `MyList`.

```VBScript
     NumberOfLongs = MyList.Count

```

Methods

### Sub **Append**( long  `iLong`)

   Adds an long integer to the end of the list.

**Parameters:**

` iLong`      The long integer to be added to the list.

**Example:**      The following example appends a long integer to the list.

```VBScript
     Dim MInteger As Long
     MInteger = 4
     Dim MyList As PspListOfLongs
     MyList.Append(MInteger)

```

### Func **Item**( long  `iIndex`) As long

   Returns a long integer from its index in the list.

**Parameters:**

` iIndex`      The index of the first long integer in the collection is 1, and the index of the last long integer is Count.

**Returns:**      the retrieved long integer.  **Example:**      The following example returns in the third long integer in the list.

```VBScript
     Dim MyLong As Integer
     Dim MyList As PspListOfLongs
     MyLong = PspListOfLongs.Item(3)

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Remove a long integer from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the long integer to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As PspListOfLongs
     MyList.RemoveByIndex (2)

```

---

# PspListOfObjects (Object)

**_Represents a collection of Objects._**

**Role** : Collection of Object.

## Properties

### Property **Count**( ) As long (Read Only)

   Returns the number of objects in the list.

**Example:**      This example retrieves in `NumberOfObjects` the number of objects currently gathered in `MyList`.

```VBScript
     NumberOfObjects = MyList.Count

```

Methods

### Sub **Append**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Adds an object to the end of the list.

**Parameters:**

` iObject`      The object to be added to the list.

**Example:**      The following example appends an object to the list.

```VBScript
     Dim MyObject As AnyObject
     Dim MyList As PspListOfObjects
     MyList.Append(MyObject)

```

### Func **Item**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns an object from its index in the list.

**Parameters:**

` iIndex`      The index of the first object in the collection is 1, and the index of the last object is Count.
` iInterfaceName`      The interface name of oObj.

**Returns:**      the retrieved object.  **Example:**      The following example returns in the third object in the list.

```VBScript
     Dim MyObject As PspID
     Dim MyList As PspListOfObjects
     Set MyObject = PspListOfObjects.Item(3,"CATIAPspID")

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Remove an object from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the object to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As PspListOfObjects
     MyList.RemoveByIndex (2)

```

---

# PspLogicalLine (Object)

**_Represents the logical line._**

**Role** : To query the logical line object's from/to members.

## Methods

### Sub **GetFromTo**( [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oListFromMajor`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oListFromMinor`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oListToMajor`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oListToMinor`)

   Retrieves the lists of major and minor from/to members from this line.
The members retrieved are all [PspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md) objects.

**Parameters:**

` oListFromMajor`      The list of major from members
` oListFromMinor`      The list of minor from members
` oListToMajor`      The list of major to members
` oListToMinor`      The list of minor to members

**Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim objArg1 As PspListOfObjects
     Dim objArg2 As PspListOfObjects
     Dim objArg3 As PspListOfObjects
     Dim objArg4 As PspListOfObjects
     ...
     objThisIntf.GetFromTo objArg1, objArg2, objArg3, objArg4

```

### Func **GetFromToInfoArrayMaxSize**( ) As long

   Returns the maximum possible size of the from-to information.

**Returns:**      The maximum possible size of the array to hold the information returned by GetFromToInformation **Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim intValueMaxSize As Integer
     ...
     intValueMaxSize = objThisIntf.GetFromToInfoArrayMaxSize

```

### Sub **GetFromToInformation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFromToLabel`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFTMajor`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFTMinor`,  long  `oSizeOfOutput`)

   Retrieves the from/to information of a logical line.

**Parameters:**

` oFromToLabel`      The array of labels ("From" or "To")
` oFTMajor`      The array of from/to major IDs
` oFTMinor`      The array of from/to minor IDs
` The`      size of the output arrays

**Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim strFromToLabel(20) As String
     Dim strFromToMajor(20) As String
     Dim strFromToMinor(20) As String
     Dim intValueMaxSize As Integer
     intValueMaxSize = objThisIntf.GetFromToInfoArrayMaxSize
     ...
     '----  make sure the array size if big enough
     If (intValueMaxSize ≤ 20)  Then
        objThisIntf.GetFromToInformation _
          strFromToLabel, strFromToMajor, strFromToMinor, intValueMaxSize
     End If

     The following table can then be filled with the output arrays.

        From/To        |   F/T Major       |    F/T Minor
     strFromToLabel(i) | strFromToMajor(i) |  strFromToMinor(i)

```

---

# PspObject (Object)

**_Represents PspObject._**

**Role** : To access Plant Ship object information.

## Properties

### Property **ApplicationID**( ) As [CatPspIDLApplicationID](../CATPlantShipInterfaces/enum_CatPspIDLApplicationID_94374.md) (Read Only)

   Returns the ApplicationID of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspObject
     Dim eApplID As CatPSPIDLApplicationID
      ...
     eApplID = objThisIntf.ApplicationID

```

### Property **DomainID**( ) As [CatPspIDLDomainID](../CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md) (Read Only)

   Returns the DomainID of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspObject
     Dim eDomanID As CatPspIDLDomainID
      ...
     eDomanID = objThisIntf.DomainID

```

### Property **StartupType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the Startup type of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspObject
     Dim strStartUp As String
     ...
     strStartUp = objThisIntf.StartupType

```

---

# PspPartConnector (Object)

**_Represent the Part Connector to manage the technological data on connectors._**

**Role** : To access the technological data on connectors.

## Properties

### Property **AlignType**( ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the alignment type for this connector.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     objArg1 = objThisIntf.AlignType

```

### Property **AttributeNames**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Returns or sets a list of attribute names associated with this connector.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim ojArg1 As PspListOfBSTRs
      ...
     Set ojArg1 = objThisIntf.AttributeNames

```

### Property **ClockType**( ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the clocking type (how symmetric this end is) for this connector.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     objArg1 = objThisIntf.ClockType

```

### Property **FaceType**( ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the face type (normal or "transparent" support) for this connector.

**Parameters:**

` oFaceType`      The face type.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     Set objArg1 = objThisIntf.FaceType

```

Methods

### Func **GetAlignmentConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the Alignmnet connector.

**Parameters:**

` oCntr`      Alignment connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetAlignmentConnector

```

### Func **GetAlignmentDirection**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Retrieves the alignment direction outward normal to the face place position.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetAlignmentVector (objArg1)

```

### Func **GetConnectorMathPlane**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the 9 doubles values for plane contains the connector position (plane origin), alignment direction (plane z-axis), and the up direction (plane y-axis). Nine double values stand for plane origin, and the two normalized vectors

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetConnectorMathPlane (objArg1)

```

### Func **GetDatumConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the Datum connector.

**Parameters:**

` oCntr`      Orientation connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetDatumConnector

```

### Func **GetFaceConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the face connector.

**Parameters:**

` oCntr`      Face connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetFaceConnector

```

### Func **GetOrientationConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Get Orientation connector.

**Parameters:**

` oCntr`      Orientation connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetOrientationConnector

```

### Func **GetPosition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the Position of the connector.

**Parameters:**

` iRelAxis`      The relative axis object (NULL means relative to parent).
` oPosition`      X-Y-Z coordinates of the part connector Three double values stand for x,y,z coordinates

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetPosition (objArg1 )

```

### Func **GetUpDirection**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the UP direction of the connector.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).
` oUpDirection`      The connector face plane.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetUpDirection (objArg1)

```

### Sub **SetAlignmentConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAlignCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieAlignType`)

   Sets the Face connector.

**Parameters:**

` iAlignCntr`      Alignment connector
` ieAlignType`      Alignment connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetFaceConnector objArg1, objArg2

```

### Sub **SetDatumConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDatumCntr`)

   Sets the Datum connector.

**Parameters:**

` iDatumCntr`      Datum connector.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     objThisIntf.SetDatumConnector objArg1

```

### Sub **SetFaceConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieFaceType`)

   Sets Face connector.

**Parameters:**

` iFaceCntr`      Face connector
` ieFaceType`      Face connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetFaceConnector objArg1, objArg2

```

### Sub **SetOrientationConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOrientCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieOrientation`)

   Sets Face connector.

**Parameters:**

` iOrientCntr`      Alignment connector
` ieOrientation`      Orientation connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetOrientationConnector objArg1, objArg2

```

---

# PspPhsyicalProduct (Object)

**_Represents the interface to manage the technological connectors on physical objects._**

**Role** : To manage connectors on physical objects.

## Properties

### Property **Connectors**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Part connectors of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct
     Dim objArg1 As PspListOfObjects
      ...
     Set objArg1 = objThisIntf.Connectors

```

Methods

### Func **AddConnector**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClassFilter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieFaceType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAlignmentCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieAlignType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iClockCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieClockType`) As [CATIAPspPartConnector](../CATPlantShipInterfaces/interface_PspPartConnector_55256.md)

   Returns the added connector on the object.

**Parameters:**

` iuClassFilter`      Connector class type. If null string application default connector class will be used.
` iFaceCntr`      A face connector
` ieFaceType`      Face connector type
` iAlignmentCntr`      An alignment connector
` ieAlignType`      Alignment connector type
` iClockCntr`      A clock connector
` ieClockType`      A clock connector type

**Returns:**      Part connector added  **Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct

     Dim strVar1 As CATBSTR
     Dim objArg2 As Reference
     Dim objArg3 As catPspIDLPartConnectorType
     Dim objArg4 As Reference
     Dim objArg5 As catPspIDLPartConnectorType
     Dim objArg6 As Reference
     Dim objArg7 As catPspIDLPartConnectorType
     Dim objArg8 As PspPartConnector
      ...
     objArg8 = objThisIntf.AddConnector (strVar1, objArg2,objArg3,objArg4, objArg5,objArg6,objArg7 )

```

### Sub **RemoveConnector**( [CATIAPspPartConnector](../CATPlantShipInterfaces/interface_PspPartConnector_55256.md)  `iCntrToRemove`)

   Removes part connector.

**Parameters:**

` iCntrToRemove`      Part connector to be removed

**Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct

     Dim objArg1 As PspPartConnector
      ...
     objThisIntf.RemoveConnector objArg1

```

---

# PspPhysical (Object)

**_Represents the object to access Plant Ship physical object information._**

**Role** : To access access Plant Ship physical object information.

## Methods

### Func **GetFunctional**( ) As [CATIAPspFunctional](../CATPlantShipInterfaces/interface_PspFunctional_36800.md)

   Returns the Function object.

**Returns:**      Functional object associated with the physical object  **Example:**

```VBScript
     Dim objThisIntf As PspPhysical
     Dim objArg1 As PspFunctional
      ...
     Set objArg1 = objThisIntf.GetFunctional

```

### Func **GetSpatial**( ) As [CATIAPspSpatial](../CATPlantShipInterfaces/interface_PspSpatial_21700.md)

   Returns the Spatial object.

**Returns:**      Spatial object associated with the physical object  **Example:**

```VBScript
     Dim objThisIntf As PspPhysical
     Dim objArg1 As PspSpatial
      ...
     Set objArg1 = objThisIntf.GetSpatial

```

---

# PspPlacePart (Object)

**_Represents the Place physical parts object._**

**Role** : To place physical parts.

## Properties

### Property **ErrorMessage**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the message associated with the last error.

**Role** : If an error occurs when placing or routing a part, a message is associated with the error.

**Returns:**      The error message associated with the last error. Null if no error.  Methods

### Func **PlacePartInSpace**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuFunctionType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiReferencePart`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiParentProduct`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiLogicalLine`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPlacedPartID`,  [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)  `iUpDirection`,  [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)  `iHorizontalOrientation`,  [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Places a part in space.

**Role** : The part instance is placed given its reference with respect to its parent product. The Part Placement engine will not perform any of it's normal checks for interactions with nearby parts. Part is placed non-spec.

**Parameters:**

` iuStandard`      The standard for application attribute values.
` iuFunctionType`      The type of function (e.g. block valve, branch). Used when no function is specified but functional part placement is required.
` ipiReferencePart`      The reference part from which to derive the instance part.
` ipiParentProduct`      The parent product (in the design model) for the new instance part.
` ipiLogicalLine`      The logical line (e.g. piping line) which contains the instance part.
` iuPlacedPartID`      The name of the placed part in the design model. Null uses the standard ID generated by the part placement engine.
` iUpDirection`      The up direction for the placed part. The list has three values which represent the x, y and z values of a unit direction vector. Value is relative to ipiParentProduct.
` iHorizontalOrientation`      The orientation of the part in "horizontal" plane (plane perpendicular to up direction). Must be perpendicular to iUpDirection. The list has three values which represent the x, y and z values of a unit direction vector. Value is relative to ipiParentProduct.
` iPosition`      The position of the part. The list has three values which represent the x, y and z values of a position in space. Value is relative to ipiParentProduct and expressed in millimeters.

**Returns:**      The placed instance part.  
### Func **RouteStringPartInSpace**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuFunctionType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiReferencePart`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiParentProduct`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ipiLogicalLine`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPlacedPartID`,  [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)  `iFirstPointUpDirection`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `ipiListPoints`,  [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)  `iListBendRadii`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Routes a string part.

**Role** : The string part instance, such as a pipe, a tube, or a duct, is placed given its reference with respect to its parent product. The Part Placement engine will not perform any of it's normal checks for interactions with nearby parts. Part is placed non-spec.

**Parameters:**

` iuStandard`      The standard for application attribute values.
` iuFunctionType`      The type of function (e.g. Block valve, branch). Used when no function is specified but functional part placement is required.
` ipiReferencePart`      The reference part from which to derive the instance part.
` ipiParentProduct`      The parent product (in the design model) for the new instance part.
` ipiLogicalLine`      The logical line (e.g. piping line) which contains the instance part.
` iuPlacedPartID`      The name of the placed part in the design model. Null uses the standard ID generated by the part placement engine.
` iFirstPointUpDirection`      The up direction of the first point of the string part. The list has three values which represent the x, y and z values of a unit direction vector. Value is relative to ipiParentProduct.
` ipiListPoints`      The list of points that describe the path of the string. If the string part is stretchable, the list should contain two points.
` iListBendRadii`      The list of bend radii at each corner of the string part. This list is ignored if the string part is stretchable. This list is only for interior points and so should have two less elements than ipiListPoints. (for example, if ipiListPoints has six points, iListBendRadii should have four radii values). Values are in milimeters.

**Returns:**      The routed string part.

---

# PspResource (Object)

**_Represents the PspResource._**

**Role** : It is used to get application resources.

## Methods

### Func **GetResourcePath**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iResourceName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the path value defined for a resource.

**Parameters:**

` iResourceName`      Resource Name

**Returns:**      Resource Path  **Example:**

```VBScript
     Dim objThisIntf As PspResource
     Dim strResourcePath As String
     Dim iResourceName As String

      ...
     strResourcePath = objThisIntf.GetResourcePath (iResourceName)

```

### Func **GetResourceValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iResourceName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the value defined for a resource.

**Parameters:**

` iResourceName`      Resource Name

**Returns:**      Resource Value  **Example:**

```VBScript
     Dim objThisIntf As PspResource
     Dim strResourceVal As String
      ...
     strResourceVal = objThisIntf.GetResourceValue (iResourceName)

```

---

# PspSpatial (Object)

**_Represents the Psp Spatial object._**

**Role** : To access Plant Ship spatial object information.

## Properties

### Property **Physicals**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns all physical objects associated to this spatial object.

**Example:**

```VBScript
     Dim objThisIntf As PspSpatial
     Dim objArg1 As CATIAPspListOfObjects
      ...
     Set objArg1 = objThisIntf.Physicals

```

---

# PspStretchableData (Object)

**_Represents the PspStretchableData object._**

**Role** : To access the technological data on stretchable objects.

## Methods

### Func **ListBendData**( ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the bend radii.

**Returns:**      List of bend radius.  **Example:**

```VBScript
     Dim objThisIntf As PspStretchableData
     Dim objArg1 As PspListOfDoubles
      ...
     Set objArg1 = objThisIntf.ListBendData

```

### Func **ListDefinitionPoints**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the points defining the object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).

**Returns:**      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.  **Example:**

```VBScript
     Dim objThisIntf As PspStretchableData
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.ListDefinitionPoints (objArg1)

```

---

# PspTempListFactory (Object)

**_Create temporary (non-persistent) lists to be used in VB environment._**

**Role** : Create lists in VB environment.

## Methods

### Func **CreateListOfBSTRs**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Returns a new empty list of strings.

**Returns:**      a empty list of strings.  **Example:**      This example illustrates how to create a new empty list of strings.

```VBScript
     Dim PspListFact As PspTempListFactory
     Dim NewList As PspListOfBSTRs
     Set NewList = PspListFact.CreateListOfBSTRs

```

### Func **CreateListOfDoubles**( ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns a new empty list of doubles.

**Returns:**      a empty list of doubles.  **Example:**      This example illustrates how to create a new empty list of doubles.

```VBScript
     Dim PspListFact As PspTempListFactory
     Dim NewList As PspListOfDoubles
     Set NewList = PspListFact.CreateListOfDoubles

```

### Func **CreateListOfLongs**( ) As [CATIAPspListOfLongs](../CATPlantShipInterfaces/interface_PspListOfLongs_41364.md)

   Returns a new empty list of long integers.

**Returns:**      a empty list of long integers.  **Example:**      This example illustrates how to create a new empty list of long integers.

```VBScript
     Dim PspListFact As PspTempListFactory
     Dim NewList As PspListOfLongs
     Set NewList = PspListFact.CreateListOfLongs

```

### Func **CreateListOfObjects**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

   Returns a new empty list of objects.

**Returns:**      a empty list of objects.  **Example:**      This example illustrates how to create a new empty list of objects.

```VBScript
     Dim PspListFact As PspTempListFactory
     Dim NewList As PspListOfObjects
     Set NewList = PspListFact.CreateListOfObjects

```

---

# PspWorkbench (Object)

**_Represents the PspWorkbench._**

**Role** : To manage application and Psp interface handlers. From this object all the queries for lists of Distributive system (PSP) objects can be made. Furthermore, all the interface handles can be obtained through this interface.

## Methods

### Sub **ExportProperties**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToExportFrom`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iXMLOutputFileName`)

   This method extracts property values of the current document to an output XML file. The format is determined by CATIA PlantShip XML-DTD file.

**Parameters:**

` iDocumentToExportFrom`      Documennt to export from
` iXMLOutputFileName`      The file name to output the data to.

**Example:**

```VBScript
     Dim objPspWorkbench As PspWorkbench
     Dim objCATIAV5CurDocument As Document
     Dim iXMLOutputFileName As String
     Set objCATIAV5CurDocument = CATIA.ActiveDocument
     Set objProductRoot = objCATIAV5CurDocument.Product
     Set objPspWorkbench = objProductRoot.GetTechnologicalObject ("PspWorkbench")
     ..
     objThisIntf.ExportProperties objCATIAV5CurDocument, iXMLOutputFileName

```

### Func **GetApplication**( [CatPspIDLApplicationID](../CATPlantShipInterfaces/enum_CatPspIDLApplicationID_94374.md)  `iApplicationID`) As [CATIAPspApplication](../CATPlantShipInterfaces/interface_PspApplication_42486.md)

   Returns the PspApplication associated with the input ApplicationID.

**Parameters:**

` CatPspIDLApplicationID`      Application ID to get.
` oApplication`      PspApplication handle found.

**Example:**

```VBScript
     Dim objPspWorkbench As PspWorkbench
     Dim objArg1 As CatPspIDLApplicationID
     Dim objArg2 As PspApplication
     objArg1 = catPspIDLCATPiping
     Set objArg2 = objPspWorkbench.GetApplication (objArg1)

```

### Func **GetInterface**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns specific interface handle on a given object.

**Parameters:**

` iInterfaceName`      interface name to search for ("CATIAxxxx")
` iObject`      The object to search for the required interface.

**Returns:**      Interface handle found  **Example:**      This example illustrates how to get a specific interface handle from a given object.

```VBScript
     Dim objPspWorkbench As PspWorkbench
     Dim objPspApplication As PspApplication
     Dim objPspAppFactory As PspAppFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objPspWorkbench = objProductRoot.GetTechnologicalObject ("PspWorkbench")
     Set objPspPipApplication = objPspWorkbench.GetApplication(catPspIDLCATPiping)

     Set objPspPipAppFactory = objPspWorkbench.GetInterface ("CATIAPspAppFactory",objPspPipApplication)

```