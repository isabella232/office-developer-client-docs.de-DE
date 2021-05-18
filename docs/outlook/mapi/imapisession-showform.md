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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412527"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="56dd5-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="56dd5-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="56dd5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56dd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56dd5-105">Zeigt ein Formular an.</span><span class="sxs-lookup"><span data-stu-id="56dd5-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="56dd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56dd5-106">Parameters</span></span>

 <span data-ttu-id="56dd5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="56dd5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="56dd5-108">[in] Ein Handle zum übergeordneten Fenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="56dd5-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="56dd5-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="56dd5-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="56dd5-110">[in] Ein Zeiger auf den Nachrichtenspeicher, der den Ordner enthält, auf den der  _lpParentFolder-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="56dd5-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="56dd5-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="56dd5-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="56dd5-112">[in] Ein Zeiger auf den Ordner, in dem die dem  _ulMessageToken-Parameter zugeordnete_ Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="56dd5-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="56dd5-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="56dd5-113">_lpInterface_</span></span>
  
> <span data-ttu-id="56dd5-114">[in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf die im Formular angezeigte Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56dd5-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="56dd5-115">Der  _lpInterface-Parameter_ muss NULL oder IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="56dd5-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="56dd5-116">Das Übergeben von NULL führt dazu, dass die Standardschnittstelle [IMessage](imessageimapiprop.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56dd5-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="56dd5-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="56dd5-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="56dd5-118">[in] Das Token, das der nachricht zugeordnet ist, die im Formular angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56dd5-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="56dd5-119">Der _ulMessageToken-Parameter_ muss auf den Inhalt des _lpulMessageToken-Parameters_ aus dem vorherigen Aufruf von [IMAPISession::P repareForm festgelegt werden.](imapisession-prepareform.md)</span><span class="sxs-lookup"><span data-stu-id="56dd5-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="56dd5-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="56dd5-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="56dd5-121">[in] Reserviert; muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="56dd5-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="56dd5-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56dd5-122">_ulFlags_</span></span>
  
> <span data-ttu-id="56dd5-123">[in] Eine Bitmaske mit Flags, die steuert, wie und ob die Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="56dd5-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="56dd5-124">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="56dd5-124">The following flags can be set:</span></span>
    
<span data-ttu-id="56dd5-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="56dd5-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="56dd5-126">Die Nachricht wurde nie gespeichert (d. h., die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) wurde nie aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="56dd5-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="56dd5-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="56dd5-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="56dd5-128">Die Nachricht sollte im übergeordneten Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="56dd5-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="56dd5-129">Die Nachricht wird nicht zum Senden verarbeitet, sondern stattdessen im Ordner bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="56dd5-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="56dd5-130">Wenn dieses Flag nicht festgelegt ist, wird die Nachricht in den Posteingang kopiert und zum Senden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56dd5-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="56dd5-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="56dd5-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="56dd5-132">[in] Eine Bitmaske mit **Flags,** die aus der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft der Nachricht kopiert wurden, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="56dd5-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="56dd5-133">Die Flags enthalten Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="56dd5-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="56dd5-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="56dd5-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="56dd5-135">[in] Eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="56dd5-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="56dd5-136">Diese Flags enthalten weitere Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="56dd5-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="56dd5-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="56dd5-137">_ulAccess_</span></span>
  
> <span data-ttu-id="56dd5-138">[in] Ein Flag, das die Berechtigungsstufe für die Nachricht angibt, die im Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="56dd5-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="56dd5-139">Diese Informationen werden aus der **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) der Nachricht kopiert, die dem Token im  _ulMessageToken-Parameter zugeordnet_ ist.</span><span class="sxs-lookup"><span data-stu-id="56dd5-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="56dd5-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="56dd5-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="56dd5-141">[in] Ein Zeiger auf die Nachrichtenklasse der Nachricht, die im Formular angezeigt wird, der aus der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der Nachricht kopiert wird, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="56dd5-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56dd5-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56dd5-142">Return value</span></span>

<span data-ttu-id="56dd5-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="56dd5-143">S_OK</span></span> 
  
> <span data-ttu-id="56dd5-144">Das Formular wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56dd5-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="56dd5-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="56dd5-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="56dd5-146">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="56dd5-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="56dd5-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56dd5-147">Remarks</span></span>

<span data-ttu-id="56dd5-148">Die **IMAPISession::ShowForm-Methode** zeigt ein Nachrichtenformular an, das von der **IMAPISession::P repareForm-Methode vorbereitet** wurde.</span><span class="sxs-lookup"><span data-stu-id="56dd5-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="56dd5-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="56dd5-149">Notes to callers</span></span>

<span data-ttu-id="56dd5-150">Sie sollten nur einen einzigen Verweis auf die Nachricht haben, die im _lpMessage-Parameter_ der **PrepareForm-Methode** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="56dd5-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="56dd5-151">Beachten Sie, dass Formularimplementierung andere Fehlerwerte als die von MAPI dokumentierten zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="56dd5-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="56dd5-152">Wenn Sie diese Fehlerwerte verwenden können, um die Fehlerbedingung genauer zu bestimmen, tun Sie dies.</span><span class="sxs-lookup"><span data-stu-id="56dd5-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="56dd5-153">Behandeln Sie andernfalls diese Fehler so, wie Sie MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="56dd5-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="56dd5-154">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="56dd5-154">MFCMAPI reference</span></span>

<span data-ttu-id="56dd5-155">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="56dd5-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="56dd5-156">**Datei**</span><span class="sxs-lookup"><span data-stu-id="56dd5-156">**File**</span></span>|<span data-ttu-id="56dd5-157">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="56dd5-157">**Function**</span></span>|<span data-ttu-id="56dd5-158">**Comment**</span><span class="sxs-lookup"><span data-stu-id="56dd5-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56dd5-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="56dd5-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="56dd5-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="56dd5-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="56dd5-161">MFCMAPI verwendet die **IMAPISession::ShowForm-Methode** zusammen mit der **PrepareForm-Methode,** um eine Nachricht in einem modalen Formular zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="56dd5-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56dd5-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56dd5-162">See also</span></span>



[<span data-ttu-id="56dd5-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="56dd5-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="56dd5-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56dd5-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="56dd5-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="56dd5-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="56dd5-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56dd5-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="56dd5-167">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="56dd5-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

