---
title: Kanonische Pidtagmessagestatus (-Eigenschaft
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
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355720"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="49d97-103">Kanonische Pidtagmessagestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49d97-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="49d97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49d97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49d97-105">Enthält eine 32-Bit-Bitmaske von Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="49d97-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49d97-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="49d97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49d97-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="49d97-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="49d97-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="49d97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49d97-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="49d97-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="49d97-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="49d97-110">Data type:</span></span>  <br/> |<span data-ttu-id="49d97-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="49d97-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="49d97-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="49d97-112">Area:</span></span>  <br/> |<span data-ttu-id="49d97-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="49d97-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49d97-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49d97-114">Remarks</span></span>

<span data-ttu-id="49d97-115">Eine Nachricht kann in einer Inhaltstabelle und in einer oder mehreren Suchergebnis Tabellen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="49d97-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="49d97-116">Diese Eigenschaft sollte nicht als Eigenschaft einer Nachricht, sondern als eine Spalte in einer Inhaltstabelle betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="49d97-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="49d97-117">Eine Clientanwendung kann eine oder mehrere der folgenden Flags in dieser Eigenschaft festlegen:</span><span class="sxs-lookup"><span data-stu-id="49d97-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="49d97-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="49d97-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="49d97-119">Die Nachricht wurde beantwortet.</span><span class="sxs-lookup"><span data-stu-id="49d97-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="49d97-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="49d97-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="49d97-121">Die Nachricht wurde zum späteren Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="49d97-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="49d97-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="49d97-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="49d97-123">Die Nachricht befindet sich im Entwurfsstatus der Revision.</span><span class="sxs-lookup"><span data-stu-id="49d97-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="49d97-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="49d97-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="49d97-125">Die Nachricht soll aus dem Ordner des Empfängers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49d97-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="49d97-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="49d97-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="49d97-127">Die Nachricht soll im Ordner des Empfängers hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="49d97-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="49d97-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="49d97-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="49d97-129">Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher markiert, ohne Sie auf den lokalen Client herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="49d97-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="49d97-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="49d97-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="49d97-131">Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="49d97-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="49d97-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="49d97-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="49d97-133">Die Nachricht wurde für einen Client definierten Zweck markiert.</span><span class="sxs-lookup"><span data-stu-id="49d97-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="49d97-134">Die **MSGSTATUS_DELMARKED**-, **MSGSTATUS_HIDDEN**-, **MSGSTATUS_HIGHLIGHTED**-und **MSGSTATUS_TAGGED** -Flags werden vom Client definiert.</span><span class="sxs-lookup"><span data-stu-id="49d97-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="49d97-135">Transport-und Speicheranbieter führen diese Bits ohne Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="49d97-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="49d97-136">Clients können diese Werte auf eine beliebige Weise interpretieren, die für Ihre Anwendungen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="49d97-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="49d97-137">Eine Möglichkeit, die diese Eigenschaft für viele Clients verwendet wird, ist das Anzeigen von zum Löschen markierten Nachrichten mit einem repräsentativen Symbol.</span><span class="sxs-lookup"><span data-stu-id="49d97-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="49d97-138">Ein Remoteanzeige Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Überschriften Ordner festlegen, der vom Remote Transportanbieter angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="49d97-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="49d97-139">Die Clientanwendung kann jeden Nachrichtenkopf in diesem Ordner überprüfen, um zu bestimmen, ob die Nachricht im Remotenachrichtenspeicher heruntergeladen oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="49d97-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="49d97-140">Anschließend wird die [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) -Methode verwendet, um das entsprechende Flag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49d97-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="49d97-141">**SetMessageStatus** ist die einzige Möglichkeit, die Flags in dieser Eigenschaft festzulegen. die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49d97-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="49d97-142">Um diese Eigenschaft abzurufen, rufen die Clients [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) anstelle von [IMAPIProp::](imapiprop-getprops.md)GetProps auf.</span><span class="sxs-lookup"><span data-stu-id="49d97-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="49d97-143">Die Bits 16 bis 31 (0x10000 bis 0x80000000) dieser Eigenschaft stehen für die Clientanwendung für die zwischenmenschlichen Nachrichten (IPM) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="49d97-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="49d97-144">Alle anderen Bits sind für die Verwendung durch MAPI reserviert; diejenigen, die nicht in der obigen Tabelle definiert sind, sollten anfänglich auf NULL festgelegt werden und nicht nachträglich geändert werden.</span><span class="sxs-lookup"><span data-stu-id="49d97-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="49d97-145">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="49d97-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49d97-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="49d97-146">Protocol specifications</span></span>

<span data-ttu-id="49d97-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49d97-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49d97-148">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="49d97-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49d97-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49d97-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49d97-150">Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="49d97-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49d97-151">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="49d97-151">Header files</span></span>

<span data-ttu-id="49d97-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49d97-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="49d97-153">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="49d97-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="49d97-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="49d97-154">Mapitags.h</span></span>
  
> <span data-ttu-id="49d97-155">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="49d97-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49d97-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d97-156">See also</span></span>



[<span data-ttu-id="49d97-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="49d97-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="49d97-158">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49d97-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49d97-159">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49d97-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49d97-160">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="49d97-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49d97-161">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="49d97-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

