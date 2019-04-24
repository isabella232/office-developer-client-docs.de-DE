---
title: Kanonische Pidtagoriginalsenderemailaddress (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ed3d84667d7be9c06d0ddf4d896b8888694edc12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355272"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="94c16-103">Kanonische Pidtagoriginalsenderemailaddress (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94c16-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="94c16-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94c16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94c16-105">Enthält die e-Mail-Adresse des Absenders der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="94c16-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94c16-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="94c16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94c16-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="94c16-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="94c16-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="94c16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94c16-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="94c16-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="94c16-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="94c16-110">Data type:</span></span>  <br/> |<span data-ttu-id="94c16-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94c16-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="94c16-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="94c16-112">Area:</span></span>  <br/> |<span data-ttu-id="94c16-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="94c16-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94c16-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94c16-114">Remarks</span></span>

<span data-ttu-id="94c16-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften des ursprünglichen Absenders einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="94c16-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="94c16-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert von **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="94c16-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="94c16-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="94c16-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94c16-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94c16-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94c16-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="94c16-119">Protocol specifications</span></span>

<span data-ttu-id="94c16-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94c16-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94c16-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="94c16-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94c16-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94c16-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94c16-123">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="94c16-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94c16-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="94c16-124">Header files</span></span>

<span data-ttu-id="94c16-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="94c16-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="94c16-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="94c16-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="94c16-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="94c16-127">Mapitags.h</span></span>
  
> <span data-ttu-id="94c16-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="94c16-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94c16-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94c16-129">See also</span></span>



[<span data-ttu-id="94c16-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94c16-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94c16-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94c16-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94c16-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="94c16-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94c16-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="94c16-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

