# CatSectionClippingMode (Enumeration)

**_The different algorithmes used to computate the section result._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the section's computation mode.

**Values:**

` catSection_Software`      The section is software computed (the result is more precise but slower).
` catSection_OpenGL`      The section is computed by the graphic card (the result is faster but less precise).