---
title: Kanonische Pidtagoriginalsentrepresentingname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 771a7c9cdf37a94875c881d8d7e8fd292893a0ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341102"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="db09f-103">Kanonische Pidtagoriginalsentrepresentingname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="db09f-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="db09f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db09f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db09f-105">Enthält den Anzeigenamen des Messaging Benutzers, in dessen Namen die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="db09f-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db09f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="db09f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db09f-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="db09f-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="db09f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="db09f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db09f-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="db09f-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="db09f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="db09f-110">Data type:</span></span>  <br/> |<span data-ttu-id="db09f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="db09f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="db09f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="db09f-112">Area:</span></span>  <br/> |<span data-ttu-id="db09f-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="db09f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db09f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db09f-114">Remarks</span></span>

<span data-ttu-id="db09f-115">Diese Eigenschaften Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="db09f-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="db09f-116">Sie wird in einem konversationsthread verwendet.</span><span class="sxs-lookup"><span data-stu-id="db09f-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="db09f-117">Eine Clientanwendung, die eine Nachricht im Auftrag eines anderen Clients sendet, sollte diese Eigenschaften beim ersten Senden der Nachricht auf den Wert der **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="db09f-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="db09f-118">Sobald festgelegt, sollte es nie geändert werden.</span><span class="sxs-lookup"><span data-stu-id="db09f-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db09f-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db09f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db09f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="db09f-120">Protocol specifications</span></span>

<span data-ttu-id="db09f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db09f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db09f-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="db09f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db09f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db09f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db09f-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="db09f-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db09f-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="db09f-125">Header files</span></span>

<span data-ttu-id="db09f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="db09f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="db09f-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="db09f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="db09f-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="db09f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="db09f-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="db09f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db09f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db09f-130">See also</span></span>



[<span data-ttu-id="db09f-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db09f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db09f-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db09f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db09f-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="db09f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db09f-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="db09f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

