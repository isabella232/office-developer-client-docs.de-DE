---
title: Rel-Element (ForeignData_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Gibt eine Beziehung zwischen einem Shape und eines Dokumentteils, das die mit dem Shape verknüpften Bilddaten enthält.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383443"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a>Rel-Element (ForeignData_Type ComplexType) ("Visio XML")

Gibt eine Beziehung zwischen einem Shape und eines Dokumentteils, das die mit dem Shape verknüpften Bilddaten enthält.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Gibt eine Instanz von Bilddaten in der Zeichnung gespeichert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|R-Id:  <br/> |XSD: String  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |erforderlich  <br/> |Gibt eine Beziehung mit einem Webpart an.  <br/> |"befassen #"  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** . Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein. Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein. 
  
Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

