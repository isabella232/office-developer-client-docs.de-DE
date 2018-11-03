---
title: 'Kapitel 7: Behandeln von ADO-Ereignissen'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58186a9f5612308c7762a815520d49ddce8eaf57
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937540"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="f28cb-102">Kapitel 7: Behandeln von ADO-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f28cb-102">Chapter 7: Handling ADO events</span></span>

<span data-ttu-id="f28cb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f28cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f28cb-p101">Das ADO-Ereignismodell unterstützt bestimmte synchrone und asynchrone ADO-Operationen, durch die *Ereignisse* oder Benachrichtigungen ausgegeben werden, bevor die Operation gestartet wird oder nachdem sie abgeschlossen ist. Ein Ereignis ist tatsächlich ein Aufruf an eine Ereignishandlerroutine, die Sie in der Anwendung definieren.</span><span class="sxs-lookup"><span data-stu-id="f28cb-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="f28cb-p102">Wenn Sie Handlerfunktionen oder -prozeduren für die Gruppe der vor dem Starten der Operation auftretenden Ereignisse bereitstellen, können Sie die an die Operation übergebenen Parameter überprüfen. Da die Operation noch nicht ausgeführt wurde, können Sie sie abbrechen oder zulassen, dass sie abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f28cb-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="f28cb-p103">Die Gruppe der nach Abschluss einer Operation auftretenden Ereignisse ist besonders wichtig, wenn Sie ADO asynchron verwenden. Beispielsweise wird eine Anwendung, durch die eine asynchrone Recordset.Open-Operation gestartet wird, von einem ExecuteComplete-Ereignis benachrichtigt, wenn die Operation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f28cb-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="f28cb-110">Durch das Verwenden des ADO-Ereignismodells entsteht mehr Aufwand für die Anwendung, jedoch wird auch erheblich mehr Flexibilität bereitgestellt als bei anderen Methoden für den Umgang mit asynchronen Operationen, z. B. beim Überwachen der [State](state-property-ado.md)-Eigenschaft eines Objekts mit einer Schleife.</span><span class="sxs-lookup"><span data-stu-id="f28cb-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

<span data-ttu-id="f28cb-111">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="f28cb-111">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="f28cb-112">Zusammenfassung der ADO-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="f28cb-112">ADO event handler summary</span></span>](ado-event-handler-summary.md)
- [<span data-ttu-id="f28cb-113">Typen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f28cb-113">Types of events</span></span>](types-of-events.md)
- [<span data-ttu-id="f28cb-114">Ereignisparameter</span><span class="sxs-lookup"><span data-stu-id="f28cb-114">Event parameters</span></span>](event-parameters.md)
- [<span data-ttu-id="f28cb-115">Zusammenarbeit von Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="f28cb-115">How event handlers work together</span></span>](how-event-handlers-work-together.md)
- [<span data-ttu-id="f28cb-116">ADO-Ereignisinstanziierung nach Sprache (ADO)</span><span class="sxs-lookup"><span data-stu-id="f28cb-116">ADO event instantiation by language (ADO)</span></span>](ado-event-instantiation-by-language-ado.md)