---
title: RefBy-Element (Trigger_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572431"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a>RefBy-Element (Trigger_Type ComplexType) ("Visio XML")

Gibt einen Verweis auf eine Seite in der Zeichnung.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> ||
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.  <br/> |

   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt das ID-Attribut des einer Seite in der Zeichnung.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|T  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs xsd: String.  <br/> |
   

