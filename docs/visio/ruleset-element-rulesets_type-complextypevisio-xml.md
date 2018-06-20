---
title: RuleSet-Element (RuleSets_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt eine Reihe von Diagramm-Validierungsregeln dar.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797954"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>RuleSet-Element (RuleSets_Type ComplexType) ("Visio XML")

Stellt eine Reihe von Diagramm-Validierungsregeln dar.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Enthält ein **RuleSet** -Element für jeden überprüfungsregelsatz im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Gibt Regelsatz-Eigenschaften.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Beschreibung  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt die Beschreibung, die in der Benutzeroberfläche für die Überprüfungsregel angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des Typs xsd: String.  <br/> |
|Aktiviert  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Regeln in der angegebenen Regelsatz überprüft werden, wenn Validierung für das aktuelle Dokument ausgelöst wird. Standardwert ist True.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der der Überprüfungsregel.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den lokalen Namen der der Überprüfungsregel an. Der Standardwert ist NameU-Attributwert.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt den universellen Namen eines der Überprüfungsregel an.  <br/> |Werte des Typs xsd: String.  <br/> |
   

