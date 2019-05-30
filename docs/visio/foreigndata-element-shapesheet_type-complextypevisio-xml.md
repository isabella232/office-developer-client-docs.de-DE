---
title: ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Enthält eine MIME-codierte BLOB-Datei (Multipurpose Internet Mail Extensions) wie Windows Metafile, Bitmap oder OLE-Daten.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539842"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)

Enthält eine MIME-codierte BLOB-Datei (Multipurpose Internet Mail Extensions) wie Windows Metafile, Bitmap oder OLE-Daten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Seite #. XML, Master #. XML  <br/> |
   
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
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die eine Form in einem **Master**-Shape, einem **Seiten**-oder Gruppen-Shape-Element definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Beziehung zu einem Teil an, das die Bilddaten enthält.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Komprimierungsstufe an, die auf die Datei angewendet wird. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein Raster basiertes fremdobjekt handelt, beispielsweise eine DIB-, JPG-, PNG-, TIFF-oder GIF-Datei.  <br/> |Werte des Typs XSD: Double.  <br/> |
|CompressionType  <br/> |XSD: Token  <br/> |Optional  <br/> |Gibt die Art der Komprimierung an, die auf die Datei angewendet wird. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein Raster basiertes fremdobjekt handelt, beispielsweise eine DIB-, JPG-, PNG-, TIFF-oder GIF-Datei.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|ExtentX  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt den horizontalen Umfang der Metadatei an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|Extenty  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt den vertikalen Umfang der Metadatei an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ForeignType  <br/> |XSD: Token  <br/> |erforderlich  <br/> |Gibt Metadatei-, EnhMetaFile-, Bitmap-, Object-oder Ink-Typ an.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|MappingMode  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Gibt den Zuordnungsmodus für die Metadatei an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Objectheight  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Höhe des Objekts in Seiteneinheiten an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ObjectType  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Ein ganzzahliger Indikator des Objekttyps. Wird verwendet, wenn der fremde Typ Object ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Objectwidth  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Breite des Objekts in Seiteneinheiten an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ShowAsIcon  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eingebettete Daten als Symbol angezeigt oder nicht angezeigt werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
   

