---
title: Recordset2.Sort-Eigenschaft (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722886"
---
# <a name="recordset2sort-property-dao"></a>Recordset2.Sort-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013 

Legt die Sortierreihenfolge für Datensätze in einem **[Recordset](recordset-object-dao.md)** -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Sortieren

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können die **Sort** -Eigenschaft mit – und Snapshot – vom Typ Dynaset **Recordset** -Objekte.

Wenn Sie diese Eigenschaft für ein Objekt festlegen, wird die Sortierung vorgenommen, wenn anhand dieses Objekts ein nachfolgendes **Recordset**-Objekt erstellt wird. Die Einstellung der **Sort**-Eigenschaft hat Vorrang vor allen für ein **[QueryDef](querydef-object-dao.md)** -Objekt festgelegten Sortierreihenfolgen.

Die Standardsortierreihenfolge ist aufsteigend (A bis Z bzw. 0 bis 100).

Die **Sort** -Eigenschaft wird nicht auf Tabelle oder Weiterleiten – Typ **Recordset** -Objekte angewendet. Um ein **Recordset** -Objekt vom Typ Tabelle sortieren möchten, verwenden Sie die **[Index](recordset2-index-property-dao.md)** -Eigenschaft.

> [!NOTE]
> [!HINWEIS] In vielen Fällen ist es schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die die Sortierkriterien enthält.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Sort** -Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues **Recordset** erstellt wird. Die SortOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

Wenn Sie die auszuwählenden Daten kennen, ist es in der Regel effizienter, ein **Recordset** mit einer SQL-Anweisung zu erstellen. In diesem Beispiel wird gezeigt, wie Sie nur ein **Recordset** erstellen und die gleichen Ergebnisse wie im vorherigen Beispiel erhalten.

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
