---
title: Recordset.Sort-Eigenschaft (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 18547162e7a0d64cc0ac7b0cdb2f0afa79185985
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926262"
---
# <a name="recordsetsort-property-dao"></a>Recordset.Sort-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt die Sortierreihenfolge für Datensätze in einem **[Recordset](recordset-object-dao.md)** -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Sortieren

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Sie können die **Sort** -Eigenschaft mit – und Snapshot – vom Typ Dynaset **Recordset** -Objekte.

Wenn Sie diese Eigenschaft für ein Objekt festlegen, wird die Sortierung vorgenommen, wenn anhand dieses Objekts ein nachfolgendes **Recordset**-Objekt erstellt wird. Die Einstellung der **Sort**-Eigenschaft hat Vorrang vor allen für ein **[QueryDef](querydef-object-dao.md)** -Objekt festgelegten Sortierreihenfolgen.

Die Standardsortierreihenfolge ist aufsteigend (A bis Z bzw. 0 bis 100).

Die **Sort** -Eigenschaft wird nicht auf Tabelle oder Weiterleiten – Typ **Recordset** -Objekte angewendet. Um ein **Recordset** -Objekt vom Typ Tabelle sortieren möchten, verwenden Sie die **[Index](recordset-index-property-dao.md)** -Eigenschaft.


> [!NOTE]
> <P>[!HINWEIS] In vielen Fällen ist es schneller, ein neues <STRONG>Recordset</STRONG>-Objekt mithilfe einer SQL-Anweisung zu öffnen, die die Sortierkriterien enthält.</P>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Sort** -Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues **Recordset** erstellt wird. Die SortOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
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
