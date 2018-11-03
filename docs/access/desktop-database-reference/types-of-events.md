---
title: Arten von Ereignissen (Access PC-Datenbank-Referenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e3f6c9bd44b53f8448a07d591869c8f0fbb8efa
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946027"
---
# <a name="types-of-events"></a><span data-ttu-id="704fa-102">Typen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="704fa-102">Types of events</span></span>


<span data-ttu-id="704fa-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="704fa-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="704fa-p101">Es gibt zwei Basisereignistypen. Will-Ereignisse, die vor dem Starten einer Operation aufgerufen werden, enthalten normalerweise "Will" im Namen - z. B. WillChangeRecordset oder WillConnect. Ereignisse, die nach Abschluss eines Ereignisses aufgerufen werden, enthalten normalerweise "Complete" im Namen - z. B. RecordChangeComplete oder ConnectComplete. Es sind Ausnahmen vorhanden - z. B. InfoMessage -, diese treten jedoch nach Abschluss der zugeordneten Operation auf.</span><span class="sxs-lookup"><span data-stu-id="704fa-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="704fa-108">Will-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="704fa-108">Will Events</span></span>

<span data-ttu-id="704fa-109">Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="704fa-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="704fa-110">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \**werden*-Ereignis \*\*\*.</span><span class="sxs-lookup"><span data-stu-id="704fa-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="704fa-111">Complete-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="704fa-111">Complete Events</span></span>

<span data-ttu-id="704fa-112">Ereignishandler wird aufgerufen, nachdem ein Vorgang abgeschlossen ist, können die Anwendung benachrichtigt, die eine Operation abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="704fa-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="704fa-113">Ein solcher Ereignishandler wird auch benachrichtigt, wenn ein Ereignishandler wird eine ausstehende Operation abbricht.</span><span class="sxs-lookup"><span data-stu-id="704fa-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="704fa-114">Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars \***Ereignis \* vollständig**.</span><span class="sxs-lookup"><span data-stu-id="704fa-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="704fa-115">Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="704fa-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="704fa-116">Andere Ereignisse</span><span class="sxs-lookup"><span data-stu-id="704fa-116">Other Events</span></span>

<span data-ttu-id="704fa-117">Die anderen Ereignishandler – d. h., Ereignisse, deren Namen nicht des Formulars **wird \* Ereignis**\* oder \***Ereignis \* Complete –** sind nur nach Abschluss einer Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="704fa-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="704fa-118">Diese Ereignisse sind **Trennen**, **EndOfRecordset**und **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="704fa-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

