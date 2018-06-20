---
title: Kanonische PidTagMessageStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21336e158d21bba6c7204eb446df3efc80b70e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794622"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="8c86e-103">Kanonische PidTagMessageStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c86e-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="8c86e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c86e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c86e-105">Enthält eine 32-Bit-Bitmaske aus Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8c86e-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c86e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8c86e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c86e-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="8c86e-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="8c86e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="8c86e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c86e-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="8c86e-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="8c86e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8c86e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c86e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c86e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c86e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8c86e-112">Area:</span></span>  <br/> |<span data-ttu-id="8c86e-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="8c86e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c86e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c86e-114">Remarks</span></span>

<span data-ttu-id="8c86e-115">Eine Nachricht kann in einer Inhaltstabelle und in eine oder mehrere Suchergebnisse Tabellen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8c86e-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="8c86e-116">Diese Eigenschaft sollten keine-Eigenschaft für eine Nachricht aber eine Spalte in einer Inhaltstabelle berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c86e-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="8c86e-117">In dieser Eigenschaft kann in eine anderen Clientanwendung eine oder mehrere der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="8c86e-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="8c86e-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="8c86e-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="8c86e-119">Die Nachricht wurde beantwortet.</span><span class="sxs-lookup"><span data-stu-id="8c86e-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="8c86e-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="8c86e-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="8c86e-121">Die Nachricht wurde für nachfolgende löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="8c86e-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="8c86e-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="8c86e-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="8c86e-123">Die Nachricht ist im Revision-Entwurfsstatus.</span><span class="sxs-lookup"><span data-stu-id="8c86e-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="8c86e-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="8c86e-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="8c86e-125">Die Nachricht wird vom Empfänger Ordner zeigt unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c86e-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="8c86e-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="8c86e-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="8c86e-127">Die Nachricht ist in zeigt der Empfänger Ordner hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="8c86e-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="8c86e-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="8c86e-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="8c86e-129">Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8c86e-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="8c86e-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="8c86e-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="8c86e-131">Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="8c86e-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="8c86e-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="8c86e-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="8c86e-133">Für einen Client definierten Zweck hat die Nachricht markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8c86e-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="8c86e-134">Vom Client werden die Kennzeichen **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**und **MSGSTATUS_TAGGED** definiert.</span><span class="sxs-lookup"><span data-stu-id="8c86e-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="8c86e-135">Transport- und -Anbieter übergeben Sie diese Bits ohne Aktion.</span><span class="sxs-lookup"><span data-stu-id="8c86e-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="8c86e-136">Clients können diese Werte in irgendeiner Weise interpretieren, die für ihre Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="8c86e-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="8c86e-137">Eine Möglichkeit, dass viele Clients verwenden Sie diese Eigenschaft ist zum Anzeigen von Nachrichten, die für die Löschung mit einem repräsentative Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c86e-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="8c86e-138">Ein remote-Viewer-Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Ordner "Kopfzeile" vom Transportanbieter remote vorgelegte festlegen.</span><span class="sxs-lookup"><span data-stu-id="8c86e-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="8c86e-139">Die Client-Anwendung kann untersuchen, jeden Nachrichtenkopf in diesem Ordner, um zu bestimmen, ob die Nachricht an die entfernten Nachrichtenspeicher gelöscht oder heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c86e-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="8c86e-140">Anschließend wird die [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) -Methode auf das entsprechende Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c86e-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="8c86e-141">**SetMessageStatus** ist die einzige Möglichkeit, einen der Werte in dieser Eigenschaft festzulegen. die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c86e-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="8c86e-142">Um diese Eigenschaft abzurufen, rufen Clients [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) statt [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="8c86e-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="8c86e-143">Bits 16 bis 31 (0 x 10000 über 0 x 80000000) dieser Eigenschaft sind für die Verwendung durch die Clientanwendung zwischen Personen Nachricht (IPM) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c86e-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="8c86e-144">Alle anderen Bits sind MAPI für die Verwendung reserviert. nicht in der obigen Tabelle definiert sollte anfänglich auf 0 (null) festgelegt und anschließend nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8c86e-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8c86e-145">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8c86e-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c86e-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8c86e-146">Protocol specifications</span></span>

<span data-ttu-id="8c86e-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c86e-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c86e-148">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8c86e-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c86e-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c86e-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c86e-150">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="8c86e-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c86e-151">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8c86e-151">Header files</span></span>

<span data-ttu-id="8c86e-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c86e-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c86e-153">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8c86e-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c86e-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c86e-154">Mapitags.h</span></span>
  
> <span data-ttu-id="8c86e-155">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8c86e-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c86e-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c86e-156">See also</span></span>



[<span data-ttu-id="8c86e-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8c86e-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="8c86e-158">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c86e-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c86e-159">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c86e-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c86e-160">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8c86e-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c86e-161">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8c86e-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
