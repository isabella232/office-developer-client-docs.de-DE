---
title: Löschen von Datensätzen mit der Delete-Methode
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293966"
---
# <a name="deleting-records-using-the-delete-method"></a>Löschen von Datensätzen mit der Delete-Methode


**Gilt für**: Access 2013, Office 2013

Mit der **Delete** -Methode wird der aktuelle Datensatz oder eine Gruppe von Datensätzen in einem **Recordset** -Objekt zum Löschen markiert. Ein Fehler tritt auf, falls das **Recordset** -Objekt das Löschen von Datensätzen nicht zulässt. Wenn der sofortige Aktualisierungsmodus aktiviert ist, werden Löschvorgänge sofort in der Datenbank ausgeführt. Wenn ein Datensatz nicht erfolgreich gelöscht werden kann (z. B. aufgrund von Verletzungen der Datenbankintegrität), verbleibt der Datensatz nach dem Aufrufen von **Update** im Bearbeitungsmodus. Dies bedeutet, dass Sie die Aktualisierung mithilfe von [CancelUpdate](cancelupdate-method-ado.md) abbrechen müssen, bevor Sie den aktuellen Datensatz verlassen (z. B. mit [Close](close-method-ado.md), [Move](move-method-ado.md) oder [NextRecordset](nextrecordset-method-ado.md)).

Wenn der Batchaktualisierungsmodus aktiviert ist, werden die Datensätze im Cache zum Löschen markiert, und der eigentliche Löschvorgang wird ausgeführt, wenn Sie die **UpdateBatch** -Methode aufrufen. (Zum Anzeigen der gelöschten Datensätze legen Sie die **Filter** -Eigenschaft auf **adFilterAffectedRecords** fest, nachdem **Delete** aufgerufen wurde.)

Beim Abrufen von Feldwerten aus dem gelöschten Datensatz wird ein Fehler generiert. Nach dem Löschen des aktuellen Datensatzes bleibt der gelöschte Datensatz aktiv, bis Sie zu einem anderen Datensatz navigieren. Sobald Sie den gelöschten Datensatz verlassen, ist der Zugriff darauf nicht mehr möglich.

Wenn Sie Löschvorgänge in einer Transaktion schachteln, können Sie gelöschte Datensätze mithilfe der **RollbackTrans** -Methode wiederherstellen. Falls der Batchaktualisierungsmodus aktiviert ist, können Sie einen ausstehenden Löschvorgang oder eine Gruppe von ausstehenden Löschvorgängen mithilfe der **CancelBatch** -Methode abbrechen.

Wenn beim Löschen von Datensätzen ein Fehler aufgrund eines Konflikts mit den zugrunde liegenden Daten erzeugt wird (z. B. wurde ein Datensatz bereits von einem anderen Benutzer gelöscht), gibt der Anbieter Warnungen an die **Errors** -Auflistung zurück, aber die Ausführung des Programms wird nicht unterbrochen. Ein Laufzeitfehler tritt nur auf, wenn für alle angeforderten Datensätze Konflikte vorhanden sind.

Wenn die dynamische Eigenschaft **Unique Table** festgelegt ist und das **Recordset** -Objekt das Ergebnis der Ausführung einer JOIN-Operation in mehreren Tabellen ist, löscht die **Delete** -Methode nur Zeilen in der in der **Unique Table** -Eigenschaft angegebenen Tabelle.

Die **Delete** -Methode verwendet ein optionales Argument, mit dem Sie angeben können, welche Datensätze von dem **Delete** -Vorgang betroffen sind. Für dieses Argument sind nur die folgenden aufgezählten **AffectEnum** -Konstanten von ADO zulässig:

  - **adAffectCurrent** Betrifft nur den aktuellen Datensatz.

  - **affectgroup** Betrifft nur Datensätze, die die aktuelle Einstellung der **Filter** -Eigenschaft erfüllen. Die **Filter** -Eigenschaft muss auf einen **FilterGroupEnum** -Wert oder ein Array von **Bookmarks** festgelegt werden, damit diese Option verwendet werden kann.

Der folgende Beispielcode veranschaulicht, wie Sie **adAffectGroup** angeben, wenn die **Delete** -Methode aufgerufen wird. In diesem Beispiel werden dem **Recordset** -Beispielobjekt Datensätze hinzugefügt und die Datenbank wird aktualisiert. Anschließend wird das **Recordset** -Objekt mithilfe der aufgezählten Filterkonstante **adFilterAffectedRecords** gefiltert, womit nur die neu hinzugefügten Datensätze im **Recordset** -Objekt angezeigt werden. Schließlich wird die **Delete** -Methode aufgerufen und angegeben, dass alle Datensätze, die die aktuelle Einstellung der **Filter** -Eigenschaft erfüllen (die neuen Datensätze), gelöscht werden sollen.

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

