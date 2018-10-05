---
title: SnapSettings-Element (DocumentSettings_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Gibt die Objekte, die Shapes einrasten, um beim Ausrichten aktiv in das Fenster ist.
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401678"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>SnapSettings-Element (DocumentSettings_Type ComplexType) ("Visio XML")

Gibt die Objekte, die Shapes einrasten, um beim Ausrichten aktiv in das Fenster ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>Hinweise

Der Wert kann die Summe der Werte in der folgenden Tabelle sein.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |Einteilung Lineal ausrichten.  <br/> |
|2  <br/> |Am Raster ausrichten.  <br/> |
|4  <br/> |An Führungslinien ausrichten.  <br/> |
|8  <br/> |An Auswahlpunkten ausrichten.  <br/> |
|16  <br/> |An Scheitelpunkten ausrichten.  <br/> |
|32  <br/> |An Verbindungspunkten ausrichten.  <br/> |
|256  <br/> |An sichtbaren Rändern von Shapes ausrichten.  <br/> |
|512  <br/> |An Ausrichtungsfeld ausrichten.  <br/> |
|1024  <br/> |An Optionen für Shape-Erweiterungen ausrichten.  <br/> |
|32768  <br/> |Snap deaktiviert.  <br/> |
|65536  <br/> |An Schnittpunkten ausrichten.  <br/> |
   

