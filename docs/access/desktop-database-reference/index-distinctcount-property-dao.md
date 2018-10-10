---
title: Index.DistinctCount Property (DAO)
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
ms.openlocfilehash: 2028334a2fc1d63262d9f109cb6f76c624b64e3a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474851"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="6fa42-102">Index.DistinctCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6fa42-102">Index.DistinctCount Property (DAO)</span></span>

<span data-ttu-id="6fa42-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fa42-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6fa42-104">Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das **[Index](index-object-dao.md)** -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="6fa42-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa42-105">Syntax</span></span>

<span data-ttu-id="6fa42-106">*Ausdruck* . DistinctCount</span><span class="sxs-lookup"><span data-stu-id="6fa42-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="6fa42-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6fa42-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa42-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fa42-108">Remarks</span></span>

<span data-ttu-id="6fa42-p101">Überprüfen Sie die **DistinctCount**-Eigenschaft, um die Anzahl von eindeutigen Werten oder Schlüsseln in einem Index zu ermitteln. Jeder Schlüssel wird nur einmal gezählt, obwohl der Wert mehrmals vorkommen kann, falls der Index doppelte Werte zulässt. Diese Informationen sind in Anwendungen nützlich, die den Zugriff auf Daten durch eine Auswertung von Indexinformationen zu optimieren versuchen. Die Anzahl von eindeutigen Werten wird auch als Kardinalität eines **Index**-Objekts bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6fa42-p101">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index. Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values. This information is useful in applications that attempt to optimize data access by evaluating index information. The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="6fa42-p102">Die **DistinctCount**-Eigenschaft gibt nicht immer die tatsächliche Anzahl von Schlüsseln zu einer bestimmten Zeit wieder. Eine Änderung, die z. B. durch einen Rollback einer Transaktion verursacht wurde, wird gegebenenfalls nicht sofort in der **DistinctCount**-Eigenschaft wiedergegeben. Möglicherweise gibt der Wert der **DistinctCount**-Eigenschaft auch das Löschen von Datensätzen mit eindeutigen Schlüsseln nicht wieder. Die Zahl ist sofort richtig, nachdem Sie die **[CreateIndex](tabledef-createindex-method-dao.md)** -Methode angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="6fa42-p102">The **DistinctCount** property won't always reflect the actual number of keys at a particular time. For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property. The **DistinctCount** property value also may not reflect the deletion of records with unique keys. The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="6fa42-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6fa42-117">Example</span></span>

<span data-ttu-id="6fa42-p103">Dieses Beispiel veranschaulicht, wie Sie mit der DistinctCount-Eigenschaft die Anzahl von eindeutigen Werten in einem Index-Objekt ermitteln können. Dieser Wert stimmt jedoch nur direkt nachdem Sie das Index-Objekt erstellt haben. Er bleibt richtig, falls sich keine Schlüssel ändern oder wenn neue Schlüssel hinzugefügt und keine alten Schlüssel gelöscht werden; andernfalls ist er nicht zuverlässig. (Wenn diese Prozedur mehrmals ausgeführt wird, zeigt sich die Auswirkung auf die Werte der DistinctCount-Eigenschaft der vorhandenen Index-Objekte.)</span><span class="sxs-lookup"><span data-stu-id="6fa42-p103">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
