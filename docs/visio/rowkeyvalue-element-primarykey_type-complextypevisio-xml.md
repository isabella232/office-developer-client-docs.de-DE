---
title: RowKeyValue-Element (PrimaryKey_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Gibt den Wert des einen Primärschlüssel für eine einzelne Zeile eines Recordset-Objekts.
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396723"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>RowKeyValue-Element (PrimaryKey_Type ComplexType) ("Visio XML")

Gibt den Wert des einen Primärschlüssel für eine einzelne Zeile eines Recordset-Objekts.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Gibt einen Primärschlüssel eines Recordset-Objekts an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|RowID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Ein eindeutiger Wert, der eine Zeile eines Recordset-Objekts identifiziert.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Wert  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Wert der Primärschlüssel für diese Zeile des Recordset-Objekts.  <br/> |Werte des Typs xsd: String.  <br/> |
   

