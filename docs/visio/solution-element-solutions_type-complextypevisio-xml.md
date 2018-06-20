---
title: Solution-Element (Solutions_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798163"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a>Solution-Element (Solutions_Type ComplexType) ("Visio XML")

Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Solutions.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Lösungen](solutions-elementvisio-xml.md) <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |Speichert die Eigenschaften der Lösungen im Dokument gespeichert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |Gibt die Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Name  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der Lösung.  <br/> |Werte des Typs xsd: String.  <br/> |
   

