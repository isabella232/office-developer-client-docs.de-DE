---
title: NextRecordset-Methode (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ca95e311f6040d5834fa24ce24d392375953990
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949936"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset-Methode (ADO)

**Betrifft**: Access 2013, Office 2013
 
Löscht das aktuelle [Recordset](recordset-object-ado.md)-Objekt, und gibt das nächste **Recordset** -Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.

## <a name="syntax"></a>Syntax

Festlegen von *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>Rückgabewert

Gibt ein **Recordset**-Objekt zurück. Im Syntaxmodell können Sie für *recordset1* und *recordset2* dasselbe **Recordset**-Objekt angeben oder separate Objekte verwenden. Wenn Sie separate **Recordset**-Objekte verwenden und die **ActiveConnection**-Eigenschaft auf das ursprüngliche **Recordset**-Objekt (*recordset1*) zurücksetzen, nachdem **NextRecordset** aufgerufen wurde, wird ein Fehler generiert.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*RecordsAffected* |Optional. Eine **Long** -Variable, an die der Anbieter die Anzahl der Datensätze zurückgibt, auf die sich der aktuelle Vorgang auswirkt.|

> [!NOTE]
> Dieser Parameter gibt nur die Anzahl der Datensätze an, auf die sich ein Vorgang auswirkt. Er gibt nicht die Anzahl der Datensätze aus einer SELECT- Anweisung zurück, die zum Generieren des Recordset-Objekts verwendet wurde.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **NextRecordset** -Methode, um die Ergebnisse des nächsten Befehls in einer zusammengesetzten befehlsanweisung oder einer gespeicherten Prozedur, die mehrere Ergebnisse zurückgibt zurückzugeben. Wenn Sie ein **Recordset** -Objekt basierend auf einer befehlsanweisung zusammengesetzter öffnen (beispielsweise "Wählen Sie \* FROM Tabelle1; SELECT \* aus Tabelle2 ") mithilfe der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode auf einen [Befehl](command-object-ado.md) oder die [Open](open-method-ado-recordset.md) -Methode für ein **Recordset-Objekt**, ADO führt nur den ersten Befehl und die Ergebnisse zu *Recordset-Objekt*zurückgibt. Rufen Sie den Zugriff auf die Ergebnisse der nachfolgenden Befehle in der Anweisung die **NextRecordset** -Methode.

Solange es weitere Ergebnisse sind und das **Recordset-Objekt** mit der zusammengesetzten Anweisungen nicht getrennt oder über Prozess hinweg gemarshallt, wird die **NextRecordset** -Methode weiterhin **Recordset** -Objekte zurück. Wenn ein Zeilen zurückgebende Befehl erfolgreich ausgeführt wird, aber keine Datensätze zurückgibt, wird das zurückgegebene **Recordset** -Objekt geöffnet, aber leer sein. In diesem Fall testen Sie, überprüfen Sie, dass die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) beide auf **"true"** sind. Wenn ein Zeilen zurückgebende Befehl erfolgreich ausgeführt wird, wird das zurückgegebene **Recordset** -Objekt geschlossen werden die können Sie überprüfen, ob Sie testen die [State](state-property-ado.md) -Eigenschaft für das **Recordset**. Wenn keine weitere Ergebnisse vorhanden sind, wird die *Recordset-Objekt* auf *Nothing*festgelegt.

Die **NextRecordset** -Methode ist in einem getrennten **Recordset** -Objekt, bei dem [ActiveConnection](activeconnection-property-ado.md) auf **Nothing** (in Microsoft Visual Basic) oder NULL (in anderen Sprachen) festgelegt wurde, nicht verfügbar.

Wenn im Modus der unmittelbaren Aktualisierung eine Bearbeitung vorgenommen wird, wird beim Aufrufen der **NextRecordset** -Methode ein Fehler generiert. Rufen Sie zunächst die [Update](update-method-ado.md)-Methode oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode auf.

Wenn Sie einen Parameter für mehrere Befehle in der Verbundanweisung übergeben möchten, indem Sie die [Parameters](parameters-collection-ado.md)-Auflistung auffüllen oder ein Array mit dem ursprünglichen Aufruf von **Open** oder **Execute** übergeben, muss die Reihenfolge der Parameter in der Auflistung oder im Array der Reihenfolge ihrer jeweiligen Befehle in der Befehlsreihe entsprechen. Sie müssen zunächst alle Ergebnisse lesen, bevor Sie die Werte der Ausgabeparameter lesen können.

Ihr OLE DB-Anbieter bestimmt, wann ein Befehl in einer Verbundanweisung ausgeführt wird. Der [Microsoft OLE DB Provider für SQL Server](microsoft-ole-db-provider-for-sql-server.md) führt beispielsweise alle Befehle nach dem Erhalt der Verbundanweisung nacheinander aus. Die resultierenden **Recordset** -Objekte werden beim Aufrufen von **NextRecordset** einfach zurückgegeben.

Andere Anbieter führen den nächsten Befehl in einer Anweisung jedoch möglicherweise erst aus, nachdem NextRecordset aufgerufen wurde. Wenn Sie das Recordset-Objekt bei diesen Anbietern explizit schließen, bevor die gesamte Befehlsanweisung durchlaufen wird, führt ADO die verbleibenden Befehle nicht aus.

