# Material (Object)

**_Represents a Material object._**

## Properties

### Property **AnalysisMaterial**( ) As [CATIAAnalysisMaterial](../CATMatInterfaces/interface_AnalysisMaterial_54904.md) (Read Only)

Returns the analysis material object from the current material.  
### Property **RenderingMaterial**( ) As [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md) (Read Only)

Returns the rendering material object from the current material.  Methods

### Sub **CopyRenderingDataFrom**( [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md)  `iRenderingMaterial`)

Copy rendering data from a material to the current material.  
### Func **CreateAnalysisData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAAnalysisMaterial](../CATMatInterfaces/interface_AnalysisMaterial_54904.md)

Create a default analysis material on the current material.  
### Func **CreateRenderingData**( ) As [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md)

Create a default rendering material on the current material.  
### Func **ExistAnalysisData**( ) As short

Returns true if a analysis material exists on the current material.  
### Func **ExistRenderingData**( ) As short

Returns true if a rendering material exists on the current material.  
### Sub **GetIcon**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Write the icon of a material to disc. The parameter is the path of the folder where the JPEG is going to be written Ex : E:\folder\  
### Sub **PutIcon**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Read the icon of a material from JPEG file. The parameter is the path of the folder where the JPEG is going to be read Ex : E:\folder\