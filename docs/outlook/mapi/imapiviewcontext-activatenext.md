---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 150a0c6eb7efa83f5ff1d12d915351bf5ca9d45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792511"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="d091e-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d091e-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="d091e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d091e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d091e-105">Aktiviert die nächste oder vorherige Nachricht in der Anzeigereihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d091e-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="d091e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d091e-106">Parameters</span></span>

<span data-ttu-id="d091e-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="d091e-107">_ulDir_</span></span>
  
> <span data-ttu-id="d091e-108">[in] Status Kennzeichen mit Informationen über die Meldung an, die aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d091e-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="d091e-109">Gültige Flageinstellungen sind:</span><span class="sxs-lookup"><span data-stu-id="d091e-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="d091e-110">VCDIR_CATEGORY: Betrachter sollte eine Nachricht in einer anderen Kategorie der Ansicht zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d091e-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="d091e-111">Wird die Meldung an, die aktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="d091e-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="d091e-112">Die erste Meldung in der nächsten Ansichtskategorie aus, wenn dieses Flag **oder**Ed mit VCDIR_NEXT ist.</span><span class="sxs-lookup"><span data-stu-id="d091e-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="d091e-113">Die letzte Meldung in der vorherigen Ansichtskategorie ist dieses Flag **OR**Ed mit VCDIR_PREV und der vorherigen Kategorie wird erweitert.</span><span class="sxs-lookup"><span data-stu-id="d091e-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="d091e-114">Die erste Meldung in der vorherigen Ansichtskategorie ist dieses Flag **OR**Ed mit VCDIR_PREV und der vorherigen Kategorie erweitert nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d091e-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="d091e-115">In diesem Fall der vorherige Kategorie Automatische Erweiterung Deklaration.</span><span class="sxs-lookup"><span data-stu-id="d091e-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="d091e-116">VCDIR_DELETE: Betrachter sollte die nächste oder der vorherige Nachricht aktiviert werden, da die aktuelle Nachricht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d091e-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="d091e-117">VCDIR_MOVE: Betrachter sollte die nächste oder der vorherige Nachricht aktiviert werden, da die aktuelle Nachricht verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="d091e-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="d091e-118">VCDIR_NEXT: Betrachter sollte die nächste Nachricht in der Anzeigereihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d091e-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="d091e-119">VCDIR_PREV: Betrachter sollte die vorherige Nachricht in der Anzeigereihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d091e-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="d091e-120">VCDIR_UNREAD: Betrachter sollte die nächste oder Vorherige ungelesene Nachricht in der Anzeigereihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d091e-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="d091e-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="d091e-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="d091e-122">[in] Zeiger auf eine Windows **Rechteck** -Struktur mit der Größe und Position des Fensters, zum Anzeigen der aktivierten Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d091e-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d091e-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d091e-123">Return value</span></span>

<span data-ttu-id="d091e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d091e-124">S_OK</span></span> 
  
> <span data-ttu-id="d091e-125">Die Nachricht wurde erfolgreich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d091e-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="d091e-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d091e-126">S_FALSE</span></span> 
  
> <span data-ttu-id="d091e-127">Die Nachricht wurde erfolgreich aktiviert, aber ein anderen Typ des Formulars im Prozess geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d091e-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d091e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d091e-128">Remarks</span></span>

<span data-ttu-id="d091e-129">Formularobjekte Aufrufen die **IMAPIViewContext::ActivateNext** -Methode zum Ändern, welche Meldung für den Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d091e-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="d091e-130">Der im _UlDir_ -Parameter übergebene Wert gibt an, welche Meldung sein sollte aktiviert und in einigen Fällen, warum.</span><span class="sxs-lookup"><span data-stu-id="d091e-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="d091e-131">Die Flags VCDIR_NEXT und VCDIR_PREVIOUS entsprechen den Benutzer, die Sie den **nächsten** oder **vorherigen** Befehl in einer Ansicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="d091e-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="d091e-132">Diese Vorgänge entsprechen in der Regel nach oben oder nach unten eine Nachricht in der Liste der Nachrichten der Formular-Viewer verschieben.</span><span class="sxs-lookup"><span data-stu-id="d091e-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="d091e-133">Die Flags VCDIR_DELETE und VCDIR_MOVE werden durch die [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) -Methoden, festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d091e-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="d091e-134">Implementierung dieser Methoden rufen Sie **ActivateNext** , wobei die entsprechende Richtung, und führen Sie dann den angeforderten Vorgang für die Nachricht, wenn der Anruf **ActivateNext** nicht fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d091e-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="d091e-135">Formular Viewer können in der Regel Benutzer geben Sie die Richtung, in der Liste zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d091e-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d091e-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d091e-136">Notes to implementers</span></span>

<span data-ttu-id="d091e-137">Die Implementierung von [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) wird die nächste oder der vorherige Nachricht im Ordner, abhängig vom Wert der _UlDir_, die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d091e-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="d091e-138">Nachdem **ActivateNext** zurückgegeben wird, rufen Sie [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) , um einen Zeiger auf den neu aktivierten Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d091e-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d091e-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d091e-139">Notes to callers</span></span>

<span data-ttu-id="d091e-140">Führen Sie Wenn **ActivateNext** S_FALSE zurückgibt, oder wenn eine aktuelle Nachricht nicht vorhanden ist, Ihre normalen Herunterfahren der enthalten sollte das Formular [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d091e-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="d091e-141">Wenn eine Nachricht nächste oder vorherige angezeigt wird, verwenden Sie das Fenster Rechteck im _PrcPosRect_ -Parameter übergeben, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d091e-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d091e-142">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="d091e-142">MFCMAPI reference</span></span>

<span data-ttu-id="d091e-143">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d091e-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d091e-144">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d091e-144">**File**</span></span>|<span data-ttu-id="d091e-145">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d091e-145">**Function**</span></span>|<span data-ttu-id="d091e-146">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d091e-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d091e-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d091e-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d091e-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d091e-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="d091e-149">MFCMAPI (engl.) implementiert die **IMAPIViewContext::ActivateNext** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="d091e-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d091e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d091e-150">See also</span></span>

- [<span data-ttu-id="d091e-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="d091e-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="d091e-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d091e-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="d091e-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d091e-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

