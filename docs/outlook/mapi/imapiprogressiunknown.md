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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792274"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="94bf4-103">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94bf4-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="94bf4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94bf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94bf4-105">Implementiert eine Fortschritt-Objekt, das Clientanwendungen mit einer Statusanzeige bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="94bf4-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="94bf4-106">Eine Statusanzeige ist eine Benutzeroberfläche anzeigen, die den Prozentsatz der Fertigstellung eines Vorgangs, wie beispielsweise Kopieren von Ordnern zwischen Nachrichtenspeicher anzeigt.</span><span class="sxs-lookup"><span data-stu-id="94bf4-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="94bf4-107">MAPI-und Clientanwendungen Implementieren des Fortschritts-Objekte und -Dienstanbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="94bf4-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94bf4-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="94bf4-108">Header file:</span></span>  <br/> |<span data-ttu-id="94bf4-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94bf4-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="94bf4-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="94bf4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="94bf4-111">Fortschritt-Objekte</span><span class="sxs-lookup"><span data-stu-id="94bf4-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="94bf4-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="94bf4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="94bf4-113">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="94bf4-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="94bf4-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="94bf4-114">Called by:</span></span>  <br/> |<span data-ttu-id="94bf4-115">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="94bf4-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="94bf4-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="94bf4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="94bf4-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="94bf4-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="94bf4-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="94bf4-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="94bf4-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="94bf4-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="94bf4-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="94bf4-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="94bf4-121">Progress</span><span class="sxs-lookup"><span data-stu-id="94bf4-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="94bf4-122">Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, sobald sie zum Abschluss des Vorgangs vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="94bf4-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="94bf4-123">"GetFlags"</span><span class="sxs-lookup"><span data-stu-id="94bf4-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="94bf4-124">Gibt kennzeichnen Einstellungen aus dem Fortschritt-Objekt für die Ebene des Vorgangs auf die Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="94bf4-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="94bf4-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="94bf4-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="94bf4-126">Gibt die maximale Anzahl von Elementen in den Vorgang für den Fortschritt Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="94bf4-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="94bf4-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="94bf4-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="94bf4-128">Gibt den kleinsten Wert in der [SetLimits](imapiprogress-setlimits.md) -Methode für die Fortschritt Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="94bf4-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="94bf4-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="94bf4-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="94bf4-130">Legt die oberen und unteren Grenzwerten für die Anzahl der Elemente in den Vorgang und die Kennzeichen, die steuern, wie die Statusinformationen für den Vorgang berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="94bf4-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94bf4-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94bf4-131">Remarks</span></span>

<span data-ttu-id="94bf4-132">MAPI enthält einen _LpProgress_ -Parameter in vielen der Methoden, die möglicherweise langwierige Operationen ausführen.</span><span class="sxs-lookup"><span data-stu-id="94bf4-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="94bf4-133">_LpProgress_ verweist auf eine Clientimplementierung eines Fortschritt-Objekts.</span><span class="sxs-lookup"><span data-stu-id="94bf4-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="94bf4-134">Clients, die die **IMAPIProgress** -Schnittstelle implementieren legen Sie diesen Parameter auf ihre Implementierung; Clients, die nicht **IMAPIProgress** implementieren festgelegt den Parameter auf NULL wurde.</span><span class="sxs-lookup"><span data-stu-id="94bf4-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="94bf4-135">Um eine Statusanzeige während der Verarbeitung des Vorgangs anzuzeigen, verwenden Sie Dienstanbieter vom Client, falls verfügbar bereitgestellte Fortschritt-Objekts oder ein MAPI-Implementierung (angegeben ist, wenn _LpProgress_ auf NULL festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="94bf4-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="94bf4-136">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="94bf4-136">MFCMAPI reference</span></span>

<span data-ttu-id="94bf4-137">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="94bf4-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="94bf4-138">**Dateien**</span><span class="sxs-lookup"><span data-stu-id="94bf4-138">**Files**</span></span>|<span data-ttu-id="94bf4-139">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="94bf4-139">**Function**</span></span>|<span data-ttu-id="94bf4-140">**Comment**</span><span class="sxs-lookup"><span data-stu-id="94bf4-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94bf4-141">MapiProgress.h und MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="94bf4-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="94bf4-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="94bf4-142">Not applicable</span></span>  <br/> |<span data-ttu-id="94bf4-143">Wenn die Einstellung IMAPIProgress aktiviert ist, wird MFCMAPI (engl.) eine Implementierung **IMAPIProgress** auf alle Funktionen, die aufruft, MFCMAPI (engl.) übergeben, die eine Implementierung akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="94bf4-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94bf4-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94bf4-144">See also</span></span>



[<span data-ttu-id="94bf4-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="94bf4-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="94bf4-146">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="94bf4-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

