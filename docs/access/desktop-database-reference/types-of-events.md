---
title: Arten von Ereignissen (Access PC-Datenbank-Referenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a420623e467fd4ba0609db5023ca0d5cec25eb38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884492"
---
# <a name="types-of-events"></a><span data-ttu-id="0f7ac-102">Ereignistypen</span><span class="sxs-lookup"><span data-stu-id="0f7ac-102">Types of Events</span></span>


<span data-ttu-id="0f7ac-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f7ac-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="0f7ac-p101">Es gibt zwei Basisereignistypen. Will-Ereignisse, die vor dem Starten einer Operation aufgerufen werden, enthalten normalerweise "Will" im Namen - z. B. WillChangeRecordset oder WillConnect. Ereignisse, die nach Abschluss eines Ereignisses aufgerufen werden, enthalten normalerweise "Complete" im Namen - z. B. RecordChangeComplete oder ConnectComplete. Es sind Ausnahmen vorhanden - z. B. InfoMessage -, diese treten jedoch nach Abschluss der zugeordneten Operation auf.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="0f7ac-108">Will-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0f7ac-108">Will Events</span></span>

<span data-ttu-id="0f7ac-109">Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="0f7ac-110">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \**werden*-Ereignis \*\*\*.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="0f7ac-111">Complete-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0f7ac-111">Complete Events</span></span>

<span data-ttu-id="0f7ac-112">Ereignishandler wird aufgerufen, nachdem ein Vorgang abgeschlossen ist, können die Anwendung benachrichtigt, die eine Operation abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="0f7ac-113">Ein solcher Ereignishandler wird auch benachrichtigt, wenn ein Ereignishandler wird eine ausstehende Operation abbricht.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="0f7ac-114">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \***Ereignis \* vollständig**.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="0f7ac-115">Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="0f7ac-116">Andere Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0f7ac-116">Other Events</span></span>

<span data-ttu-id="0f7ac-117">Die anderen Ereignishandler – d. h., Ereignisse, deren Namen nicht des Formulars **wird \* Ereignis**\* oder \***Ereignis \* Complete –** sind nur nach Abschluss einer Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="0f7ac-118">Diese Ereignisse sind **Trennen**, **EndOfRecordset**und **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="0f7ac-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

