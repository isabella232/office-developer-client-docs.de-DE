---
title: RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordsets an.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538130"
---
# <a name="rowkeyvalue-element-primarykey_type-complextype-visio-xml"></a>RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)

Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordsets an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Gibt einen Primärschlüssel eines Recordsets an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|RowID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Ein eindeutiger Wert, der eine Zeile eines Recordsets identifiziert.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Wert  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Wert des Primärschlüssels für diese Zeile des Recordsets.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

