# CatDistanceComputationType (Enumeration)

**_The different types of clash computation._**
It is used by the [Distance](../SpaceAnalysisInterfaces/interface_Distance_13954.md) object to specify the computation type.

**Values:**

` catDistanceComputationTypeInsideOne`      The computation tests each product of the selection/group against all other products in the same selection.
` catDistanceComputationTypeAgainstAll`      The computation tests each product in the defined selection/group against all other products in the document.
` catDistanceComputationTypeBetweenTwo`      The computation tests each product in the first selection/group against all products in the second group.