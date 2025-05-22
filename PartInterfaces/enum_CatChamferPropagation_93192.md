# CatChamferPropagation (Enumeration)

**_Chamfer propagation mode._**
Once running on an egde, a chamfer operation may propagate onto other edges that extend the first one. This mode controls the chamfer ability to do so.

**Values:**

` catTangencyChamfer`      The chamfer operation also chamfers any other edges found at the first edge extremities, as long as they are tangent with it. This process repeats until no more tangent edges to chamfer are found at extremities of already chamfered ones.
` catMinimalChamfer`      The chamfer operation stops as soon as an edge to chamfer cuts one or the two chamfer created edges