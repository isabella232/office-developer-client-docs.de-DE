---
title: Rel-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Gibt eine Beziehung zu einem Teil mit den zugeordneten Recordset- und Datenbindungsinformationen an.
ms.openlocfilehash: 9e6d94206f3776a83d1a4782ffc38e87a54dc703
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623145"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a>Rel-Element (DataRecordSet_Type complexType) (Visio XML)

Gibt eine Beziehung zu einem Teil mit den zugeordneten Recordset- und Datenbindungsinformationen an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Gibt eine Instanz eines Recordsets und Datenbindungsinformationen an, die in der Zeichnung gespeichert sind.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |Erforderlich  <br/> |Gibt eine Beziehung zu einem Teil an.  <br/> |"rId#"  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert des **r:id-Attributs** muss ein **ST_RelationshipID** Typ sein. Der **ST_RelationshipID** Typ ist eine Zeichenfolge im Format "rId#", wobei das letzte Zeichen eine Zahl sein muss. Die Zahl muss unter allen gleichgeordneten Elementen des **Rel-Elements** eindeutig sein. 
  
Weitere Informationen zum typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Part 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)
  

