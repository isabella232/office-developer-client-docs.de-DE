---
title: IssueTarget-Element (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Hängt vom Ziel des übergeordneten Validierungs Problems ab, ob die Seite oder sowohl die Seite als auch die Form dem übergeordneten Validierungs Problem zugeordnet ist. Wenn das Ziel des übergeordneten Validierungs Problems ein Dokument ist, IssueTarget angibt weder eine Seite noch eine Form.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332522"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>IssueTarget-Element (Issue_Type complexType) (' Visio XML ')

Hängt vom Ziel des übergeordneten Validierungs Problems ab, ob die Seite oder sowohl die Seite als auch die Form dem übergeordneten Validierungs Problem zugeordnet ist. Wenn das Ziel des übergeordneten Validierungs Problems ein Dokument ist, **IssueTarget** angibt weder eine Seite noch eine Form. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Problem](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Stellt ein einzelnes Validierungs Problem im Dokument dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Seite an, die dem übergeordneten Validierungs Problem zugeordnet ist. Wenn das Ziel das Dokument ist, kann der Wert der Page-0xFFFFFFFF werden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ShapeID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Form an, die dem übergeordneten Validierungs Problem zugeordnet ist. Wenn das Ziel das Dokument oder eine Seite ist, kann der Wert der 0xFFFFFFFF werden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

