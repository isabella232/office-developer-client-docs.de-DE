---
title: PidTagOriginalSenderSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 97ab08d3da3725187ef2d5c70bec80e9142bdd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342602"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="51808-103">PidTagOriginalSenderSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51808-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="51808-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51808-105">Enthält den Suchschlüssel für den Absender der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="51808-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51808-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51808-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51808-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="51808-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="51808-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="51808-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51808-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="51808-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="51808-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="51808-110">Data type:</span></span>  <br/> |<span data-ttu-id="51808-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="51808-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="51808-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51808-112">Area:</span></span>  <br/> |<span data-ttu-id="51808-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="51808-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51808-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51808-114">Remarks</span></span>

<span data-ttu-id="51808-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="51808-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="51808-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="51808-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="51808-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="51808-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51808-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51808-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51808-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="51808-119">Protocol specifications</span></span>

<span data-ttu-id="51808-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51808-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51808-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="51808-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51808-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51808-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51808-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="51808-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51808-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="51808-124">Header files</span></span>

<span data-ttu-id="51808-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51808-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="51808-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51808-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="51808-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51808-127">Mapitags.h</span></span>
  
> <span data-ttu-id="51808-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="51808-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51808-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51808-129">See also</span></span>



[<span data-ttu-id="51808-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51808-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51808-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="51808-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51808-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51808-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51808-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51808-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

