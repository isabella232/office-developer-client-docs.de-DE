---
title: RuleInfo-Element (Issue_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797937"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>RuleInfo-Element (Issue_Type ComplexType) ("Visio XML")

Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Problem](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Stellt ein einzelnes Überprüfungsproblem im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Regel-ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Überprüfungsregel, die für das übergeordnete Problem relevant ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|RuleSetID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der der Überprüfungsregel, die für das übergeordnete Problem relevant ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

