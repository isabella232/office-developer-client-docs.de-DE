---
title: Kanonische PidTagParentEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ba30514df028805135e9e31e7214ca336b1b3f85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794787"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="1f58b-103">Kanonische PidTagParentEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f58b-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1f58b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f58b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f58b-105">Enthält die Eintrags-ID des Ordners, der einen Ordner oder eine Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1f58b-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f58b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1f58b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f58b-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1f58b-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1f58b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1f58b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f58b-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="1f58b-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="1f58b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1f58b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f58b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1f58b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1f58b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1f58b-112">Area:</span></span>  <br/> |<span data-ttu-id="1f58b-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f58b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f58b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f58b-114">Remarks</span></span>

<span data-ttu-id="1f58b-115">Diese Eigenschaft wird durch Nachrichtenspeicher für alle Ordner und Nachrichten berechnet.</span><span class="sxs-lookup"><span data-stu-id="1f58b-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="1f58b-116">Für eine Nachricht Store Stammordner enthält diese Eigenschaft die Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="1f58b-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="1f58b-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) und diese Eigenschaft nicht miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1f58b-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="1f58b-118">Zielgerichtet auf völlig andere Kontexte.</span><span class="sxs-lookup"><span data-stu-id="1f58b-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f58b-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f58b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f58b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1f58b-120">Protocol specifications</span></span>

<span data-ttu-id="1f58b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1f58b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f58b-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-124">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="1f58b-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="1f58b-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-126">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="1f58b-126">Handles folder operations.</span></span>
    
<span data-ttu-id="1f58b-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="1f58b-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1f58b-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-130">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1f58b-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="1f58b-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-132">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="1f58b-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="1f58b-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f58b-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f58b-134">Gibt die Methode spielt Offlineadressbuch (OAB) Adressbuchdaten vom Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="1f58b-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f58b-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1f58b-135">Header files</span></span>

<span data-ttu-id="1f58b-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f58b-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f58b-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1f58b-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f58b-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f58b-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1f58b-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1f58b-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f58b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f58b-140">See also</span></span>



[<span data-ttu-id="1f58b-141">Kanonische PidTagFolderType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f58b-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="1f58b-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f58b-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f58b-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f58b-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f58b-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1f58b-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f58b-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1f58b-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

