---
title: Recordset.UpdateOptions-Eigenschaft (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e267e913ed89707ca79642b96dafa2cae85a574
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927533"
---
# <a name="recordsetupdateoptions-property-dao"></a>Recordset.UpdateOptions-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . UpdateOptions

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn eine **[Update](recordset-update-method-dao.md)** -Anweisung im Batchmodus ausgeführt wird, erstellen DAO und die Client-Batchcursorbibliothek eine Reihe von SQL UPDATE-Anweisungen, um die erforderlichen Änderungen auszuführen. Für jede Aktualisierung wird eine SQL WHERE-Klausel erstellt, um die Datensätze zu isolieren, die von der **[RecordStatus](recordset-recordstatus-property-dao.md)** -Eigenschaft als geändert markiert wurden. Da einige Remoteserver Trigger oder andere Wege verwenden, um die referenzielle Integrität zu erzwingen, müssen häufig die zu aktualisierenden Felder auf die Felder beschränkt werden, die von der Änderung betroffen sind. 

Hierzu legen Sie die **UpdateOptions**-Eigenschaft auf eine der Konstanten **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** oder **dbCriteriaTimeStamp** fest. Auf diese Weise wird nur der absolut notwendige Triggercode ausgeführt. Als Ergebnis wird der Aktualisierungsvorgang schneller und mit weniger potenziellen Fehlern ausgeführt.

Sie können auch die Konstanten **dbCriteriaDeleteInsert** und **dbCriteriaUpdate** verketten, um festzustellen, ob für jede Aktualisierung eine Gruppe von SQL DELETE- und INSERT-Anweisungen oder eine SQL UPDATE-Anweisung verwendet werden sollen, wenn Änderungen in einem Batch an den Server zurückgesendet werden. Im ersten Fall sind zwei separate Vorgänge erforderlich, um den Datensatz zu aktualisieren. In einigen Fällen, v. a. wenn das Remotesystem DELETE-, INSERT- und UPDATE-Trigger implementiert, kann die Wahl der richtigen **UpdateOptions**-Eigenschaft erheblichen Einfluss auf die Leistung haben.

Wenn Sie keine Konstanten angeben, werden **dbCriteriaUpdate** und **dbCriteriaKey** verwendet.

Neu hinzugefügte Datensätze generieren immer INSERT-Anweisungen, und gelöschte Datensätze generieren immer DELETE-Anweisungen, sodass diese Eigenschaft nur angibt, wie die Cursorbibliothek geänderte Datensätze aktualisiert.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften **BatchSize** und **UpdateOptions** verwendet, um Aspekte von Batchaktualisierungen für das angegebene **Recordset**-Objekt zu steuern.

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

