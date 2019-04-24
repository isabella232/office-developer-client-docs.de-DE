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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333047"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="8d195-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="8d195-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="8d195-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d195-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d195-105">Gibt an, ob in Microsoft Office Outlook Ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgabenordner, beim Start gescannt werden sollen, um den Navigationsbereich aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="8d195-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8d195-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8d195-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d195-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="8d195-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="8d195-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="8d195-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="8d195-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="8d195-109">Created by:</span></span>  <br/> |<span data-ttu-id="8d195-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="8d195-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="8d195-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="8d195-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="8d195-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="8d195-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="8d195-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="8d195-113">Property type:</span></span>  <br/> |<span data-ttu-id="8d195-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d195-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d195-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="8d195-115">Access type:</span></span>  <br/> |<span data-ttu-id="8d195-116">Je nach Speicheranbieter schreibgeschützt oder Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="8d195-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d195-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d195-117">Remarks</span></span>

<span data-ttu-id="8d195-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d195-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="8d195-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8d195-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="8d195-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8d195-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="8d195-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d195-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="8d195-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="8d195-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d195-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="8d195-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="8d195-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8d195-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8d195-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="8d195-125">ulKind:</span></span>  <br/> |<span data-ttu-id="8d195-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="8d195-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="8d195-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="8d195-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="8d195-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="8d195-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="8d195-129">Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, anzugeben, ob Outlook verschiedene Ordner in einem Speicher überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="8d195-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="8d195-130">Er wird beim Start verwendet, wenn Outlook vorhandene Ordner in jedem geöffneten Speicher überprüft, um den **Navigations** Bereich zu füllen. Outlook überprüft das vorhanden sein und den Wert dieser Eigenschaft in einem Speicher, bevor die Überprüfung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="8d195-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="8d195-131">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar, was bedeutet, dass Outlook Ordner im Speicher überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="8d195-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="8d195-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="8d195-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="8d195-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="8d195-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="8d195-134">Outlook kann Ordner im Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8d195-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="8d195-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="8d195-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="8d195-136">Outlook sollte Ordner im Speicher nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8d195-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="8d195-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8d195-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="8d195-138">Clients dürfen diese Eigenschaft nicht im Speicher ändern.</span><span class="sxs-lookup"><span data-stu-id="8d195-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="8d195-139">Beachten Sie, dass die Konstante **CSM_CLIENT_DO_NOT_CHANGE** als zukünftige Referenz dient und derzeit nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d195-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="8d195-140">Im Moment kann ein Speicher verhindern, dass Clients dieses Flag ändern, indem der Wert hart codiert wird, den der Store für diese Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8d195-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

