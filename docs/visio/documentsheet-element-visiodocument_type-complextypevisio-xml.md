---
title: DocumentSheet-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Gibt eine DocumentSheet-Struktur an.
ms.openlocfilehash: 064404fa38d05a774f46394a9768f677d370efbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590289"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a>DocumentSheet-Element (VisioDocument_Type complexType) (Visio XML)

Gibt eine DocumentSheet-Struktur an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Das Stammelement eines Microsoft Visio-Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Zelle in einem DocumentSheet an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Beschreibt, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:Boolean".  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Beschreibt, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:Boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den sprachabhängigen Namen des DocumentSheets an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den sprachunabhängigen Namen des DocumentSheets an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Optionaler string-Wert. Eine GUID (global eindeutiger Bezeichner), die das Shape identifiziert.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

