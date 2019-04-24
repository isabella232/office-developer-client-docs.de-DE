---
title: DataColumns-Element (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Enthält alle DataColumn-Elemente in einem Datenrecordset.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345248"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a>DataColumns-Element (DataRecordSet_Type complexType) (' Visio XML ')

Enthält alle **DataColumn** -Elemente in einem Datenrecordset. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Die Spalte, in der die Daten sortiert werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|SortColumn  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, ob die **SortColumn** -Spalte in aufsteigend (1) oder absteigend (0) sortiert werden soll.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

