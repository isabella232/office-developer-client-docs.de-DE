---
title: MasterShortcut_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538060"
---
# <a name="mastershortcut_type-complextype-visio-xml"></a>MasterShortcut_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|MasterType  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs xsd:unsignedShort.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs xsd:unsignedShort.  <br/> |
|Eingabeaufforderung  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
   

