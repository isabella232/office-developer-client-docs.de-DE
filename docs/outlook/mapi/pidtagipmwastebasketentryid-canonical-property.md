---
title: PidTagIpmWastebasketEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9b8cff0a552c5c12108bdc4b31fe9c3930ab5d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794553"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="1ca79-103">PidTagIpmWastebasketEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1ca79-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1ca79-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ca79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ca79-105">Enthält die Eintrags-ID des Ordners "Gelöschte Elemente standard zwischen Personen Nachricht (IPM)".</span><span class="sxs-lookup"><span data-stu-id="1ca79-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ca79-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1ca79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ca79-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ca79-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1ca79-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1ca79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ca79-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="1ca79-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="1ca79-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1ca79-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ca79-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ca79-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ca79-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1ca79-112">Area:</span></span>  <br/> |<span data-ttu-id="1ca79-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="1ca79-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ca79-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ca79-114">Remarks</span></span>

<span data-ttu-id="1ca79-115">Eine Clientanwendung sollte gelöschte Nachrichten zwischen Personen in den Ordner Gelöschte Objekte verschieben.</span><span class="sxs-lookup"><span data-stu-id="1ca79-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="1ca79-116">Wenn die Nachricht bereits in diesem Ordner befindet, oder wenn diese Eigenschaft nicht unterstützt wird, sollte der Client die Nachricht zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1ca79-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1ca79-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ca79-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1ca79-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1ca79-118">Header files</span></span>

<span data-ttu-id="1ca79-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ca79-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ca79-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1ca79-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ca79-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ca79-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1ca79-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1ca79-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ca79-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ca79-123">See also</span></span>



[<span data-ttu-id="1ca79-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ca79-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ca79-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ca79-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ca79-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1ca79-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ca79-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1ca79-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

