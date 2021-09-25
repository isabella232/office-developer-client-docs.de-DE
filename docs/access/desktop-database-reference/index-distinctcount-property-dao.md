---
title: Index.DistinctCount-Eigenschaft (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 50a649478a117e79e3cf931976f2520a107ac38d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606625"
---
# <a name="indexdistinctcount-property-dao"></a>Index.DistinctCount-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das **[Index](index-object-dao.md)** -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . DistinctCount

*Ausdruck* Eine Variable, die ein **Index-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Überprüfen Sie die **DistinctCount**-Eigenschaft, um die Anzahl von eindeutigen Werten oder Schlüsseln in einem Index zu ermitteln. Jeder Schlüssel wird nur einmal gezählt, obwohl der Wert mehrmals vorkommen kann, falls der Index doppelte Werte zulässt. Diese Informationen sind in Anwendungen nützlich, die den Zugriff auf Daten durch eine Auswertung von Indexinformationen zu optimieren versuchen. Die Anzahl von eindeutigen Werten wird auch als Kardinalität eines **Index**-Objekts bezeichnet.

Die **DistinctCount**-Eigenschaft gibt nicht immer die tatsächliche Anzahl von Schlüsseln zu einer bestimmten Zeit wieder. Eine Änderung, die z. B. durch einen Rollback einer Transaktion verursacht wurde, wird gegebenenfalls nicht sofort in der **DistinctCount**-Eigenschaft wiedergegeben. Möglicherweise gibt der Wert der **DistinctCount**-Eigenschaft auch das Löschen von Datensätzen mit eindeutigen Schlüsseln nicht wieder. Die Zahl ist sofort richtig, nachdem Sie die **[CreateIndex](tabledef-createindex-method-dao.md)** -Methode angewendet haben.

## <a name="example"></a>Beispiel

This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
