---
title: Arten von Ereignissen (Access PC-Datenbank-Referenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718140"
---
# <a name="types-of-events"></a><span data-ttu-id="b91de-102">Typen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="b91de-102">Types of events</span></span>


<span data-ttu-id="b91de-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b91de-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b91de-p101">Es gibt zwei Basisereignistypen. Will-Ereignisse, die vor dem Starten einer Operation aufgerufen werden, enthalten normalerweise "Will" im Namen - z. B. WillChangeRecordset oder WillConnect. Ereignisse, die nach Abschluss eines Ereignisses aufgerufen werden, enthalten normalerweise "Complete" im Namen - z. B. RecordChangeComplete oder ConnectComplete. Es sind Ausnahmen vorhanden - z. B. InfoMessage -, diese treten jedoch nach Abschluss der zugeordneten Operation auf.</span><span class="sxs-lookup"><span data-stu-id="b91de-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="b91de-108">Will-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b91de-108">Will Events</span></span>

<span data-ttu-id="b91de-109">Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="b91de-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="b91de-110">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \**werden*-Ereignis \*\*\*.</span><span class="sxs-lookup"><span data-stu-id="b91de-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="b91de-111">Complete-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b91de-111">Complete Events</span></span>

<span data-ttu-id="b91de-112">Ereignishandler wird aufgerufen, nachdem ein Vorgang abgeschlossen ist, können die Anwendung benachrichtigt, die eine Operation abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b91de-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="b91de-113">Ein solcher Ereignishandler wird auch benachrichtigt, wenn ein Ereignishandler wird eine ausstehende Operation abbricht.</span><span class="sxs-lookup"><span data-stu-id="b91de-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="b91de-114">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \***Ereignis \* vollständig**.</span><span class="sxs-lookup"><span data-stu-id="b91de-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="b91de-115">Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="b91de-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="b91de-116">Andere Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b91de-116">Other Events</span></span>

<span data-ttu-id="b91de-117">Die anderen Ereignishandler – d. h., Ereignisse, deren Namen nicht des Formulars **wird \* Ereignis**\* oder \***Ereignis \* Complete –** sind nur nach Abschluss einer Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b91de-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="b91de-118">Diese Ereignisse sind **Trennen**, **EndOfRecordset**und **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="b91de-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

