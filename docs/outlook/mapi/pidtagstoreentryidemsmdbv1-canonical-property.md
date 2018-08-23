---
title: PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576323"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="efeb7-103">PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="efeb7-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="efeb7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efeb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efeb7-105">Enthält das alte Format von Eintrags-ID des Microsoft Exchange Server 2010 oder Exchange Server 2013-Nachrichtenspeichers (Microsoft Outlook 2002 und früheren Versionen).</span><span class="sxs-lookup"><span data-stu-id="efeb7-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efeb7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="efeb7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efeb7-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="efeb7-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="efeb7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="efeb7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efeb7-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="efeb7-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="efeb7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="efeb7-110">Data type:</span></span>  <br/> |<span data-ttu-id="efeb7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="efeb7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="efeb7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="efeb7-112">Area:</span></span>  <br/> |<span data-ttu-id="efeb7-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efeb7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efeb7-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="efeb7-114">Remarks</span></span>

<span data-ttu-id="efeb7-115">Ab Microsoft Outlook 2003, wurden in die Eintrags-IDs, wodurch Vermeidung von zusätzlichen RPCs für Verweise auf die Server-FQDNs integriert werden.</span><span class="sxs-lookup"><span data-stu-id="efeb7-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="efeb7-116">Allerdings Dies macht die Eintrags-IDs länger und führt weitere Szenarien, in dem die **CompareEntryIDs** -Methode verwendet werden muss, um festzustellen, ob zwei Eintrag IDs gleichwertig sind.</span><span class="sxs-lookup"><span data-stu-id="efeb7-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="efeb7-117">Die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft (PidTagStoreIdEmsbdbV1) greift auf das ältere Format von der Exchange Server-Eintrags-ID, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efeb7-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="efeb7-118">Speicherplatz sparen Sie können und auch reduziert die Anzahl der **CompareEntryIDs** -Anrufe zu bestimmen, wann der Eintrag IDs gleichwertig sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="efeb7-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="efeb7-119">Beachten Sie, dass mit älteren Eintrags-IDs Öffnen eines Postfachs einige zusätzliche RPCs anfallen kann, wenn ein Verweis erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="efeb7-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="efeb7-120">Zugriff auf die Eigenschaft PR_STORE_ENTRYID_EMSMDB_V1 im Cache-Modus müssen Sie mit dem das Kennzeichen MAPI_NO_CACHE mit der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode im Cache umgehen.</span><span class="sxs-lookup"><span data-stu-id="efeb7-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="efeb7-121">Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="efeb7-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="efeb7-122">Nur Outlook 2003 über Microsoft Outlook 2013 unterstützen die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="efeb7-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efeb7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efeb7-123">See also</span></span>



[<span data-ttu-id="efeb7-124">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="efeb7-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="efeb7-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efeb7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efeb7-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efeb7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efeb7-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="efeb7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efeb7-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="efeb7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

