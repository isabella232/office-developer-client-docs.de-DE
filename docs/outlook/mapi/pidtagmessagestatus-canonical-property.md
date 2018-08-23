---
title: PidTagMessageStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 626bd945851155c20850ee7f367ec6073ad57bc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570387"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="25d88-103">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25d88-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="25d88-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25d88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25d88-105">Enthält eine 32-Bit-Bitmaske aus Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="25d88-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25d88-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="25d88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25d88-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="25d88-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="25d88-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="25d88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25d88-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="25d88-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="25d88-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="25d88-110">Data type:</span></span>  <br/> |<span data-ttu-id="25d88-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25d88-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25d88-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="25d88-112">Area:</span></span>  <br/> |<span data-ttu-id="25d88-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="25d88-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25d88-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="25d88-114">Remarks</span></span>

<span data-ttu-id="25d88-115">Eine Nachricht kann in einer Inhaltstabelle und in eine oder mehrere Suchergebnisse Tabellen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25d88-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="25d88-116">Diese Eigenschaft sollten keine-Eigenschaft für eine Nachricht aber eine Spalte in einer Inhaltstabelle berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="25d88-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="25d88-117">In dieser Eigenschaft kann in eine anderen Clientanwendung eine oder mehrere der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="25d88-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="25d88-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="25d88-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="25d88-119">Die Nachricht wurde beantwortet.</span><span class="sxs-lookup"><span data-stu-id="25d88-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="25d88-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="25d88-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="25d88-121">Die Nachricht wurde für nachfolgende löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="25d88-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="25d88-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="25d88-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="25d88-123">Die Nachricht ist im Revision-Entwurfsstatus.</span><span class="sxs-lookup"><span data-stu-id="25d88-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="25d88-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="25d88-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="25d88-125">Die Nachricht wird vom Empfänger Ordner zeigt unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25d88-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="25d88-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="25d88-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="25d88-127">Die Nachricht ist in zeigt der Empfänger Ordner hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="25d88-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="25d88-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="25d88-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="25d88-129">Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="25d88-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="25d88-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="25d88-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="25d88-131">Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="25d88-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="25d88-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="25d88-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="25d88-133">Für einen Client definierten Zweck hat die Nachricht markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="25d88-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="25d88-134">Vom Client werden die Kennzeichen **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**und **MSGSTATUS_TAGGED** definiert.</span><span class="sxs-lookup"><span data-stu-id="25d88-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="25d88-135">Transport- und -Anbieter übergeben Sie diese Bits ohne Aktion.</span><span class="sxs-lookup"><span data-stu-id="25d88-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="25d88-136">Clients können diese Werte in irgendeiner Weise interpretieren, die für ihre Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="25d88-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="25d88-137">Eine Möglichkeit, dass viele Clients verwenden Sie diese Eigenschaft ist zum Anzeigen von Nachrichten, die für die Löschung mit einem repräsentative Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="25d88-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="25d88-138">Ein remote-Viewer-Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Ordner "Kopfzeile" vom Transportanbieter remote vorgelegte festlegen.</span><span class="sxs-lookup"><span data-stu-id="25d88-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="25d88-139">Die Client-Anwendung kann untersuchen, jeden Nachrichtenkopf in diesem Ordner, um zu bestimmen, ob die Nachricht an die entfernten Nachrichtenspeicher gelöscht oder heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="25d88-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="25d88-140">Anschließend wird die [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) -Methode auf das entsprechende Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="25d88-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="25d88-141">**SetMessageStatus** ist die einzige Möglichkeit, einen der Werte in dieser Eigenschaft festzulegen. die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25d88-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="25d88-142">Um diese Eigenschaft abzurufen, rufen Clients [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) statt [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="25d88-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="25d88-143">Bits 16 bis 31 (0 x 10000 über 0 x 80000000) dieser Eigenschaft sind für die Verwendung durch die Clientanwendung zwischen Personen Nachricht (IPM) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="25d88-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="25d88-144">Alle anderen Bits sind MAPI für die Verwendung reserviert. nicht in der obigen Tabelle definiert sollte anfänglich auf 0 (null) festgelegt und anschließend nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="25d88-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25d88-145">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25d88-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25d88-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="25d88-146">Protocol specifications</span></span>

<span data-ttu-id="25d88-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25d88-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25d88-148">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="25d88-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25d88-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25d88-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25d88-150">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="25d88-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25d88-151">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="25d88-151">Header files</span></span>

<span data-ttu-id="25d88-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25d88-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="25d88-153">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="25d88-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="25d88-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="25d88-154">Mapitags.h</span></span>
  
> <span data-ttu-id="25d88-155">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="25d88-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25d88-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25d88-156">See also</span></span>



[<span data-ttu-id="25d88-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="25d88-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="25d88-158">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25d88-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25d88-159">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25d88-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25d88-160">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="25d88-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25d88-161">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="25d88-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

