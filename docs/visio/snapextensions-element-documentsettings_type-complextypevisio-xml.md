---
title: SnapExtensions-Element (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334531"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions-Element (DocumentSettings_Type complexType) (' Visio XML ')

Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
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

Der Wert des **SnapExtensions** -Elements kann eine Summe der Werte in der folgenden Tabelle sein. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |Ausrichtungsfeld Erweiterung.  <br/> |
|2  <br/> |An der Mittelachse anDocken.  <br/> |
|4  <br/> |An Kurventangenten Erweiterung ausrichten.  <br/> |
|8  <br/> |An Endpunkt Erweiterung ausrichten.  <br/> |
|16  <br/> |AnDocken an Mittelpunkt.  <br/> |
|32  <br/> |An lineare Erweiterung ausrichten.  <br/> |
|64  <br/> |An Kurven Erweiterung ausrichten.  <br/> |
|128  <br/> |An Endpunkt senkrecht anDocken.  <br/> |
|256  <br/> |An Mittelpunkt senkrecht anDocken.  <br/> |
|512  <br/> |An Endpunkt horizontaler Durchwahl ausrichten.  <br/> |
|1024  <br/> |Ausrichtung an Endpunkt vertikaler Durchwahl.  <br/> |
|2048  <br/> |An Ellipse Center-Erweiterung ausrichten.  <br/> |
|4096  <br/> |An isometrische Winkel Erweiterung ausrichten.  <br/> |
   

