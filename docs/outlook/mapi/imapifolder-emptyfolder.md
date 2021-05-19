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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416783"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="8b8a2-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="8b8a2-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="8b8a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b8a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b8a2-105">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8b8a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b8a2-106">Parameters</span></span>

 <span data-ttu-id="8b8a2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8b8a2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8b8a2-108">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="8b8a2-109">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8b8a2-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8b8a2-110">_lpProgress_</span></span>
  
> <span data-ttu-id="8b8a2-111">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="8b8a2-112">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="8b8a2-113">Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8b8a2-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b8a2-114">_ulFlags_</span></span>
  
> <span data-ttu-id="8b8a2-115">[in] Eine Bitmaske mit Flags, die steuert, wie der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="8b8a2-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8b8a2-116">The following flags can be set:</span></span>
    
<span data-ttu-id="8b8a2-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="8b8a2-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="8b8a2-118">Löscht alle Unterordner, einschließlich Unterordner, die Nachrichten mit zugeordneten Inhalten enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="8b8a2-119">Das DEL_ASSOCIATED hat nur eine Bedeutung für den Ordner auf oberster Ebene, auf dem der Anruf funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="8b8a2-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="8b8a2-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="8b8a2-121">Entfernt dauerhaft alle Nachrichten, einschließlich der gelöschten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="8b8a2-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8b8a2-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="8b8a2-123">Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b8a2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b8a2-124">Return value</span></span>

<span data-ttu-id="8b8a2-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-125">S_OK</span></span> 
  
> <span data-ttu-id="8b8a2-126">Der Ordner wurde erfolgreich geleert.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="8b8a2-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8b8a2-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="8b8a2-128">Der Aufruf ist erfolgreich, der Ordner wurde jedoch nicht vollständig geleert.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="8b8a2-129">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8b8a2-130">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8b8a2-131">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8b8a2-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b8a2-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b8a2-132">Remarks</span></span>

<span data-ttu-id="8b8a2-133">Die **IMAPIFolder::EmptyFolder-Methode** löscht alle Inhalte eines Ordners, ohne den Ordner selbst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="8b8a2-134">Während eines **EmptyFolder-Anrufs** werden übermittelte Nachrichten nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="8b8a2-135">Zu den zugeordneten Inhalten eines Ordners gehören Nachrichten, die zum Beschreiben von Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefiniertem Lösungsspeicher verwendet werden, und können auch Formulardefinitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b8a2-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8b8a2-136">Notes to implementers</span></span>

<span data-ttu-id="8b8a2-137">Rufen Sie die [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) nicht für Nachrichten im Ordner auf, die übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="8b8a2-138">Übermittelte Nachrichten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8b8a2-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8b8a2-139">Notes to callers</span></span>

<span data-ttu-id="8b8a2-140">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="8b8a2-141">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="8b8a2-141">**Condition**</span></span>|<span data-ttu-id="8b8a2-142">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="8b8a2-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b8a2-143">**EmptyFolder** hat den Ordner erfolgreich geleert.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="8b8a2-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="8b8a2-145">**EmptyFolder** konnte den Ordner nicht vollständig leeren.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="8b8a2-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8b8a2-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="8b8a2-147">**EmptyFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="8b8a2-148">Beliebiger Fehlerwert</span><span class="sxs-lookup"><span data-stu-id="8b8a2-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="8b8a2-149">Wenn **EmptyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="8b8a2-150">**EmptyFolder** konnte möglicherweise einige Inhalte des Ordners löschen, bevor der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8b8a2-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8b8a2-151">MFCMAPI reference</span></span>

<span data-ttu-id="8b8a2-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8b8a2-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8b8a2-153">**File**</span></span>|<span data-ttu-id="8b8a2-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8b8a2-154">**Function**</span></span>|<span data-ttu-id="8b8a2-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8b8a2-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b8a2-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8b8a2-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="8b8a2-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="8b8a2-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="8b8a2-158">MFCMAPI verwendet die **IMAPIFolder::EmptyFolder-Methode,** um den Inhalt des angegebenen Ordners zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b8a2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b8a2-159">See also</span></span>



[<span data-ttu-id="8b8a2-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="8b8a2-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="8b8a2-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8b8a2-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="8b8a2-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8b8a2-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8b8a2-163">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="8b8a2-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

