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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410616"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="386a5-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="386a5-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="386a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="386a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="386a5-105">Aktiviert die nächste oder vorherige Nachricht in der Ansichtsreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="386a5-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="386a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="386a5-106">Parameters</span></span>

<span data-ttu-id="386a5-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="386a5-107">_ulDir_</span></span>
  
> <span data-ttu-id="386a5-108">[in] Statuskennzeichen, die Informationen zur zu aktivierende Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="386a5-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="386a5-109">Gültige Kennzeicheneinstellungen sind:</span><span class="sxs-lookup"><span data-stu-id="386a5-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="386a5-110">VCDIR_CATEGORY: Der Viewer sollte eine Nachricht in einer anderen Kategorie der Ansicht aktivieren.</span><span class="sxs-lookup"><span data-stu-id="386a5-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="386a5-111">Die zu aktivierende Nachricht lautet:</span><span class="sxs-lookup"><span data-stu-id="386a5-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="386a5-112">Die erste Nachricht in der nächsten Ansichtskategorie, wenn dieses Flag **or** ed with VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="386a5-112">The first message in the next view category if this flag is **OR** ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="386a5-113">Die letzte Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag **or** ed mit VCDIR_PREV und die vorherige Kategorie erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="386a5-113">The last message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="386a5-114">Die erste Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag **or** ed mit VCDIR_PREV und die vorherige Kategorie nicht erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="386a5-114">The first message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="386a5-115">In diesem Fall wird die vorherige Kategorie automatisch enpaniert.</span><span class="sxs-lookup"><span data-stu-id="386a5-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="386a5-116">VCDIR_DELETE: Der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="386a5-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="386a5-117">VCDIR_MOVE: Der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="386a5-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="386a5-118">VCDIR_NEXT: Der Viewer sollte die nächste Nachricht in der Ansichtsreihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="386a5-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="386a5-119">VCDIR_PREV: Der Viewer sollte die vorherige Nachricht in der Ansichtsreihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="386a5-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="386a5-120">VCDIR_UNREAD: Der Viewer sollte die nächste oder vorherige ungelesene Nachricht in der Ansichtsreihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="386a5-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="386a5-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="386a5-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="386a5-122">[in] Zeiger auf eine Windows **RECT-Struktur,** die die Größe und Position des Fensters enthält, das zum Anzeigen der aktivierten Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="386a5-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="386a5-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="386a5-123">Return value</span></span>

<span data-ttu-id="386a5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="386a5-124">S_OK</span></span> 
  
> <span data-ttu-id="386a5-125">Die Nachricht wurde erfolgreich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="386a5-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="386a5-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="386a5-126">S_FALSE</span></span> 
  
> <span data-ttu-id="386a5-127">Die Nachricht wurde erfolgreich aktiviert, es wurde jedoch ein anderer Formulartyp geöffnet.</span><span class="sxs-lookup"><span data-stu-id="386a5-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="386a5-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="386a5-128">Remarks</span></span>

<span data-ttu-id="386a5-129">Form-Objekte rufen die **IMAPIViewContext::ActivateNext-Methode** auf, um zu ändern, welche Nachricht für den Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="386a5-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="386a5-130">Der im  _ulDir-Parameter_ übergebene Wert gibt an, welche Nachricht aktiviert werden soll und in einigen Fällen warum.</span><span class="sxs-lookup"><span data-stu-id="386a5-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="386a5-131">Die VCDIR_NEXT und VCDIR_PREVIOUS entsprechen benutzern, die den **Befehl**  Weiter bzw. Zurück in einer Ansicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="386a5-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="386a5-132">Diese Vorgänge entsprechen in der Regel dem Verschieben einer Nachricht nach oben oder unten in der Liste der Nachrichten der Formularanzeige.</span><span class="sxs-lookup"><span data-stu-id="386a5-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="386a5-133">Die VCDIR_DELETE und VCDIR_MOVE werden von den [Methoden IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="386a5-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="386a5-134">Implementierungen dieser Methoden rufen **ActivateNext** mit der entsprechenden Richtung auf und führen dann den angeforderten Vorgang für die Nachricht aus, wenn beim **ActivateNext-Aufruf** kein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="386a5-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="386a5-135">Mit Formularanzeigen können Benutzer in der Regel die Richtung angeben, die in der Nachrichtenliste bewegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="386a5-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="386a5-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="386a5-136">Notes to implementers</span></span>

<span data-ttu-id="386a5-137">Ihre Implementierung von [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) erstellt die nächste oder vorherige Nachricht im Ordner, abhängig vom Wert von  _ulDir_, der aktuellen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="386a5-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="386a5-138">Rufen Sie nach der Rückgabe von **ActivateNext** [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) auf, um einen Zeiger auf die neu aktivierte Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="386a5-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="386a5-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="386a5-139">Notes to callers</span></span>

<span data-ttu-id="386a5-140">Wenn **ActivateNext** S_FALSE oder eine aktuelle Nachricht nicht vorhanden ist, führen Sie die normale Herunterfahrensprozedur aus, die das Aufrufen der [IMAPIForm::ShutdownForm-Methode](imapiform-shutdownform.md) Ihres Formulars umfassen sollte.</span><span class="sxs-lookup"><span data-stu-id="386a5-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="386a5-141">Wenn eine nächste oder vorherige Nachricht angezeigt wird, verwenden Sie das Fensterrechteck, das im  _prcPosRect-Parameter_ übergeben wird, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="386a5-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="386a5-142">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="386a5-142">MFCMAPI reference</span></span>

<span data-ttu-id="386a5-143">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="386a5-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="386a5-144">**Datei**</span><span class="sxs-lookup"><span data-stu-id="386a5-144">**File**</span></span>|<span data-ttu-id="386a5-145">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="386a5-145">**Function**</span></span>|<span data-ttu-id="386a5-146">**Comment**</span><span class="sxs-lookup"><span data-stu-id="386a5-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="386a5-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="386a5-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="386a5-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="386a5-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="386a5-149">MFCMAPI implementiert die **IMAPIViewContext::ActivateNext-Methode** in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="386a5-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="386a5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="386a5-150">See also</span></span>

- [<span data-ttu-id="386a5-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="386a5-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="386a5-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="386a5-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="386a5-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="386a5-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

