---
title: RuleInfo-Element (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356987"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>RuleInfo-Element (Issue_Type complexType) (' Visio XML ')

Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Problem](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Stellt ein einzelnes Validierungs Problem im Dokument dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Validierungsregel an, zu der das übergeordnete Problem gehört.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Regelsatz  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Validierungsregel Satzes an, zu dem das übergeordnete Problem gehört.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

