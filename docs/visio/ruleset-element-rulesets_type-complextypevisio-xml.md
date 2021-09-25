---
title: RuleSet-Element (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt einen Satz von Regeln für die Diagrammüberprüfung dar.
ms.openlocfilehash: ab46da07b39a36bc34f21f73e155ac2e62af6d39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598269"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>RuleSet-Element (RuleSets_Type complexType) (Visio XML)

Stellt einen Satz von Regeln für die Diagrammüberprüfung dar.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Enthält ein **RuleSet-Element** für jeden Überprüfungsregelsatz im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Gibt Regelsatzeigenschaften an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Beschreibung  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt die Beschreibung an, die auf der Benutzeroberfläche für den Überprüfungsregelsatz angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Aktiviert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Regeln im angegebenen Überprüfungsregelsatz überprüft werden, wenn die Überprüfung für das aktuelle Dokument ausgelöst wird. Der Standardwert ist True.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Überprüfungsregelsatzes an.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den lokalen Namen des Überprüfungsregelsatzes an. Der Standardwert ist der NameU-Attributwert.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den universellen Namen des Überprüfungsregelsatzes an.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

