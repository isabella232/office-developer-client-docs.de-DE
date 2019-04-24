---
title: SnapSettings-Element (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Gibt die Objekte an, bei denen die Formen einrasten, wenn Snap im Fenster aktiv ist.
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334489"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>SnapSettings-Element (DocumentSettings_Type complexType) (' Visio XML ')

Gibt die Objekte an, bei denen die Formen einrasten, wenn Snap im Fenster aktiv ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>Bemerkungen

Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |An Linealen ausrichten.  <br/> |
|2  <br/> |Am Raster ausrichten.  <br/> |
|4  <br/> |An Führungslinien ausrichten.  <br/> |
|8  <br/> |An Auswahlpunkten ausrichten.  <br/> |
|16  <br/> |An Scheitelpunkten ausrichten.  <br/> |
|32  <br/> |An Verbindungspunkten ausrichten.  <br/> |
|256  <br/> |An sichtbaren Kanten von Formen ausrichten.  <br/> |
|512  <br/> |An Ausrichtungsfeld ausrichten.  <br/> |
|1024  <br/> |An Optionen für Shape-Erweiterungen ausrichten.  <br/> |
|32768  <br/> |Snap deaktiviert.  <br/> |
|65536  <br/> |An Schnittpunkten ausrichten.  <br/> |
   

