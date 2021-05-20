---
title: RuleSet-Element (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt einen Satz von Diagrammüberprüfungsregeln dar.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541638"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>RuleSet-Element (RuleSets_Type complexType) (Visio XML)

Stellt einen Satz von Diagrammüberprüfungsregeln dar.
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Enthält ein **RuleSet-Element** für jeden Überprüfungsregelsatz im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Gibt Eigenschaften für Regelsatz an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Beschreibung  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt die Beschreibung an, die auf der Benutzeroberfläche für den Überprüfungsregelsatz angezeigt wird. Der Standardwert ist eine leere Zeichenfolge.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Aktiviert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Regeln im angegebenen Überprüfungsregelsatz überprüft werden, wenn die Überprüfung für das aktuelle Dokument ausgelöst wird. Der Standardwert ist True.  <br/> |Werte des typs xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Überprüfungsregelsatzs an.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den lokalen Namen des Überprüfungsregelsatzs an. Standardmäßig wird der NameU-Attributwert verwendet.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den universellen Namen des Überprüfungsregelsatzs an.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

