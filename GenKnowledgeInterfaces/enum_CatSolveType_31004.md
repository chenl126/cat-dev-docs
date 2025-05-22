# CatSolveType (Enumeration)

**_Type for controlling the resolution in Knowledge Expert._**

An optimized resolution is a resolution taking into account only the objects modified since the previous resolution.

A complete resolution is a resolution starting from scratch : nothing from the past is taken into account.

**Values:**

` ManualSolveType`      0 : the complete resolution is not called when the part/product is updated.
` AutomaticOptimizedSolveType`      1 : the optimized resolution is called when the part/product is updated.
` AutomaticCompleteSolveType`      2 : the complete resolution is called when the part/product is updated.