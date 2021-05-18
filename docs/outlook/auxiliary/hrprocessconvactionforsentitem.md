---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Führt eine Post-Send-Kategorisierung für ein E-Mail-Element basierend auf seiner PidTagConversationId durch.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318900"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="93266-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="93266-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="93266-104">Führt die Post-Send-Kategorisierung für ein E-Mail-Element basierend auf seiner [PidTagConversationId aus.](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93266-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="93266-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="93266-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93266-106">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="93266-106">Exported by:</span></span>  <br/> |<span data-ttu-id="93266-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="93266-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="93266-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="93266-108">Called by:</span></span>  <br/> |<span data-ttu-id="93266-109">Client</span><span class="sxs-lookup"><span data-stu-id="93266-109">Client</span></span>  <br/> |
|<span data-ttu-id="93266-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="93266-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="93266-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="93266-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="93266-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93266-112">Parameters</span></span>

<span data-ttu-id="93266-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="93266-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="93266-114">[in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des Speichers oder [die PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des E-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="93266-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="93266-115">Kann nicht NULL oder ungültig sein.</span><span class="sxs-lookup"><span data-stu-id="93266-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="93266-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="93266-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="93266-117">[in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des E-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="93266-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="93266-118">Kann nicht NULL oder ungültig sein.</span><span class="sxs-lookup"><span data-stu-id="93266-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="93266-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="93266-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="93266-120">[in] Die [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des E-Mail-Elements.</span><span class="sxs-lookup"><span data-stu-id="93266-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="93266-121">Kann nicht NULL oder ungültig sein.</span><span class="sxs-lookup"><span data-stu-id="93266-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="93266-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="93266-122">_dwFlags_</span></span>
  
> <span data-ttu-id="93266-123">[in] Eine Bitmaske, die zusätzliche Informationen zum Methodenaufruf angibt.</span><span class="sxs-lookup"><span data-stu-id="93266-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="93266-124">0 – In diesem Methodenaufruf werden keine zusätzlichen Optionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="93266-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="93266-125">Dies ist der empfohlene Wert.</span><span class="sxs-lookup"><span data-stu-id="93266-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="93266-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**– _pmbinMsgEid_ ist tatsächlich [der PidTagSearchKey der](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="93266-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="93266-127">Die Verwendung **eines PidTagSearchKey** ist ressourcenintensiv und sollte vermieden werden, wenn [eine PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="93266-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="93266-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="93266-128">Return values</span></span>

|<span data-ttu-id="93266-129">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="93266-129">**HRESULT**</span></span>|<span data-ttu-id="93266-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="93266-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93266-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="93266-131">S_OK</span></span>  <br/> |<span data-ttu-id="93266-132">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="93266-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="93266-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="93266-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="93266-134">_dwFlags_ enthält ein unbekanntes Flag.</span><span class="sxs-lookup"><span data-stu-id="93266-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93266-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93266-135">Remarks</span></span>

<span data-ttu-id="93266-136">Kategorien gelten als persönliche Informationen und sollten nicht außerhalb des Postfachs des Benutzers übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="93266-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="93266-137">Rufen Sie daher **hrProcessConvActionForSentItem** nicht für ein nicht gesendetes E-Mail-Element auf.</span><span class="sxs-lookup"><span data-stu-id="93266-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="93266-138">Senden Sie stattdessen das Element, und rufen Sie **dann HrProcessConvActionForSentItem** für die archivierte Kopie auf.</span><span class="sxs-lookup"><span data-stu-id="93266-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="93266-139">Die archivierte Kopie kann im Ordner "Gesendete Elemente" oder an einem entsprechenden Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="93266-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="93266-140">Ihre Anwendung muss mit Outlook.exe, z. B. von einem COM-Add-In, in Prozess sein, um **HrProcessConvActionForSentItem aufrufen** zu können.</span><span class="sxs-lookup"><span data-stu-id="93266-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="93266-141">Wenn Sie versuchen, **HrProcessConvActionForSentItem** nicht mehr zu verarbeiten, wird von **HrProcessConvActionForSentItem** eine Zugriffsverletzungsausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="93266-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

