---
title: Kanonische PidTagIpmSentMailEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2bf7665d7867b9c7151f787bbc6b3cfd802bca35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794522"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="1ea00-103">Kanonische PidTagIpmSentMailEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ea00-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1ea00-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ea00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ea00-105">Enthält die Eintrags-ID des Ordners gesendete Objekte standard zwischen Personen Nachricht (IPM).</span><span class="sxs-lookup"><span data-stu-id="1ea00-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ea00-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1ea00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ea00-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ea00-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1ea00-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1ea00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ea00-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="1ea00-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="1ea00-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1ea00-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ea00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ea00-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1ea00-112">Area:</span></span>  <br/> |<span data-ttu-id="1ea00-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="1ea00-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ea00-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ea00-114">Remarks</span></span>

<span data-ttu-id="1ea00-115">Nachdem dieses gesendet, werden Nachrichten zwischen Personen in der Regel im Ordner "Gesendete Elemente" platziert.</span><span class="sxs-lookup"><span data-stu-id="1ea00-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="1ea00-116">Ein Client können diese Eigenschaft zum Festlegen der Eigenschaft **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1ea00-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1ea00-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ea00-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1ea00-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1ea00-118">Header files</span></span>

<span data-ttu-id="1ea00-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ea00-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ea00-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1ea00-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ea00-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ea00-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1ea00-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1ea00-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ea00-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ea00-123">See also</span></span>



[<span data-ttu-id="1ea00-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ea00-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ea00-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ea00-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ea00-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1ea00-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ea00-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1ea00-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

