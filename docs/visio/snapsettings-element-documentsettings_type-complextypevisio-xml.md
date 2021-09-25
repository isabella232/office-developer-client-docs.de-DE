---
title: SnapSettings-Element (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Gibt die Objekte an, an denen Shapes angedockt werden, wenn die Ausrichtung im Fenster aktiv ist.
ms.openlocfilehash: 01fdc54a559b43baefbdbdfa436c3281b919bd65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553795"
---
# <a name="snapsettings-element-documentsettings_type-complextype-visio-xml"></a>SnapSettings-Element (DocumentSettings_Type complexType) (Visio XML)

Gibt die Objekte an, an denen Shapes angedockt werden, wenn die Ausrichtung im Fenster aktiv ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |An Linealunterteilungen ausrichten.  <br/> |
|2  <br/> |Am Raster ausrichten.  <br/> |
|4   <br/> |An Führungslinien ausrichten.  <br/> |
|8   <br/> |An Auswahlpunkten ausrichten.  <br/> |
|16   <br/> |An Scheitelpunkten ausrichten.  <br/> |
|32  <br/> |An Verbindungspunkten ausrichten.  <br/> |
|256  <br/> |An sichtbaren Rändern von Formen ausrichten.  <br/> |
|512  <br/> |Am Ausrichtungsfeld ausrichten.  <br/> |
|1024  <br/> |An Optionen für Shape-Erweiterungen ausrichten.  <br/> |
|32768  <br/> |Ausrichten deaktiviert.  <br/> |
|65536  <br/> |An Schnittpunkten ausrichten.  <br/> |
   

