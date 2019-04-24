---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326264"
---
# <a name="nofolderscan"></a><span data-ttu-id="390c9-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="390c9-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="390c9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="390c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="390c9-105">Gibt an, ob Microsoft Office Outlook Kontakteordner in einem Speicher überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="390c9-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="390c9-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="390c9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="390c9-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="390c9-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="390c9-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="390c9-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="390c9-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="390c9-109">Created by:</span></span>  <br/> |<span data-ttu-id="390c9-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="390c9-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="390c9-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="390c9-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="390c9-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="390c9-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="390c9-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="390c9-113">Property type:</span></span>  <br/> |<span data-ttu-id="390c9-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="390c9-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="390c9-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="390c9-115">Access type:</span></span>  <br/> |<span data-ttu-id="390c9-116">Je nach Speicheranbieter schreibgeschützt oder Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="390c9-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="390c9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="390c9-117">Remarks</span></span>

<span data-ttu-id="390c9-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="390c9-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="390c9-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="390c9-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="390c9-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="390c9-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="390c9-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="390c9-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="390c9-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="390c9-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="390c9-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="390c9-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="390c9-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="390c9-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="390c9-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="390c9-125">ulKind:</span></span>  <br/> |<span data-ttu-id="390c9-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="390c9-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="390c9-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="390c9-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="390c9-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="390c9-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="390c9-129">Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, Outlook nicht zu überprüfen, um die Leistungsbeeinträchtigung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="390c9-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="390c9-130">Sie wird in Seriendruck Vorgängen verwendet, in denen Outlook vor dem Initiieren der Überprüfung auf Anwesenheit und Wert dieser Eigenschaft prüft.</span><span class="sxs-lookup"><span data-stu-id="390c9-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="390c9-131">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar, was bedeutet, dass Outlook den Ordner "Kontakte" im Speicher überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="390c9-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="390c9-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="390c9-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="390c9-133">NULL (0): Outlook kann die Überprüfung ausführen.</span><span class="sxs-lookup"><span data-stu-id="390c9-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="390c9-134">Wert unGleich NULL: Outlook sollte Kontakteordner im Speicher nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="390c9-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

