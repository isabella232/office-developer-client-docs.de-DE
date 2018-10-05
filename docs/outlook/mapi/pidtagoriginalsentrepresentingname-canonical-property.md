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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401482"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="269d0-103">PidTagOriginalSentRepresentingName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="269d0-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="269d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269d0-105">Enthält den Anzeigenamen des messaging Benutzers in dessen Namen die ursprüngliche Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="269d0-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="269d0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="269d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="269d0-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="269d0-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="269d0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="269d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="269d0-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="269d0-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="269d0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="269d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="269d0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="269d0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="269d0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="269d0-112">Area:</span></span>  <br/> |<span data-ttu-id="269d0-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="269d0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="269d0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="269d0-114">Remarks</span></span>

<span data-ttu-id="269d0-115">Diese Eigenschaften Beispiele für die Adresseigenschaften für den Absender einer Nachricht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="269d0-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="269d0-116">Es wird in einem Thread Unterhaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="269d0-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="269d0-117">Eine Clientanwendung Senden einer Nachricht im Auftrag einer anderen Client sollte diese Eigenschaften auf den Wert der Eigenschaft **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) auf der ersten Übermittlung der Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="269d0-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="269d0-118">Einmal festgelegt ist, sollte es nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="269d0-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="269d0-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="269d0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="269d0-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="269d0-120">Protocol specifications</span></span>

<span data-ttu-id="269d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="269d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="269d0-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="269d0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="269d0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="269d0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="269d0-124">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="269d0-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="269d0-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="269d0-125">Header files</span></span>

<span data-ttu-id="269d0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="269d0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="269d0-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="269d0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="269d0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="269d0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="269d0-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="269d0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="269d0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="269d0-130">See also</span></span>



[<span data-ttu-id="269d0-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="269d0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="269d0-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="269d0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="269d0-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="269d0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="269d0-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="269d0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

