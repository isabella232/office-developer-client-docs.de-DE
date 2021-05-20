---
title: Solution-Element (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Gibt eine Instanz von Lösungs-XML an, die in der Zeichnung gespeichert ist.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540266"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a>Solution-Element (Solutions_Type complexType) (Visio XML)

Gibt eine Instanz von Lösungs-XML an, die in der Zeichnung gespeichert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |solutions.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Lösungen](solutions-elementvisio-xml.md) <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |Speichert die Eigenschaften der im Dokument gespeicherten Lösungen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |Gibt die Beziehung zu einem Teil mit der Lösungs-XML an, die dieser Lösung zugeordnet ist.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Name  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Name der Lösung.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

