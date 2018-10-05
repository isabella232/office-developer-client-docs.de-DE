---
title: PidTagParentEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401216"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="16f80-103">PidTagParentEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16f80-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="16f80-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16f80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16f80-105">Enthält die Eintrags-ID des Ordners, der einen Ordner oder eine Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="16f80-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16f80-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="16f80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16f80-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="16f80-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="16f80-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="16f80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16f80-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="16f80-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="16f80-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="16f80-110">Data type:</span></span>  <br/> |<span data-ttu-id="16f80-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="16f80-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="16f80-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="16f80-112">Area:</span></span>  <br/> |<span data-ttu-id="16f80-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16f80-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16f80-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16f80-114">Remarks</span></span>

<span data-ttu-id="16f80-115">Diese Eigenschaft wird durch Nachrichtenspeicher für alle Ordner und Nachrichten berechnet.</span><span class="sxs-lookup"><span data-stu-id="16f80-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="16f80-116">Für eine Nachricht Store Stammordner enthält diese Eigenschaft die Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="16f80-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="16f80-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) und diese Eigenschaft nicht miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="16f80-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="16f80-118">Zielgerichtet auf völlig andere Kontexte.</span><span class="sxs-lookup"><span data-stu-id="16f80-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16f80-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="16f80-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16f80-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="16f80-120">Protocol specifications</span></span>

<span data-ttu-id="16f80-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="16f80-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16f80-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-124">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="16f80-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="16f80-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-126">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="16f80-126">Handles folder operations.</span></span>
    
<span data-ttu-id="16f80-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="16f80-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="16f80-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-130">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="16f80-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="16f80-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-132">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="16f80-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="16f80-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16f80-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16f80-134">Gibt die Methode spielt Offlineadressbuch (OAB) Adressbuchdaten vom Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="16f80-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16f80-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="16f80-135">Header files</span></span>

<span data-ttu-id="16f80-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16f80-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="16f80-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="16f80-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="16f80-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16f80-138">Mapitags.h</span></span>
  
> <span data-ttu-id="16f80-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="16f80-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16f80-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f80-140">See also</span></span>



[<span data-ttu-id="16f80-141">PidTagFolderType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16f80-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="16f80-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16f80-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16f80-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16f80-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16f80-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="16f80-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16f80-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="16f80-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

