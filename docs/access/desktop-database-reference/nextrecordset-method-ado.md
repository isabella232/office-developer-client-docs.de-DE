---
title: NextRecordset-Methode (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288617"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset-Methode (ADO)

**Gilt für**: Access 2013, Office 2013
 
Löscht das aktuelle [Recordset](recordset-object-ado.md)-Objekt, und gibt das nächste **Recordset**-Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.

## <a name="syntax"></a>Syntax

Legen Sie *Recordset2* = *Recordset1*fest. NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>Rückgabewert

Gibt ein **Recordset**-Objekt zurück. Im Syntaxmodell können Sie für *recordset1* und *recordset2* dasselbe **Recordset**-Objekt angeben oder separate Objekte verwenden. Wenn Sie separate **Recordset**-Objekte verwenden und die **ActiveConnection**-Eigenschaft auf das ursprüngliche **Recordset**-Objekt (*recordset1*) zurücksetzen, nachdem **NextRecordset** aufgerufen wurde, wird ein Fehler generiert.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*RecordsAffected* |Optional. Eine **Long** -Variable, an die der Anbieter die Anzahl der Datensätze zurückgibt, auf die sich der aktuelle Vorgang auswirkt.|

> [!NOTE]
> This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the **Recordset**.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **NextRecordset**-Methode, um die Ergebnisse des nächsten Befehls in einer Verbundbefehlsanweisung oder einer gespeicherten Prozedur, die mehrere Ergebnisse zurückgibt, zurückzugeben. Wenn Sie ein **Recordset** -Objekt basierend auf einer zusammengesetzten Befehlsanweisung öffnen (beispielsweise \* "SELECT FROM Tabelle1; SELECT \* from Tab ") mithilfe der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode für einen [Befehl](command-object-ado.md) oder der [Open](open-method-ado-recordset.md) -Methode für ein **Recordset**-Objekt führt ADO nur den ersten Befehl aus und gibt die Ergebnisse an das *Recordset*-Objekt zurück. Rufen Sie die **NextRecordset**-Methode auf, um auf die Ergebnisse nachfolgender Befehle in der Anweisung zuzugreifen.

Solange zusätzliche Ergebnisse vorhanden sind und das **Recordset** -Objekt, das die zusammengesetzten Anweisungen enthält, nicht getrennt oder über Prozessgrenzen hinweg gemarshallt wird, gibt die **NextRecordset** -Methode weiterhin **Recordset** -Objekte zurück. Wenn ein Befehl zur Zeilenrückgabe erfolgreich ausgeführt wird, aber keine Datensätze zurückgegeben wird, ist das zurückgegebene **Recordset** -Objekt geöffnet, aber leer. Testen Sie für diesen Fall, indem Sie sicherstellen, dass die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) beide **true**sind. Wenn ein Befehl ohne Zeilenrückgabe erfolgreich ausgeführt wird, wird das zurückgegebene **Recordset** -Objekt geschlossen, das Sie überprüfen können, indem Sie die [State](state-property-ado.md) -Eigenschaft des **Recordset**-Objekts testen. Wenn keine weiteren Ergebnisse vorhanden sind, wird *Recordset* auf *Nothing*festgelegt.

Die **NextRecordset** -Methode ist in einem getrennten **Recordset** -Objekt, bei dem [ActiveConnection](activeconnection-property-ado.md) auf **Nothing** (in Microsoft Visual Basic) oder NULL (in anderen Sprachen) festgelegt wurde, nicht verfügbar.

Wenn im Modus der unmittelbaren Aktualisierung eine Bearbeitung vorgenommen wird, wird beim Aufrufen der **NextRecordset** -Methode ein Fehler generiert. Rufen Sie zunächst die [Update](update-method-ado.md)-Methode oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode auf.

Wenn Sie einen Parameter für mehrere Befehle in der Verbundanweisung übergeben möchten, indem Sie die [Parameters](parameters-collection-ado.md)-Auflistung auffüllen oder ein Array mit dem ursprünglichen Aufruf von **Open** oder **Execute** übergeben, muss die Reihenfolge der Parameter in der Auflistung oder im Array der Reihenfolge ihrer jeweiligen Befehle in der Befehlsreihe entsprechen. Sie müssen zunächst alle Ergebnisse lesen, bevor Sie die Werte der Ausgabeparameter lesen können.

Ihr OLE DB-Anbieter bestimmt, wann ein Befehl in einer Verbundanweisung ausgeführt wird. Der [Microsoft OLE DB Provider für SQL Server](microsoft-ole-db-provider-for-sql-server.md) führt beispielsweise alle Befehle nach dem Erhalt der Verbundanweisung nacheinander aus. Die resultierenden **Recordset** -Objekte werden beim Aufrufen von **NextRecordset** einfach zurückgegeben.

However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.

