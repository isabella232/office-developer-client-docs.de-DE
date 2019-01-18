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
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699261"
---
# <a name="recordset2recordcount-property-dao"></a>Recordset2.RecordCount-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Gibt die Anzahl der Datensätze zurück, auf die in einem **[Recordset](recordset-object-dao.md)** -Objekt zugegriffen wird, oder die Gesamtzahl der Datensätze in einem **Recordset** -Objekt vom "table"-Typ oder in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschütztes **Long** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordCount

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **RecordCount** -Eigenschaft, um herauszufinden, auf wie viele Datensätze in einem **Recordset** - oder **TableDef** -Objekt zugegriffen wurde. Die **RecordCount** -Eigenschaft gibt nicht an, wie viele Datensätze in einem Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt enthalten sind, bis alle Datensätze zugegriffen wurde. Sobald auf den letzten Datensatz zugegriffen wurde, gibt die **RecordCount** -Eigenschaft die Gesamtzahl ungelöschter Datensätze im **Recordset** - oder **TableDef** -Objekt an. Um den Zugriff auf den letzten Datensatz zu erzwingen, verwenden Sie die **[MoveLast](recordset2-movelast-method-dao.md)** -Methode für das **Recordset** -Objekt. Sie können auch eine SQL- **Count** -Funktion verwenden, um die ungefähre Anzahl von Datensätzen zu bestimmen, die die Abfrage zurückgibt.

> [!NOTE]
> [!HINWEIS] Die Verwendung der **MoveLast**-Methode zum Auffüllen eines neu geöffneten **Recordset**-Objekts hat negative Auswirkungen auf die Leistung. Sofern beim Öffnen eines **Recordset**-Objekts nicht sofort ein genauer **RecordCount**-Wert erforderlich ist, sollte das **Recordset**-Objekt mit anderen Codeteilen aufgefüllt werden, bevor die **RecordCount**-Eigenschaft geprüft wird.

Wenn Ihre Anwendung Datensätze in einem **Recordset** -Objekt vom "dynaset"-Typ löscht, nimmt der Wert der **RecordCount** -Eigenschaft ab. Datensätze, die von anderen Benutzern gelöscht werden, werden allerdings erst von der **RecordCount** -Eigenschaft wiedergegeben, wenn der aktuelle Datensatz auf einem gelöschten Datensatz positioniert wird. Wenn Sie eine Transaktion ausführen, die sich auf die Einstellung der **RecordCount** -Eigenschaft auswirkt und Sie dann ein Rollback für die Transaktion ausführen, gibt die **RecordCount** -Eigenschaft nicht die tatsächliche Anzahl verbleibender Datensätze wieder.

Änderungen in den zugrunde liegenden Tabellen wirkt sich nicht auf die **RecordCount** -Eigenschaft eines **Recordset** -Objekts Snapshot oder vorwärts – Typ aus.

Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.

Bei der Verwendung der **[Requery](recordset2-requery-method-dao.md)** -Methode für ein **Recordset**-Objekt wird die **RecordCount**-Eigenschaft zurückgesetzt, so als würde die Abfrage erneut ausgeführt.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht die **RecordCount**-Eigenschaft für unterschiedliche Typen von **Recordsets**-Objekten vor und nach ihrer Auffüllung.

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
