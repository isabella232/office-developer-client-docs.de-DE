---
title: Rule-Element (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: f3794d59aedab9a79d39cc2868845df48eb6702e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598283"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Stellt einen Satz von Regeln für die Diagrammüberprüfung dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob die Überprüfungsregel auf ein Zielobjekt angewendet werden soll.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob das Zielobjekt der Gültigkeitsprüfungsregel entspricht.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kategorie  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Text an, der in der Spalte **Kategorie** des Fensters Probleme angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Beschreibung  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt die Beschreibung der Überprüfungsregel an, die auf der Benutzeroberfläche angezeigt wird. Der Standardwert ist "Unbekannt".  <br/> |Werte des Typs "xsd:string".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner für die Gültigkeitsprüfungsregel an.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Ignoriert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Überprüfungsregel derzeit ignoriert wird. Der Standardwert ist False.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|NameU  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den universellen Namen der Gültigkeitsprüfungsregel an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt den Objekttyp an, auf den die Gültigkeitsprüfungsregel angewendet wird.  <br/> |Werte des Typs "xsd:int".  <br/> |
   

