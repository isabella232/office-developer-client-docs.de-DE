---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581776"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="4e0e7-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="4e0e7-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="4e0e7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e0e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e0e7-105">Gibt an, ob Microsoft Office Outlook-Ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgaben Ordner, auf Start, um das Füllen Sie im Navigationsbereich gescannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4e0e7-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4e0e7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e0e7-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="4e0e7-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="4e0e7-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="4e0e7-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-109">Created by:</span></span>  <br/> |<span data-ttu-id="4e0e7-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="4e0e7-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="4e0e7-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="4e0e7-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="4e0e7-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="4e0e7-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-113">Property type:</span></span>  <br/> |<span data-ttu-id="4e0e7-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4e0e7-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4e0e7-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-115">Access type:</span></span>  <br/> |<span data-ttu-id="4e0e7-116">Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="4e0e7-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e0e7-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4e0e7-117">Remarks</span></span>

<span data-ttu-id="4e0e7-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="4e0e7-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="4e0e7-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="4e0e7-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="4e0e7-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e0e7-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="4e0e7-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4e0e7-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4e0e7-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-125">ulKind:</span></span>  <br/> |<span data-ttu-id="4e0e7-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="4e0e7-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="4e0e7-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="4e0e7-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="4e0e7-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="4e0e7-129">Diese Eigenschaft bietet eine Möglichkeit für den Anbieter an, ob Outlook verschiedenen Ordnern in einem Speicher gescannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="4e0e7-130">Beim Starten wird verwendet, wenn Outlook führt eine Überprüfung auf vorhandene Ordner für jede geöffnete Speicher zum Auffüllen im **Navigationsbereich** ; Outlook überprüft das Vorhandensein und der Wert dieser Eigenschaft in einem Speicher, bevor die Überprüfung initiieren.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="4e0e7-131">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook-Ordnern auf den Speicher gescannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="4e0e7-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="4e0e7-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="4e0e7-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="4e0e7-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="4e0e7-134">Outlook kann-Ordnern auf den Speicher gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="4e0e7-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="4e0e7-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="4e0e7-136">Outlook sollte-Ordnern auf den Speicher nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="4e0e7-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="4e0e7-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="4e0e7-138">Lassen Sie Clients so ändern Sie diese Eigenschaft im Store nicht zu.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="4e0e7-139">Beachten Sie, dass die Konstante **CSM_CLIENT_DO_NOT_CHANGE** für die zukünftige ist und ist derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="4e0e7-140">Jetzt kann ein Speicher verhindern Clients ändern dieses Flag hartzucodieren der Wert, der der Speicher für diese Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4e0e7-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

