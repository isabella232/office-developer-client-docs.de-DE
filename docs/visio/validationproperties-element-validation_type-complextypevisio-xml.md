---
title: ValidationProperties-Element (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Kapselt die Eigenschaften, die im Zusammenhang mit der Überprüfung des Dokuments stehen.
ms.openlocfilehash: 35e6f3f13eecef826fdef0d664bba35fceb0e069
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538522"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a>ValidationProperties-Element (Validation_Type complexType) (Visio XML)

Kapselt die Eigenschaften, die im Zusammenhang mit der Überprüfung des Dokuments stehen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|LastValidated  <br/> |XSD: DateTime  <br/> |erforderlich  <br/> |Das Datum und die Uhrzeit, zu der das Dokument zuletzt überprüft wurde.  <br/> |Werte des Typs XSD: DateTime.  <br/> |
|ShowIgnored  <br/> |XSD: Boolean  <br/> |erforderlich  <br/> |Gibt an, ob ignorierte Überprüfungsprobleme im Fenster Probleme angezeigt werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
   

