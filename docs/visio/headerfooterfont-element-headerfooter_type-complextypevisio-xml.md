---
title: HeaderFooterFont-Element (HeaderFooter_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Gibt die Schriftart für den Text Kopf- und Fußzeile verwendet.
ms.openlocfilehash: 249040702b1594cc650ccf1304ed7c1c79581ea3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797130"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>HeaderFooterFont-Element (HeaderFooter_Type ComplexType) ("Visio XML")

Gibt die Schriftart für den Text Kopf- und Fußzeile verwendet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Enthält Elemente für Kopf- und Fußzeile eines Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt den Zeichensatz der Schriftart an. Entspricht dem Feld GDI LOGFONTlfCharSet.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt die Genauigkeit für das Ausschneiden der Schriftart an. Entspricht dem Feld GDI LOGFONTlfClipPrecision.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Vorschub  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt das Attribut Vorschub der Schriftart an. Entspricht dem Feld GDI LOGFONTlfEscapement.  <br/> |Werte des Typs xsd: int.  <br/> |
|FaceName  <br/> |XSD: String  <br/> |Optional  <br/> |Enthält Informationen zu einer Schriftart.  <br/> |Werte des Typs xsd: String.  <br/> |
|Höhe  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Höhe des Shapes in Zeichnungseinheiten fest.  <br/> |Werte des Typs xsd: int.  <br/> |
|Kursiv  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart kursiv ist. Entspricht dem Feld GDI LOGFONTlfItalic.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Ausrichtung  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Ausrichtung der Schriftart. Entspricht dem Feld GDI LOGFONTlfOrientation.  <br/> |Werte des Typs xsd: int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt das Ausgabe Genauigkeit der Schriftart. Entspricht dem Feld GDI LOGFONTlfOutPrecision.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt die Zeichenbreite und Familie der Schriftart an. Entspricht dem Feld GDI LOGFONTlfPitchAndFamily.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Qualität  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt die Ausgabequalität der Schriftart an. Entspricht dem Feld GDI LOGFONTlfQuality.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Durchgestrichen  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart eine Schriftart durchgestrichen aufweist. Entspricht dem Feld GDI LOGFONTlfStrikeOut.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Unterstrichen  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart unterstrichen ist. Entspricht dem Feld GDI LOGFONTlfUnderline.  <br/> |Werte des Typs Xsd:unsignedByte.  <br/> |
|Gewicht  <br/> |XSD: int  <br/> |Optional  <br/> |Gibt die Breite der Schriftart an. Entspricht dem Feld GDI LOGFONTlfWeight.  <br/> |Werte des Typs xsd: int.  <br/> |
|Breite  <br/> |XSD: int  <br/> |Optional  <br/> |Enthält die Breite des zugeordneten Shapes in Zeichnungseinheiten fest.  <br/> |Werte des Typs xsd: int.  <br/> |
   

