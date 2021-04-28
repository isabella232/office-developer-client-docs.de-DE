---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI-Initialisierungsmonitor
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062053"
---
# <a name="createmapiinitializationmonitor"></a><span data-ttu-id="1b278-103">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="1b278-103">CreateMAPIInitializationMonitor</span></span>

<span data-ttu-id="1b278-104">**Gilt für**: Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="1b278-104">**Applies to**: Outlook 2016 | Outlook 2019</span></span>
  
## <a name="mapi-initialization-monitor"></a><span data-ttu-id="1b278-105">MAPI-Initialisierungsmonitor</span><span class="sxs-lookup"><span data-stu-id="1b278-105">MAPI Initialization Monitor</span></span>

<span data-ttu-id="1b278-106">Es gibt Zeiten, in denen eine Anwendung, die MAPI verwendet, wissen möchte, wann die Initialisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b278-106">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="1b278-107">Sie verfügt beispielsweise über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion darauf, dass MAPI initialisiert wird, möchte die Anwendung einige Aufgaben ausführen, möchte aber nicht immer den MAPI-Stapel spinn.</span><span class="sxs-lookup"><span data-stu-id="1b278-107">For example, it have multiple threads which could initialize MAPI, or in response to MAPI being initialize the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="1b278-108">Der Initialisierungsmonitor stellt diese Funktionalität über eine Funktion (exportiert aus OLMAPI32.DLL) und einige einfache Schnittstellen bereit, die unten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b278-108">The initialization monitor provides this functionality through a function (exported from OLMAPI32.DLL) and a couple of simple interfaces described below.</span></span>

<span data-ttu-id="1b278-109">Dies ist ein Einstiegspunkt, der aus OLMAPI32.DLL dadurch kann der Aufrufer eine Schnittstelle abrufen, um den aktuellen Initialisierungsstatus abzurufen, einen Rückruf für den Initialisierungsabschluss einrichten oder den aktuellen Thread blockieren, bis er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b278-109">This is entry point exported from OLMAPI32.DLL this allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="1b278-110">Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur vom Thread, der es abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="1b278-110">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="1b278-111">Im Gegensatz zu anderen Objekten, die von MAPI verfügbar gemacht werden, ist dieses Objekt auch gültig, solange die DLL geladen wird, sie kann in initialisierungssitzungen erneut verwendet werden und vor oder nach dem Aufrufen von MAPIInitialize verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b278-111">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="1b278-112">Gibt Erfolg oder Fehler über ein COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen out-Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="1b278-112">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a><span data-ttu-id="1b278-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="1b278-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span></span>

<span data-ttu-id="1b278-114">Dieser aus OLMAPI32.DLL exportierte Einstiegspunkt ermöglicht dem Aufrufer das Abrufen einer Schnittstelle zum Abfragen des aktuellen Initialisierungszustands, zum Einrichten eines Rückrufs für den Initialisierungsabschluss oder zum Blockieren des aktuellen Threads, bis er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b278-114">This entry point exported from OLMAPI32.DLL allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="1b278-115">Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur vom Thread, der es abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="1b278-115">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="1b278-116">Im Gegensatz zu anderen Objekten, die von MAPI verfügbar gemacht werden, ist dieses Objekt auch gültig, solange die DLL geladen wird, sie kann in initialisierungssitzungen erneut verwendet werden und vor oder nach dem Aufrufen von MAPIInitialize verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b278-116">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="1b278-117">Gibt Erfolg oder Fehler über ein COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen out-Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="1b278-117">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1b278-118">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1b278-118">Quick info</span></span>

| <span data-ttu-id="1b278-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1b278-119">identifier</span></span> | <span data-ttu-id="1b278-120">result</span><span class="sxs-lookup"><span data-stu-id="1b278-120">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="1b278-121">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="1b278-121">Exported by:</span></span>  <br/> |<span data-ttu-id="1b278-122">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="1b278-122">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="1b278-123">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1b278-123">Called by:</span></span>  <br/> |<span data-ttu-id="1b278-124">Client</span><span class="sxs-lookup"><span data-stu-id="1b278-124">Client</span></span>  <br/> |
|<span data-ttu-id="1b278-125">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1b278-125">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b278-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="1b278-126">Outlook</span></span>  <br/> |

## <a name="parameters"></a><span data-ttu-id="1b278-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b278-127">Parameters</span></span>
  
 <span data-ttu-id="1b278-128">_ppInitMonitor_</span><span class="sxs-lookup"><span data-stu-id="1b278-128">_ppInitMonitor_</span></span>
> <span data-ttu-id="1b278-129">[out] Ein Zeiger zum Empfangen der neu erstellten Instanz des MAPI-Initialisierungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="1b278-129">[out] A pointer to receive the newly created instance of the MAPI initialization monitor.</span></span>
  
## <a name="return-values"></a><span data-ttu-id="1b278-130">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1b278-130">Return values</span></span>

<span data-ttu-id="1b278-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b278-131">S_OK</span></span>
> <span data-ttu-id="1b278-132">Eine neue Instanz des Initialisierungsmonitors wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b278-132">A new instance of the initialization monitor was created successfully.</span></span>

<span data-ttu-id="1b278-133">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1b278-133">E_OUTOFMEMORY</span></span>
> <span data-ttu-id="1b278-134">Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu kisten.</span><span class="sxs-lookup"><span data-stu-id="1b278-134">There was not enough memory to crate a new object.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b278-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b278-135">See also</span></span>
[<span data-ttu-id="1b278-136">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="1b278-136">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="1b278-137">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="1b278-137">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
