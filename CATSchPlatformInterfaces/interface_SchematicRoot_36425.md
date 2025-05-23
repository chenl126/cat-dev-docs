# SchematicRoot (Object)

**_Represents the top node of the schematic object tree._**
From this node all the queries for lists of schematic objects can be made. Furthermore, all the factories handles can be obtained through this interface.

## Methods

### Func **GetApplObjFactFromVirtualType**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iApplicationID`) As [CATIASchAppObjectFactory](../CATSchPlatformInterfaces/interface_SchAppObjectFactory_75566.md)

   Returns the object factory for specific schematic application.

**Example:**      This example illustrates how to get the object factory of user defined virtual type. User provides implementation to this type.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchObjFact As SchAppObjectFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchObjFact = objSchPlatformRoot.GetApplObjFactFromVirtualType("UserDefined")(

```

### Func **GetApplicationObjectFactory**( [CatSchIDLApplicationID](../CATSchPlatformInterfaces/enum_CatSchIDLApplicationID_93680.md)  `iApplicationID`) As [CATIASchAppObjectFactory](../CATSchPlatformInterfaces/interface_SchAppObjectFactory_75566.md)

   Returns the object factory for specific schematic application.

**Example:**      This example illustrates how to get the object factory of Piping and Instrumentation Diagram application.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchObjFact As SchAppObjectFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchObjFact = objSchPlatformRoot.GetApplicationObjectFactory("CatSchIDLCATPID")(

```

### Func **GetCompGroupFromCatalog**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCatalogEntryName`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iCtlgDoc`) As [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)

   Returns specific component group entry in a schematic component catalog document.

**Example:**      This example illustrates how to get a specific component group entry in a schematic component catalog document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchComponent As SchComponent
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Dim objCtlgDoc As Document
     Set objCtlgDoc = CATIA.Documents.Open ("Electrical_ANSI_PartFunctions.catalog")
     Set objSchComponent = objSchPlatformRoot.GetCompGroupFromCatalog ("JuncBox-TermBoard",objCtlgDoc)

```

### Func **GetCompSymbolFromCatalog**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCatalogEntryName`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iCtlgDoc`) As [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)

   Returns specific entry in a schematic component catalog document.

**Example:**      This example illustrates how to get a specific entry in a schematic component catalog document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchGRRComp As SchGRRComp
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Dim objCtlgDoc As Document
     Set objCtlgDoc = CATIA.Documents.Open ("PID_ANSI_Equipment.catalog")
     Set objSchGRRComp = objSchPlatformRoot.GetCompSymbolFromCatalog ("Blower",objCtlgDoc)

```

### Func **GetComponents**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Returns a list of schematic component instances under the root.

**Example:**      This example illustrates how to get the list of component instances from a schematic product document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchListComps As SchListOfObjects
     Set objoSchListComps = objSchPlatformRoot.GetComponents

```

### Func **GetDrawing**( ) As [CATIADrawingDrawing](../DraftingInterfaces/interface_DrawingRoot_26516.md)

   Retrieves the drawing root in the schematic document.

**Example:**      This example illustrates how to get the drawing of a schematic document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Dim objDrawRoot As DrawingRoot
     Set objDrawRoot = objSchPlatformRoot.GetDrawing

```

### Func **GetDrawingStandard**( ) As [CatDrawingStandard](../DraftingInterfaces/enum_CatDrawingStandard_67878.md)

   Get the drawing standard.

**Example:**      This example illustrates how to get the drafting standard of a schematic document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchLSymbols As SchListOfObjects
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     oDrwStd = objSchPlatformRoot.GetDrawingStandard

```

### Func **GetInterface**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns specific interface handle on a given object.

**Example:**      This example illustrates how to get a specific interface handle from a given object.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchObjFact As SchAppObjectFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchObjFact = SchPlatformRoot.GetApplicationObjectFactory("CatSchIDLCATPID")
     Set objSchObjFact2 = objSchPlatformRoot.GetInterface ("CATIASchAppObjectFactory2",SchObjFact)

```

### Func **GetRefComponents**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Returns a list of schematic component references under the root.

**Example:**      This example illustrates how to get the list of component references from a schematic product document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchListComps As SchListOfObjects
     Set objSchListComps = objSchPlatformRoot.GetRefComponents

```

### Func **GetRoutes**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Returns a list of schematic routes under the root.

**Example:**      This example illustrates how to get the list of routes from a schematic product document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchListRoutes As SchListOfObjects
     Set objSchListRoutes = objSchPlatformRoot.GetRoutes

```

### Func **GetSchBaseFactory**( ) As [CATIASchBaseFactory](../CATSchPlatformInterfaces/interface_SchBaseFactory_41394.md)

   Returns schematic base object factory.

**Example:**      This example illustrates how to get the schematic base factory.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchBaseFact As SchBaseFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchBaseFact = objSchPlatformRoot.GetBaseFactory

```

### Func **GetSchematicSession**( ) As [CATIASchSession](../CATSchPlatformInterfaces/interface_SchSession_21988.md)

   Returns the schematic session the document containing the root is associated with.

**Example:**      This example illustrates how to get the schematic session.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchSession As SchSession
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchSession = objSchPlatformRoot.GetSession

```

### Func **GetTemporaryListFactory**( ) As [CATIASchTempListFactory](../CATSchPlatformInterfaces/interface_SchTempListFactory_68916.md)

   Returns the factory to create lists of various types. These lists will not be saved with the model.

**Example:**      This example illustrates how to get the list factory from a schematic product document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchList As SchTempListFactory
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchList = objSchPlatformRoot.GetTemporaryListFactory

```

### Func **GetUnassociatedSymbols**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Returns a list of unassociated symbol.

**Example:**      This example illustrates how to get a list of unassociated symbol.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchLSymbols As SchListOfObjects
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     Set objSchLSymbols = objSchPlatformRoot.GetUnassociatedSymbols

```

### Sub **SetDrawingStandard**( [CatDrawingStandard](../DraftingInterfaces/enum_CatDrawingStandard_67878.md)  `iDrwStd`)

   Set the drawing standard.

**Example:**      This example illustrates how to set the drafting standard of a schematic document.

```VBScript
     Dim objSchPlatformRoot As SchematicRoot
     Dim objSchLSymbols As SchListOfObjects
     Dim objProductRoot As Product
     Set objProductRoot = CATIA.ActiveDocument.Product
     Set objSchPlatformRoot = objProductRoot.GetTechnologicalObject ("SchematicRoot")
     objSchPlatformRoot.SetDrawingStandard catISO

```