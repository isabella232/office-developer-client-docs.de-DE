---
title: ValidationProperties-Element (Validation_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Die Eigenschaften, die im Zusammenhang mit dem Dokument Validierung kapselt.
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385221"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a>ValidationProperties-Element (Validation_Type ComplexType) ("Visio XML")

Die Eigenschaften, die im Zusammenhang mit dem Dokument Validierung kapselt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Prüfung](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Speichert Informationen zur Diagrammüberprüfung des Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |XSD: DateTime  <br/> |erforderlich  <br/> |Das Datum und die Uhrzeit, der das Dokument zuletzt überprüft wurde.  <br/> |Werte des Typs xsd: DateTime.  <br/> |
|ShowIgnored  <br/> |XSD: Boolean  <br/> |erforderlich  <br/> |Gibt an, ob für ignorierten Überprüfungsprobleme im Problemfenster angezeigt.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
   

