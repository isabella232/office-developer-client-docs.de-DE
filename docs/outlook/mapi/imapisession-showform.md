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
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335665"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="a13d7-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="a13d7-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="a13d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a13d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a13d7-105">Zeigt ein Formular an.</span><span class="sxs-lookup"><span data-stu-id="a13d7-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a13d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a13d7-106">Parameters</span></span>

 <span data-ttu-id="a13d7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a13d7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a13d7-108">in Ein Handle für das übergeordnete Fenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="a13d7-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="a13d7-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a13d7-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="a13d7-110">in Ein Zeiger auf den Nachrichtenspeicher, der den Ordner enthält, auf den durch den _lpParentFolder_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a13d7-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="a13d7-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="a13d7-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="a13d7-112">in Ein Zeiger auf den Ordner, in dem die dem _ulMessageToken_ -Parameter zugeordnete Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a13d7-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="a13d7-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a13d7-113">_lpInterface_</span></span>
  
> <span data-ttu-id="a13d7-114">in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf die im Formular angezeigte Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a13d7-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="a13d7-115">Der _lpInterface_ -Parameter muss NULL oder IID_IMessage sein.</span><span class="sxs-lookup"><span data-stu-id="a13d7-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="a13d7-116">Übergeben von NULL-Ergebnissen in der Standardschnittstelle, [IMessage](imessageimapiprop.md), wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13d7-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="a13d7-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="a13d7-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="a13d7-118">in Das Token, das der im Formular anzuzeigenden Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a13d7-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="a13d7-119">Der _ulMessageToken_ -Parameter muss auf den Inhalt des paraMeters _lpulMessageToken_ des vorherigen Aufrufs an IMAPISession festgelegt werden [::P repareform](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="a13d7-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="a13d7-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="a13d7-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="a13d7-121">in Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a13d7-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="a13d7-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a13d7-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a13d7-123">in Eine Bitmaske von Flags, die Steuern, wie und ob die Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a13d7-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="a13d7-124">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a13d7-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a13d7-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a13d7-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="a13d7-126">Die Nachricht wurde nie gespeichert (das heißt, Ihre [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode wurde nie aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="a13d7-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="a13d7-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a13d7-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="a13d7-128">Die Nachricht sollte im übergeordneten Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a13d7-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="a13d7-129">Die Nachricht wird nicht zum Senden verarbeitet, sondern stattdessen in den Ordner geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a13d7-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="a13d7-130">Wenn dieses Flag nicht festgelegt ist, wird die Nachricht in den Postausgang kopiert und zum Senden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a13d7-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="a13d7-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a13d7-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="a13d7-132">in Eine Bitmaske von Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der dem Token im _ulMessageToken_ -Parameter zugeordneten Nachricht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="a13d7-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a13d7-133">Die Flags enthalten Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a13d7-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="a13d7-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="a13d7-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="a13d7-135">in Eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der dem Token im _ulMessageToken_ -Parameter zugeordneten Nachricht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="a13d7-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a13d7-136">Diese Kennzeichnungen enthalten weitere Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a13d7-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="a13d7-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="a13d7-137">_ulAccess_</span></span>
  
> <span data-ttu-id="a13d7-138">in Ein Flag, das die Berechtigungsstufe für die im Formular angezeigte Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="a13d7-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="a13d7-139">Diese Informationen werden aus der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft der Nachricht kopiert, die dem Token im _ulMessageToken_ -Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a13d7-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="a13d7-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a13d7-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="a13d7-141">in Ein Zeiger auf die Nachrichtenklasse der Nachricht, die im Formular angezeigt wird, kopiert aus der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der Nachricht, die dem Token im _ulMessageToken_ -Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a13d7-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a13d7-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a13d7-142">Return value</span></span>

<span data-ttu-id="a13d7-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="a13d7-143">S_OK</span></span> 
  
> <span data-ttu-id="a13d7-144">Das Formular wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a13d7-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="a13d7-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a13d7-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a13d7-146">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a13d7-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a13d7-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a13d7-147">Remarks</span></span>

<span data-ttu-id="a13d7-148">Die **IMAPISession:: ShowForm** -Methode zeigt ein Nachrichtenformular an, das von der **IMAPISession::P repareform** -Methode vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a13d7-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a13d7-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a13d7-149">Notes to callers</span></span>

<span data-ttu-id="a13d7-150">Sie sollten nur einen einzigen Verweis auf die Nachricht haben, die im _lpMessage_ -Parameter der **PrepareForm** -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a13d7-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="a13d7-151">Beachten Sie, dass Formular Implementierungen andere Fehlerwerte als die unter MAPI zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="a13d7-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="a13d7-152">Wenn Sie diese Fehlerwerte verwenden können, um eine genauere Ermittlung der Fehlerbedingung vorzunehmen, tun Sie dies.</span><span class="sxs-lookup"><span data-stu-id="a13d7-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="a13d7-153">Andernfalls behandeln Sie diese Fehler wie MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a13d7-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a13d7-154">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a13d7-154">MFCMAPI reference</span></span>

<span data-ttu-id="a13d7-155">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a13d7-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a13d7-156">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a13d7-156">**File**</span></span>|<span data-ttu-id="a13d7-157">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a13d7-157">**Function**</span></span>|<span data-ttu-id="a13d7-158">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a13d7-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a13d7-159">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="a13d7-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a13d7-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="a13d7-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="a13d7-161">MFCMAPI verwendet die **IMAPISession:: ShowForm** -Methode zusammen mit der **PrepareForm** -Methode, um eine Nachricht in einem modalen Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a13d7-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a13d7-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a13d7-162">See also</span></span>



[<span data-ttu-id="a13d7-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a13d7-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a13d7-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a13d7-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="a13d7-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a13d7-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="a13d7-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a13d7-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a13d7-167">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a13d7-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

