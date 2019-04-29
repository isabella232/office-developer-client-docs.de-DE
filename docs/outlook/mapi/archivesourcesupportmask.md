---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418092"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="d01ae-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="d01ae-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="d01ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d01ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d01ae-105">Gibt an, ob in Microsoft Office Outlook Ordner in einem Speicher gescannt und automatisch archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d01ae-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d01ae-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d01ae-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d01ae-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="d01ae-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="d01ae-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="d01ae-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="d01ae-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="d01ae-109">Created by:</span></span>  <br/> |<span data-ttu-id="d01ae-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="d01ae-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="d01ae-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="d01ae-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="d01ae-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="d01ae-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="d01ae-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="d01ae-113">Property type:</span></span>  <br/> |<span data-ttu-id="d01ae-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d01ae-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d01ae-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="d01ae-115">Access type:</span></span>  <br/> |<span data-ttu-id="d01ae-116">Je nach Speicheranbieter schreibgeschützt oder Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="d01ae-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d01ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d01ae-117">Remarks</span></span>

<span data-ttu-id="d01ae-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d01ae-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="d01ae-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d01ae-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="d01ae-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d01ae-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="d01ae-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d01ae-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="d01ae-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="d01ae-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d01ae-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="d01ae-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="d01ae-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d01ae-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d01ae-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="d01ae-125">ulKind:</span></span>  <br/> |<span data-ttu-id="d01ae-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d01ae-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="d01ae-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="d01ae-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="d01ae-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="d01ae-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="d01ae-129">Mit dieser Eigenschaft können Speicheranbieter angeben, ob Outlook Ordner in einem Speicher überprüfen und automatisch archivieren soll.</span><span class="sxs-lookup"><span data-stu-id="d01ae-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="d01ae-130">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar, was bedeutet, dass Outlook Ordner im Speicher überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="d01ae-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="d01ae-131">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="d01ae-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="d01ae-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d01ae-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="d01ae-133">Outlook kann Ordner im Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d01ae-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="d01ae-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="d01ae-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="d01ae-135">Outlook sollte Ordner im Speicher nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d01ae-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="d01ae-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d01ae-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="d01ae-137">Clients dürfen diese Eigenschaft nicht im Speicher ändern.</span><span class="sxs-lookup"><span data-stu-id="d01ae-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="d01ae-138">Beachten Sie, dass die Konstante **ASM_CLIENT_DO_NOT_CHANGE** als zukünftige Referenz dient und derzeit nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d01ae-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="d01ae-139">Im Moment kann ein Speicher verhindern, dass Clients dieses Flag ändern, indem der Wert hart codiert wird, den der Store für diese Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d01ae-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

