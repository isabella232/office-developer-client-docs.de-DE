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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415152"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="ee273-103">PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee273-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="ee273-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee273-105">Enthält die alte Formatvorlage (Microsoft Outlook 2002 und frühere Versionen) des Eintragsbezeichners eines Microsoft Exchange Server 2010- oder Exchange Server 2013-Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="ee273-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee273-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ee273-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee273-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="ee273-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="ee273-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ee273-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee273-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="ee273-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="ee273-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ee273-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee273-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ee273-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ee273-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ee273-112">Area:</span></span>  <br/> |<span data-ttu-id="ee273-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee273-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee273-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee273-114">Remarks</span></span>

<span data-ttu-id="ee273-115">Ab Microsoft Outlook 2003 wurden die Server-FQDNs in die Eintrags-IDs integriert, wodurch zusätzliche RPCs für Verweise vermieden wurden.</span><span class="sxs-lookup"><span data-stu-id="ee273-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="ee273-116">Dies führt jedoch zu längeren Eintrags-IDs und führt zu weiteren Szenarien, in denen die **CompareEntryIDs-Methode** verwendet werden muss, um zu ermitteln, ob zwei Eintrags-IDs gleichwertig sind.</span><span class="sxs-lookup"><span data-stu-id="ee273-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="ee273-117">Die PR_STORE_ENTRYID_EMSMDB_V1 -Eigenschaft (PidTagStoreIdEmsbdbV1) zugrifft auf das ältere Format der Exchange Server-Eintrags-ID, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee273-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="ee273-118">Dies kann Platz sparen und auch die Anzahl der **CompareEntryIDs-Aufrufe** reduzieren, die erforderlich sind, um zu bestimmen, wann Eintrags-IDs gleichwertig sind.</span><span class="sxs-lookup"><span data-stu-id="ee273-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="ee273-119">Beachten Sie, dass bei Verwendung der älteren Eintrags-IDs zum Öffnen eines Postfachs möglicherweise zusätzliche RPCs erforderlich sind, wenn ein Verweis erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ee273-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="ee273-120">Um auf die PR_STORE_ENTRYID_EMSMDB_V1 im zwischengespeicherten Modus zu zugreifen, müssen Sie den Cache mithilfe des MAPI_NO_CACHE-Flag mit der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) umgehen.</span><span class="sxs-lookup"><span data-stu-id="ee273-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="ee273-121">Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf die PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="ee273-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="ee273-122">Nur Outlook 2003 bis Microsoft Outlook 2013 unterstützen die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ee273-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee273-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee273-123">See also</span></span>



[<span data-ttu-id="ee273-124">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee273-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="ee273-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee273-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee273-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ee273-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee273-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ee273-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee273-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ee273-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

