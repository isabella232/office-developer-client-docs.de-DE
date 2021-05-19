---
title: PidTagOriginalSentRepresentingName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 771a7c9cdf37a94875c881d8d7e8fd292893a0ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341102"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="e54ac-103">PidTagOriginalSentRepresentingName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e54ac-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="e54ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e54ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e54ac-105">Enthält den Anzeigenamen des Messagingbenutzers, in dessen Auftrag die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e54ac-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e54ac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e54ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e54ac-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e54ac-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e54ac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e54ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e54ac-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="e54ac-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="e54ac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e54ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="e54ac-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e54ac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e54ac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e54ac-112">Area:</span></span>  <br/> |<span data-ttu-id="e54ac-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="e54ac-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e54ac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e54ac-114">Remarks</span></span>

<span data-ttu-id="e54ac-115">Diese Eigenschaftenbeispiele der Adresseigenschaften für den ursprünglich dargestellten Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e54ac-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="e54ac-116">Sie wird in einem Unterhaltungsthread verwendet.</span><span class="sxs-lookup"><span data-stu-id="e54ac-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="e54ac-117">Eine Clientanwendung, die eine Nachricht im Auftrag eines anderen Clients sendet, sollte diese Eigenschaften auf den Wert der **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))-Eigenschaft bei der ersten Übermittlung der Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="e54ac-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="e54ac-118">Nachdem festgelegt, sollte es niemals geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e54ac-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e54ac-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e54ac-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e54ac-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e54ac-120">Protocol specifications</span></span>

<span data-ttu-id="e54ac-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e54ac-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e54ac-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e54ac-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e54ac-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e54ac-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e54ac-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e54ac-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e54ac-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e54ac-125">Header files</span></span>

<span data-ttu-id="e54ac-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e54ac-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e54ac-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e54ac-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e54ac-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e54ac-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e54ac-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e54ac-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e54ac-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e54ac-130">See also</span></span>



[<span data-ttu-id="e54ac-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e54ac-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e54ac-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e54ac-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e54ac-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e54ac-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e54ac-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e54ac-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

