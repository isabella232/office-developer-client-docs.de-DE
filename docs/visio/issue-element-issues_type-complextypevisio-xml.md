---
title: Issue-Element (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Überprüfungsproblem im Dokument dar.
ms.openlocfilehash: 5c4dd15cc86f22fb465b4b2a1856ec46802d7fdc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570379"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a>Issue-Element (Issues_Type complexType) (Visio XML)

Stellt ein einzelnes Überprüfungsproblem im Dokument dar.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Enthält alle **Issue-Elemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[IssueTarget](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |Gibt abhängig vom Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder die Seite und das Shape an, die dem übergeordneten Überprüfungsproblem zugeordnet sind.  <br/> |
|[RuleInfo](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Überprüfungsproblems an.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Ignoriert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
   

