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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395224"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="bb586-103">PidTagOriginalSentRepresentingEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb586-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bb586-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb586-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb586-105">Enthält die Eintrags-ID des messaging Benutzers in dessen Namen die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bb586-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb586-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bb586-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb586-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bb586-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bb586-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bb586-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb586-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="bb586-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="bb586-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bb586-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb586-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb586-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb586-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bb586-112">Area:</span></span>  <br/> |<span data-ttu-id="bb586-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="bb586-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb586-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb586-114">Remarks</span></span>

<span data-ttu-id="bb586-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender einer Nachricht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bb586-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="bb586-116">Es wird in einem Thread Unterhaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb586-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="bb586-117">Senden einer Nachricht im Auftrag einer anderen Client-Clientanwendung sollte diese Eigenschaft auf den Wert der Eigenschaft **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) auf der ersten Übermittlung der Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb586-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="bb586-118">Einmal festgelegt ist, sollte es nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bb586-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb586-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb586-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb586-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bb586-120">Protocol specifications</span></span>

<span data-ttu-id="bb586-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb586-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb586-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bb586-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb586-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb586-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb586-124">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bb586-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb586-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bb586-125">Header files</span></span>

<span data-ttu-id="bb586-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb586-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb586-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bb586-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb586-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb586-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bb586-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bb586-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb586-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb586-130">See also</span></span>



[<span data-ttu-id="bb586-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb586-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb586-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb586-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb586-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bb586-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb586-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bb586-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

