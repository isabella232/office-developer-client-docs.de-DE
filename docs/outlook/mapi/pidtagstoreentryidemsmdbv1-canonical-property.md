---
title: Kanonische Pidtagstoreentryidemsmdbv1 (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278771"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="bc08e-103">Kanonische Pidtagstoreentryidemsmdbv1 (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bc08e-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="bc08e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc08e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc08e-105">Enthält den alten Stil (Microsoft Outlook 2002 und frühere Versionen) der Eintrags-ID eines Microsoft Exchange Server 2010-oder Exchange Server 2013-Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="bc08e-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc08e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc08e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc08e-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="bc08e-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="bc08e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bc08e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc08e-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="bc08e-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="bc08e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc08e-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc08e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc08e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc08e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc08e-112">Area:</span></span>  <br/> |<span data-ttu-id="bc08e-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc08e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc08e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc08e-114">Remarks</span></span>

<span data-ttu-id="bc08e-115">Beginnend mit Microsoft Outlook 2003 wurden die Server-FQDNs in die Eintrags-IDs integriert, wodurch zusätzliche RPCs für Verweise vermieden wurden.</span><span class="sxs-lookup"><span data-stu-id="bc08e-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="bc08e-116">Dadurch werden die Eintrags-IDs jedoch länger und es werden weitere Szenarien eingeführt, in denen die **CompareEntryIDs** -Methode verwendet werden muss, um zu bestimmen, ob zwei Eintrags-IDs äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="bc08e-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="bc08e-117">Die PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1)-Eigenschaft greift auf das ältere Format der Exchange Server-Eintrags-ID zu, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc08e-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="bc08e-118">Dies kann Speicherplatz sparen und auch die Anzahl der **CompareEntryIDs** -Aufrufe reduzieren, die erforderlich sind, um zu bestimmen, wann die Eintrags-IDs äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="bc08e-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="bc08e-119">Beachten Sie, dass bei Verwendung der älteren Eintrags-IDs zum Öffnen eines Postfachs möglicherweise zusätzliche RPCs auftreten, wenn ein Verweis erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bc08e-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="bc08e-120">Um im zwischengespeicherten Modus auf die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft zuzugreifen, müssen Sie den Cache mithilfe des MAPI_NO_CACHE-Flags mit der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode umgehen.</span><span class="sxs-lookup"><span data-stu-id="bc08e-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="bc08e-121">Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="bc08e-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="bc08e-122">Die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft wird nur von Outlook 2003 über Microsoft Outlook 2013 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc08e-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc08e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc08e-123">See also</span></span>



[<span data-ttu-id="bc08e-124">Kanonische Pidtagstoreentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bc08e-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="bc08e-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc08e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc08e-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc08e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc08e-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc08e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc08e-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc08e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

