---
title: Rel-Element (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Gibt eine Beziehung zwischen einem Shape und einem Dokumentteil an, die die dem Shape zugeordneten Bilddaten enthält.
ms.openlocfilehash: 1179468fc4679dc3aa6892949d0fe43fba55cb6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623103"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a>Rel-Element (ForeignData_Type complexType) (Visio XML)

Gibt eine Beziehung zwischen einem Shape und einem Dokumentteil an, die die dem Shape zugeordneten Bilddaten enthält.
  
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
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Gibt eine Instanz von Bilddaten an, die in der Zeichnung gespeichert sind.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |Erforderlich  <br/> |Gibt eine Beziehung zu einem Teil an.  <br/> |"rId#"  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert des **r:id-Attributs** muss ein **ST_RelationshipID** Typ sein. Der **ST_RelationshipID** Typ ist eine Zeichenfolge im Format "rId#", wobei das letzte Zeichen eine Zahl sein muss. Die Zahl muss unter allen gleichgeordneten Elementen des **Rel-Elements** eindeutig sein. 
  
Weitere Informationen zum typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Part 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)
  

