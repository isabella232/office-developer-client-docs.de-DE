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
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351156"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="307bb-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="307bb-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="307bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="307bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="307bb-105">Aktiviert die nächste oder vorherige Nachricht in der Ansichts Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="307bb-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="307bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="307bb-106">Parameters</span></span>

<span data-ttu-id="307bb-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="307bb-107">_ulDir_</span></span>
  
> <span data-ttu-id="307bb-108">in Status Kennzeichen mit Informationen über die zu aktivierende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="307bb-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="307bb-109">Gültige Flageinstellungen sind:</span><span class="sxs-lookup"><span data-stu-id="307bb-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="307bb-110">VCDIR_CATEGORY: der Viewer sollte eine Nachricht in einer anderen Kategorie der Ansicht aktivieren.</span><span class="sxs-lookup"><span data-stu-id="307bb-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="307bb-111">Die zu aktivierende Nachricht lautet:</span><span class="sxs-lookup"><span data-stu-id="307bb-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="307bb-112">Die erste Meldung in der nächsten Ansichtskategorie, wenn dieses Flag mit VCDIR_NEXT **oder**Ed ist.</span><span class="sxs-lookup"><span data-stu-id="307bb-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="307bb-113">Die letzte Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag mit VCDIR_PREV **oder**Ed ist und die vorherige Kategorie erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="307bb-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="307bb-114">Die erste Meldung in der Kategorie vorherige Ansicht, wenn dieses Flag mit VCDIR_PREV **oder**Ed ist und die vorherige Kategorie nicht erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="307bb-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="307bb-115">In diesem Fall wird die vorherige Kategorie automatisch erweitert.</span><span class="sxs-lookup"><span data-stu-id="307bb-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="307bb-116">VCDIR_DELETE: der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="307bb-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="307bb-117">VCDIR_MOVE: der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="307bb-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="307bb-118">VCDIR_NEXT: der Viewer sollte die nächste Nachricht in der Ansichts Reihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="307bb-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="307bb-119">VCDIR_PREV: der Viewer sollte die vorherige Nachricht im Ansichts Auftrag aktivieren.</span><span class="sxs-lookup"><span data-stu-id="307bb-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="307bb-120">VCDIR_UNREAD: der Viewer sollte die nächste oder vorherige ungelesene Nachricht in der Ansichts Reihenfolge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="307bb-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="307bb-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="307bb-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="307bb-122">in Zeiger auf eine Windows- **Rect** -Struktur mit der Größe und Position des Fensters, das zum Anzeigen der aktivierten Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="307bb-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="307bb-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="307bb-123">Return value</span></span>

<span data-ttu-id="307bb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="307bb-124">S_OK</span></span> 
  
> <span data-ttu-id="307bb-125">Die Nachricht wurde erfolgreich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="307bb-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="307bb-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="307bb-126">S_FALSE</span></span> 
  
> <span data-ttu-id="307bb-127">Die Nachricht wurde erfolgreich aktiviert, aber im Prozess wurde ein anderer Formulartyp geöffnet.</span><span class="sxs-lookup"><span data-stu-id="307bb-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="307bb-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="307bb-128">Remarks</span></span>

<span data-ttu-id="307bb-129">Formularobjekte rufen die **IMAPIViewContext:: ActivateNext** -Methode auf, um zu ändern, welche Nachricht dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="307bb-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="307bb-130">Der Wert, der im Parameter _ulDir_ übergeben wird, gibt an, welche Nachricht aktiviert werden soll und in einigen Fällen warum.</span><span class="sxs-lookup"><span data-stu-id="307bb-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="307bb-131">Die VCDIR_NEXT-und VCDIR_PREVIOUS-Flags entsprechen Benutzern, die den **nächsten** oder **vorherigen** Befehl in einer Ansicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="307bb-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="307bb-132">Diese Vorgänge entsprechen in der Regel dem nach oben oder nach unten eine Nachricht in der Liste der Nachrichten des Formular Viewers.</span><span class="sxs-lookup"><span data-stu-id="307bb-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="307bb-133">Die VCDIR_DELETE-und VCDIR_MOVE-Flags werden durch die Methoden [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="307bb-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="307bb-134">Implementierungen dieser Methoden rufen **ActivateNext** mit der entsprechenden Richtung auf und führen dann den angeforderten Vorgang für die Nachricht aus, wenn der **ActivateNext** -Aufruf nicht fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="307bb-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="307bb-135">In der Formularanzeige können Benutzer in der Regel die Richtung angeben, die in der Nachrichtenliste verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="307bb-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="307bb-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="307bb-136">Notes to implementers</span></span>

<span data-ttu-id="307bb-137">Die Implementierung von [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) macht die nächste oder vorherige Nachricht im Ordner abhängig vom Wert von _ulDir_, der aktuellen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="307bb-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="307bb-138">Rufen Sie nach dem Zurückgeben von **ActivateNext** [IMAPIMessageSite:: getMessage](imapimessagesite-getmessage.md) auf, um einen Zeiger auf die neu aktivierte Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="307bb-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="307bb-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="307bb-139">Notes to callers</span></span>

<span data-ttu-id="307bb-140">Wenn **ActivateNext** den Wert S_FALSE zurückgibt oder eine aktuelle Nachricht nicht vorhanden ist, führen Sie den normalen Shutdown-Vorgang aus, der den Aufruf der [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) -Methode des Formulars umfasst.</span><span class="sxs-lookup"><span data-stu-id="307bb-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="307bb-141">Wenn eine nächste oder eine vorherige Nachricht angezeigt wird, verwenden Sie das Fensterrechteck, das im _prcPosRect_ -Parameter übergeben wurde, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="307bb-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="307bb-142">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="307bb-142">MFCMAPI reference</span></span>

<span data-ttu-id="307bb-143">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="307bb-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="307bb-144">**Datei**</span><span class="sxs-lookup"><span data-stu-id="307bb-144">**File**</span></span>|<span data-ttu-id="307bb-145">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="307bb-145">**Function**</span></span>|<span data-ttu-id="307bb-146">**Comment**</span><span class="sxs-lookup"><span data-stu-id="307bb-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="307bb-147">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="307bb-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="307bb-148">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="307bb-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="307bb-149">MFCMAPI implementiert die **IMAPIViewContext:: ActivateNext** -Methode in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="307bb-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="307bb-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="307bb-150">See also</span></span>

- [<span data-ttu-id="307bb-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="307bb-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="307bb-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="307bb-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="307bb-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="307bb-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

