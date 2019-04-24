---
title: Primary-Element (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355996"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>Primary-Element (DataRecordSet_Type complexType) (' Visio XML ')

Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |Gibt den Wert dieser Komponente des Primärschlüssels für eine einzelne Zeile eines Recordset-Objekts an. Dieses untergeordnete Element muss mindestens ein Vorkommen aufweisen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName-Nr.  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den Namen eines Felds an, das eine Komponente des Primärschlüssels darstellt. Es muss der Wert des **ColumnName** -Attributs eines DataColumn_Type-Nachfolger Elements des DataRecordSet_Type sein, dessen Primärschlüssel angegeben wird.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

