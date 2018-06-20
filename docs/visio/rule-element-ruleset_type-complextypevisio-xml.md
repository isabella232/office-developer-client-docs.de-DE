---
title: Rule-Element (RuleSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797934"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Rule-Element (RuleSet_Type ComplexType) ("Visio XML")

Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Regelsatz](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Stellt eine Reihe von Diagramm-Validierungsregeln dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck, der bestimmt, ob das Zielobjekt der Überprüfungsregel erfüllt.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kategorie  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den Text in der **Kategorie** -Spalte der Problemfenster angezeigt. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des Typs xsd: String.  <br/> |
|Beschreibung  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt die Beschreibung der Überprüfungsregel, die in der Benutzeroberfläche angezeigt wird. Der Standardwert lautet "Unknown".  <br/> |Werte des Typs xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner für die Überprüfungsregel.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Ignoriert  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Überprüfungsregel derzeit ignoriert wird. Standard ist False.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|NameU  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt den universellen Namen der Überprüfungsregel.  <br/> |Werte des Typs xsd: String.  <br/> |
|RuleTarget  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt den Typ des Objekts an die der Überprüfungsregel angewendet wird.  <br/> |Werte des Typs xsd: int.  <br/> |
   

