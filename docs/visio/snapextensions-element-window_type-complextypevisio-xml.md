---
title: SnapExtensions-Element (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Gibt an, ob eine bestimmte Einstellung für die Snap-Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist. Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
ms.openlocfilehash: b1cf16a59480c9a800309f4a8c1411dfba52f4dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598024"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>SnapExtensions-Element (Window_Type complexType) (Visio XML)

Gibt an, ob eine bestimmte Einstellung für die Snap-Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist. Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert des **SnapExtensions-Elements** kann eine Summe der Werte in der folgenden Tabelle sein. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |An Ausrichtungsfelderweiterung ausrichten.  <br/> |
|2  <br/> |Ausrichten an der Mittelachsenerweiterung.  <br/> |
|4   <br/> |An der Tangenserweiterung der Kurve ausrichten.  <br/> |
|8   <br/> |An Endpunkterweiterung ausrichten.  <br/> |
|16   <br/> |An Der Mitte der Erweiterung ausrichten.  <br/> |
|32  <br/> |An linearer Erweiterung ausrichten.  <br/> |
|64  <br/> |An Kurvenerweiterung ausrichten.  <br/> |
|128  <br/> |Ausrichten an der senkrechten Endpunkterweiterung.  <br/> |
|256  <br/> |An senkrechter Mittelpunkterweiterung ausrichten.  <br/> |
|512  <br/> |An horizontaler Endpunkterweiterung ausrichten.  <br/> |
|1024  <br/> |An der vertikalen Erweiterung des Endpunkts ausrichten.  <br/> |
|2048  <br/> |An Ellipse Center-Erweiterung ausrichten.  <br/> |
|4096  <br/> |Ausrichten an der Erweiterung für isometrische Winkel.  <br/> |
   

