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
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793784"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="7054b-103">PidLidSideEffects (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7054b-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="7054b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7054b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7054b-105">Steuert, wie ein Meldungsobjekt vom Client verarbeitet wird, wenn bei der Eingabe der Endbenutzer fungiert.</span><span class="sxs-lookup"><span data-stu-id="7054b-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7054b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7054b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7054b-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="7054b-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="7054b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7054b-108">Property set:</span></span>  <br/> |<span data-ttu-id="7054b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7054b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7054b-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7054b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7054b-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="7054b-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="7054b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7054b-112">Data type:</span></span>  <br/> |<span data-ttu-id="7054b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7054b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7054b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7054b-114">Area:</span></span>  <br/> |<span data-ttu-id="7054b-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7054b-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7054b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7054b-116">Remarks</span></span>

<span data-ttu-id="7054b-117">Muss auf eine bitweise oder 0 (null) oder mehrere der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7054b-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="7054b-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="7054b-118">**Name**</span></span>|<span data-ttu-id="7054b-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7054b-119">**Value**</span></span>|<span data-ttu-id="7054b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7054b-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7054b-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="7054b-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="7054b-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="7054b-122">0x0001</span></span>  <br/> |<span data-ttu-id="7054b-123">Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Löschen.</span><span class="sxs-lookup"><span data-stu-id="7054b-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="7054b-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="7054b-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="7054b-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="7054b-125">0x0008</span></span>  <br/> |<span data-ttu-id="7054b-126">Keine Benutzeroberfläche ist Message-Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7054b-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="7054b-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="7054b-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="7054b-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="7054b-128">0x0010</span></span>  <br/> |<span data-ttu-id="7054b-129">Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Verschieben oder Kopieren auf ein Folder-Objekt mit einer **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md))-Eigenschaft des "IPF. Hinweis".</span><span class="sxs-lookup"><span data-stu-id="7054b-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="7054b-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="7054b-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="7054b-131">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="7054b-131">0x0020</span></span>  <br/> |<span data-ttu-id="7054b-132">Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Kopieren in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7054b-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="7054b-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="7054b-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="7054b-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="7054b-134">0x0040</span></span>  <br/> |<span data-ttu-id="7054b-135">Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Wechsel zu einem anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7054b-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="7054b-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="7054b-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="7054b-137">0 x 0100</span><span class="sxs-lookup"><span data-stu-id="7054b-137">0x0100</span></span>  <br/> |<span data-ttu-id="7054b-138">Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Anzeigen von Verben für den Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="7054b-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="7054b-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="7054b-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="7054b-140">0 x 0400</span><span class="sxs-lookup"><span data-stu-id="7054b-140">0x0400</span></span>  <br/> |<span data-ttu-id="7054b-141">Löschvorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenToDelete" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7054b-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="7054b-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="7054b-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="7054b-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="7054b-143">0x0800</span></span>  <br/> |<span data-ttu-id="7054b-144">Kopiervorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenTocopy" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7054b-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="7054b-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="7054b-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="7054b-146">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="7054b-146">0x1000</span></span>  <br/> |<span data-ttu-id="7054b-147">Move-Vorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenToMove" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7054b-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="7054b-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="7054b-148">seHasScript</span></span>  <br/> |<span data-ttu-id="7054b-149">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="7054b-149">0x2000</span></span>  <br/> |<span data-ttu-id="7054b-150">Message-Objekts enthält Endbenutzer Skript.</span><span class="sxs-lookup"><span data-stu-id="7054b-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="7054b-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="7054b-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="7054b-152">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="7054b-152">0x4000</span></span>  <br/> |<span data-ttu-id="7054b-153">Zusätzliche Verarbeitung ist erforderlich, um das Objekt "Message" endgültig löschen.</span><span class="sxs-lookup"><span data-stu-id="7054b-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7054b-154">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7054b-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7054b-155">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7054b-155">Protocol specifications</span></span>

<span data-ttu-id="7054b-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7054b-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7054b-157">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7054b-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7054b-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7054b-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7054b-159">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="7054b-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7054b-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7054b-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7054b-161">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="7054b-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7054b-162">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7054b-162">Header files</span></span>

<span data-ttu-id="7054b-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7054b-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="7054b-164">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7054b-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7054b-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7054b-165">See also</span></span>



[<span data-ttu-id="7054b-166">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7054b-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7054b-167">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7054b-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7054b-168">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7054b-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7054b-169">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7054b-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

