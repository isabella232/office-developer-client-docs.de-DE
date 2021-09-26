---
title: RuleFilter-Element (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Gibt den logischen Ausdruck an, der bestimmt, ob die Überprüfungsregel auf ein Zielobjekt angewendet werden soll.
ms.openlocfilehash: 261cd934d0350a9e045f4795c5b5ce58464eb742
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627576"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a>RuleFilter-Element (Rule_Type complexType) (Visio XML)

Gibt den logischen Ausdruck an, der bestimmt, ob die Überprüfungsregel auf ein Zielobjekt angewendet werden soll.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Formel  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt die Formel des Elements dar.  <br/> |Werte des xsd:string-Werts.  <br/> |
   

