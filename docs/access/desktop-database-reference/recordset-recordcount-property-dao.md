---
title: Recordset.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ecaddcb30428b167811ab1eafcec149deb4da3ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891303"
---
# <a name="recordsetrecordcount-property-dao"></a>Recordset.RecordCount-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt die Anzahl der Datensätze zurück, auf die in einem **[Recordset](recordset-object-dao.md)** -Objekt zugegriffen wird, oder die Gesamtzahl der Datensätze in einem **Recordset** -Objekt vom "table"-Typ oder in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschütztes **Long** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordCount

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **RecordCount** -Eigenschaft, um herauszufinden, auf wie viele Datensätze in einem **Recordset** - oder **TableDef** -Objekt zugegriffen wurde. Die **RecordCount** -Eigenschaft gibt nicht an, wie viele Datensätze in einem Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt enthalten sind, bis alle Datensätze zugegriffen wurde. Sobald auf den letzten Datensatz zugegriffen wurde, gibt die **RecordCount** -Eigenschaft die Gesamtzahl ungelöschter Datensätze im **Recordset** - oder **TableDef** -Objekt an. Um den Zugriff auf den letzten Datensatz zu erzwingen, verwenden Sie die **[MoveLast](recordset-movelast-method-dao.md)** -Methode für das **Recordset** -Objekt. Sie können auch eine SQL- **Count** -Funktion verwenden, um die ungefähre Anzahl von Datensätzen zu bestimmen, die die Abfrage zurückgibt.


> [!NOTE]
> <P>[!HINWEIS] Die Verwendung der <STRONG>MoveLast</STRONG>-Methode zum Auffüllen eines neu geöffneten <STRONG>Recordset</STRONG>-Objekts hat negative Auswirkungen auf die Leistung. Sofern beim Öffnen eines <STRONG>Recordset</STRONG>-Objekts nicht sofort ein genauer <STRONG>RecordCount</STRONG>-Wert erforderlich ist, sollte das <STRONG>Recordset</STRONG>-Objekt mit anderen Codeteilen aufgefüllt werden, bevor die <STRONG>RecordCount</STRONG>-Eigenschaft geprüft wird.</P>



Wenn Ihre Anwendung Datensätze in einem **Recordset** -Objekt vom "dynaset"-Typ löscht, nimmt der Wert der **RecordCount** -Eigenschaft ab. Datensätze, die von anderen Benutzern gelöscht werden, werden allerdings erst von der **RecordCount** -Eigenschaft wiedergegeben, wenn der aktuelle Datensatz auf einem gelöschten Datensatz positioniert wird. Wenn Sie eine Transaktion ausführen, die sich auf die Einstellung der **RecordCount** -Eigenschaft auswirkt und Sie dann ein Rollback für die Transaktion ausführen, gibt die **RecordCount** -Eigenschaft nicht die tatsächliche Anzahl verbleibender Datensätze wieder.

Änderungen in den zugrunde liegenden Tabellen wirkt sich nicht auf die **RecordCount** -Eigenschaft eines **Recordset** -Objekts Snapshot oder vorwärts – Typ aus.

Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.

Bei der Verwendung der **[Requery](recordset-requery-method-dao.md)** -Methode für ein **Recordset**-Objekt wird die **RecordCount**-Eigenschaft zurückgesetzt, so als würde die Abfrage erneut ausgeführt.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht die **RecordCount**-Eigenschaft für unterschiedliche Typen von **Recordsets**-Objekten vor und nach ihrer Auffüllung.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
