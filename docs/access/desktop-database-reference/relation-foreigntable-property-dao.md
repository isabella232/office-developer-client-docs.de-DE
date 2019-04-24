---
title: Relation. Foreignable-Eigenschaft (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307047"
---
# <a name="relationforeigntable-property-dao"></a>Relation. Foreignable-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen der Fremdtabelle in einer Beziehung zurück (nur Microsoft Access-Arbeitsbereiche). .

## <a name="syntax"></a>Syntax

*Ausdruck* . ForeignTable

*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Für diese Eigenschaft besteht bei einem neuen **[Relation](relation-object-dao.md)** -Objekt, das noch keiner Auflistung angefügt wurde, Lese-/Schreibzugriff, und bei einem vorhandenen **Relation**-Objekt in der **[Relations](relations-collection-dao.md)** -Auflistung ist sie schreibgeschützt.

Die Einstellung der **ForeignTable**-Eigenschaft eines **Relation**-Objekts ist die Einstellung der **[Name](connection-name-property-dao.md)** -Eigenschaft des **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts, das die Fremdtabelle oder Abfrage darstellt. Die Einstellung der **[Table](relation-table-property-dao.md)** -Eigenschaft ist die Einstellung der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts, das die Primärtabelle oder Abfrage darstellt.

For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.

In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.

## <a name="example"></a>Beispiel

In diesem Beispiel wird gezeigt, wie die Eigenschaften **Table**, **ForeignTable** und **ForeignName** die Beziehungen eines **Relation**-Objekts zwischen zwei Tabellen definieren.

```vb 
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
