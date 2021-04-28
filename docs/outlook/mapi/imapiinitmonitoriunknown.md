---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062046"
---
# <a name="imapiinitmonitor--iunknown"></a><span data-ttu-id="b23c4-103">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b23c4-103">IMAPIInitMonitor : IUnknown</span></span>

<span data-ttu-id="b23c4-104">**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="b23c4-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="b23c4-105">Es gibt Zeiten, in denen eine Anwendung, die MAPI verwendet, wissen möchte, wann die Initialisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b23c4-105">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="b23c4-106">Sie verfügt beispielsweise über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion auf die initialisierte MAPI möchte die Anwendung einige Aufgaben ausführen, möchte jedoch nicht immer den MAPI-Stapel spinn.</span><span class="sxs-lookup"><span data-stu-id="b23c4-106">For example, it has multiple threads which could initialize MAPI, or in response to MAPI being initialized the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="b23c4-107">Der Initialisierungsmonitor stellt diese Funktionalität über ein [CreateMAPIInitializationMonitor-Objekt](createmapiinitializationmonitor.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="b23c4-107">The initialization monitor provides this functionality through a [CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md) object.</span></span>

| <span data-ttu-id="b23c4-108">Schnellinfos</span><span class="sxs-lookup"><span data-stu-id="b23c4-108">quick info</span></span> | <span data-ttu-id="b23c4-109">result</span><span class="sxs-lookup"><span data-stu-id="b23c4-109">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="b23c4-110">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="b23c4-110">Inherits from:</span></span>  <br/> |<span data-ttu-id="b23c4-111">IUnknown</span><span class="sxs-lookup"><span data-stu-id="b23c4-111">IUnknown</span></span>  <br/> |
|<span data-ttu-id="b23c4-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b23c4-112">Implemented by:</span></span>  <br/> | <span data-ttu-id="b23c4-113">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="b23c4-113">OLMAPI32.DLL</span></span> <br/> |
|<span data-ttu-id="b23c4-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b23c4-114">Called by:</span></span>  <br/> |<span data-ttu-id="b23c4-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b23c4-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="b23c4-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b23c4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b23c4-117">IID_IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="b23c4-117">IID_IMAPIInitMonitor</span></span>  <br/> |

## <a name="vtable-order"></a><span data-ttu-id="b23c4-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b23c4-118">Vtable order</span></span>

| <span data-ttu-id="b23c4-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="b23c4-119">function</span></span> | <span data-ttu-id="b23c4-120">description</span><span class="sxs-lookup"><span data-stu-id="b23c4-120">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="b23c4-121">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="b23c4-121">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md) <br/> |<span data-ttu-id="b23c4-122">Gibt den aktuellen Status der MAPI-Initialisierung zurück.</span><span class="sxs-lookup"><span data-stu-id="b23c4-122">Returns the current state of MAPI initialization.</span></span>  <br/> |
|[<span data-ttu-id="b23c4-123">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="b23c4-123">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md) <br/> |<span data-ttu-id="b23c4-124">Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b23c4-124">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span>  <span data-ttu-id="b23c4-125">INFINITE kann für unendliche Wartezeiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b23c4-125">INFINITE can be used to for an infinite wait.</span></span>  <br/> |
|[<span data-ttu-id="b23c4-126">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="b23c4-126">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md) <br/> |<span data-ttu-id="b23c4-127">Starten Sie eine Wartezeit auf die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden bis zum Verstreichen.</span><span class="sxs-lookup"><span data-stu-id="b23c4-127">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="b23c4-128">Dadurch wird eine IMAPIWaitResult-Schnittstelle zurück, die "End" aufgerufen haben sollte, um mit dem Warten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b23c4-128">This return an IMAPIWaitResult interface which should have “End” called in order begin the wait.</span></span>  <span data-ttu-id="b23c4-129">Dadurch kann der Aufrufer steuern, welcher Thread während der Wartezeit blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="b23c4-129">This allows the caller to control which thread is blocked while we are waiting.</span></span> <br/> |
