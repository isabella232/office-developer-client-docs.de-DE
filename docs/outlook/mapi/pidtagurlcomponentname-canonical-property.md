---
title: Kanonische Pidtagurlcomponentname (-Eigenschaft
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
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320426"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="8fda6-103">Kanonische Pidtagurlcomponentname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8fda6-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="8fda6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fda6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fda6-105">Der Name der URL-Komponente für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fda6-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fda6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8fda6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fda6-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8fda6-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8fda6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8fda6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fda6-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="8fda6-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="8fda6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8fda6-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fda6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8fda6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8fda6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8fda6-112">Area:</span></span>  <br/> |<span data-ttu-id="8fda6-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="8fda6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fda6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fda6-114">Remarks</span></span>

<span data-ttu-id="8fda6-115">Diese Eigenschaften sollten innerhalb eines Ordners eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8fda6-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="8fda6-116">Wenn nicht festgelegt, wenn die Nachricht erstellt wird, sollte der Nachrichtenspeicher diese Eigenschaften basierend auf verschiedenen Nachrichteneigenschaften abhängig von der Nachrichtenklasse festlegen.</span><span class="sxs-lookup"><span data-stu-id="8fda6-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="8fda6-117">Beispielsweise wird die **IPM. Hinweis** und **IPM. Termin** Nachrichten sollten diese Eigenschaft basierend auf der **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft und der IPM-Gruppe aufweisen **. Bei Kontakt** Nachrichten sollte diese Eigenschaft basierend auf der **dispidFileUnder** ([pidlidfileunder (](pidlidfileunder-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8fda6-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="8fda6-118">Für die meisten anderen Nachrichtenklassen sollte diese Eigenschaft auf der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft basieren.</span><span class="sxs-lookup"><span data-stu-id="8fda6-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8fda6-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8fda6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8fda6-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8fda6-120">Protocol specifications</span></span>

<span data-ttu-id="8fda6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fda6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fda6-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8fda6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8fda6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fda6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fda6-124">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="8fda6-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8fda6-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fda6-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fda6-126">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="8fda6-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8fda6-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8fda6-127">Header files</span></span>

<span data-ttu-id="8fda6-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8fda6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fda6-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8fda6-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fda6-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8fda6-130">Mapitags.h</span></span>
  
> <span data-ttu-id="8fda6-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8fda6-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fda6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fda6-132">See also</span></span>



[<span data-ttu-id="8fda6-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fda6-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fda6-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fda6-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fda6-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8fda6-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fda6-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8fda6-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

