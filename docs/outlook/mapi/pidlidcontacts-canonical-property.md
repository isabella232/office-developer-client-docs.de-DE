---
title: Kanonische PidLidContacts-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6182c9dfc0c4de24bd587e626fe74d02ed23968b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793479"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="6e33c-103">Kanonische PidLidContacts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e33c-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="6e33c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e33c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e33c-105">Enthält die Namen der Kontakte, die mit dem Element verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6e33c-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e33c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e33c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e33c-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="6e33c-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="6e33c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6e33c-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e33c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e33c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e33c-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6e33c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e33c-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="6e33c-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="6e33c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e33c-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e33c-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e33c-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6e33c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e33c-114">Area:</span></span>  <br/> |<span data-ttu-id="6e33c-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="6e33c-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e33c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e33c-116">Remarks</span></span>

<span data-ttu-id="6e33c-117">Diese Eigenschaft enthält die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft der einzelnen Adressbuch **EntryID** , die den Wert der Eigenschaft **DispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6e33c-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="6e33c-118">Es kann keine Verweise in **DispidContactLinkEntry**enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e33c-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e33c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e33c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e33c-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e33c-120">Protocol specifications</span></span>

<span data-ttu-id="6e33c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e33c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e33c-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6e33c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e33c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e33c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e33c-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="6e33c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6e33c-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e33c-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e33c-126">Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6e33c-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="6e33c-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e33c-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e33c-128">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6e33c-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e33c-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6e33c-129">Header files</span></span>

<span data-ttu-id="6e33c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e33c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e33c-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6e33c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e33c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e33c-132">See also</span></span>



[<span data-ttu-id="6e33c-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e33c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e33c-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e33c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e33c-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e33c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e33c-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e33c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

