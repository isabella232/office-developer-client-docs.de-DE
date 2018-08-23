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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587502"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="d71a2-103">PidTagHasAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d71a2-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="d71a2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d71a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d71a2-105">Enthält True, wenn eine Nachricht mindestens eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="d71a2-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d71a2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d71a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d71a2-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="d71a2-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="d71a2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d71a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d71a2-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="d71a2-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="d71a2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d71a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="d71a2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d71a2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d71a2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d71a2-112">Area:</span></span>  <br/> |<span data-ttu-id="d71a2-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="d71a2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d71a2-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d71a2-114">Remarks</span></span>

<span data-ttu-id="d71a2-115">Der Nachrichtenspeicher kopiert diese Eigenschaft aus der **MSGFLAG_HASATTACH** Kennzeichnung der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d71a2-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="d71a2-116">Eine Clientanwendung können dann **PR_HASATTACH** auf e-Mail-Anlagen in einem Viewer Nachricht sortiert.</span><span class="sxs-lookup"><span data-stu-id="d71a2-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="d71a2-117">Der Wert, den diese Eigenschaft mit der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d71a2-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d71a2-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d71a2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d71a2-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d71a2-119">Protocol specifications</span></span>

<span data-ttu-id="d71a2-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d71a2-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d71a2-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d71a2-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d71a2-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d71a2-122">Header files</span></span>

<span data-ttu-id="d71a2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d71a2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d71a2-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d71a2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d71a2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d71a2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d71a2-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d71a2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d71a2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d71a2-127">See also</span></span>



[<span data-ttu-id="d71a2-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d71a2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d71a2-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d71a2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d71a2-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d71a2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d71a2-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d71a2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

