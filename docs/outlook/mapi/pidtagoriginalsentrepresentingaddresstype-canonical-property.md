---
title: PidTagOriginalSentRepresentingAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce3678c5137caec2e9f80c7fc15cde0ae99441ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572529"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="1294c-103">PidTagOriginalSentRepresentingAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1294c-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="1294c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1294c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1294c-105">Enthält den Adresstyp des messaging Benutzers in dessen Namen die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1294c-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1294c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1294c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1294c-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1294c-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="1294c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1294c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1294c-109">0 x 0068</span><span class="sxs-lookup"><span data-stu-id="1294c-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="1294c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1294c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1294c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1294c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1294c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1294c-112">Area:</span></span>  <br/> |<span data-ttu-id="1294c-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="1294c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1294c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1294c-114">Remarks</span></span>

<span data-ttu-id="1294c-115">Diese Eigenschaften werden der Typ für den ursprünglichen dargestellte Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1294c-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="1294c-116">Sie werden in einem Thread Unterhaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1294c-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="1294c-117">Eine Clientanwendung Senden einer Nachricht im Auftrag einer anderen Client sollte diese Eigenschaften auf den Wert der Eigenschaft **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) auf der ersten Übermittlung der Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1294c-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="1294c-118">Einmal festgelegt ist, sollte es nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1294c-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1294c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1294c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1294c-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1294c-120">Protocol specifications</span></span>

<span data-ttu-id="1294c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1294c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1294c-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1294c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1294c-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1294c-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1294c-124">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1294c-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1294c-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1294c-125">Header files</span></span>

<span data-ttu-id="1294c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1294c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1294c-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1294c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1294c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1294c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1294c-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1294c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1294c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1294c-130">See also</span></span>



[<span data-ttu-id="1294c-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1294c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1294c-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1294c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1294c-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1294c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1294c-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1294c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

