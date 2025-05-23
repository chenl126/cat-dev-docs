# FreeParameter (Object)

**_Interface to access a CATIAFreeParameter._**

## Properties

### Property **InfRange**(| ) As double

   Returns or sets the inferior bound of the free parameter object. The optimization cannot escape those bounds.  
### Property **Parameter**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns or sets which parameter (CATIAParameter) is linked to this object. The parameter must be real.  
### Property **Step**( ) As double

   Returns or sets the initial step used by the optimisation to look for a better solution. This step is just a preliminary indication. It will vary during the optimisation process.  
### Property **SupRange**( ) As double

   Returns or sets the superior bound of the free parameter object. The optimization cannot escape those bounds.