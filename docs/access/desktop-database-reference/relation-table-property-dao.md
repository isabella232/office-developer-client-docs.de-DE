---
title: Relation. Table-Eigenschaft (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306993"
---
# <a name="relationtable-property-dao"></a>Relation. Table-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen der Primärtabelle eines **[Relation](relation-object-dao.md)** -Objekts an. Dieser Name sollte mit dem Wert der **[Name](connection-name-property-dao.md)** -Eigenschaft eines **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts übereinstimmen (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Tabelle

*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein neues **Relation**-Objekt, das noch an keine Auflistung angefügt wurde, hat Lese-/Schreibzugriff auf den Wert der **Table**-Eigenschaft. Für ein vorhandenes **Relation**-Objekt in einer **[Relations](relations-collection-dao.md)** -Auflistung ist die Eigenschaft schreibgeschützt.

Verwenden Sie die **Table**-Eigenschaft zusammen mit der **[ForeignTable](relation-foreigntable-property-dao.md)** -Eigenschaft, um ein **Relation**-Objekt zu definieren, das die Beziehung zwischen Feldern in zwei Tabellen oder Abfragen darstellt. Legen Sie die **Table**-Eigenschaft auf den Wert der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts der Primärtabelle fest und die **ForeignTable**-Eigenschaft auf den Wert der **Name**-Eigenschaft des verweisenden **TableDef**- oder **QueryDef**-Objekts der Fremdtabelle. Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft bestimmt den Typ der Beziehung zwischen den beiden Objekten.

For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.

In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.

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
