---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436810"
---
# <a name="nofolderscan"></a><span data-ttu-id="da63d-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="da63d-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="da63d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da63d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da63d-105">Gibt an, Microsoft Office Outlook Kontakteordner in einem Speicher überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="da63d-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="da63d-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="da63d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da63d-107">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="da63d-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="da63d-108">[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="da63d-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="da63d-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="da63d-109">Created by:</span></span>  <br/> |<span data-ttu-id="da63d-110">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="da63d-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="da63d-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="da63d-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="da63d-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="da63d-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="da63d-113">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="da63d-113">Property type:</span></span>  <br/> |<span data-ttu-id="da63d-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da63d-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da63d-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="da63d-115">Access type:</span></span>  <br/> |<span data-ttu-id="da63d-116">Schreibgeschützt oder Lese-/Schreibzugriff je nach Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="da63d-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da63d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da63d-117">Remarks</span></span>

<span data-ttu-id="da63d-118">Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da63d-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="da63d-119">Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="da63d-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="da63d-120">Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="da63d-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="da63d-121">Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="da63d-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="da63d-122">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="da63d-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da63d-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="da63d-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="da63d-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="da63d-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="da63d-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="da63d-125">ulKind:</span></span>  <br/> |<span data-ttu-id="da63d-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="da63d-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="da63d-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="da63d-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="da63d-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="da63d-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="da63d-129">Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, anzugeben, Outlook Kontakteordner im Speicher nicht zu überprüfen, um Leistungseinbußen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="da63d-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="da63d-130">Sie wird in Seriendruckvorgängen verwendet, Outlook vor dem Starten der Überprüfung auf das Vorhandensein und den Wert dieser Eigenschaft überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="da63d-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="da63d-131">Diese Eigenschaft wird standardmäßig nicht in einem Speicher verfügbar gemacht, d. h., Outlook den Ordner Kontakte im Speicher überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="da63d-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="da63d-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="da63d-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="da63d-133">Null (0): Outlook können den Scan durchführen.</span><span class="sxs-lookup"><span data-stu-id="da63d-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="da63d-134">Non-Zero-Wert: Outlook sollte keine Kontakteordner im Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="da63d-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

