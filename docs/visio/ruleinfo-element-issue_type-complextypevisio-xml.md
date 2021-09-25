---
title: RuleInfo-Element (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.
ms.openlocfilehash: 367c678d14531bd9e9d5dc86956aeb0ff42757fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623019"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a>RuleInfo-Element (Issue_Type complexType) (Visio XML)

Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Problem](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Stellt ein einzelnes Überprüfungsproblem im Dokument dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Überprüfungsregel an, auf die sich das übergeordnete Problem bezieht.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|RuleSetID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Überprüfungsregelsatzes an, auf den sich das übergeordnete Problem bezieht.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

