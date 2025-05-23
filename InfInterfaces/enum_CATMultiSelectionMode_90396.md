# CATMultiSelectionMode (Enumeration)

**_Types of multi-selection._**

**Role** : This enum is used by the [Selection.SelectElement3](../InfInterfaces/interface_Selection_18040.htm#SelectElement3) method.

**Values:**

` CATMonoSel`      Multi-selection is not supported
` CATMultiSelTriggWhenSelPerf`      Multi-selection is supported (through a dedicated "Tools Palette" toolbar). The selection (through a trap for example) is triggered when the selection is performed.
The CTRL and SHIFT keys are not supported.
` CATMultiSelTriggWhenUserValidatesSelection`      Multi-selection is supported (through a dedicated "Tools Palette" toolbar). The selection (through a trap for example) is triggered when the user validates the selection.
The CTRL and SHIFT keys are supported.