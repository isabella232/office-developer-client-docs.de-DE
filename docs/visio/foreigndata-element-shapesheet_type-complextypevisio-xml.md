---
title: ForeignData-Element (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: MIME (Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten wie Windows-Metadatei, Bitmap oder OLE-Daten enthält.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382681"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData-Element (ShapeSheet_Type ComplexType) ("Visio XML")

MIME (Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten wie Windows-Metadatei, Bitmap oder OLE-Daten enthält.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Seite # .xml, Gestaltungsvorlagen # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Beziehung mit einem Webpart, das die Bilddaten enthält.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Ebene der Komprimierung auf die Datei angewendet. Dieses Attribut ist nur sinnvoll, wenn die fremden Daten ein Raster-basierte fremdes Objekt, wie etwa einer DIB, JPG, PNG, TIFF oder GIF-Datei.  <br/> |Werte des Typs xsd: Double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |Optional  <br/> |Gibt den Typ der Komprimierung auf die Datei angewendet. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten ein Raster-basierte fremdes Objekt, wie etwa einer DIB, JPG, PNG, TIFF oder GIF-Datei  <br/> |Werte des Typs Xsd:token.  <br/> |
|ExtentX  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die horizontale Umfang der Metadatei an. Dieses Attribut ist nur sinnvoll, wenn die fremden Daten eine Metadatei ist.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ExtentY  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die vertikale Umfang der Metadatei an. Dieses Attribut ist nur sinnvoll, wenn die fremden Daten eine Metadatei ist.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |erforderlich  <br/> |Metadatei EnhMetaFile, Bitmap, Object oder Freihand Typ wird angegeben.  <br/> |Werte des Typs Xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Gibt den Modus der Metadatei-Zuordnung. Dieses Attribut ist nur sinnvoll, wenn die fremden Daten eine Metadatei ist.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Höhe des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten OLE2 eingebettetes Objekt ist.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Eine ganze Zahl Indikator Objekttyp. Verwendet, wenn der Typ Foreign-Objekt ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD: Double  <br/> |Optional  <br/> |Gibt die Breite des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn die fremden Daten OLE2 eingebettetes Objekt ist.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ShowAsIcon  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob angezeigt oder nicht eingebettete Daten als Symbol angezeigt.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
   

