---
title: PidTagOriginalSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331143"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="e940b-103">PidTagOriginalSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e940b-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="e940b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e940b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e940b-105">Enthält den Betreff einer ursprünglichen Nachricht zur Verwendung in einem Bericht über die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e940b-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e940b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e940b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e940b-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="e940b-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="e940b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e940b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e940b-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="e940b-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="e940b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e940b-110">Data type:</span></span>  <br/> |<span data-ttu-id="e940b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e940b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e940b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e940b-112">Area:</span></span>  <br/> |<span data-ttu-id="e940b-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="e940b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e940b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e940b-114">Remarks</span></span>

<span data-ttu-id="e940b-115">Diese Eigenschaften sind ursprünglich auf denselben Wert wie die **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e940b-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e940b-116">Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **Ole-IStream-Schnittstelle** (Object Linking and Embedding) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e940b-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="e940b-117">Der Client sollte immer zuerst den Zugriff über die **IMAPIProp-Schnittstelle** versuchen und nur dann auf **IStream** zugreifen, **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e940b-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e940b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e940b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e940b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e940b-119">Protocol specifications</span></span>

<span data-ttu-id="e940b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e940b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e940b-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e940b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e940b-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e940b-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e940b-123">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="e940b-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="e940b-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e940b-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e940b-125">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e940b-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e940b-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e940b-126">Header files</span></span>

<span data-ttu-id="e940b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e940b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e940b-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e940b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e940b-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e940b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e940b-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e940b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e940b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e940b-131">See also</span></span>



[<span data-ttu-id="e940b-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e940b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e940b-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e940b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e940b-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e940b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e940b-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e940b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

