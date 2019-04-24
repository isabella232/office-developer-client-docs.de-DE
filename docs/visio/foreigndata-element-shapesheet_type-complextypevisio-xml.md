---
title: ForeignData-Element (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Enthält eine MIME (Multipurpose Internet Mail Extensions) codiertes BLOB von Bild Daten wie Windows Metafile, Bitmap oder OLE-Daten.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346032"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData-Element (ShapeSheet_Type complexType) (' Visio XML ')

Enthält eine MIME (Multipurpose Internet Mail Extensions) codiertes BLOB von Bild Daten wie Windows Metafile, Bitmap oder OLE-Daten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Page #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die eine Form in einem **Master**-, **Page**-oder Group Shape-Element definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Beziehung zu einem Teil an, das die Bilddaten enthält.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Komprimierungsstufe an, die auf die Datei angewendet wird. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den Fremddaten um ein Raster basiertes fremdes Objekt handelt, beispielsweise eine DIB-, JPG-, PNG-, TIFF-oder GIF-Datei.  <br/> |Werte des Typs XSD: Double.  <br/> |
|CompressionType  <br/> |XSD: Token  <br/> |Optional  <br/> |Gibt den Komprimierungstyp an, der auf die Datei angewendet wird. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den Fremddaten um ein Raster basiertes fremdes Objekt handelt, beispielsweise eine DIB-, JPG-, PNG-, TIFF-oder GIF-Datei.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|ExtentX  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die horizontale Ausdehnung der Metadatei an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten eine Metadatei sind.  <br/> |Werte des Typs XSD: Double.  <br/> |
|Umfang  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die vertikale Ausdehnung der Metadatei an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten eine Metadatei sind.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ForeignType  <br/> |XSD: Token  <br/> |erforderlich  <br/> |Gibt Metadatei, EnhMetaFile, Bitmap, Objekt oder Freihandtyp an.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|MappingMode  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Gibt den Metadatei-Zuordnungsmodus an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten eine Metadatei sind.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|ObjectHeight  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Höhe des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten ein eingebettetes OLE2-Objekt sind.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ObjectType  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Ein ganzzahliger Indikator für den Objekttyp. Wird verwendet, wenn der fremde Typ Object ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ObjectWidth  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Breite des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten ein eingebettetes OLE2-Objekt sind.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ShowAsIcon  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eingebettete Daten als Symbol angezeigt oder nicht angezeigt werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
   

