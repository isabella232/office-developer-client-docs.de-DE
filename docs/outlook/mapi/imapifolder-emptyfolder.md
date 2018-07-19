---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792122"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="40ec9-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="40ec9-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="40ec9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40ec9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40ec9-105">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst löschen.</span><span class="sxs-lookup"><span data-stu-id="40ec9-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="40ec9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40ec9-106">Parameters</span></span>

 <span data-ttu-id="40ec9-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="40ec9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="40ec9-108">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="40ec9-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="40ec9-109">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40ec9-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="40ec9-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="40ec9-110">_lpProgress_</span></span>
  
> <span data-ttu-id="40ec9-111">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40ec9-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="40ec9-112">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40ec9-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="40ec9-113">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40ec9-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="40ec9-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40ec9-114">_ulFlags_</span></span>
  
> <span data-ttu-id="40ec9-115">[in] Eine Bitmaske aus Flags, die steuert, wie der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="40ec9-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="40ec9-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="40ec9-116">The following flags can be set:</span></span>
    
<span data-ttu-id="40ec9-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="40ec9-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="40ec9-118">Löscht alle Unterordner, einschließlich Unterordner, die Nachrichten mit zugeordneten Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="40ec9-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="40ec9-119">Das Flag DEL_ASSOCIATED ist nur für Ordner der obersten Ebene, die, dem der Anruf auf fungiert.</span><span class="sxs-lookup"><span data-stu-id="40ec9-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="40ec9-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="40ec9-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="40ec9-121">Entfernt alle Nachrichten, einschließlich vorläufig Gelöschte Objekte.</span><span class="sxs-lookup"><span data-stu-id="40ec9-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="40ec9-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="40ec9-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="40ec9-123">Eine Statusanzeige angezeigt, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="40ec9-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40ec9-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40ec9-124">Return value</span></span>

<span data-ttu-id="40ec9-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="40ec9-125">S_OK</span></span> 
  
> <span data-ttu-id="40ec9-126">Der Ordner wurde erfolgreich geleert.</span><span class="sxs-lookup"><span data-stu-id="40ec9-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="40ec9-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="40ec9-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="40ec9-128">Der Aufruf war erfolgreich, aber der Ordner wurde nicht vollständig geleert.</span><span class="sxs-lookup"><span data-stu-id="40ec9-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="40ec9-129">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40ec9-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="40ec9-130">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="40ec9-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="40ec9-131">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="40ec9-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40ec9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40ec9-132">Remarks</span></span>

<span data-ttu-id="40ec9-133">Die **IMAPIFolder::EmptyFolder** -Methode löscht alle eines Ordners ohne den Ordner selbst löschen.</span><span class="sxs-lookup"><span data-stu-id="40ec9-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="40ec9-134">Während eines Anrufs **EmptyFolder** werden gesendete Nachrichten nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="40ec9-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="40ec9-135">Zugehörige Inhalt eines Ordners enthalten Nachrichten, die Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefinierte im Lösungsspeicher beschreiben und können auch Formulardefinitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="40ec9-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="40ec9-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="40ec9-136">Notes to implementers</span></span>

<span data-ttu-id="40ec9-137">Rufen Sie die [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) -Methode nicht für Nachrichten in den Ordner, die gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="40ec9-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="40ec9-138">Gesendete Nachrichten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="40ec9-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="40ec9-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="40ec9-139">Notes to callers</span></span>

<span data-ttu-id="40ec9-140">Diese Rückgabewerte unter folgenden Umständen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="40ec9-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="40ec9-141">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="40ec9-141">**Condition**</span></span>|<span data-ttu-id="40ec9-142">**Rückgabewert**</span><span class="sxs-lookup"><span data-stu-id="40ec9-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40ec9-143">**EmptyFolder** wurde erfolgreich den Ordner geleert.</span><span class="sxs-lookup"><span data-stu-id="40ec9-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="40ec9-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="40ec9-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="40ec9-145">**EmptyFolder** konnte den Ordner zu leeren.</span><span class="sxs-lookup"><span data-stu-id="40ec9-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="40ec9-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="40ec9-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="40ec9-147">**EmptyFolder** konnte nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="40ec9-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="40ec9-148">Einen anderen Fehlerwert als</span><span class="sxs-lookup"><span data-stu-id="40ec9-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="40ec9-149">Wenn **EmptyFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="40ec9-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="40ec9-150">Möglicherweise wurden **EmptyFolder** können einige der Inhalt des Ordners löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="40ec9-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="40ec9-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="40ec9-151">MFCMAPI reference</span></span>

<span data-ttu-id="40ec9-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="40ec9-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40ec9-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="40ec9-153">**File**</span></span>|<span data-ttu-id="40ec9-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="40ec9-154">**Function**</span></span>|<span data-ttu-id="40ec9-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="40ec9-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40ec9-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="40ec9-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="40ec9-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="40ec9-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="40ec9-158">MFCMAPI (engl.) verwendet die **IMAPIFolder::EmptyFolder** -Methode, um den Inhalt des angegebenen Ordners zu löschen.</span><span class="sxs-lookup"><span data-stu-id="40ec9-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40ec9-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40ec9-159">See also</span></span>



[<span data-ttu-id="40ec9-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="40ec9-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="40ec9-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="40ec9-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="40ec9-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="40ec9-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="40ec9-163">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="40ec9-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

