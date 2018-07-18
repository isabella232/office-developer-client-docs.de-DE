---
title: PidTagUrlComponentName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795282"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="a112d-103">PidTagUrlComponentName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a112d-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="a112d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a112d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a112d-105">Der URL-Name der Komponente für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a112d-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a112d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a112d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a112d-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a112d-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a112d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a112d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a112d-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="a112d-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="a112d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a112d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a112d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a112d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a112d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a112d-112">Area:</span></span>  <br/> |<span data-ttu-id="a112d-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="a112d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a112d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a112d-114">Remarks</span></span>

<span data-ttu-id="a112d-115">Diese Eigenschaften sollten innerhalb eines Ordners eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a112d-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="a112d-116">Wenn dies nicht festgelegt, wenn die Nachricht erstellt wird, sollte der Nachrichtenspeicher diese Eigenschaften basierend auf verschiedenen Nachrichteneigenschaften, abhängig von der Nachrichtenklasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a112d-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="a112d-117">Beispielsweise die **IPM. Hinweis** und **IPM. Termin** Nachrichten sollten diese Eigenschaft auf Basis der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft und die **IPM festgelegt haben. Kontakt** Nachrichten sollten diese Eigenschaft basierend auf der **DispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md))-Eigenschaft festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="a112d-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="a112d-118">Für die meisten anderen Nachrichtenklassen sollte diese Eigenschaft auf die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) basieren.</span><span class="sxs-lookup"><span data-stu-id="a112d-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a112d-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a112d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a112d-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a112d-120">Protocol specifications</span></span>

<span data-ttu-id="a112d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a112d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a112d-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a112d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a112d-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a112d-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a112d-124">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="a112d-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a112d-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a112d-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a112d-126">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="a112d-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a112d-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a112d-127">Header files</span></span>

<span data-ttu-id="a112d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a112d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a112d-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a112d-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="a112d-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a112d-130">Mapitags.h</span></span>
  
> <span data-ttu-id="a112d-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a112d-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a112d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a112d-132">See also</span></span>



[<span data-ttu-id="a112d-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a112d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a112d-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a112d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a112d-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a112d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a112d-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a112d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

