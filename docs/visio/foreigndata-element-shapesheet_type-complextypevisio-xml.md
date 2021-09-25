---
title: ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Enthält ein MIME(Multipurpose Internet Mail Extensions) codiertes BLOB von Bilddaten, z. B. Windows Metadatei, Bitmap oder OLE-Daten.
ms.openlocfilehash: 64e61e8919f780e9a3cc8d776d267af38929aba9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554782"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>ForeignData-Element (ShapeSheet_Type complexType) (Visio XML)

Enthält ein MIME(Multipurpose Internet Mail Extensions) codiertes BLOB von Bilddaten, z. B. Windows Metadatei, Bitmap oder OLE-Daten.
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppen-Shape-Element definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Beziehung zu einem Teil an, der die Bilddaten enthält.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Komprimierungsebene an, die auf die Datei angewendet wird. Dieses Attribut ist nur von Bedeutung, wenn es sich bei den Fremddaten um ein rasterbasiertes fremdes Objekt handelt, z. B. eine DIB-, JPG-, PNG-, TIFF- oder GIF-Datei.  <br/> |Werte des Typs "xsd:double".  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |Optional  <br/> |Gibt den Typ der auf die Datei angewendeten Komprimierung an. Dieses Attribut ist nur von Bedeutung, wenn es sich bei den Fremddaten um ein rasterbasiertes fremdes Objekt handelt, z. B. eine DIB-, JPG-, PNG-, TIFF- oder GIF-Datei.  <br/> |Werte des Typs "xsd:token".  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die horizontale Erweiterung der Metadatei an. Dieses Attribut ist nur dann von Bedeutung, wenn es sich bei den Fremddaten um eine Metadatei handelt.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die vertikale Erweiterung der Metadatei an. Dieses Attribut ist nur dann von Bedeutung, wenn es sich bei den Fremddaten um eine Metadatei handelt.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |erforderlich  <br/> |Gibt metafile-, EnhMetaFile-, Bitmap-, Object- oder Ink-Typ an.  <br/> |Werte des Typs "xsd:token".  <br/> |
|Mappingmode  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Gibt den Metadateizuordnungsmodus an. Dieses Attribut ist nur dann von Bedeutung, wenn es sich bei den Fremddaten um eine Metadatei handelt.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Höhe des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn es sich bei den Fremddaten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Ein ganzzahliger Indikator des Objekttyps. Wird verwendet, wenn der Fremde Typ ein Objekt ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |Optional  <br/> |Gibt die Breite des Objekts in Seiteneinheiten an. Dieses Attribut ist nur von Bedeutung, wenn es sich bei den Fremddaten um ein eingebettetes OLE2-Objekt handelt.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eingebettete Daten als Symbol angezeigt werden sollen.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
   

