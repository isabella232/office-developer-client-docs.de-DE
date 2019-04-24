---
title: Zusammenspiel von Ereignishandlern
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e772e93f27d6bb5f30d865e3435d4bde6bdc5e73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291922"
---
# <a name="how-event-handlers-work-together"></a>Zusammenspiel von Ereignishandlern

**Gilt für**: Access 2013, Office 2013

Wenn Sie nicht in Visual Basic programmieren, müssen, unabhängig davon, ob Sie tatsächlich alle Ereignisse verarbeiten, alle Ereignishandler für die Ereignisse **Connection** und **Recordset** implementiert werden. Der Implementierungsaufwand hängt von der Programmiersprache ab. Weitere Informationen finden Sie unter [ADO-Ereignisinstanziierung nach Sprache](https://docs.microsoft.com/office/client-developer/access/desktop-database-reference/ado-event-instantiation-by-language-ado).

## <a name="paired-event-handlers"></a>Paarweise Ereignishandler

Each Will event handler has an associated Complete event handler. For example, when your application changes the value of a field, the **WillChangeField** event handler is called. If the change is acceptable, your application leaves the **adStatus** parameter unchanged and the operation is performed. When the operation completes, a **FieldChangeComplete** event notifies your application that the operation has finished. If it completed successfully, **adStatus** contains **adStatusOK**; otherwise, **adStatus** contains **adStatusErrorsOccurred** and you must check the **Error** object to determine the cause of the error.

Wenn **WillChangeField** aufgerufen wird, ermitteln Sie möglicherweise, dass die Änderung nicht vorgenommen werden soll. Legen Sie in diesen Fall **adStatus** auf **adStatusCancel** fest. Die Operation wird abgebrochen, und das **FieldChangeComplete** -Ereignis empfängt für **adStatus** den Wert **adStatusErrorsOccurred**. Das **Error** -Objekt enthält **adErrOperationCancelled**, sodass dem **FieldChangeComplete** -Handler mitgeteilt wird, dass die Operation abgebrochen wurde. Sie müssen jedoch den Wert des **adStatus** -Parameters vor dem Ändern überprüfen, da das Festlegen von **adStatus** auf **adStatusCancel** keine Auswirkung hat, wenn der Parameter bei Beginn des Verfahrens auf **adStatusCantDeny** festgelegt war.

Sometimes an operation can raise more than one event. For example, the **Recordset** object has paired events for **Field** changes and **Record** changes. When your application changes the value of a **Field**, the **WillChangeField** event handler is called. If it determines that the operation can continue, the **WillChangeRecord** event handler is also raised. If this handler also allows the event to continue, the change is made and the **FieldChangeComplete** and **RecordChangeComplete** event handlers are called. The order in which the Will event handlers for a particular operation are called is not defined, so you should avoid writing code that depends on calling handlers in a particular sequence.

In instances when multiple Will events are raised, one of the events might cancel the pending operation. For example, when your application changes the value of a **Field**, both **WillChangeField** and **WillChangeRecord** event handlers would normally be called. However, if the operation is canceled in the first event handler, its associated Complete handler is immediately called with **adStatusOperationCancelled**. The second handler is never called. If, however, the first event handler allows the event to proceed, the other event handler will be called. If it then cancels the operation, both Complete events will be called as in the earlier examples.

## <a name="unpaired-event-handlers"></a>Nicht gekoppelte Ereignishandler

Solange der an das Ereignis übergebene Status nicht **adStatusCantDeny festgelegt**ist, können Sie Ereignisbenachrichtigungen für jedes Ereignis deaktivieren, indem Sie **adStatusUnwantedEvent** im Parameter *Status* zurückgeben. For example, when your Complete event handler is called the first time, you can return **adStatusUnwantedEvent**. You will subsequently receive only Will events. However, some events can be triggered for more than one reason. In diesem Fall hat das Ereignis einen *reason* -Parameter. When you return **adStatusUnwantedEvent**, you will stop receiving notifications for that event only when they occur for that particular reason. In other words, you will potentially receive notification for each possible reason that the event could be triggered.

Single Will event handlers can be useful when you want to examine the parameters that will be used in an operation. You can modify those operation parameters or cancel the operation.

Alternatively, leave Complete event notification enabled. When your first Will event handler is called, return **adStatusUnwantedEvent**. You will subsequently receive only Complete events.

Single Complete event handlers can be useful for managing asynchronous operations. Each asynchronous operation has an appropriate Complete event.

Beispielsweise kann das Auffüllen eines großen [Recordset](recordset-object-ado.md)-Objekts viel Zeit beanspruchen. Wenn die Anwendung ordnungsgemäß geschrieben ist, können Sie einen Vorgang starten und mit anderer Verarbeitung fortfahren. Sie werden schließlich benachrichtigt, wenn das **Recordset** mit einem **ExecuteComplete** -Ereignis aufgefüllt ist.

## <a name="single-event-handlers-and-multiple-objects"></a>Einzelne Ereignishandler und mehrere Objekte

Die Flexibilität einer Programmiersprache wie Microsoft Visual C++ ermöglicht die Verarbeitung von Ereignissen mehrerer Objekte durch einen Ereignishandler. Beispielsweise können Sie einen **Disconnect** -Ereignishandler Ereignisse von verschiedenen **Connection** -Objekten verarbeiten lassen. Wenn eine der Verbindungen beendet wird, wird der **Disconnect** -Ereignishandler aufgerufen. Sie können erkennen, durch welche Verbindung das Ereignis verursacht wurde, da der Objektparameter des Ereignishandlers auf das entsprechende **Connection** -Objekt festgelegt ist.

> [!NOTE]
> [!HINWEIS] Diese Technik kann in Visual Basic nicht verwendet werden, da die Sprache nur ein Objekt zu einem Ereignishandler korrelieren kann.


