---
title: pp-Element (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Gibt den Anfang der Ausführung von Absatzeigenschaften an. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 051650db1aa1d0bcf109bdca63d0909f94fb9479
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598416"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a>pp-Element (Text_Type complexType) (Visio XML)

Gibt den Anfang der Ausführung von Absatzeigenschaften an. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Enthält den Text einer Form.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Der Index  des Para-Elements, das die Formatierung angibt, die auf diese Ausführung angewendet wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

