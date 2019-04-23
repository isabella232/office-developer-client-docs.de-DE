---
title: ADO-Fehlerreferenz
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283394"
---
# <a name="ado-error-reference"></a><span data-ttu-id="c9154-102">ADO-Fehlerreferenz</span><span class="sxs-lookup"><span data-stu-id="c9154-102">ADO error reference</span></span>

<span data-ttu-id="c9154-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9154-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9154-p101">Die **ErrorValueEnum**-Konstante beschreibt die ADO-Fehlerwerte. Eine vollständige Aufstellung dieser aufgezählten Konstanten, einschließlich Werten, finden Sie in [Anhang B: ADO-Fehler](appendix-b-ado-errors.md). In diesem Abschnitt werden einige der interessanteren Fehler betrachtet. Außerdem werden Situationen, in denen diese ausgelöst werden können, oder Lösungen zum Beheben des Problems erläutert. Die **ErrorValueEnum**-Konstante und die Kurzform als positive Dezimalzahl werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c9154-p101">The **ErrorValueEnum** constant describes the ADO error values. For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md). This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem. Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9154-108">Zahl</span><span class="sxs-lookup"><span data-stu-id="c9154-108">Number</span></span></p></th>
<th><p><span data-ttu-id="c9154-109">ErrorValueEnum-Konstante</span><span class="sxs-lookup"><span data-stu-id="c9154-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="c9154-110">Beschreibung/mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="c9154-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9154-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-113">Der Anbieter konnte den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9154-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p102">Die Argumente haben den falschen Datentyp, liegen außerhalb des gültigen Bereichs oder stehen miteinander in Konflikt. Dieser Fehler wird häufig durch einen Tippfehler in einer SELECT-Anweisung von SQL verursacht. Beispielsweise kann dieser Fehler durch einen falsch geschriebenen Feldnamen oder Tabellennamen generiert werden. Dieser Fehler kann auch auftreten, wenn ein Feld oder eine Tabelle, das bzw. die in einer SELECT-Anweisung angegeben ist, im Datenspeicher nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c9154-p102">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another. This error is often caused by a typographical error in an SQL SELECT statement. For example, a misspelled field name or table name can generate this error. This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p103">Die Datei konnte nicht geöffnet werden. Ein falsch geschriebener Dateiname wurde angegeben, oder eine Datei wurde verschoben, umbenannt oder gelöscht. Möglicherweise war über ein Netzwerk das Laufwerk vorübergehend nicht verfügbar, oder der Netzwerkverkehr verhinderte eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c9154-p103">File could not be opened. A misspelled file name was specified, or a file has been moved, renamed, or deleted. Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p104">Die Datei konnte nicht gelesen werden. Der Name der Datei ist falsch angegeben, die Datei wurde möglicherweise verschoben oder gelöscht, oder die Datei wurde beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c9154-p104">File could not be read. The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p105">Fehler beim Schreiben in die Datei. Möglicherweise haben Sie eine Datei geschlossen und dann versucht in diese zu schreiben, oder die Datei ist beschädigt. Wenn sich die Datei auf einem Netzlaufwerk befindet, können vorübergehende Netzwerkbedingungen das Schreiben auf ein Netzlaufwerk verhindern.</span><span class="sxs-lookup"><span data-stu-id="c9154-p105">Write to file failed. You might have closed a file and then tried to write to it, or the file might be corrupted. If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p106">Entweder ist <strong>BOF</strong> oder <strong>EOF</strong> „True", oder der aktuelle Datensatz wurde gelöscht. Für den angeforderten Datensatz ist ein aktueller Datensatz erforderlich. Es wurde versucht, Datensätze mithilfe von <strong>Find</strong> oder <strong>Seek</strong> zu aktualisieren, um den Datensatzzeiger auf den gewünschten Datensatz zu verschieben. Wenn der Datensatz nicht gefunden wird, ist <strong>EOF</strong> gleich „True". Dieser Fehler kann auch nach einem Fehler bei der Methode <strong>AddNew</strong> oder <strong>Delete</strong> auftreten, weil kein aktueller Datensatz vorhanden ist, wenn diese Methoden einen Fehler erzeugen.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p106">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record. An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record. If the record is not found, <strong>EOF</strong> will be True. This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-143">Der Vorgang ist in diesem Zusammenhang nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c9154-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-146">Der bereitgestellte Anbieter unterscheidet sich von dem bereits verwendeten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c9154-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p107">Das <strong>Connection</strong> -Objekt kann während einer Transaktion nicht explizit geschlossen werden. Ein <strong>Recordset</strong> - oder <strong>Connection</strong> -Objekt, das derzeit an einer Transaktion beteiligt ist, kann nicht geschlossen werden. Rufen Sie <strong>RollbackTrans</strong> oder <strong>CommitTrans</strong> vor dem Schließen des Objekts auf.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p107"><strong>Connection</strong> object cannot be explicitly closed while in a transaction. A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed. Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p108">Das Objekt oder der Anbieter kann den angeforderten Vorgang nicht ausführen. Einige Vorgänge hängen von einer bestimmten Anbieterversion ab.</span><span class="sxs-lookup"><span data-stu-id="c9154-p108">The object or provider is not capable of performing the requested operation. Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p109">Das Element, das dem angeforderten Namen oder der angeforderten Zahl entspricht, wurde in der Auflistung nicht gefunden. Ein falscher Feld- oder Tabellenname wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9154-p109">Item cannot be found in the collection corresponding to the requested name or ordinal. An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p110">Das Objekt ist bereits in der Auflistung vorhanden. Das Anfügen ist nicht möglich. Ein Objekt kann nicht zweimal derselben Auflistung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c9154-p110">Object is already in collection. Cannot append. An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-167">Das Objekt ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="c9154-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p111">Die Anwendung verwendet für den aktuellen Vorgang einen Wert des falschen Datentyps. Beispielsweise könnten Sie für einen Vorgang, der einen Datenstrom erwartet, eine Zeichenfolge eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c9154-p111">Application uses a value of the wrong type for the current operation. You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p112">Der Vorgang ist nicht zulässig, wenn das Objekt geschlossen ist. Das Objekt <strong>Connection</strong> oder <strong>Recordset</strong> wurde geschlossen. Beispielsweise könnte ein globales Objekt durch eine andere Routine geschlossen worden sein. Sie können diesen Fehler verhindern, indem Sie die <strong>State</strong> -Eigenschaft überprüfen, bevor Sie einen Vorgang auszuführen versuchen.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p112">Operation is not allowed when the object is closed. The <strong>Connection</strong> or <strong>Recordset</strong> has been closed. For example, some other routine might have closed a global object. You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p113">Der Vorgang ist nicht zulässig, wenn das Objekt geöffnet ist. Ein geöffnetes Objekt kann nicht geöffnet werden. An ein geöffnetes <strong>Recordset</strong> -Objekt können keine Felder angefügt werden.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p113">Operation is not allowed when the object is open. An object that is open cannot be opened. Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p114">Der Anbieter wurde nicht gefunden. Möglicherweise wurde er nicht ordnungsgemäß installiert. Möglicherweise wurde der Name des Anbieters falsch angegeben, der angegebene Anbieter ist nicht auf dem Computer installiert, auf dem der Code ausgeführt wird, oder die Installation wurde beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c9154-p114">Provider cannot be found. It may not be properly installed. The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p115">Die <strong>ActiveConnection</strong> -Eigenschaft eines <strong>Recordset</strong> -Objekts, das ein <strong>Command</strong> -Objekt als Quelle aufweist, kann nicht geändert werden. Die Anwendung versuchte, ein neues <strong>Connection</strong> -Objekt einem <strong>Recordset</strong> -Objekt zuzuweisen, das ein <strong>Command</strong> -Objekt als Quelle aufweist.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p115">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed. The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p116">Das <strong>Parameter</strong> -Objekt ist nicht ordnungsgemäß definiert. Inkonsistente oder unvollständige Informationen wurden eingegeben.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p116"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p117">Die Verbindung kann nicht für diesen Vorgang verwendet werden. Die Verbindung ist entweder geschlossen oder in diesem Kontext ungültig.</span><span class="sxs-lookup"><span data-stu-id="c9154-p117">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p118">Der Vorgang kann während der Verarbeitung des Ereignisses nicht ausgeführt werden. Ein Vorgang kann innerhalb eines Ereignishandlers, durch den das Ereignis erneut ausgelöst wird, nicht ausgeführt werden. Beispielsweise sollten Navigationsmethoden nicht innerhalb eines <strong>WillMove</strong> -Ereignishandlers aufgerufen werden.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p118">Operation cannot be performed while processing event. An operation cannot be performed within an event handler that causes the event to fire again. For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-207">Der Vorgang kann im asynchronen Modus nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9154-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p119">Der Vorgang wurde vom Benutzer abgebrochen. Die Anwendung hat die Methode <strong>CancelUpdate</strong> oder <strong>CancelBatch</strong> aufgerufen, und der aktuelle Vorgang wurde abgebrochen.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p119">Operation has been canceled by the user. The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-214">Der Vorgang kann für eine asynchrone Verbindung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9154-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-217">Die Koordinierungstransaktion ist ungültig oder wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9154-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-220">Der Vorgang kann nicht verarbeitet werden, wenn er nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9154-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-223">Die Sicherheitseinstellungen dieses Computers lassen den Zugriff auf eine Datenquelle in einer anderen Domäne nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c9154-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p120">Nur für die interne Verwendung. Verwenden Sie diese Konstante nicht. (Der Eintrag ist der Vollständigkeit halber enthalten; dieser Fehler sollte im Code nicht angezeigt werden.)</span><span class="sxs-lookup"><span data-stu-id="c9154-p120">For internal use only. Don't use. (Entry was included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p121">Nur für die interne Verwendung. Verwenden Sie diese Konstante nicht. (Der Eintrag ist der Vollständigkeit halber enthalten; dieser Fehler sollte im Code nicht angezeigt werden.)</span><span class="sxs-lookup"><span data-stu-id="c9154-p121">For internal use only. Don't use. (Entry included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p122">Der Datenwert steht in Konflikt mit den Integritätseinschränkungen des Felds. Ein neuer Wert für ein <strong>Field</strong> -Objekt würde zu einem doppelten Schlüssel führen. Ein Wert, der eine Seite einer Beziehung zwischen zwei Datensätzen darstellt, kann möglicherweise nicht aktualisiert werden.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p122">Data value conflicts with the integrity constraints of the field. A new value for a <strong>Field</strong> would cause a duplicate key. A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p123">Unzureichende Berechtigungen verhindern das Schreiben in das Feld. Der in der Verbindungszeichenfolge genannte Benutzer hat nicht die erforderlichen Berechtigungen, um in ein <strong>Field</strong> -Objekt zu schreiben.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p123">Insufficient permission prevents writing to the field. The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p124">Der Datenwert ist zu groß, um vom Felddatentyp dargestellt zu werden. Ein numerischer Wert wurde zugewiesen, der für das beabsichtigte Feld zu groß ist. Beispielsweise wurde ein Wert vom Typ Long Integer einem Feld vom Typ Short Integer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c9154-p124">Data value is too large to be represented by the field data type. A numeric value that is too large for the intended field was assigned. For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p125">Der Datenwert steht in Konflikt mit dem Datentyp oder mit Einschränkungen des Felds. Der Datenspeicher weist Gültigkeitseinschränkungen auf, die vom Wert des <strong>Field</strong> -Objekts abweichen.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p125">Data value conflicts with the data type or constraints of the field. The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-256">Fehler bei der Konvertierung, da der Datenwert ein Vorzeichen hat, der vom Anbieter verwendete Felddatentyp aber kein Vorzeichen aufweist.</span><span class="sxs-lookup"><span data-stu-id="c9154-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p126">Der Datenwert kann aus anderen Gründen als einem Vorzeichenkonflikt oder einem Datenüberlauf nicht konvertiert werden. Beispielsweise könnten bei der Konvertierung Daten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="c9154-p126">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-263">Der Datenwert kann nicht festgelegt oder abgerufen werden, da der Felddatentyp unbekannt war, oder der Anbieter verfügte über unzureichende Ressourcen zum Ausführen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c9154-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p127">Der Datensatz enthält dieses Feld nicht. Ein falscher Feldname wurde angegeben, oder es wurde auf ein Feld verwiesen, das nicht in der <strong>Fields</strong> -Auflistung des aktuellen Datensatzes vorhanden ist.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p127">Record does not contain this field. An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-270">Entweder die Quell-URL oder das übergeordnete Element der Ziel-URL ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c9154-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="c9154-271">In der Quell- oder Ziel-URL ist ein Tippfehler vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c9154-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="c9154-272">Sie haben https://mysite/photo/myphoto.jpg möglicherweise, wenn Sie https://mysite/photos/myphoto.jpg stattdessen tatsächlich haben sollten.</span><span class="sxs-lookup"><span data-stu-id="c9154-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="c9154-273">Der Tippfehler in der übergeordneten URL (in diesem Fall <em>Foto</em> anstelle von <em>Fotos</em>) hat den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="c9154-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p129">Unzureichende Berechtigungen für den Zugriff auf die Struktur oder die Unterstruktur. Der in der Verbindungszeichenfolge genannte Benutzer hat nicht die erforderlichen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="c9154-p129">Permissions are insufficient to access tree or subtree. The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p130">Die URL enthält ungültige Zeichen. Stellen Sie sicher, dass die URL richtig eingegeben ist. Die URL folgt dem für den aktuellen Anbieter registrierten Schema (z. B. ist der Internet Publishing-Anbieter für HTTP registriert).</span><span class="sxs-lookup"><span data-stu-id="c9154-p130">URL contains invalid characters. Make sure the URL is typed correctly. The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p131">Das von der angegebenen URL dargestellte Objekt ist von mindestens einem anderen Prozess gesperrt. Warten Sie, bis der Prozess abgeschlossen wurde, und wiederholen Sie dann den Vorgang. Das Objekt, auf das Sie zuzugreifen versuchen, wurde von einem anderen Benutzer oder einem anderen Prozess in Ihrer Anwendung gesperrt. Diese Situation ist in einer Mehrbenutzerumgebung am wahrscheinlichsten.</span><span class="sxs-lookup"><span data-stu-id="c9154-p131">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again. The object you are trying to access has been locked by another user or by another process in your application. This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p132">Der Kopiervorgang kann nicht ausgeführt werden. Das durch die Ziel-URL genannte Objekt ist bereits vorhanden. Geben Sie <strong>AdCopyOverwrite</strong> an, um das Objekt zu ersetzen. Falls Sie <strong>AdCopyOverwrite</strong> beim Kopieren von Dateien in ein Verzeichnis nicht angeben, wird beim Kopieren ein Fehler erzeugt, wenn Sie versuchen, ein im Zielordner bereits vorhandenes Element zu kopieren.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p132">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object. If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p133">Der Server kann den Vorgang nicht abschließen. Dies könnte darauf zurückzuführen sein, dass der Server mit anderen Vorgängen ausgelastet ist oder unzureichende Ressourcen aufweist.</span><span class="sxs-lookup"><span data-stu-id="c9154-p133">The server cannot complete the operation. This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p134">Der Anbieter konnte das von der URL angegebene Speichergerät nicht finden. Stellen Sie sicher, dass die URL richtig eingegeben ist. Die URL des Speichergeräts stimmt möglicherweise nicht, aber dieser Fehler kann auch andere Ursachen haben. Das Gerät war möglicherweise offline, oder das Herstellen der Verbindung wurde durch hohen Netzwerkverkehr verhindert.</span><span class="sxs-lookup"><span data-stu-id="c9154-p134">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly. The URL of the storage device might be incorrect, but this error can occur for other reasons. The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p135">Der Vorgang kann nicht ausgeführt werden. Der Anbieter kann nicht genügend Speicherplatz abrufen. Möglicherweise gibt es für temporäre Dateien auf dem Server nicht genügend Arbeitsspeicher (RAM) oder freien Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="c9154-p135">Operation cannot be performed. Provider cannot obtain enough storage space. There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-312">Die Quell- oder Ziel-URL liegt außerhalb des Bereichs des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c9154-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p136">Der Vorgang konnte nicht abgeschlossen werden, und der Status ist nicht verfügbar. Möglicherweise ist das Feld nicht verfügbar, oder der Vorgang wurde nicht ausgeführt. Ein anderer Benutzer hat möglicherweise das Feld, auf das Sie zuzugreifen versuchen, geändert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c9154-p136">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted. Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p137">Der von dieser URL genannte Datensatz ist nicht vorhanden. Beim Öffnen einer Datei mithilfe eines <strong>Record</strong> -Objekts war entweder der Dateiname oder der Pfad zur Datei falsch geschrieben.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p137">Record named by this URL does not exist. While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-324">Die URL des Objekts, das gelöscht werden soll, liegt außerhalb des Bereichs des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c9154-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-327">Für den Vorgang ist ein gültiger <strong>ParentCatalog</strong> erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9154-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p138">Die Verbindung wurde verweigert. Die angeforderte neue Verbindung weist andere Merkmale als die bereits verwendete Verbindung auf.</span><span class="sxs-lookup"><span data-stu-id="c9154-p138">Connection was denied. The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p139">Fehler beim Aktualisieren von Feldern. Weitere Informationen erhalten Sie in der <strong>Status</strong> -Eigenschaft einzelner Feldobjekte. Dieser Fehler kann in zwei Situationen auftreten: beim Ändern des Werts eines <strong>Field</strong> -Objekt während des Änderns oder Hinzufügens eines Datensatzes zur Datenbank und beim Ändern der Eigenschaften des <strong>Field</strong> -Objekts selbst. Die Aktualisierung von <strong>Record</strong> oder <strong>Recordset</strong> ist aufgrund eines Problems mit einem der Felder im aktuellen Datensatz fehlgeschlagen. Zählen Sie die <strong>Fields</strong> -Auflistung auf, und überprüfen Sie die <strong>Status</strong> -Eigenschaft für jedes Feld, um die Ursache des Problems zu ermitteln.  </span><span class="sxs-lookup"><span data-stu-id="c9154-p139">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects. This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself. The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record. Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9154-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p140">Der Anbieter unterstützt Freigabeeinschränkungen nicht. Es wurde versucht, die Dateifreigabe einzuschränken, aber dies wird vom Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9154-p140">Provider does not support sharing restrictions. An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9154-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="c9154-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="c9154-p141">Der Anbieter unterstützt die angeforderte Art von Freigabeeinschränkung nicht. Es wurde versucht, einen bestimmten Typ von Dateifreigabeeinschränkung einzurichten, der von Ihrem Anbieter nicht unterstützt wird. In der Dokumentation des Anbieters finden Sie Informationen, welche Dateifreigabeeinschränkungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c9154-p141">Provider does not support the requested kind of sharing restriction. An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider. See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

