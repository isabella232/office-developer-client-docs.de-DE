---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792524"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="a5f72-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="a5f72-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="a5f72-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5f72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5f72-105">Ruft den aktuellen Status der Viewer ab.</span><span class="sxs-lookup"><span data-stu-id="a5f72-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="a5f72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5f72-106">Parameters</span></span>

 <span data-ttu-id="a5f72-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="a5f72-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="a5f72-108">[out] Zeiger auf eine Bitmaske aus Flags, die den Status der Viewer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a5f72-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="a5f72-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a5f72-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a5f72-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="a5f72-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="a5f72-111">Es ist eine Nachricht nächste oder vorherige in einer anderen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="a5f72-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="a5f72-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="a5f72-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="a5f72-113">Das Formular ermöglicht Nachrichten entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5f72-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="a5f72-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="a5f72-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="a5f72-115">Das Formular sollte eine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5f72-115">The form should display a user interface.</span></span> <span data-ttu-id="a5f72-116">Wenn dieses Flag nicht festgelegt ist, sollte das Formular unterdrückt werden, auch als Antwort auf ein Verb an, die in der Regel eine Benutzeroberfläche anzuzeigende bewirkt, dass eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5f72-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="a5f72-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="a5f72-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="a5f72-118">Das Formular ist für den Betrachter modal.</span><span class="sxs-lookup"><span data-stu-id="a5f72-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="a5f72-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="a5f72-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="a5f72-120">Es ist eine nächste Nachricht in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a5f72-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="a5f72-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="a5f72-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="a5f72-122">Es ist eine vorherige Nachricht in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a5f72-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="a5f72-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="a5f72-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="a5f72-124">Die Nachricht ist im schreibgeschützten Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a5f72-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="a5f72-125">Löschen Sie, senden Sie, und verschieben Sie Vorgänge deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5f72-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="a5f72-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="a5f72-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="a5f72-127">Es ist eine nächste oder Vorherige ungelesene Nachricht in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a5f72-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5f72-128">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a5f72-128">Return value</span></span>

<span data-ttu-id="a5f72-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5f72-129">S_OK</span></span> 
  
> <span data-ttu-id="a5f72-130">Der Zeichnungsanzeige Status wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5f72-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5f72-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5f72-131">Remarks</span></span>

<span data-ttu-id="a5f72-132">Formular-Objekte aufrufen, die **IMAPIViewContext::GetViewStatus** -Methode, um zu bestimmen, ob es sind weitere Nachrichten an, die in einer Ansicht des Formulars in einem aktiviert werden, oder beide Richtungen d. h., in die Richtung, in dem ein Befehl **Weiter** aktiviert, Nachrichten in der Richtung, in dem ein **Vorherige** Befehl Nachrichten, aktiviert, oder in beide Richtungen.</span><span class="sxs-lookup"><span data-stu-id="a5f72-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="a5f72-133">Der Wert, der auf den durch den Parameter _LpulStatus_ wird verwendet, um festzustellen, ob die Flags VCSTATUS_NEXT und VCSTATUS_PREV für [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a5f72-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="a5f72-134">Wenn das Flag VCSTATUS_DELETE Set, aber nicht das Flag VCSTATUS_READONLY ist, kann die Nachricht mit der [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) -Methode gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a5f72-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="a5f72-135">Formulare deaktivieren in der Regel Menübefehle und Schaltflächen, wenn sie nicht für den Viewer Kontext gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a5f72-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="a5f72-136">Ein Viewer kann ein Formular auf eine Änderung im Status durch Aufrufen der [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) -Methode benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="a5f72-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="a5f72-137">Das Flag VCSTATUS_MODAL festgelegt ist, wenn das Formular in das Fenster gebunden sein muss, dessen Handle übergeben wird, in den früheren [IMAPIForm::DoVerb](imapiform-doverb.md) -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="a5f72-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="a5f72-138">Wenn VCSTATUS_MODAL festgelegt ist, können das Formular Threads auf dem der **DoVerb** -Anruf getätigt wurde, bis das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a5f72-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="a5f72-139">Wenn VCSTATUS_MODAL nicht festgelegt ist, wird das Formular nicht modal in diesem Fenster werden und muss nicht den Thread verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5f72-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a5f72-140">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a5f72-140">MFCMAPI reference</span></span>

<span data-ttu-id="a5f72-141">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a5f72-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a5f72-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a5f72-142">**File**</span></span>|<span data-ttu-id="a5f72-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a5f72-143">**Function**</span></span>|<span data-ttu-id="a5f72-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a5f72-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5f72-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a5f72-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a5f72-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="a5f72-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="a5f72-147">MFCMAPI (engl.) implementiert die **IMAPIViewContext::GetViewStatus** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="a5f72-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5f72-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5f72-148">See also</span></span>



[<span data-ttu-id="a5f72-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="a5f72-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="a5f72-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5f72-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="a5f72-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a5f72-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

