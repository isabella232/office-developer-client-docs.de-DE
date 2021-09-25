---
title: Recordset2.Sort-Eigenschaft (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2ec38f55bf28b93ae35348800aee85bdbc0de512
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615060"
---
# <a name="recordset2sort-property-dao"></a>Recordset2.Sort-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013 

Legt die Sortierreihenfolge von Datensätzen in einem **[Recordset](recordset-object-dao.md)**-Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*expression* .Sort

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können die **Sort**-Eigenschaft mit **Recordset**-Objekten vom Typ „Dynaset“ und „Snapshot“ verwenden.

Wenn Sie diese Eigenschaft für ein Objekt festlegen, findet die Sortierung bei der nächsten Erstellung eines **Recordset**-Objekts aus diesem Objekt statt. Die **Sort**-Eigenschafteneinstellung überschreibt alle Sortierreihenfolgen, die für ein **[QueryDef](querydef-object-dao.md)**-Objekt angegeben wurden.

Standardmäßig ist die aufsteigende Sortierreihenfolge (A bis Z oder 0 bis 100) festgelegt.

Die **Sort**-Eigenschaft gilt nicht für **Recordset**-Objekte vom Typ „Tabelle“ oder „Vorwärts“. Verwenden Sie zum Sortieren eines **Recordset**-Objekts vom Typ „Tabelle“ die **[Index](recordset2-index-property-dao.md)**-Eigenschaft.

> [!NOTE]
> In vielen Fällen ist geht schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die die Sortierkriterien enthält.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Sort**-Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues **Recordset** erstellt wird. Die SortOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.

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
