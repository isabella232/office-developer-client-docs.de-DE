---
title: HeaderFooterFont-Element (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541085"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>HeaderFooterFont-Element (HeaderFooter_Type complexType) (Visio XML)

Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Enthält Elemente für die Kopf-und Fußzeile eines Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt den Zeichensatz der Schriftart an. Entspricht dem GDI-LOGFONTlfCharSet-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|ClipPrecision  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt die Clipping-Genauigkeit der Schriftart an. Entspricht dem GDI-LOGFONTlfClipPrecision-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Hemmung  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt das Escapement-Attribut der Schriftart an. Entspricht dem GDI-LOGFONTlfEscapement-Feld.  <br/> |Werte des Typs XSD: int.  <br/> |
|FaceName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Enthält Informationen zu einer Schriftart.  <br/> |Werte des Typs XSD: String.  <br/> |
|Height  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Höhe der Form in Zeichnungseinheiten an.  <br/> |Werte des Typs XSD: int.  <br/> |
|Kursiv  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart kursiv formatiert ist. Entspricht dem GDI-LOGFONTlfItalic-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Orientierung  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Ausrichtung der Schriftart an. Entspricht dem GDI-LOGFONTlfOrientation-Feld.  <br/> |Werte des Typs XSD: int.  <br/> |
|OutPrecision  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt das Ausgabe Genauigkeits Attribut der Schriftart an. Entspricht dem GDI-LOGFONTlfOutPrecision-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|PitchAndFamily  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt die Tonhöhe und die Schriftfamilie der Schriftart an. Entspricht dem GDI-LOGFONTlfPitchAndFamily-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Quality  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt die Ausgabequalität der Schriftart an. Entspricht dem GDI-LOGFONTlfQuality-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Durchgestrichen  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart eine durchgestrichen Schriftart ist. Entspricht dem GDI-LOGFONTlfStrikeOut-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Unterstrichen  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart unterstrichen ist. Entspricht dem GDI-LOGFONTlfUnderline-Feld.  <br/> |Werte des XSD: unsignedByte-Typs.  <br/> |
|Schriftbreite  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Gewichtung der Schriftart an. Entspricht dem GDI-LOGFONTlfWeight-Feld.  <br/> |Werte des Typs XSD: int.  <br/> |
|Width  <br/> |XSD: int  <br/> |Optional  <br/> |Enthält die Breite der zugeordneten Form in Zeichnungseinheiten.  <br/> |Werte des Typs XSD: int.  <br/> |
   

