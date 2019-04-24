---
title: Kanonische Pidtagownstoreentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335448"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="cbcba-103">Kanonische Pidtagownstoreentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cbcba-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cbcba-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbcba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbcba-105">Enthält die Eintrags-ID des eng gekoppelten Nachrichtenspeichers eines Transports.</span><span class="sxs-lookup"><span data-stu-id="cbcba-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbcba-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cbcba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbcba-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cbcba-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cbcba-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cbcba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbcba-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="cbcba-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="cbcba-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cbcba-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbcba-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cbcba-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cbcba-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cbcba-112">Area:</span></span>  <br/> |<span data-ttu-id="cbcba-113">Nachrichtenspeichereigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbcba-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbcba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbcba-114">Remarks</span></span>

<span data-ttu-id="cbcba-115">Diese Eigenschaft gibt die Eintrags-ID für den eng gekoppelten Speicher an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cbcba-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="cbcba-116">Ein Transportanbieter kann beispielsweise die Eintrags-ID des privaten Ordnerspeichers angeben, sodass der MAPI-Spooler den Transportanbieter mit dem Speicher verbinden kann.</span><span class="sxs-lookup"><span data-stu-id="cbcba-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cbcba-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cbcba-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cbcba-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cbcba-118">Header files</span></span>

<span data-ttu-id="cbcba-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cbcba-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbcba-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cbcba-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbcba-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cbcba-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cbcba-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="cbcba-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbcba-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbcba-123">See also</span></span>



[<span data-ttu-id="cbcba-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbcba-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbcba-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbcba-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbcba-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cbcba-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbcba-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cbcba-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

