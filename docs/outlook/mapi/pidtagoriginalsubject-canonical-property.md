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
ms.openlocfilehash: b49398b822e6972a8a6d02e1dff9c2316ce6eb33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566635"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="ab1bd-103">PidTagOriginalSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab1bd-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="ab1bd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1bd-105">Enthält den Betreff der ursprünglichen Nachricht für die Verwendung in einem Bericht zur Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab1bd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab1bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab1bd-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="ab1bd-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="ab1bd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ab1bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab1bd-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="ab1bd-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="ab1bd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab1bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab1bd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab1bd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab1bd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab1bd-112">Area:</span></span>  <br/> |<span data-ttu-id="ab1bd-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="ab1bd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab1bd-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ab1bd-114">Remarks</span></span>

<span data-ttu-id="ab1bd-115">Diese Eigenschaften werden auf den gleichen Wert wie die Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) ursprünglich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ab1bd-116">Die Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, klicken sie auf die Object Linking and Embedding (OLE) **IStream** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="ab1bd-117">Der Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab1bd-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab1bd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab1bd-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab1bd-119">Protocol specifications</span></span>

<span data-ttu-id="ab1bd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab1bd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab1bd-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab1bd-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab1bd-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab1bd-123">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="ab1bd-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab1bd-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab1bd-125">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab1bd-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab1bd-126">Header files</span></span>

<span data-ttu-id="ab1bd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab1bd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab1bd-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab1bd-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab1bd-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ab1bd-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab1bd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab1bd-131">See also</span></span>



[<span data-ttu-id="ab1bd-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1bd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab1bd-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1bd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab1bd-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab1bd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab1bd-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab1bd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

