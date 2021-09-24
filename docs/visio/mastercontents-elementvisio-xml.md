---
title: MasterContents-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Gibt Informationen zu den Formen in einem Master-Shape in einer Zeichnung an.
ms.openlocfilehash: 840ee05bf23e1fac70da62a0b3a3a534292f6002
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549630"
---
# <a name="mastercontents-element-visio-xml"></a>MasterContents-Element (Visio XML)

Gibt Informationen zu den Formen in einem Master-Shape in einer Zeichnung an. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
|[Formen](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **Shape-Elementen.**  <br/> |
   
### <a name="attributes"></a>Attribute

Keine.
  

