---
title: Rule-Element (RuleSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358800"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Rule-Element (RuleSet_Type complexType) (' Visio XML ')

Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Stellt einen Satz von Diagramm Validierungsregeln dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob die Validierungsregel auf ein Zielobjekt angewendet werden soll.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Gibt den logischen Ausdruck an, der bestimmt, ob das Zielobjekt der Validierungsregel entspricht.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kategorie  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den Text an, der in der Spalte **Kategorie** des Fensters Probleme angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des XSD: String-Typs.  <br/> |
|Beschreibung  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt die Beschreibung der Validierungsregel an, die auf der Benutzeroberfläche angezeigt wird. Der Standardwert ist "unknown".  <br/> |Werte des XSD: String-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner für die Validierungsregel an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Ignoriert  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Validierungsregel derzeit ignoriert wird. Der Standardwert ist False.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den universellen Namen der Validierungsregel an.  <br/> |Werte des XSD: String-Typs.  <br/> |
|RuleTarget  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt den Objekttyp an, auf den die Validierungsregel angewendet wird.  <br/> |Werte des XSD: int-Typs.  <br/> |
   

