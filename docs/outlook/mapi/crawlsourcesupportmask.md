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
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420913"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="6a567-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="6a567-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="6a567-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a567-105">Gibt an, Microsoft Office Outlook Ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgaben, beim Start überprüfen soll, um den Navigationsbereich zu füllen.</span><span class="sxs-lookup"><span data-stu-id="6a567-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6a567-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6a567-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a567-107">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="6a567-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="6a567-108">[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="6a567-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="6a567-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="6a567-109">Created by:</span></span>  <br/> |<span data-ttu-id="6a567-110">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="6a567-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="6a567-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="6a567-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="6a567-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="6a567-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="6a567-113">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="6a567-113">Property type:</span></span>  <br/> |<span data-ttu-id="6a567-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6a567-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6a567-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="6a567-115">Access type:</span></span>  <br/> |<span data-ttu-id="6a567-116">Schreibgeschützt oder Lese-/Schreibzugriff je nach Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="6a567-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a567-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a567-117">Remarks</span></span>

<span data-ttu-id="6a567-118">Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6a567-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="6a567-119">Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6a567-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="6a567-120">Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="6a567-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="6a567-121">Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a567-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="6a567-122">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="6a567-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a567-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="6a567-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="6a567-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6a567-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6a567-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="6a567-125">ulKind:</span></span>  <br/> |<span data-ttu-id="6a567-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="6a567-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="6a567-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="6a567-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="6a567-128">L"CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="6a567-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="6a567-129">Mit dieser Eigenschaft können Speicheranbieter angeben, ob Outlook Ordner in einem Speicher überprüfen sollen.</span><span class="sxs-lookup"><span data-stu-id="6a567-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="6a567-130">Sie wird beim Start verwendet, Outlook vorhandenen Ordner in jedem geöffneten Speicher überprüft, um den **Navigationsbereich auffüllen zu** können. Outlook vor dem Starten der Überprüfung auf das Vorhandensein und den Wert dieser Eigenschaft in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="6a567-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="6a567-131">Diese Eigenschaft wird standardmäßig nicht in einem Speicher verfügbar gemacht, was bedeutet, Outlook Ordner im Speicher überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="6a567-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="6a567-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="6a567-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="6a567-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6a567-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="6a567-134">Outlook können Ordner im Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6a567-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="6a567-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="6a567-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="6a567-136">Outlook sollten keine Ordner im Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6a567-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="6a567-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="6a567-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="6a567-138">Lassen Sie nicht zu, dass Clients diese Eigenschaft im Store ändern.</span><span class="sxs-lookup"><span data-stu-id="6a567-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="6a567-139">Beachten Sie, dass die **konstante CSM_CLIENT_DO_NOT_CHANGE** zur zukünftigen Referenz verwendet wird und derzeit nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6a567-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="6a567-140">Derzeit kann ein Speicher verhindern, dass Clients dieses Kennzeichen ändern, indem der Wert hartcodiert wird, den der Speicher für diese Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6a567-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

