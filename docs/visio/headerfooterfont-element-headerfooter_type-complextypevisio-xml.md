---
title: HeaderFooterFont-Element (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.
ms.openlocfilehash: a862141d12234efeaecdfe6976a1c19f18cbe6ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574153"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt den Zeichensatz der Schriftart an. Entspricht dem GDI LOGFONTlfCharSet-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt die Beschneidungsgenauigkeit der Schriftart an. Entspricht dem GDI LOGFONTlfClipPrecision-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Hemmung  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt das Escapezeichenattribut der Schriftart an. Entspricht dem GDI LOGFONTlfEscapement-Feld.  <br/> |Werte des Typs "xsd:int".  <br/> |
|FaceName  <br/> |xsd:string  <br/> |Optional  <br/> |Enthält Informationen zu einer Schriftart.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Height  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Höhe der Form in Zeichnungseinheiten an.  <br/> |Werte des Typs "xsd:int".  <br/> |
|Kursiv  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart kursiv formatiert ist. Entspricht dem GDI LOGFONTlfItalic-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Orientierung  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Ausrichtung der Schriftart an. Entspricht dem GDI LOGFONTlfOrientation-Feld.  <br/> |Werte des Typs "xsd:int".  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt das Ausgabegenauigkeitsattribut der Schriftart an. Entspricht dem GDI LOGFONTlfOutPrecision-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt den Schriftgrad und die Schriftfamilie an. Entspricht dem GDI LOGFONTlfPitchAndFamily-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Qualität  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt die Ausgabequalität der Schriftart an. Entspricht dem GDI LOGFONTlfQuality-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Durchgestrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob es sich bei der Schriftart um eine Durchstausschriftart handelt. Entspricht dem GDI LOGFONTlfStrikeOut-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Unterstrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> |Gibt an, ob die Schriftart unterstrichen ist. Entspricht dem GDI LOGFONTlfUnderline-Feld.  <br/> |Werte des Typs "xsd:unsignedByte".  <br/> |
|Schriftbreite  <br/> |xsd:int  <br/> |Optional  <br/> |Gibt die Schriftbreite an. Entspricht dem GDI LOGFONTlfWeight-Feld.  <br/> |Werte des Typs "xsd:int".  <br/> |
|Width  <br/> |xsd:int  <br/> |Optional  <br/> |Enthält die Breite der zugeordneten Form in Zeichnungseinheiten.  <br/> |Werte des Typs "xsd:int".  <br/> |
   

