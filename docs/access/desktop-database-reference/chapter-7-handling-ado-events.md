---
title: 'Kapitel 7: Behandeln von ADO-Ereignissen'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475312"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="75bfc-102">Kapitel 7: Behandeln von ADO-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="75bfc-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="75bfc-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75bfc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75bfc-p101">Das ADO-Ereignismodell unterstützt bestimmte synchrone und asynchrone ADO-Operationen, durch die *Ereignisse* oder Benachrichtigungen ausgegeben werden, bevor die Operation gestartet wird oder nachdem sie abgeschlossen ist. Ein Ereignis ist tatsächlich ein Aufruf an eine Ereignishandlerroutine, die Sie in der Anwendung definieren.</span><span class="sxs-lookup"><span data-stu-id="75bfc-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="75bfc-p102">Wenn Sie Handlerfunktionen oder -prozeduren für die Gruppe der vor dem Starten der Operation auftretenden Ereignisse bereitstellen, können Sie die an die Operation übergebenen Parameter überprüfen. Da die Operation noch nicht ausgeführt wurde, können Sie sie abbrechen oder zulassen, dass sie abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="75bfc-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="75bfc-p103">Die Gruppe der nach Abschluss einer Operation auftretenden Ereignisse ist besonders wichtig, wenn Sie ADO asynchron verwenden. Beispielsweise wird eine Anwendung, durch die eine asynchrone Recordset.Open-Operation gestartet wird, von einem ExecuteComplete-Ereignis benachrichtigt, wenn die Operation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="75bfc-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="75bfc-110">Durch das Verwenden des ADO-Ereignismodells entsteht mehr Aufwand für die Anwendung, jedoch wird auch erheblich mehr Flexibilität bereitgestellt als bei anderen Methoden für den Umgang mit asynchronen Operationen, z. B. beim Überwachen der [State](state-property-ado.md)-Eigenschaft eines Objekts mit einer Schleife.</span><span class="sxs-lookup"><span data-stu-id="75bfc-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

