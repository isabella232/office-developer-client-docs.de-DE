---
title: Rule-Element (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541708"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a>Rule-Element (RuleSet_Type complexType) (Visio XML)

Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Stellt einen Satz von Diagrammüberprüfungsregeln dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob die Gültigkeitsprüfungsregel auf ein Zielobjekt angewendet werden soll.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob das Zielobjekt der Gültigkeitsprüfungsregel entspricht.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kategorie  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Text an, der in der **Spalte Kategorie** des Fensters Probleme angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Beschreibung  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt die Beschreibung der Überprüfungsregel an, die auf der Benutzeroberfläche angezeigt wird. Der Standardwert ist "Unknown".  <br/> |Werte des xsd:string-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner für die Gültigkeitsprüfungsregel an.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Ignoriert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Gültigkeitsprüfungsregel derzeit ignoriert wird. Der Standardwert ist False.  <br/> |Werte des typs xsd:boolean.  <br/> |
|NameU  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den universellen Namen der Gültigkeitsprüfungsregel an.  <br/> |Werte des xsd:string-Typs.  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt den Objekttyp an, auf den die Überprüfungsregel angewendet wird.  <br/> |Werte des xsd:int-Typs.  <br/> |
   

