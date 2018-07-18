---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792333"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="b5822-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="b5822-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="b5822-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5822-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5822-105">Zeigt ein Formular an.</span><span class="sxs-lookup"><span data-stu-id="b5822-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="b5822-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5822-106">Parameters</span></span>

 <span data-ttu-id="b5822-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b5822-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b5822-108">[in] Ein Handle für das übergeordnete Fenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="b5822-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="b5822-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="b5822-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="b5822-110">[in] Ein Zeiger auf den Nachrichtenspeicher mit dem Ordner, auf den durch den Parameter _LpParentFolder_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="b5822-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="b5822-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="b5822-112">[in] Ein Zeiger auf den Ordner, in dem die Nachricht mit dem Parameter _UlMessageToken_ verbundenen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5822-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="b5822-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b5822-113">_lpInterface_</span></span>
  
> <span data-ttu-id="b5822-114">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um die Nachricht zuzugreifen, die in dem Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="b5822-115">Der Parameter _LpInterface_ muss NULL oder IID_IMessage sein.</span><span class="sxs-lookup"><span data-stu-id="b5822-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="b5822-116">Bei Übergabe von NULL führt die standard-Schnittstelle, [IMessage](imessageimapiprop.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="b5822-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="b5822-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="b5822-118">[in] Das Token, das die Nachricht im Formular anzuzeigende zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5822-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="b5822-119">Der Parameter _UlMessageToken_ muss auf den Inhalt des Parameters _LpulMessageToken_ aus dem vorherigen Aufruf von [IMAPISession::PrepareForm](imapisession-prepareform.md)festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b5822-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="b5822-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="b5822-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="b5822-121">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b5822-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="b5822-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5822-122">_ulFlags_</span></span>
  
> <span data-ttu-id="b5822-123">[in] Eine Bitmaske aus Flags, die steuert, ob und wie die Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="b5822-124">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b5822-124">The following flags can be set:</span></span>
    
<span data-ttu-id="b5822-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b5822-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="b5822-126">Die Nachricht wurde noch nie gespeichert wurde (d. h., seine [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode noch nie aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="b5822-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="b5822-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b5822-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="b5822-128">Die Nachricht sollte in seinem übergeordneten Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b5822-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="b5822-129">Die Nachricht wird nicht für das Senden von verarbeitet, aber es wird in den Ordner bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b5822-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="b5822-130">Wenn dieses Flag nicht festgelegt ist, wird die Nachricht im Ordner Postausgang kopiert und für das Senden von verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="b5822-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="b5822-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="b5822-132">[in] Eine Bitmaske aus Flags, die von der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert.</span><span class="sxs-lookup"><span data-stu-id="b5822-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="b5822-133">Die Kennzeichen liefern Informationen zu den Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b5822-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="b5822-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="b5822-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="b5822-135">[in] Eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert.</span><span class="sxs-lookup"><span data-stu-id="b5822-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="b5822-136">Diese Flags bieten weitere Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b5822-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="b5822-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="b5822-137">_ulAccess_</span></span>
  
> <span data-ttu-id="b5822-138">[in] Ein Flag, das die Berechtigungsstufe für die Nachricht gibt an, die im Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5822-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="b5822-139">Diese Informationen werden aus der Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert.</span><span class="sxs-lookup"><span data-stu-id="b5822-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="b5822-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="b5822-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b5822-141">[in] Ein Zeiger auf die Nachrichtenklasse der Nachricht angezeigt wird, klicken Sie im Formular aus der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert.</span><span class="sxs-lookup"><span data-stu-id="b5822-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5822-142">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b5822-142">Return value</span></span>

<span data-ttu-id="b5822-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5822-143">S_OK</span></span> 
  
> <span data-ttu-id="b5822-144">Das Formular wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5822-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="b5822-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b5822-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b5822-146">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b5822-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b5822-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5822-147">Remarks</span></span>

<span data-ttu-id="b5822-148">Die **IMAPISession::ShowForm** -Methode zeigt ein Formular für Nachrichten, die von der **IMAPISession::PrepareForm** -Methode vorbereitet wurden.</span><span class="sxs-lookup"><span data-stu-id="b5822-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b5822-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b5822-149">Notes to callers</span></span>

<span data-ttu-id="b5822-150">Sie sollten nur einen Verweis auf die Nachricht im _LpMessage_ -Parameter der **PrepareForm** -Methode übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="b5822-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="b5822-151">Beachten Sie, dass das Formular Implementierungen Fehlerwerte als derjenigen, die von MAPI dokumentiert zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="b5822-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="b5822-152">Wenn Sie diese Fehlerwerte verwenden können, um eine genauere Bestimmung des Fehlers, dazu.</span><span class="sxs-lookup"><span data-stu-id="b5822-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="b5822-153">Anderenfalls behandeln Sie diese Fehler wie MAPI_E_CALL_FAILED behandeln.</span><span class="sxs-lookup"><span data-stu-id="b5822-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b5822-154">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="b5822-154">MFCMAPI reference</span></span>

<span data-ttu-id="b5822-155">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b5822-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b5822-156">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b5822-156">**File**</span></span>|<span data-ttu-id="b5822-157">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b5822-157">**Function**</span></span>|<span data-ttu-id="b5822-158">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b5822-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5822-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b5822-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b5822-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="b5822-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="b5822-161">MFCMAPI (engl.) verwendet die **IMAPISession::ShowForm** -Methode, zusammen mit der **PrepareForm** -Methode, um eine Nachricht in ein modales Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b5822-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5822-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5822-162">See also</span></span>



[<span data-ttu-id="b5822-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b5822-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="b5822-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b5822-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="b5822-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="b5822-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="b5822-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5822-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b5822-167">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b5822-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

