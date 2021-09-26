---
title: ValidationProperties-Element (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Kapselt die Eigenschaften, die sich auf die Überprüfung des Dokuments beziehen.
ms.openlocfilehash: c6608a723a689e958e4a4858753055480fb6d2f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627191"
---
# <a name="validationproperties-element-validation_type-complextype-visio-xml"></a>ValidationProperties-Element (Validation_Type complexType) (Visio XML)

Kapselt die Eigenschaften, die sich auf die Überprüfung des Dokuments beziehen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Speichert Informationen zur Diagrammüberprüfung des Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |xsd:dateTime  <br/> |Erforderlich  <br/> |Datum und Uhrzeit der letzten Überprüfung des Dokuments.  <br/> |Werte des Typs "xsd:dateTime".  <br/> |
|ShowIgnored  <br/> |xsd:boolean  <br/> |erforderlich  <br/> |Gibt an, ob ignorierte Überprüfungsprobleme im Fenster "Probleme" angezeigt werden sollen.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
   

