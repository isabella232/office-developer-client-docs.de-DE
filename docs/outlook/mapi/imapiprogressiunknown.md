---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419646"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="237b0-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="237b0-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="237b0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="237b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="237b0-105">Implementiert ein Statusobjekt, das Clientanwendungen eine Statusanzeige bietet.</span><span class="sxs-lookup"><span data-stu-id="237b0-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="237b0-106">Ein Statusindikator ist eine Benutzeroberflächenanzeige, die den Prozentsatz des Abschlusses eines Vorgangs zeigt, z. B. das Kopieren von Ordnern zwischen Nachrichtenspeichern.</span><span class="sxs-lookup"><span data-stu-id="237b0-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="237b0-107">MAPI- und Clientanwendungen implementieren Statusobjekte, und Dienstanbieter verwenden sie.</span><span class="sxs-lookup"><span data-stu-id="237b0-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="237b0-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="237b0-108">Header file:</span></span>  <br/> |<span data-ttu-id="237b0-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="237b0-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="237b0-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="237b0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="237b0-111">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="237b0-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="237b0-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="237b0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="237b0-113">MAPI- und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="237b0-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="237b0-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="237b0-114">Called by:</span></span>  <br/> |<span data-ttu-id="237b0-115">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="237b0-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="237b0-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="237b0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="237b0-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="237b0-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="237b0-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="237b0-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="237b0-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="237b0-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="237b0-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="237b0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="237b0-121">Progress</span><span class="sxs-lookup"><span data-stu-id="237b0-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="237b0-122">Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, der zum Abschluss des Vorgangs erfolgt.</span><span class="sxs-lookup"><span data-stu-id="237b0-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="237b0-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="237b0-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="237b0-124">Gibt Kennzeicheneinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="237b0-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="237b0-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="237b0-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="237b0-126">Gibt die maximale Anzahl von Elementen im Vorgang zurück, für die Statusinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="237b0-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="237b0-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="237b0-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="237b0-128">Gibt den Minimalwert in der [SetLimits-Methode](imapiprogress-setlimits.md) zurück, für den Statusinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="237b0-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="237b0-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="237b0-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="237b0-130">Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="237b0-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="237b0-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="237b0-131">Remarks</span></span>

<span data-ttu-id="237b0-132">MAPI enthält einen  _lpProgress-Parameter_ in vielen Methoden, die potenziell langwierige Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="237b0-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="237b0-133">_lpProgress_ verweist auf eine Clientimplementierung eines Progress-Objekts.</span><span class="sxs-lookup"><span data-stu-id="237b0-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="237b0-134">Clients, die die **IMAPIProgress-Schnittstelle** implementieren, legen diesen Parameter fest, um auf ihre Implementierung zu verweisen. Clients, die **IMAPIProgress** nicht implementieren, legen den Parameter auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="237b0-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="237b0-135">Zum Anzeigen eines Statusindikators während der Verarbeitung des Vorgangs verwenden Dienstanbieter das vom Client bereitgestellte Progress-Objekt( sofern verfügbar) oder eine MAPI-Implementierung (angegeben,  _wenn lpProgress_ auf NULL festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="237b0-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="237b0-136">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="237b0-136">MFCMAPI reference</span></span>

<span data-ttu-id="237b0-137">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="237b0-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="237b0-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="237b0-138">**Files**</span></span>|<span data-ttu-id="237b0-139">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="237b0-139">**Function**</span></span>|<span data-ttu-id="237b0-140">**Comment**</span><span class="sxs-lookup"><span data-stu-id="237b0-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="237b0-141">MapiProgress.h und MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="237b0-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="237b0-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="237b0-142">Not applicable</span></span>  <br/> |<span data-ttu-id="237b0-143">Wenn die EINSTELLUNG IMAPIProgress aktiviert ist, übernimmt MFCMAPI eine **IMAPIProgress-Implementierung** an alle Funktionen, die MFCMAPI aufruft, die eine Implementierung akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="237b0-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="237b0-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="237b0-144">See also</span></span>



[<span data-ttu-id="237b0-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="237b0-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="237b0-146">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="237b0-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

