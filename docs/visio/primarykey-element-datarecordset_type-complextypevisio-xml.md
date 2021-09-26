---
title: PrimaryKey-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.
ms.openlocfilehash: 3d537c0f8cf808da5ce8490fd584420b0a6e72b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627681"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a>PrimaryKey-Element (DataRecordSet_Type complexType) (Visio XML)

Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |Gibt den Wert dieser Komponente des Primärschlüssels für eine einzelne Zeile eines Recordsets an. Dieses untergeordnete Element muss mindestens ein Vorkommen aufweisen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnNameID  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Namen eines Felds an, das eine Komponente des Primärschlüssels ist. Es MUSS der Wert des **ColumnNameID-Attributs** eines DataColumn_Type untergeordneten Elements des DataRecordSet_Type sein, dessen Primärschlüssel angegeben wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

