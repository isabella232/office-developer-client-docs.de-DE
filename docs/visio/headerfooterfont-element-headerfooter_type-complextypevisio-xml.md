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
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>HeaderFooterFont-Element (HeaderFooter_Type complexType) (Visio XML)

Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt den Zeichensatz der Schriftart an. Entspricht dem Feld GDI LOGFONTlfCharSet.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt die Zuschneidegenauigkeit der Schriftart an. Entspricht dem Feld GDI LOGFONTlfClipPrecision.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt das escapement-Attribut der Schriftart an. Entspricht dem GDI LOGFONTlfEscapement-Feld.  <br/> |Werte des xsd:int-Typs.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |Optional  <br/> |Enthält Informationen zu einer Schriftart.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Height  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Höhe der Form in Zeichnungseinheiten an.  <br/> |Werte des xsd:int-Typs.  <br/> |
|Kursiv  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart italisch ist. Entspricht dem GDI LOGFONTlfItalic-Feld.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|Orientierung  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Ausrichtung der Schriftart an. Entspricht dem Feld GDI LOGFONTlfOrientation.  <br/> |Werte des xsd:int-Typs.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt das Ausgabegenauigkeitsattribut der Schriftart an. Entspricht dem Feld GDI LOGFONTlfOutPrecision.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt die Tonhöhe und Familie der Schriftart an. Entspricht dem GDI LOGFONTlfPitchAndFamily-Feld.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|Qualität  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt die Ausgabequalität der Schriftart an. Entspricht dem Feld GDI LOGFONTlfQuality.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob es sich bei der Schriftart um eine Streichschriftart handelt. Entspricht dem Feld GDI LOGFONTlfStrikeOut.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|Unterstrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart unterstrichen ist. Entspricht dem GDI LOGFONTlfUnderline-Feld.  <br/> |Werte des xsd:unsignedByte-Typs.  <br/> |
|Schriftbreite  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Gewichtung der Schriftart an. Entspricht dem Feld GDI LOGFONTlfWeight.  <br/> |Werte des xsd:int-Typs.  <br/> |
|Width  <br/> |xsd:int  <br/> |Optional  <br/> |Enthält die Breite der zugeordneten Form in Zeichnungseinheiten.  <br/> |Werte des xsd:int-Typs.  <br/> |
   

