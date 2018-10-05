---
title: DocumentSheet-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Gibt eine DocumentSheet-Struktur an.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383464"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSheet-Element (VisioDocument_Type ComplexType) ("Visio XML")

Gibt eine DocumentSheet-Struktur an.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Das Stammelement eines Microsoft Visio-Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Zelle in einem DocumentSheet an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Beschreibt, ob der Name des Benutzers angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Beschreibt, ob der universelle Name durch den Benutzer angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den Namen der Sprache abhängig von der DocumentSheet.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der sprachenunabhängige Name des die DocumentSheet gibt.  <br/> |Werte des Typs xsd: String.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |Optional  <br/> |Optionaler string-Wert. Eine GUID (globally unique Identifier), die das Shape identifiziert.  <br/> |Werte des Typs xsd: String.  <br/> |
   

