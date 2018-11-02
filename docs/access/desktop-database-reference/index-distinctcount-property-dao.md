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
ms.openlocfilehash: 62c8681baebf0c1959fcb86df91d61387070adc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923644"
---
# <a name="indexdistinctcount-property-dao"></a>Index.DistinctCount-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das **[Index](index-object-dao.md)** -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . DistinctCount

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Überprüfen Sie die **DistinctCount**-Eigenschaft, um die Anzahl von eindeutigen Werten oder Schlüsseln in einem Index zu ermitteln. Jeder Schlüssel wird nur einmal gezählt, obwohl der Wert mehrmals vorkommen kann, falls der Index doppelte Werte zulässt. Diese Informationen sind in Anwendungen nützlich, die den Zugriff auf Daten durch eine Auswertung von Indexinformationen zu optimieren versuchen. Die Anzahl von eindeutigen Werten wird auch als Kardinalität eines **Index**-Objekts bezeichnet.

Die **DistinctCount**-Eigenschaft gibt nicht immer die tatsächliche Anzahl von Schlüsseln zu einer bestimmten Zeit wieder. Eine Änderung, die z. B. durch einen Rollback einer Transaktion verursacht wurde, wird gegebenenfalls nicht sofort in der **DistinctCount**-Eigenschaft wiedergegeben. Möglicherweise gibt der Wert der **DistinctCount**-Eigenschaft auch das Löschen von Datensätzen mit eindeutigen Schlüsseln nicht wieder. Die Zahl ist sofort richtig, nachdem Sie die **[CreateIndex](tabledef-createindex-method-dao.md)** -Methode angewendet haben.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht, wie Sie mit der DistinctCount-Eigenschaft die Anzahl von eindeutigen Werten in einem Index-Objekt ermitteln können. Dieser Wert stimmt jedoch nur direkt nachdem Sie das Index-Objekt erstellt haben. Er bleibt richtig, falls sich keine Schlüssel ändern oder wenn neue Schlüssel hinzugefügt und keine alten Schlüssel gelöscht werden; andernfalls ist er nicht zuverlässig. (Wenn diese Prozedur mehrmals ausgeführt wird, zeigt sich die Auswirkung auf die Werte der DistinctCount-Eigenschaft der vorhandenen Index-Objekte.)

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
