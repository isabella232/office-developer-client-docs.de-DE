---
title: RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordset-Objekts an.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538130"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)

Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordset-Objekts an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Gibt einen Primärschlüssel eines Recordset-Objekts an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ROWID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Ein eindeutiger Wert, der eine Zeile eines Recordset-Objekts identifiziert.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Wert  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Der Wert des Primärschlüssels für diese Zeile des Recordset-Objekts.  <br/> |Werte des Typs XSD: String.  <br/> |
   

