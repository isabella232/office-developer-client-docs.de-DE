---
title: PidTagOriginalSentRepresentingSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388497"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="14080-103">PidTagOriginalSentRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="14080-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="14080-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14080-105">Enthält die suchen-Taste die messaging-Benutzer in den Namen die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="14080-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14080-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="14080-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14080-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="14080-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="14080-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="14080-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14080-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="14080-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="14080-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="14080-110">Data type:</span></span>  <br/> |<span data-ttu-id="14080-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="14080-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="14080-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="14080-112">Area:</span></span>  <br/> |<span data-ttu-id="14080-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="14080-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14080-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14080-114">Remarks</span></span>

<span data-ttu-id="14080-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender einer Nachricht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="14080-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="14080-116">Es wird in einem Thread Unterhaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="14080-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="14080-117">Senden einer Nachricht im Auftrag einer anderen Client-Clientanwendung sollte diese Eigenschaft auf den Wert der Eigenschaft **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) auf der ersten Übermittlung der Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14080-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="14080-118">Einmal festgelegt ist, sollte es nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="14080-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14080-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14080-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14080-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="14080-120">Protocol specifications</span></span>

<span data-ttu-id="14080-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14080-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14080-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="14080-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14080-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14080-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14080-124">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="14080-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14080-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="14080-125">Header files</span></span>

<span data-ttu-id="14080-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14080-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="14080-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="14080-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="14080-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14080-128">Mapitags.h</span></span>
  
> <span data-ttu-id="14080-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="14080-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14080-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14080-130">See also</span></span>



[<span data-ttu-id="14080-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14080-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14080-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14080-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14080-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="14080-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14080-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="14080-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

