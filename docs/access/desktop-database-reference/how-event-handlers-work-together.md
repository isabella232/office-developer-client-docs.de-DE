---
title: Zusammenarbeit von Ereignishandlern
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a926bed97cf3f21e81fbf01eae554aaec45406a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947784"
---
# <a name="how-event-handlers-work-together"></a>Zusammenarbeit von Ereignishandlern

**Betrifft**: Access 2013, Office 2013

Wenn Sie nicht in Visual Basic programmieren, müssen, unabhängig davon, ob Sie tatsächlich alle Ereignisse verarbeiten, alle Ereignishandler für die Ereignisse **Connection** und **Recordset** implementiert werden. Der Implementierungsaufwand hängt von der Programmiersprache ab. Weitere Informationen finden Sie unter [ADO-Ereignisinstanziierung nach Sprache](https://msdn.microsoft.com/library/jj250244\(v=office.15\)).

## <a name="paired-event-handlers"></a>Kombinierte Ereignishandler

Jedem Will-Ereignishandler ist ein Complete-Ereignishandler zugeordnet. Wenn z. B. durch die Anwendung der Wert eines Felds geändert wird, wird der WillChangeField-Ereignishandler aufgerufen. Wenn die Änderung akzeptabel ist, bleibt der adStatus-Parameter unverändert, und die Operation wird ausgeführt. Wenn die Operation abgeschlossen ist, wird die Anwendung durch ein FieldChangeComplete-Ereignis benachrichtigt, dass die Operation beendet ist. Wenn sie erfolgreich abgeschlossen wurde, enthält adStatus den Wert adStatusOK; andernfalls enthält adStatus den Wert adStatusErrorsOccurred, und Sie müssen das Error-Objekt überprüfen, um die Ursache des Fehlers zu ermitteln.

Wenn **WillChangeField** aufgerufen wird, ermitteln Sie möglicherweise, dass die Änderung nicht vorgenommen werden soll. Legen Sie in diesen Fall **adStatus** auf **adStatusCancel** fest. Die Operation wird abgebrochen, und das **FieldChangeComplete** -Ereignis empfängt für **adStatus** den Wert **adStatusErrorsOccurred**. Das **Error** -Objekt enthält **adErrOperationCancelled**, sodass dem **FieldChangeComplete** -Handler mitgeteilt wird, dass die Operation abgebrochen wurde. Sie müssen jedoch den Wert des **adStatus** -Parameters vor dem Ändern überprüfen, da das Festlegen von **adStatus** auf **adStatusCancel** keine Auswirkung hat, wenn der Parameter bei Beginn des Verfahrens auf **adStatusCantDeny** festgelegt war.

Manchmal wird von einer Operation mehr als ein Ereignis ausgelöst. Beispielsweise verfügt das Recordset-Objekt über kombinierte Ereignisse für Field- und Record-Änderungen. Wenn der Wert eines Field-Objekts von der Anwendung geändert wird, wird der WillChangeField-Ereignishandler aufgerufen. Wenn durch ihn bestimmt wird, dass die Operation fortgesetzt werden kann, wird außerdem der WillChangeRecord-Ereignishandler ausgelöst. Wenn auch durch diesen Handler das Fortsetzen des Ereignisses zugelassen wird, wird die Änderung vorgenommen, und die Ereignishandler FieldChangeComplete und RecordChangeComplete werden aufgerufen. Da die Reihenfolge, in der die Will-Ereignishandler für eine bestimmte Operation aufgerufen werden, nicht definiert ist, sollten Sie das Schreiben von Code vermeiden, der davon abhängt, dass Handler in einer bestimmten Reihenfolge aufgerufen werden.

In Fällen, in denen mehrere Will-Ereignisse ausgelöst werden, wird die Operation möglicherweise durch eines der Ereignisse abgebrochen. Wenn die Anwendung z. B. den Wert eines Field-Objekts ändert, werden normalerweise die Ereignishandler WillChangeField und WillChangeRecord aufgerufen. Wenn die Operation jedoch im ersten Ereignishandler abgebrochen wird, wird sofort der diesem zugeordnete Complete-Handler mit adStatusOperationCancelled aufgerufen. Der zweite Handler wird nie aufgerufen. Wenn jedoch durch den ersten Ereignishandler die Fortsetzung des Ereignisses zugelassen wird, wird der andere Ereignishandler aufgerufen. Wenn dann von diesem die Operation abgebrochen wird, werden wie in den vorherigen Beispielen beide Complete-Ereignisse aufgerufen.

## <a name="unpaired-event-handlers"></a>Nicht kombinierte Ereignishandler

Solange der dem Ergebnis übergebene Status nicht adStatusCantDeny entspricht, können Sie Ereignisbenachrichtigungen für ein Ereignis deaktivieren, indem Sie adStatusUnwantedEvent im Status-Parameter zurückgeben. Wenn z. B. der Complete-Ereignishandler zum ersten Mal aufgerufen wird, können Sie adStatusUnwantedEvent zurückgeben. Anschließend empfangen Sie nur Will-Ereignisse. Manche Ereignisse können jedoch aus mehreren Gründen ausgelöst werden. In diesem Fall hat das Ereignis einen Reason-Parameter. Wenn Sie adStatusUnwantedEvent zurückgeben, empfangen Sie für dieses Ereignis nur dann keine Benachrichtigungen mehr, wenn sie aus dem jeweiligen Grund auftreten. Mit anderen Worten: Sie empfangen potenziell Benachrichtigungen für jeden möglichen Grund, durch den das Ereignis ausgelöst werden kann.

Einzelne Will-Ereignishandler können hilfreich sein, wenn Sie die Parameter überprüfen möchten, die in einer Operation verwendet werden sollen. Sie können diese Operationsparameter ändern oder die Operation abbrechen.

Lassen Sie alternativ die Benachrichtigung für Complete-Ereignisse aktiviert. Wenn der erste Will-Ereignishandler aufgerufen wird, geben Sie adStatusUnwantedEvent zurück. Anschließend empfangen Sie nur Complete-Ereignisse.

Einzelne Complete-Ereignishandler können hilfreich sein beim Verwalten asynchroner Operationen. Jede asynchrone Operation hat ein entsprechendes Complete-Ereignis.

Beispielsweise kann das Auffüllen eines großen [Recordset](recordset-object-ado.md)-Objekts viel Zeit beanspruchen. Wenn die Anwendung entsprechend geschrieben ist, können Sie einen Vorgang starten und andere Verarbeitung fort. Sie werden schließlich benachrichtigt, wenn das **Recordset** mit einem **ExecuteComplete** -Ereignis aufgefüllt ist.

## <a name="single-event-handlers-and-multiple-objects"></a>Einzelne Ereignishandler und mehrere Objekte

Die Flexibilität einer Programmiersprache wie Microsoft Visual C++ ermöglicht die Verarbeitung von Ereignissen mehrerer Objekte durch einen Ereignishandler. Beispielsweise können Sie einen **Disconnect** -Ereignishandler Ereignisse von verschiedenen **Connection** -Objekten verarbeiten lassen. Wenn eine der Verbindungen beendet wird, wird der **Disconnect** -Ereignishandler aufgerufen. Sie können erkennen, durch welche Verbindung das Ereignis verursacht wurde, da der Objektparameter des Ereignishandlers auf das entsprechende **Connection** -Objekt festgelegt ist.


> [!NOTE]
> <P>[!HINWEIS] Diese Technik kann in Visual Basic nicht verwendet werden, da die Sprache nur ein Objekt zu einem Ereignishandler korrelieren kann.</P>


