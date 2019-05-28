---
title: Kanonische pidlidcontacts (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319460"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="506e7-103">Kanonische pidlidcontacts (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="506e7-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="506e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="506e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="506e7-105">Enthält die Namen der Kontakte, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="506e7-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="506e7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="506e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="506e7-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="506e7-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="506e7-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="506e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="506e7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="506e7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="506e7-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="506e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="506e7-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="506e7-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="506e7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="506e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="506e7-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="506e7-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="506e7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="506e7-114">Area:</span></span>  <br/> |<span data-ttu-id="506e7-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="506e7-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="506e7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="506e7-116">Remarks</span></span>

<span data-ttu-id="506e7-117">Diese Eigenschaft enthält die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft der einzelnen Adress \*\*\*\* Buch-Eintrags-Nr, auf die im Wert der **dispidContactLinkEntry** ([pidlidcontactlinkentry (](pidlidcontactlinkentry-canonical-property.md))-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="506e7-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="506e7-118">Es kann Namen enthalten, die nicht in **dispidContactLinkEntry**referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="506e7-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="506e7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="506e7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="506e7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="506e7-120">Protocol specifications</span></span>

<span data-ttu-id="506e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="506e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="506e7-122">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="506e7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="506e7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="506e7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="506e7-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="506e7-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="506e7-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="506e7-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="506e7-126">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="506e7-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="506e7-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="506e7-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="506e7-128">Verarbeitet Nachrichten-und Attachment-Objekte.</span><span class="sxs-lookup"><span data-stu-id="506e7-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="506e7-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="506e7-129">Header files</span></span>

<span data-ttu-id="506e7-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="506e7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="506e7-131">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="506e7-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="506e7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="506e7-132">See also</span></span>



[<span data-ttu-id="506e7-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="506e7-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="506e7-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="506e7-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="506e7-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="506e7-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="506e7-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="506e7-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

