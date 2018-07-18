---
title: PidTagHasAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b618e5a79c3b7e3810ea541aa9b905dfa4188a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794423"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="7f2a6-103">PidTagHasAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7f2a6-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="7f2a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f2a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f2a6-105">Enthält True, wenn eine Nachricht mindestens eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f2a6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7f2a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f2a6-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="7f2a6-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="7f2a6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="7f2a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f2a6-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="7f2a6-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="7f2a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7f2a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f2a6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7f2a6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7f2a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7f2a6-112">Area:</span></span>  <br/> |<span data-ttu-id="7f2a6-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="7f2a6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f2a6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f2a6-114">Remarks</span></span>

<span data-ttu-id="7f2a6-115">Der Nachrichtenspeicher kopiert diese Eigenschaft aus der **MSGFLAG_HASATTACH** Kennzeichnung der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="7f2a6-116">Eine Clientanwendung können dann **PR_HASATTACH** auf e-Mail-Anlagen in einem Viewer Nachricht sortiert.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="7f2a6-117">Der Wert, den diese Eigenschaft mit der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f2a6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f2a6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f2a6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7f2a6-119">Protocol specifications</span></span>

<span data-ttu-id="7f2a6-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f2a6-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f2a6-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f2a6-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7f2a6-122">Header files</span></span>

<span data-ttu-id="7f2a6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f2a6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f2a6-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f2a6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f2a6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7f2a6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7f2a6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f2a6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f2a6-127">See also</span></span>



[<span data-ttu-id="7f2a6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f2a6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f2a6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f2a6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f2a6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7f2a6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f2a6-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7f2a6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

