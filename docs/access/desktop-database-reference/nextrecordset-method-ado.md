---
title: NextRecordset-Methode (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 282d6ff3646800ebc107a1e2a7c96f80926e463f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589379"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset-Methode (ADO)

**Gilt für**: Access 2013, Office 2013
 
Löscht das aktuelle [Recordset](recordset-object-ado.md)-Objekt, und gibt das nächste **Recordset**-Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.

## <a name="syntax"></a>Syntax

Set *recordset2*  =  *recordset1*. NextRecordset(*RecordsAffected* )

## <a name="return-value"></a>Rückgabewert

Gibt ein **Recordset**-Objekt zurück. Im Syntaxmodell können Sie für *recordset1* und *recordset2* dasselbe **Recordset**-Objekt angeben oder separate Objekte verwenden. Wenn Sie separate **Recordset**-Objekte verwenden und die **ActiveConnection**-Eigenschaft auf das ursprüngliche **Recordset**-Objekt (*recordset1*) zurücksetzen, nachdem **NextRecordset** aufgerufen wurde, wird ein Fehler generiert.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*RecordsAffected* |Optional. Eine **Long** -Variable, an die der Anbieter die Anzahl der Datensätze zurückgibt, auf die sich der aktuelle Vorgang auswirkt.|

> [!NOTE]
> This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the **Recordset**.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **NextRecordset**-Methode, um die Ergebnisse des nächsten Befehls in einer Verbundbefehlsanweisung oder einer gespeicherten Prozedur, die mehrere Ergebnisse zurückgibt, zurückzugeben. Wenn Sie ein **Recordset-Objekt** basierend auf einer zusammengesetzten Befehlsanweisung öffnen (z. B. "SELECT \* FROM Table1; SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*. Rufen Sie die **NextRecordset**-Methode auf, um auf die Ergebnisse nachfolgender Befehle in der Anweisung zuzugreifen.

Solange zusätzliche Ergebnisse vorliegen und das **Recordset,** das die zusammengesetzten Anweisungen enthält, nicht getrennt oder über Prozessgrenzen gemarshallt wird, gibt die **NextRecordset-Methode** weiterhin **Recordset-Objekte** zurück. Wenn ein Zeilenrückgabebefehl erfolgreich ausgeführt wird, aber keine Datensätze zurückgibt, ist das **zurückgegebene Recordset-Objekt** geöffnet, aber leer. Testen Sie diesen Fall, indem Sie überprüfen, ob die [Eigenschaften BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) **true** sind. Wenn ein Befehl ohne Zeilenrückgabe erfolgreich ausgeführt wird, wird das **zurückgegebene Recordset-Objekt** geschlossen, was Sie überprüfen können, indem Sie die [State-Eigenschaft](state-property-ado.md) im **Recordset** testen. Wenn keine weiteren Ergebnisse vorhanden sind, wird *recordset* auf *Nothing* festgelegt.

Die **NextRecordset** -Methode ist in einem getrennten **Recordset** -Objekt, bei dem [ActiveConnection](activeconnection-property-ado.md) auf **Nothing** (in Microsoft Visual Basic) oder NULL (in anderen Sprachen) festgelegt wurde, nicht verfügbar.

Wenn im Modus der unmittelbaren Aktualisierung eine Bearbeitung vorgenommen wird, wird beim Aufrufen der **NextRecordset** -Methode ein Fehler generiert. Rufen Sie zunächst die [Update](update-method-ado.md)-Methode oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode auf.

Wenn Sie einen Parameter für mehrere Befehle in der Verbundanweisung übergeben möchten, indem Sie die [Parameters](parameters-collection-ado.md)-Auflistung auffüllen oder ein Array mit dem ursprünglichen Aufruf von **Open** oder **Execute** übergeben, muss die Reihenfolge der Parameter in der Auflistung oder im Array der Reihenfolge ihrer jeweiligen Befehle in der Befehlsreihe entsprechen. Sie müssen zunächst alle Ergebnisse lesen, bevor Sie die Werte der Ausgabeparameter lesen können.

Ihr OLE DB-Anbieter bestimmt, wann ein Befehl in einer Verbundanweisung ausgeführt wird. Der [Microsoft OLE DB Provider für SQL Server](microsoft-ole-db-provider-for-sql-server.md) führt beispielsweise alle Befehle nach dem Erhalt der Verbundanweisung nacheinander aus. Die resultierenden **Recordset** -Objekte werden beim Aufrufen von **NextRecordset** einfach zurückgegeben.

However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.

