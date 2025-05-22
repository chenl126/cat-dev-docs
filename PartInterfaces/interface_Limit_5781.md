# Limit (Object)

**_Represents the limit of a prism or a hole shape._**

**See also:**      [Prism](../PartInterfaces/interface_Prism_5871.md), [Hole](../PartInterfaces/interface_Hole_3612.md)

## Properties

### Property **Dimension**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns or sets the limit dimension. This property is valid for the offset limit mode only, that is when [CatLimitMode](../PartInterfaces/enum_CatLimitMode_29900.md) is set to `catOffsetLimit` .  
### Property **LimitMode**( ) As [CatLimitMode](../PartInterfaces/enum_CatLimitMode_29900.md)

Returns or sets the limit mode.  
### Property **LimitingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the limiting element. This property is valid when the limiting object is a surface or a plane, that is when [CatLimitMode](../PartInterfaces/enum_CatLimitMode_29900.md) is set to `catUpToSurfaceLimit` and `catUpToPlaneLimit`.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [Face](../MecModInterfaces/interface_Face_3398.md).