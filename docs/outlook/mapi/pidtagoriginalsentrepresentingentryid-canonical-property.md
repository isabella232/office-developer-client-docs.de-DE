---
title: PidTagOriginalSentRepresentingEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eaf91472794c5188a63897bccaa900c4882407bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341755"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="45198-103">PidTagOriginalSentRepresentingEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45198-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="45198-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45198-105">Enthält die Eintrags-ID des Messagingbenutzers, in dessen Auftrag die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="45198-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45198-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45198-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45198-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="45198-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="45198-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="45198-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45198-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="45198-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="45198-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45198-110">Data type:</span></span>  <br/> |<span data-ttu-id="45198-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45198-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45198-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45198-112">Area:</span></span>  <br/> |<span data-ttu-id="45198-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="45198-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45198-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45198-114">Remarks</span></span>

<span data-ttu-id="45198-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglich dargestellten Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="45198-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="45198-116">Sie wird in einem Unterhaltungsthread verwendet.</span><span class="sxs-lookup"><span data-stu-id="45198-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="45198-117">Eine **Clientanwendung,** die eine Nachricht im Namen eines anderen Clients sendet, sollte diese Eigenschaft auf den Wert der PR_SENT_REPRESENTING_ENTRYID ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))-Eigenschaft bei der ersten Übermittlung der Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="45198-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="45198-118">Nachdem festgelegt, sollte es niemals geändert werden.</span><span class="sxs-lookup"><span data-stu-id="45198-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45198-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45198-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45198-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45198-120">Protocol specifications</span></span>

<span data-ttu-id="45198-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45198-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45198-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="45198-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45198-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45198-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45198-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="45198-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45198-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="45198-125">Header files</span></span>

<span data-ttu-id="45198-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45198-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45198-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45198-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45198-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45198-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45198-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="45198-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45198-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45198-130">See also</span></span>



[<span data-ttu-id="45198-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45198-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45198-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="45198-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45198-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45198-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45198-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45198-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

