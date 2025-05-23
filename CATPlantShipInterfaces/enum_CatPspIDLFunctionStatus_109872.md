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