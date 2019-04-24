---
title: Kanonische Pidtaghasattachments (-Eigenschaft
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
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316128"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="14f99-103">Kanonische Pidtaghasattachments (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14f99-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="14f99-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14f99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14f99-105">Enthält TRUE, wenn eine Nachricht mindestens eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="14f99-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14f99-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="14f99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14f99-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="14f99-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="14f99-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="14f99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14f99-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="14f99-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="14f99-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="14f99-110">Data type:</span></span>  <br/> |<span data-ttu-id="14f99-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="14f99-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="14f99-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="14f99-112">Area:</span></span>  <br/> |<span data-ttu-id="14f99-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="14f99-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14f99-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14f99-114">Remarks</span></span>

<span data-ttu-id="14f99-115">Der Nachrichtenspeicher kopiert diese Eigenschaft aus dem **MSGFLAG_HASATTACH** -Flag der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="14f99-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="14f99-116">Eine Clientanwendung kann dann **PR_HASATTACH** verwenden, um Nachrichtenanlagen in einer Nachrichtenanzeige zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="14f99-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="14f99-117">Der Wert, den diese Eigenschaft mit der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="14f99-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="14f99-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14f99-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14f99-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="14f99-119">Protocol specifications</span></span>

<span data-ttu-id="14f99-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14f99-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14f99-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="14f99-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14f99-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="14f99-122">Header files</span></span>

<span data-ttu-id="14f99-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="14f99-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="14f99-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="14f99-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="14f99-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="14f99-125">Mapitags.h</span></span>
  
> <span data-ttu-id="14f99-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="14f99-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14f99-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14f99-127">See also</span></span>



[<span data-ttu-id="14f99-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14f99-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14f99-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14f99-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14f99-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="14f99-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14f99-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="14f99-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

