---
title: ValidationProperties-Element (Validation_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Kapselt die Eigenschaften, die im Zusammenhang mit der Validierung des Dokuments stehen.
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355958"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a>ValidationProperties-Element (Validation_Type complexType) (' Visio XML ')

Kapselt die Eigenschaften, die im Zusammenhang mit der Validierung des Dokuments stehen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Speichert Informationen zur Diagrammüberprüfung des Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |XSD: dateTime  <br/> |erforderlich  <br/> |Datum und Uhrzeit der letzten Validierung des Dokuments.  <br/> |Werte des XSD: dateTime-Typs.  <br/> |
|ShowIgnored  <br/> |XSD: Boolean  <br/> |erforderlich  <br/> |Gibt an, ob ignorierte Validierungsprobleme im Fenster Probleme angezeigt werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
   

