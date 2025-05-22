# AnalysisImport (Object)

**_The interface to access a CATIAAnalysisExport_**

## Methods

### Sub **AddSupport**( [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductSupport`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iSupport`)

AddSupport for loads import if needed.
)

**Parameters:**

` iManager`      The Analysis manager.
)
` iProductSupport`      Product of the geometrical support.
)
` iSupports`      Geometrical support.
)

### Sub **ImportDisp**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iFatherCase`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFullPath`,  [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAxis`)

Import displacements from a CATAnalysisExport file.
)

**Parameters:**

` iFatherCase`      case where Displacements will be exported.
)
` iFullPath`      The full path of the file.
)
` iManager`      analysis manager where the disp is exported.
)
` iAxis`      The user axis system to be taken into account.
)

### Sub **ImportForce**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iFatherCase`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFullPath`,  [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAxis`)

Import loads from a CATAnalysisExport file.
)

**Parameters:**

` iFatherCase`      case where loads will be exported.
)
` iFullPath`      The full path of the file.
)
` iManager`      analysis manager where the disp is exported.
)
` iAxis`      The user axis system to be taken into account.
)