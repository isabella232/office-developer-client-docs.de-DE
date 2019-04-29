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
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="59a68-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="59a68-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="59a68-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59a68-105">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="59a68-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="59a68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59a68-106">Parameters</span></span>

 <span data-ttu-id="59a68-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="59a68-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="59a68-108">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="59a68-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="59a68-109">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59a68-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="59a68-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="59a68-110">_lpProgress_</span></span>
  
> <span data-ttu-id="59a68-111">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="59a68-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="59a68-112">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="59a68-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="59a68-113">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59a68-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="59a68-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59a68-114">_ulFlags_</span></span>
  
> <span data-ttu-id="59a68-115">in Eine Bitmaske von Flags, die steuert, wie der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="59a68-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="59a68-116">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="59a68-116">The following flags can be set:</span></span>
    
<span data-ttu-id="59a68-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="59a68-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="59a68-118">Löscht alle Unterordner, einschließlich der Unterordner, die Nachrichten mit dem dazugehörigen Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="59a68-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="59a68-119">Das DEL_ASSOCIATED-Flag hat nur für den Ordner auf oberster Ebene eine Bedeutung, für den der Anruf fungiert.</span><span class="sxs-lookup"><span data-stu-id="59a68-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="59a68-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="59a68-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="59a68-121">Entfernt alle Nachrichten, einschließlich der gelöschten, dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="59a68-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="59a68-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="59a68-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="59a68-123">Zeigt während des Vorgangs eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="59a68-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59a68-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59a68-124">Return value</span></span>

<span data-ttu-id="59a68-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="59a68-125">S_OK</span></span> 
  
> <span data-ttu-id="59a68-126">Der Ordner wurde erfolgreich geleert.</span><span class="sxs-lookup"><span data-stu-id="59a68-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="59a68-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="59a68-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="59a68-128">Der Aufruf war erfolgreich, aber der Ordner wurde nicht vollständig geleert.</span><span class="sxs-lookup"><span data-stu-id="59a68-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="59a68-129">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="59a68-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="59a68-130">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="59a68-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="59a68-131">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="59a68-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59a68-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59a68-132">Remarks</span></span>

<span data-ttu-id="59a68-133">Mit der **IMAPIFolder:: EmptyFolder** -Methode werden alle Inhalte eines Ordners gelöscht, ohne dass der Ordner selbst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="59a68-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="59a68-134">Während eines **EmptyFolder** -Aufrufs werden übermittelte Nachrichten nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="59a68-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="59a68-135">Zu den zugeordneten Inhalten eines Ordners gehören Nachrichten, die zum Beschreiben von Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefiniertem Lösungsspeicher verwendet werden, und können auch Formulardefinitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59a68-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="59a68-136">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="59a68-136">Notes to implementers</span></span>

<span data-ttu-id="59a68-137">Rufen Sie die [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) -Methode nicht für Nachrichten im Ordner auf, die übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="59a68-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="59a68-138">ÜberMittelte Nachrichten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="59a68-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="59a68-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="59a68-139">Notes to callers</span></span>

<span data-ttu-id="59a68-140">Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="59a68-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="59a68-141">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="59a68-141">**Condition**</span></span>|<span data-ttu-id="59a68-142">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="59a68-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59a68-143">**EmptyFolder** hat den Ordner erfolgreich geleert.</span><span class="sxs-lookup"><span data-stu-id="59a68-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="59a68-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="59a68-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="59a68-145">**EmptyFolder** konnte den Ordner nicht vollständig leeren.</span><span class="sxs-lookup"><span data-stu-id="59a68-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="59a68-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="59a68-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="59a68-147">**EmptyFolder** konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="59a68-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="59a68-148">Beliebiger Fehlerwert</span><span class="sxs-lookup"><span data-stu-id="59a68-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="59a68-149">Wenn **EmptyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="59a68-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="59a68-150">**EmptyFolder** kann möglicherweise einige Inhalte des Ordners löschen, bevor der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="59a68-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="59a68-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="59a68-151">MFCMAPI reference</span></span>

<span data-ttu-id="59a68-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59a68-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="59a68-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="59a68-153">**File**</span></span>|<span data-ttu-id="59a68-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="59a68-154">**Function**</span></span>|<span data-ttu-id="59a68-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="59a68-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59a68-156">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="59a68-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="59a68-157">CMsgStoreDlg:: OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="59a68-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="59a68-158">MFCMAPI verwendet die **IMAPIFolder:: EmptyFolder** -Methode, um den Inhalt des angegebenen Ordners zu löschen.</span><span class="sxs-lookup"><span data-stu-id="59a68-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59a68-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a68-159">See also</span></span>



[<span data-ttu-id="59a68-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="59a68-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="59a68-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="59a68-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="59a68-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="59a68-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="59a68-163">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="59a68-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

