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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426352"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="cec04-103">PidTagIpmWastebasketEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cec04-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cec04-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cec04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cec04-105">Enthält die Eintrags-ID des Ordners "Gelöschte Elemente" (IPM).</span><span class="sxs-lookup"><span data-stu-id="cec04-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cec04-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cec04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cec04-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cec04-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cec04-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cec04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cec04-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="cec04-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="cec04-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cec04-110">Data type:</span></span>  <br/> |<span data-ttu-id="cec04-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cec04-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cec04-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cec04-112">Area:</span></span>  <br/> |<span data-ttu-id="cec04-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="cec04-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cec04-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cec04-114">Remarks</span></span>

<span data-ttu-id="cec04-115">Eine Clientanwendung sollte gelöschte zwischenpersönliche Nachrichten in den Ordner "Gelöschte Elemente" verschieben.</span><span class="sxs-lookup"><span data-stu-id="cec04-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="cec04-116">Wenn sich die Nachricht bereits in diesem Ordner befindet oder diese Eigenschaft nicht unterstützt wird, sollte der Client die Nachricht löschen.</span><span class="sxs-lookup"><span data-stu-id="cec04-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cec04-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cec04-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cec04-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="cec04-118">Header files</span></span>

<span data-ttu-id="cec04-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cec04-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cec04-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cec04-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cec04-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cec04-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cec04-122">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cec04-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cec04-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cec04-123">See also</span></span>



[<span data-ttu-id="cec04-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cec04-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cec04-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="cec04-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cec04-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cec04-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cec04-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cec04-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

