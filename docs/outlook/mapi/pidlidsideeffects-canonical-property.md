---
title: PidLidSideEffects (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331297"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="19285-103">PidLidSideEffects (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="19285-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="19285-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19285-105">Steuert, wie ein Nachrichtenobjekt vom Client behandelt wird, wenn es auf Endbenutzereingaben angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="19285-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19285-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="19285-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19285-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="19285-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="19285-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="19285-108">Property set:</span></span>  <br/> |<span data-ttu-id="19285-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="19285-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="19285-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="19285-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19285-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="19285-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="19285-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="19285-112">Data type:</span></span>  <br/> |<span data-ttu-id="19285-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="19285-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="19285-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="19285-114">Area:</span></span>  <br/> |<span data-ttu-id="19285-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="19285-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19285-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19285-116">Remarks</span></span>

<span data-ttu-id="19285-117">Muss auf einen bitweisen oder null oder mehr der folgenden Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="19285-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="19285-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="19285-118">**Name**</span></span>|<span data-ttu-id="19285-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="19285-119">**Value**</span></span>|<span data-ttu-id="19285-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19285-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19285-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="19285-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="19285-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="19285-122">0x0001</span></span>  <br/> |<span data-ttu-id="19285-123">Beim Löschen ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19285-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="19285-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="19285-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="19285-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="19285-125">0x0008</span></span>  <br/> |<span data-ttu-id="19285-126">Dem Message-Objekt ist keine Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="19285-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="19285-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="19285-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="19285-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="19285-128">0x0010</span></span>  <br/> |<span data-ttu-id="19285-129">Beim Verschieben oder Kopieren in ein Folder-Objekt mit einer **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md))-Eigenschaft von "IPF" ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich. Hinweis".</span><span class="sxs-lookup"><span data-stu-id="19285-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="19285-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="19285-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="19285-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="19285-131">0x0020</span></span>  <br/> |<span data-ttu-id="19285-132">Beim Kopieren in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19285-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="19285-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="19285-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="19285-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="19285-134">0x0040</span></span>  <br/> |<span data-ttu-id="19285-135">Beim Verschieben in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19285-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="19285-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="19285-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="19285-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="19285-137">0x0100</span></span>  <br/> |<span data-ttu-id="19285-138">Beim Anzeigen von Verben für den Endbenutzer ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19285-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="19285-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="19285-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="19285-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="19285-140">0x0400</span></span>  <br/> |<span data-ttu-id="19285-141">Löschvorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenToDelete" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19285-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="19285-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="19285-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="19285-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="19285-143">0x0800</span></span>  <br/> |<span data-ttu-id="19285-144">Kopiervorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenTocopy" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19285-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="19285-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="19285-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="19285-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="19285-146">0x1000</span></span>  <br/> |<span data-ttu-id="19285-147">Vorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenToMove" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19285-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="19285-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="19285-148">seHasScript</span></span>  <br/> |<span data-ttu-id="19285-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="19285-149">0x2000</span></span>  <br/> |<span data-ttu-id="19285-150">Das Message-Objekt enthält ein Endbenutzerskript.</span><span class="sxs-lookup"><span data-stu-id="19285-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="19285-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="19285-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="19285-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="19285-152">0x4000</span></span>  <br/> |<span data-ttu-id="19285-153">Zusätzliche Verarbeitung ist erforderlich, um das Nachrichtenobjekt dauerhaft zu löschen.</span><span class="sxs-lookup"><span data-stu-id="19285-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="19285-154">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="19285-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19285-155">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="19285-155">Protocol specifications</span></span>

<span data-ttu-id="19285-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19285-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19285-157">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="19285-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19285-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19285-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19285-159">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="19285-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="19285-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19285-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19285-161">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="19285-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19285-162">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="19285-162">Header files</span></span>

<span data-ttu-id="19285-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19285-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="19285-164">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="19285-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19285-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19285-165">See also</span></span>



[<span data-ttu-id="19285-166">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19285-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19285-167">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="19285-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19285-168">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="19285-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19285-169">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="19285-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

