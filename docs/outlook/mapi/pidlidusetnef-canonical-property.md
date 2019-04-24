---
title: Kanonische Pidlidusetnef (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315421"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="43881-103">Kanonische Pidlidusetnef (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="43881-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="43881-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43881-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43881-105">Gibt an, ob TNEF (Transport Neutral Encapsulation Format) in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von MAPI zu Multipurpose Internet Mail Extensions (MIME) oder SMTP-Format (Simple Mail Transfer Protocol) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="43881-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43881-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43881-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43881-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="43881-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="43881-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="43881-108">Property set:</span></span>  <br/> |<span data-ttu-id="43881-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="43881-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="43881-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="43881-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="43881-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="43881-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="43881-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43881-112">Data type:</span></span>  <br/> |<span data-ttu-id="43881-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="43881-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="43881-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43881-114">Area:</span></span>  <br/> |<span data-ttu-id="43881-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="43881-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43881-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43881-116">Remarks</span></span>

<span data-ttu-id="43881-117">Diese Eigenschaft gibt an, ob TNEF in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von TNEF in MIME oder SMTP-Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="43881-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="43881-118">Diese Eigenschaft ist möglicherweise abwesend, und wenn dies der Fall ist, muss TNEF in der Nachricht nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="43881-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="43881-119">Diese Eigenschaft gilt nur, wenn die Nachricht von einem POP3/SMTP-e-Mail-Konto gesendet wird und nicht angewendet wird, wenn die Nachricht von anderen Anbietern wie Microsoft Exchange Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="43881-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="43881-120">Unter bestimmten Umständen, beispielsweise bei der Aktivierung von Abstimmungsschaltflächen oder einem eingebetteten OLE-Objekt an eine Nachricht, kann Outlook diese Eigenschaft festlegen, um die Verwendung von TNEF zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="43881-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="43881-121">Die **PR_MSG_EDITOR_FORMAT** ([pidtagmessageeditorformat (](pidtagmessageeditorformat-canonical-property.md))-Eigenschaft kann verwendet werden, um beim Senden einer Nachricht nur einfachen Text und nicht TNEF zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="43881-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="43881-122">Da **pidlidusetnef (** die Einstellung in **PR_MSG_EDITOR_FORMAT**überschreibt, sollte eine Anwendung, die nur Text in einer ausgehenden Nachricht erzwingen möchte, auch nach **PIDLIDUSETNEF (** suchen und Sie auf false zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="43881-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="43881-123">Darüber hinaus muss das Add-in die Nachrichten Features entfernen, die TNEF benötigt haben, um unbrauchbare Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="43881-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="43881-124">Verwenden Sie das **CCSF_USE_TNEF** -Flag beim Aufrufen von [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="43881-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="43881-125">Dies gilt auch dann, wenn **pidlidusetnef (** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="43881-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43881-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43881-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43881-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="43881-127">Protocol specifications</span></span>

<span data-ttu-id="43881-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43881-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43881-129">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="43881-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43881-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43881-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43881-131">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="43881-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="43881-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43881-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43881-133">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="43881-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43881-134">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="43881-134">Header files</span></span>

<span data-ttu-id="43881-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="43881-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="43881-136">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="43881-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43881-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43881-137">See also</span></span>



[<span data-ttu-id="43881-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43881-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43881-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43881-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43881-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43881-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43881-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43881-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

