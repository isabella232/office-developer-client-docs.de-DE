---
title: PidTagIpmSentMailEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd29afc93bc952bb619dfac752fae232bf7991cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437322"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="d6bcc-103">PidTagIpmSentMailEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6bcc-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d6bcc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6bcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6bcc-105">Enthält die Eintrags-ID des Ordners "Gesendete Elemente" (IPM) für zwischenpersonale Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d6bcc-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6bcc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d6bcc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6bcc-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d6bcc-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d6bcc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d6bcc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6bcc-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="d6bcc-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="d6bcc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d6bcc-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6bcc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d6bcc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d6bcc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d6bcc-112">Area:</span></span>  <br/> |<span data-ttu-id="d6bcc-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="d6bcc-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6bcc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6bcc-114">Remarks</span></span>

<span data-ttu-id="d6bcc-115">Nach dem Senden werden zwischenpersönliche Nachrichten in der Regel im Ordner "Gesendete Elemente" platziert.</span><span class="sxs-lookup"><span data-stu-id="d6bcc-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="d6bcc-116">Ein Client kann diese Eigenschaft verwenden, **um die PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) -Eigenschaft für eine übermittelte Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6bcc-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6bcc-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d6bcc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d6bcc-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d6bcc-118">Header files</span></span>

<span data-ttu-id="d6bcc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6bcc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6bcc-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6bcc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6bcc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6bcc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d6bcc-122">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d6bcc-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6bcc-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6bcc-123">See also</span></span>



[<span data-ttu-id="d6bcc-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6bcc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6bcc-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d6bcc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6bcc-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d6bcc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6bcc-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d6bcc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

