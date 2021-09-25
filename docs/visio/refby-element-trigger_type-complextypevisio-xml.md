---
title: RefBy-Element (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
ms.openlocfilehash: 4b38c508b2c6d417ffbddbf1cfed9945050ce670
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565905"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a>RefBy-Element (Trigger_Type complexType) (Visio XML)

Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> ||
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio Datei neu zu berechnen.  <br/> |

   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt das ID-Attribut eines Zeichenblatts in der Zeichnung an.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|T  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

