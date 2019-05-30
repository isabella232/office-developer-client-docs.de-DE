---
title: IssueTarget-Element (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Gibt je nach Ziel des übergeordneten Überprüfungs Problems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten überprüfungsproblem zugeordnet ist. Wenn das Ziel des übergeordneten Überprüfungs Problems ein Dokument ist, IssueTarget gibt an weder eine Seite noch eine Form.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542954"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>IssueTarget-Element (Issue_Type complexType) (Visio XML)

Gibt je nach Ziel des übergeordneten Überprüfungs Problems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten überprüfungsproblem zugeordnet ist. Wenn das Ziel des übergeordneten Überprüfungs Problems ein Dokument ist, **IssueTarget** gibt an weder eine Seite noch eine Form. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|PageID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Seite an, die dem übergeordneten überprüfungsproblem zugeordnet ist. Wenn es sich bei dem Ziel um das Dokument handelt, kann der Wert für die Seiten-0xFFFFFFFF werden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ShapeID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Form an, die dem übergeordneten überprüfungsproblem zugeordnet ist. Wenn das Ziel das Dokument oder eine Seite ist, kann der Wert der Shape-0xFFFFFFFF werden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

