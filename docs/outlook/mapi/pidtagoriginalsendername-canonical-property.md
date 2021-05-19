---
title: PidTagOriginalSenderName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 521fb544152dcb903450ff7dbd05ecbac808afe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342609"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="c8463-103">PidTagOriginalSenderName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c8463-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="c8463-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8463-105">Enthält den Anzeigenamen des Absenders der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="c8463-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8463-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c8463-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8463-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c8463-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c8463-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c8463-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8463-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="c8463-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="c8463-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c8463-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8463-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8463-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c8463-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c8463-112">Area:</span></span>  <br/> |<span data-ttu-id="c8463-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="c8463-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8463-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8463-114">Remarks</span></span>

<span data-ttu-id="c8463-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c8463-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="c8463-116">Bei der ersten Übermittlung der Nachricht sollte eine Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c8463-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="c8463-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="c8463-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8463-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8463-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8463-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c8463-119">Protocol specifications</span></span>

<span data-ttu-id="c8463-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8463-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8463-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c8463-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8463-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8463-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8463-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c8463-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8463-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c8463-124">Header files</span></span>

<span data-ttu-id="c8463-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8463-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8463-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c8463-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8463-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8463-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c8463-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c8463-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8463-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8463-129">See also</span></span>



[<span data-ttu-id="c8463-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8463-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8463-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c8463-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8463-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c8463-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8463-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c8463-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

