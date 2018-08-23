---
title: PidTagOwnStoreEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 54014ab25d268c161465349b4e33c6a1df19f140
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591697"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="4749d-103">PidTagOwnStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4749d-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4749d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4749d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4749d-105">Enthält die Eintrags-ID des Nachrichtenspeichers an einen Transport eng gekoppelten.</span><span class="sxs-lookup"><span data-stu-id="4749d-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4749d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4749d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4749d-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4749d-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4749d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4749d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4749d-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="4749d-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="4749d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4749d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4749d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4749d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4749d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4749d-112">Area:</span></span>  <br/> |<span data-ttu-id="4749d-113">Nachrichtenspeicher-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4749d-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4749d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4749d-114">Remarks</span></span>

<span data-ttu-id="4749d-115">Diese Eigenschaft gibt die Eintrags-ID für den Informationsspeicher eng gekoppelten, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4749d-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="4749d-116">Beispielsweise kann ein Transportdienstes angeben der private Ordner speichern Eintrags-ID, damit die MAPI-Warteschlange in der Adressbuchhierarchie im Speicher eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4749d-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4749d-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4749d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4749d-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4749d-118">Header files</span></span>

<span data-ttu-id="4749d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4749d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4749d-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4749d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4749d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4749d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4749d-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4749d-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4749d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4749d-123">See also</span></span>



[<span data-ttu-id="4749d-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4749d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4749d-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4749d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4749d-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4749d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4749d-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4749d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

