---
title: AutoLinkComparison-Element (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, mit der eine Spalte im übergeordneten dataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion in der Benutzeroberfläche verglichen wird.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338318"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>AutoLinkComparison-Element (DataRecordSet_Type complexType) (' Visio XML ')

Definiert eine Regel, mit der eine Spalte im über **** geordnetEn DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion in der Benutzeroberfläche verglichen wird. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Gibt ein Recordset-Objekt und die Datenbindung zwischen dem Recordset-Objekt und den Shapes auf Zeichnungs Seiten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Entspricht einem Spaltennamen im ADO-Recordset-Objekt.  <br/> |Werte des XSD: String-Typs.  <br/> |
|ContextType  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt die Eigenschaften der Gruppe oder Form an, die für den Vergleich verwendet werden soll. Mögliche Werte sind in der folgenden Tabelle dargestellt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ContextTypeLabel  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Wenn der Wert für ContextType 2 oder 3 ist, ist dieses Attribut erforderlich, um einen Vergleich zu definieren. Für ContextType = 2 muss ContextTypeLabel die Bezeichnung des Shape-Datenelements und, wenn **ContextType** = 3, ContextTypeLabel der lokale Zeilenname sein.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

