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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791310"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="07100-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="07100-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="07100-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07100-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07100-105">Gibt an, ob Microsoft Office Outlook Scannen von Ordnern in einem Speicher und automatisch archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07100-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="07100-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="07100-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07100-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="07100-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="07100-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="07100-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="07100-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="07100-109">Created by:</span></span>  <br/> |<span data-ttu-id="07100-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="07100-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="07100-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="07100-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="07100-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="07100-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="07100-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="07100-113">Property type:</span></span>  <br/> |<span data-ttu-id="07100-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07100-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07100-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="07100-115">Access type:</span></span>  <br/> |<span data-ttu-id="07100-116">Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="07100-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07100-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07100-117">Remarks</span></span>

<span data-ttu-id="07100-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="07100-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="07100-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="07100-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="07100-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="07100-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="07100-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="07100-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="07100-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="07100-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07100-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="07100-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="07100-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="07100-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="07100-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="07100-125">ulKind:</span></span>  <br/> |<span data-ttu-id="07100-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="07100-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="07100-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="07100-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="07100-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="07100-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="07100-129">Mit dieser Eigenschaft können Anbieter an, ob Outlook Scannen von Ordnern in einem Speicher und automatisch archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07100-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="07100-130">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook-Ordnern auf den Speicher gescannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="07100-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="07100-131">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="07100-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="07100-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="07100-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="07100-133">Outlook kann-Ordnern auf den Speicher gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="07100-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="07100-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="07100-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="07100-135">Outlook sollte-Ordnern auf den Speicher nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="07100-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="07100-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="07100-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="07100-137">Lassen Sie Clients so ändern Sie diese Eigenschaft im Store nicht zu.</span><span class="sxs-lookup"><span data-stu-id="07100-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="07100-138">Beachten Sie, dass die Konstante **ASM_CLIENT_DO_NOT_CHANGE** für die zukünftige ist und ist derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="07100-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="07100-139">Jetzt kann ein Speicher verhindern Clients ändern dieses Flag hartzucodieren der Wert, der der Speicher für diese Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="07100-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

