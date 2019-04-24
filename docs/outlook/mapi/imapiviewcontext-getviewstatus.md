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
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351177"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="ea8e1-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ea8e1-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="ea8e1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea8e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea8e1-105">Ruft den aktuellen viewerstatus ab.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="ea8e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8e1-106">Parameters</span></span>

 <span data-ttu-id="ea8e1-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="ea8e1-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="ea8e1-108">Out Zeiger auf eine Bitmaske von Flags, die den Status des Viewers bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="ea8e1-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ea8e1-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ea8e1-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="ea8e1-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="ea8e1-111">Es gibt eine nächste oder eine vorherige Nachricht in einer anderen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="ea8e1-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="ea8e1-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="ea8e1-113">Das Formular ermöglicht das Entfernen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="ea8e1-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="ea8e1-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="ea8e1-115">Im Formular sollte eine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-115">The form should display a user interface.</span></span> <span data-ttu-id="ea8e1-116">Wenn dieses Flag nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche auch als Reaktion auf ein Verb unterdrücken, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="ea8e1-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="ea8e1-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="ea8e1-118">Das Formular ist für den Viewer modal.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="ea8e1-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="ea8e1-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="ea8e1-120">In der Ansicht wird eine nächste Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="ea8e1-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="ea8e1-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="ea8e1-122">In der Ansicht ist eine vorherige Nachricht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="ea8e1-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="ea8e1-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="ea8e1-124">Die Nachricht soll im schreibgeschützten Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="ea8e1-125">Lösch-, Sende-und Verschiebungsvorgänge sollten deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="ea8e1-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="ea8e1-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="ea8e1-127">Es gibt eine nächste oder vorherige ungelesene Nachricht in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea8e1-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea8e1-128">Return value</span></span>

<span data-ttu-id="ea8e1-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea8e1-129">S_OK</span></span> 
  
> <span data-ttu-id="ea8e1-130">Der Status des Viewers wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea8e1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea8e1-131">Remarks</span></span>

<span data-ttu-id="ea8e1-132">Formularobjekte rufen die **IMAPIViewContext:: GetViewStatus** -Methode auf, um zu bestimmen, ob in einer Formularansicht in einer oder in beide Richtungen Weitere Nachrichten aktiviert werden sollen, die in der Richtung, in der ein **Nächster** Befehl Nachrichten aktiviert, in der Richtung, in der \*\*\*\* ein vorheriger Befehl Nachrichten aktiviert, oder in beide Richtungen.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="ea8e1-133">Der Wert, auf den durch den _lpulStatus_ -Parameter verwiesen wird, wird verwendet, um zu bestimmen, ob die VCSTATUS_NEXT-und VCSTATUS_PREV-Flags für [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md)gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="ea8e1-134">Wenn das VCSTATUS_DELETE-Flag festgelegt ist, aber nicht das VCSTATUS_READONLY-Flag, kann die Nachricht mithilfe der [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) -Methode gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="ea8e1-135">In der Regel werden Menübefehle und Schaltflächen von Formularen deaktiviert, wenn Sie nicht für den Kontext des Betrachters gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="ea8e1-136">Ein Betrachter kann ein Formular durch Aufrufen seiner [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) -Methode auf eine Änderung des Statushinweisen.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="ea8e1-137">Das VCSTATUS_MODAL-Flag wird festgelegt, wenn das Formular in das Fenster gebunden werden muss, dessen Handle im früheren [IMAPIForm::D overb](imapiform-doverb.md) -Aufruf übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="ea8e1-138">Wenn VCSTATUS_MODAL festgelegt ist, kann das Formular den Thread verwenden, in dem der **DoVerb** -Aufruf vorgenommen wurde, bis das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="ea8e1-139">Wenn VCSTATUS_MODAL nicht festgelegt ist, sollte das Formular nicht in dieses Fenster gebunden sein und den Thread nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea8e1-140">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ea8e1-140">MFCMAPI reference</span></span>

<span data-ttu-id="ea8e1-141">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea8e1-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ea8e1-142">**File**</span></span>|<span data-ttu-id="ea8e1-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ea8e1-143">**Function**</span></span>|<span data-ttu-id="ea8e1-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ea8e1-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea8e1-145">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="ea8e1-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ea8e1-146">CMyMAPIFormViewer:: GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ea8e1-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="ea8e1-147">MFCMAPI implementiert die **IMAPIViewContext:: GetViewStatus** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="ea8e1-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea8e1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea8e1-148">See also</span></span>



[<span data-ttu-id="ea8e1-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="ea8e1-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="ea8e1-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea8e1-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="ea8e1-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ea8e1-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

