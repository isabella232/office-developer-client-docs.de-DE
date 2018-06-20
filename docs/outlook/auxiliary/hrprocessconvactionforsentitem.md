---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Dient zum Senden nach der Kategorisierung auf ein e-Mail-Element basierend auf der PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790954"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="c14b3-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="c14b3-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="c14b3-104">Dient zum Senden nach der Kategorisierung auf ein e-Mail-Element basierend auf der [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c14b3-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c14b3-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c14b3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c14b3-106">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="c14b3-106">Exported by:</span></span>  <br/> |<span data-ttu-id="c14b3-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="c14b3-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="c14b3-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c14b3-108">Called by:</span></span>  <br/> |<span data-ttu-id="c14b3-109">Client</span><span class="sxs-lookup"><span data-stu-id="c14b3-109">Client</span></span>  <br/> |
|<span data-ttu-id="c14b3-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c14b3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c14b3-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="c14b3-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="c14b3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c14b3-112">Parameters</span></span>

<span data-ttu-id="c14b3-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="c14b3-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="c14b3-114">[in] Die [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) der im Store oder der [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des e-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="c14b3-114">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="c14b3-115">Kann nicht NULL sein oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="c14b3-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="c14b3-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="c14b3-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="c14b3-117">[in] Die [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des e-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="c14b3-117">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="c14b3-118">Kann nicht NULL sein oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="c14b3-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="c14b3-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="c14b3-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="c14b3-120">[in] Die [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des e-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="c14b3-120">[in] The [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="c14b3-121">Kann nicht NULL sein oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="c14b3-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="c14b3-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="c14b3-122">_dwFlags_</span></span>
  
> <span data-ttu-id="c14b3-123">[in] Eine Bitmaske, die zusätzliche Informationen über den Aufruf der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="c14b3-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="c14b3-124">0 – keine zusätzlichen Optionen in diesem Methodenaufruf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c14b3-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="c14b3-125">Dies ist der empfohlene Wert.</span><span class="sxs-lookup"><span data-stu-id="c14b3-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="c14b3-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**– _PmbinMsgEid_ ist tatsächlich [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c14b3-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="c14b3-127">Verwenden einer **PidTagSearchKey** ressourcenintensiv und sollte vermieden werden, wenn eine [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c14b3-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c14b3-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c14b3-128">Return values</span></span>

|<span data-ttu-id="c14b3-129">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="c14b3-129">**HRESULT**</span></span>|<span data-ttu-id="c14b3-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c14b3-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c14b3-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="c14b3-131">S_OK</span></span>  <br/> |<span data-ttu-id="c14b3-132">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c14b3-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="c14b3-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c14b3-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="c14b3-134">_DwFlags_ enthält eine unbekannte Kennzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c14b3-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c14b3-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c14b3-135">Remarks</span></span>

<span data-ttu-id="c14b3-136">Kategorien werden persönlichen Informationen berücksichtigt und sollten nicht außerhalb des Postfachs des Benutzers übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c14b3-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="c14b3-137">Rufen Sie daher nicht **HrProcessConvActionForSentItem** für ein Element nicht gesendeten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c14b3-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="c14b3-138">Stattdessen senden Sie des Elements, und rufen Sie dann auf der archivierten **HrProcessConvActionForSentItem** .</span><span class="sxs-lookup"><span data-stu-id="c14b3-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="c14b3-139">Der archivierten kann in den Ordner Gesendete Objekte oder einen entsprechenden Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c14b3-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="c14b3-140">Ihre Anwendung muss in-Process mit Outlook.exe, z. B. von einem COM-add-in, **HrProcessConvActionForSentItem**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c14b3-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="c14b3-141">Wenn Sie versuchen, **HrProcessConvActionForSentItem** Out-of-Process aufrufen, wird **HrProcessConvActionForSentItem** eine zugriffsverletzung Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c14b3-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

