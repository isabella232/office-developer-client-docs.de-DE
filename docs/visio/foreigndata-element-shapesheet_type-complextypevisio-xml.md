---
title: ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Enthält einen MIME(Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten, z. B. Windows Metadatei, Bitmap- oder OLE-Daten.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539842"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)

Enthält einen MIME(Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten, z. B. Windows Metadatei, Bitmap- oder OLE-Daten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppenformelement definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Beziehung zu einem Teil an, der die Bilddaten enthält.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Komprimierungsstufe an, die auf die Datei angewendet wird. Dieses Attribut ist nur sinnvoll, wenn es sich bei den fremden Daten um ein rasterbasiertes fremdes Objekt handelt, z. B. eine DIB-, JPG-, PNG-, TIFF- oder GIF-Datei.  <br/> |Werte des xsd:double-Typs.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |Optional  <br/> |Gibt den Komprimierungstyp an, der auf die Datei angewendet wird. Dieses Attribut ist nur sinnvoll, wenn es sich bei den fremden Daten um ein rasterbasiertes fremdes Objekt handelt, z. B. eine DIB-, JPG-, PNG-, TIFF- oder GIF-Datei.  <br/> |Werte des xsd:token-Typs.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die horizontale Ausdehnung der Metadatei an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die vertikale Ausdehnung der Metadatei an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |erforderlich  <br/> |Gibt metafile, EnhMetaFile, Bitmap, Object oder Ink-Typ an.  <br/> |Werte des xsd:token-Typs.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Gibt den Metadateizuordnungsmodus an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um eine Metadatei handelt.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Höhe des Objekts in Seiteneinheiten an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Ein ganzzahliger Indikator des Objekttyps. Wird verwendet, wenn fremder Typ Objekt ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Breite des Objekts in Seiteneinheiten an. Dieses Attribut ist nur dann sinnvoll, wenn es sich bei den fremden Daten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eingebettete Daten als Symbol angezeigt werden.  <br/> |Werte des typs xsd:boolean.  <br/> |
   

