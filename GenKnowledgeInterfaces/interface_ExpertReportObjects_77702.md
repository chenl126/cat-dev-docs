# ExpertReportObjects (Collection)

**_Represents the collection of (succeeded or failed) report objects._**

## Properties

### Property **CountFail**( ) As long (Read Only)

Returns the number of failed tuples in the failed tuples collection. It is redundant with [Collection.Count](../System/interface_Collection_22150.htm#Count) for [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collection. For [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collection, it will fail.

**Example:**      This example retrieves in `ObjectNumber` the number of tuples currently gathered in `MyCollection`.

```VBScript
ObjectNumber = MyCollection.CountFail

```

### Property **CountSucceed**( ) As long (Read Only)

Returns the number of succeeded tuples in the succeeded tuples collection. It is redundant with [Collection.Count](../System/interface_Collection_22150.htm#Count) for [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collection. For [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collection, it will fail.

**Example:**      This example retrieves in `ObjectNumber` the number of tuples currently gathered in `MyCollection`.

```VBScript
ObjectNumber = MyCollection.CountSucceed

```

Methods

### Func **FailItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

Retrieves a report failed component from a failed tuples collection, using its index or its name from the Check collection. It is redundant with [ExpertReportObjects.Item](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.htm#Item) for [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collections. For [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collections, it will fail.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

Retrieves a Report component using its index or its name from the Check collection.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component  
### Func **SucceedItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

Retrieves a report component from a succeeded tuples collection, using its index or its name from the Check collection. It is redundant with [ExpertReportObjects.Item](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.htm#Item) for [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collections. For [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collections, it will fail.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component