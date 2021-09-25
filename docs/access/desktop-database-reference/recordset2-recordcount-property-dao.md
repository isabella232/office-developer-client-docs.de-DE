---
title: Recordset2.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: f8181738ddf39ba00dca921cc192e2e68deaaf82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617531"
---
# <a name="recordset2recordcount-property-dao"></a>Recordset2.RecordCount-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.

## <a name="syntax"></a>Syntax

*expression* .RecordCount

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **RecordCount**-Eigenschaft, um herauszufinden, auf wie viele Datensätze in einem **Recordset**- oder **TableDef**-Objekt zugegriffen wurde. Die **RecordCount**-Eigenschaft gibt erst an, wie viele Datensätze in einem **Recordset**-Objekt vom "dynaset"-, "snapshot"- oder "forward-only"-Typ enthalten sind, wenn auf alle Datensätze zugegriffen wurde. Sobald auf den letzten Datensatz zugegriffen wurde, gibt die **RecordCount**-Eigenschaft die Gesamtzahl ungelöschter Datensätze im **Recordset**- oder **TableDef**-Objekt an. To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object. You can also use an SQL **Count** function to determine the approximate number of records your query will return.

> [!NOTE]
> Die Verwendung der **MoveLast**-Methode zum Auffüllen eines neu geöffneten **Recordset**-Objekts hat negative Auswirkungen auf die Leistung. Sofern beim Öffnen eines **Recordset**-Objekts nicht sofort ein genauer **RecordCount**-Wert erforderlich ist, sollte das **Recordset**-Objekt mit anderen Codeteilen aufgefüllt werden, bevor die **RecordCount**-Eigenschaft geprüft wird.

As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.

Die **RecordCount**-Eigenschaft eines **Recordset**-Objekts vom "snapshot"- oder "forward-only"-Typ ist nicht von den Änderungen in zugrunde liegenden Tabellen betroffen.

Ein **Recordset**- oder **TableDef**-Objekt ohne Datensätze hat eine **RecordCount**-Eigenschaftseinstellung von "0".

Bei der Verwendung der **[Requery](recordset2-requery-method-dao.md)** -Methode für ein **Recordset**-Objekt wird die **RecordCount**-Eigenschaft zurückgesetzt, so als würde die Abfrage erneut ausgeführt.

## <a name="example"></a>Beispiel

Dieses Beispiel demonstriert die **RecordCount**-Eigenschaft mit verschiedenen **Recordset**-Typen vor und nach der Auffüllung.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
