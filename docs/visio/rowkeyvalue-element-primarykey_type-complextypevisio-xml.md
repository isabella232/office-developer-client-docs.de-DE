---
title: RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordsets an.
ms.openlocfilehash: e1f4e4b7b21503a8f209b6f9466f8ac58510c71d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573411"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Primarykey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Gibt einen Primärschlüssel eines Recordsets an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Rowid  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Ein eindeutiger Wert, der eine Zeile eines Recordsets identifiziert.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Wert  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Wert des Primärschlüssels für diese Zeile des Recordsets.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

