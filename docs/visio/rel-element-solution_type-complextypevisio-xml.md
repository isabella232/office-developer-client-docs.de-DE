---
title: Rel-Element (Solution_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Gibt eine Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797796"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a>Rel-Element (Solution_Type ComplexType) ("Visio XML")

Gibt eine Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Solution](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|R-Id:  <br/> |XSD: String  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |erforderlich  <br/> |Gibt eine Beziehung mit einem Webpart an.  <br/> |"befassen #"  <br/> Weitere Informationen finden Sie in der "Anmerkungen".  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** . Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein. Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein. 
  
Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

