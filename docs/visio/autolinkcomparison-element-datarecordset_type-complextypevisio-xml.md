---
title: AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537871"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)

Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde. **** 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Gibt ein Recordset-Objekt und die Datenbindung zwischen dem Recordset-Objekt und Shapes auf Zeichen Seiten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Entspricht einem Spaltennamen im ADO-Recordset-Objekt.  <br/> |Werte des Typs XSD: String.  <br/> |
|ContextType  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt die Eigenschaften der Gruppe oder der Form an, die für den Vergleich verwendet werden sollen. Mögliche Werte sind in der folgenden Tabelle dargestellt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ContextTypeLabel  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Wenn der ContextType-Wert 2 oder 3 ist, ist dieses Attribut erforderlich, um einen Vergleich zu definieren. Bei ContextType = 2 muss ContextTypeLabel die Shape-Datenelement Bezeichnung sein, und wenn **ContextType** = 3 lautet, muss ContextTypeLabel der Name der lokalen Zeile sein.  <br/> |Werte des Typs XSD: String.  <br/> |
   

