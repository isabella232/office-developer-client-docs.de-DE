---
title: RuleFilter-Element (Rule_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797929"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a>RuleFilter-Element (Rule_Type ComplexType) ("Visio XML")

Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Formel  <br/> |XSD: String  <br/> |Optional  <br/> |Formel für das Element darstellt.  <br/> |Die Werte für die XSD: String.  <br/> |
   

